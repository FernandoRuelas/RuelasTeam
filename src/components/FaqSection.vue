<template>
  <section id="faq" style="background: #000; padding: 120px 0">
    <v-container>
      <div class="text-center mb-16 fade-in" :class="{ visible: faqVisible }">
        <div class="decorative-line"></div>
        <h2 style="font-size: clamp(2rem, 5vw, 3rem); font-weight: 700; margin-bottom: 16px; letter-spacing: -1px">
          <span class="gradient-text">Preguntas Frecuentes</span>
        </h2>
        <p style="opacity: 0.6; font-size: 1.1rem">Resuelve tus dudas más comunes</p>
      </div>

      <!-- FAQ Items -->
      <v-row justify="center" class="fade-in" :class="{ visible: faqVisible }">
        <v-col cols="12" md="10" lg="8">
          <div style="display: flex; flex-direction: column; gap: 16px">
            <div
              v-for="(faq, index) in faqs"
              :key="index"
              class="minimal-card"
              style="border-radius: 16px; overflow: hidden; transition: all 0.3s ease"
            >
              <button
                @click="toggleFAQ(index)"
                style="
                  width: 100%;
                  padding: 20px 24px;
                  display: flex;
                  align-items: center;
                  justify-content: space-between;
                  text-align: left;
                  background: transparent;
                  border: none;
                  cursor: pointer;
                  transition: background 0.3s ease;
                "
                @mouseover="$event.currentTarget.style.background = 'rgba(255, 255, 255, 0.05)'"
                @mouseleave="$event.currentTarget.style.background = 'transparent'"
              >
                <h3 style="font-size: 1.1rem; font-weight: 600; padding-right: 16px; color: #fff">{{ faq.pregunta }}</h3>
                <v-icon
                  :style="{
                    transform: openFAQIndex === index ? 'rotate(180deg)' : 'rotate(0deg)',
                    transition: 'transform 0.3s ease',
                    flexShrink: 0
                  }"
                  color="blue"
                >
                  mdi-chevron-down
                </v-icon>
              </button>

              <div
                :style="{
                  maxHeight: openFAQIndex === index ? '500px' : '0',
                  opacity: openFAQIndex === index ? '1' : '0',
                  overflow: 'hidden',
                  transition: 'all 0.3s ease'
                }"
              >
                <div style="padding: 0 24px 20px 24px">
                  <div style="border-top: 1px solid rgba(255, 255, 255, 0.05); padding-top: 16px">
                    <p style="color: #b0b0b0; line-height: 1.7; font-size: 0.95rem">{{ faq.respuesta }}</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </v-col>
      </v-row>

      <!-- CTA Footer -->
      <v-row justify="center" style="margin-top: 64px" class="fade-in" :class="{ visible: faqVisible }">
        <v-col cols="12" md="6">
          <div
            style="
              background: rgba(33, 150, 243, 0.1);
              border: 1px solid rgba(33, 150, 243, 0.2);
              border-radius: 16px;
              padding: 32px;
              text-align: center;
            "
          >
            <p style="color: #b0b0b0; margin-bottom: 16px; font-size: 1rem">¿Tienes más preguntas?</p>
            <v-btn
              href="#contacto"
              color="blue"
              size="large"
              class="minimal-btn"
              style="text-transform: none; font-weight: 600; letter-spacing: 0"
            >
              Contáctame
            </v-btn>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'FaqSection',
  data() {
    return {
      faqVisible: true,
      openFAQIndex: null,
      faqs: [
        {
          pregunta: "¿En cuánto tiempo veré resultados?",
          respuesta:
            "Los resultados dependen de tu compromiso, esfuerzo y dedicación. Sin embargo, recomiendo un mínimo de 3 meses para lograr cambios más sostenibles y significativos. Los primeros cambios visibles pueden apreciarse desde la primera quincena o el primer mes, pero la verdadera transformación requiere constancia y paciencia.",
        },
        {
          pregunta: "¿Qué pasa si no tengo mucho tiempo para entrenar?",
          respuesta:
            "No te preocupes, tu rutina será completamente ajustada a tu estilo de vida, horarios y actividades diarias. Diseñaremos un plan eficiente que se adapte a tu tiempo disponible, priorizando ejercicios efectivos que maximicen tus resultados sin comprometer tu agenda.",
        },
        {
          pregunta: "¿Qué pasa si no puedo seguir una dieta estrictamente?",
          respuesta:
            "Entiendo que la vida real no siempre es perfecta. Por eso planificamos juntos una estrategia nutricional flexible y sostenible que se adapte a tu rutina y preferencias. El objetivo es lograr un equilibrio saludable sin que tengas que sacrificar tu vida social o familiar, creando hábitos que puedas mantener a largo plazo.",
        },
        {
          pregunta: "¿Necesito experiencia previa en el gimnasio?",
          respuesta:
            "Para nada. Trabajo con personas de todos los niveles, desde principiantes completos hasta atletas avanzados. Si eres nuevo, te guiaré paso a paso con técnicas correctas desde el inicio. Si ya tienes experiencia, optimizaremos tu entrenamiento para llevarte al siguiente nivel.",
        },
        {
          pregunta: "¿Qué incluye el seguimiento constante?",
          respuesta:
            "El seguimiento incluye revisiones periódicas de tu progreso, ajustes en tu plan según tus resultados, resolución de dudas vía WhatsApp, y evaluaciones detalladas mediante formularios de seguimiento. Estaré disponible para apoyarte en cada etapa de tu proceso.",
        },
        {
          pregunta: "¿Puedo cambiar de plan después de comenzar?",
          respuesta:
            "Por supuesto. Si sientes que necesitas más o menos acompañamiento, podemos ajustar tu plan. Mi prioridad es que obtengas el nivel de soporte adecuado para alcanzar tus objetivos de la manera más efectiva.",
        },
        {
          pregunta: "¿Los planes incluyen suplementación obligatoria?",
          respuesta:
            "No. La suplementación es opcional y siempre personalizada según tus objetivos, presupuesto y necesidades. Te asesoraré sobre qué suplementos podrían beneficiarte, pero nunca es obligatorio comprar nada específico para seguir el plan.",
        },
      ],
    }
  },
  methods: {
    toggleFAQ(index) {
      this.openFAQIndex = this.openFAQIndex === index ? null : index
    },
  },
}
</script>
