<template>
  <section id="planes" style="background: #0a0a0a; padding: 120px 0">
    <v-container>
      <div class="text-center mb-16 fade-in" :class="{ visible: planesVisible }">
        <div class="decorative-line"></div>
        <h2 style="font-size: clamp(2rem, 5vw, 3rem); font-weight: 700; margin-bottom: 16px; letter-spacing: -1px">
          <span class="gradient-text">Planes</span>
        </h2>
        <p style="opacity: 0.6; font-size: 1.1rem">Elige el plan ideal para ti</p>
      </div>

      <v-row class="scale-in" :class="{ visible: planesVisible }" style="margin-bottom: 40px">
        <v-col cols="12" md="4" v-for="plan in planesRegulares" :key="plan.nombre">
          <div
            class="minimal-card"
            :style="{
              padding: '40px',
              borderRadius: '16px',
              height: '100%',
              border: plan.popular ? '2px solid #2196F3' : '1px solid rgba(255, 255, 255, 0.08)',
              position: 'relative'
            }"
          >
            <div
              v-if="plan.popular"
              style="
                position: absolute;
                top: -12px;
                left: 50%;
                transform: translateX(-50%);
                background: #2196f3;
                padding: 6px 20px;
                border-radius: 20px;
                font-size: 0.75rem;
                font-weight: 600;
                text-transform: uppercase;
                letter-spacing: 0.5px;
              "
            >
              Popular
            </div>
            <h3 style="font-size: 1.5rem; font-weight: 700; margin-bottom: 24px; text-align: center">{{ plan.nombre }}</h3>
            <div style="text-align: center; margin-bottom: 32px">
              <div v-if="plan.precioAnterior" style="display: flex; align-items: center; justify-content: center; gap: 8px; margin-bottom: 4px">
                <span style="
                  font-size: 1.1rem;
                  font-weight: 600;
                  color: #ef5350;
                  text-decoration: line-through;
                  text-decoration-color: #ef5350;
                  text-decoration-thickness: 2px;
                  opacity: 0.85;
                ">${{ plan.precioAnterior }}</span>
                <span style="
                  background: linear-gradient(135deg, #ef5350, #c62828);
                  color: #fff;
                  font-size: 0.65rem;
                  font-weight: 700;
                  padding: 2px 8px;
                  border-radius: 20px;
                  text-transform: uppercase;
                  letter-spacing: 0.5px;
                ">Promo</span>
              </div>
              <div style="font-size: 3rem; font-weight: 800; color: #2196f3; line-height: 1">
                ${{ plan.precio }}
                <span style="font-size: 1.2rem; opacity: 0.6; font-weight: 400">/mes</span>
              </div>
              <div v-if="plan.precioTrimestral" style="margin-top: 8px; opacity: 0.5; font-size: 0.9rem">
                ${{ plan.precioTrimestral }} / 3 meses
              </div>
            </div>
            <div style="margin-bottom: 32px">
              <div v-for="car in plan.caracteristicas" :key="car" style="display: flex; align-items: flex-start; margin-bottom: 12px">
                <v-icon color="blue" size="18" style="margin-right: 12px; margin-top: 2px; flex-shrink: 0">mdi-check</v-icon>
                <span style="opacity: 0.8; font-size: 0.95rem; line-height: 1.5">{{ car }}</span>
              </div>
            </div>
            <v-btn
              :color="plan.popular ? 'blue' : ''"
              :variant="plan.popular ? 'flat' : 'outlined'"
              block
              size="large"
              @click="abrirLink(plan.link)"
              target="_blank"
              class="minimal-btn"
              style="text-transform: none; font-weight: 600; letter-spacing: 0"
            >
              Contratar
            </v-btn>
          </div>
        </v-col>
      </v-row>



      <!-- Plan Competencia -->
  
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'PlanesSection',
  data() {
    return {
      planesVisible: true,
      planesRegulares: [
        {
          nombre: "Estudiante",
          precioAnterior: 1000,
          precio: 800,
          precioTrimestral: 2500,
          popular: false,
          caracteristicas: [
            "Acceso a app personalizada con tu plan y videos",
            "Formulario inicial completo",
            "Plan de alimentación personalizado",
            "Plan de suplementación adaptado",
            "Plan de entrenamiento estético",
            "Seguimiento constante",
            "Formularios de seguimiento",
          ],
          link: "https://link.mercadopago.com.mx/ruelasteam"
        },
        {
          nombre: "Estándar",
          precio: 900,
          precioAnterior: 1200,
          precioTrimestral: 3000,
          popular: true,
          caracteristicas: ["Acceso a app personalizada con tu plan y videos", "Todo lo del plan Estudiante"],
          link: "https://link.mercadopago.com.mx/ruelasteam"
        },
        {
          nombre: "Plan de Alimentación",
          precio: 550,
          precioAnterior: 600,
          precioTrimestral: null,
          popular: false,
          caracteristicas: ["Acceso a app personalizada con tu plan y videos", "Formulario de hábitos", "Plan nutricional personalizado", "Adaptado a tu vida", "Plan de suplementación"],
          link: "https://link.mercadopago.com.mx/ruelasteam"
        },
        {
          nombre: "Plan de Entrenamiento",
          precio: 550,
          precioTrimestral: null,
          popular: false,
          caracteristicas: ["Acceso a app personalizada con tu plan y videos", "Evaluacion inicial", "Plan de entrenamiento personalizado", "Mejora continua", "Seguimiento"],
          link: "https://link.mercadopago.com.mx/ruelasteam"
        },
        {
          nombre: "Preparación Competencia",
          popular: false,
          precio: 1300,
          precioAnterior: 0,
          precioTrimestral: 3900,
          caracteristicas: [
            "Acceso a app personalizada con tu plan y videos",
            "Anticipo 3 meses requerido",
            "Planificación completa",
            "Periodización detallada",
            "Peak week especializado",
            "Seguimiento constante",
          ],
          link: "https://link.mercadopago.com.mx/ruelasteam"
        },
      ],
      planCompetencia: {
        nombre: "Preparación Competencia",
        precio: 1300,
        precioTrimestral: 3900,
        caracteristicas: [
          "Acceso a app personalizada con tu plan y videos",
          "Anticipo 3 meses requerido",
          "Planificación completa",
          "Periodización detallada",
          "Peak week especializado",
          "Seguimiento constante",
        ]
      },
    }
  },
  mounted() {
    const observer = new IntersectionObserver(
      ([entry]) => { if (entry.isIntersecting) this.planesVisible = true },
      { threshold: 0 }
    )
    observer.observe(this.$el)
  },
  methods: {
    abrirLink(url) {
      console.log(url)
      if (url) window.open(url, '_blank', 'noopener')
    },
  },
}
</script>
