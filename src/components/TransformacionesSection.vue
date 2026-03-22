<template>
  <section id="transformaciones" style="background: #0a0a0a; padding: 120px 0; overflow: hidden">
    <v-container>
      <div class="text-center mb-16 fade-in" :class="{ visible: transformacionesVisible }">
        <div class="decorative-line"></div>
        <h2 style="font-size: clamp(2rem, 5vw, 3rem); font-weight: 700; margin-bottom: 16px; letter-spacing: -1px">
          <span class="gradient-text">Transformaciones Reales</span>
        </h2>
        <p style="opacity: 0.6; font-size: 1.1rem">Resultados que hablan por sí mismos</p>
      </div>

      <!-- Carrusel de Vuetify -->
      <div class="fade-in" :class="{ visible: transformacionesVisible }">
        <v-carousel
          v-model="currentSlide"
          height="auto"
          hide-delimiter-background
          show-arrows="hover"
          style="border-radius: 16px; overflow: hidden"
        >
          <!-- <template v-slot:prev="{ props }">
            <v-btn
              icon
              size="large"
              @click="props.onClick"
              style="background: rgba(33, 150, 243, 0.3); backdrop-filter: blur(10px); margin-left: 16px"
            >
              <v-icon color="white" size="32">mdi-chevron-left</v-icon>
            </v-btn>
          </template>

          <template v-slot:next="{ props }">
            <v-btn
              icon
              size="large"
              @click="props.onClick"
              style="background: rgba(33, 150, 243, 0.3); backdrop-filter: blur(10px); margin-right: 16px"
            >
              <v-icon color="white" size="32">mdi-chevron-right</v-icon>
            </v-btn>
          </template> -->

          <v-carousel-item v-for="(transformacion, index) in transformaciones" :key="index" :src="transformacion.imagen" cover>
            <div style="position: absolute; inset: 0; display: flex; flex-direction: column; justify-content: flex-end">
              <!-- Badge "Transformación" -->
              <!-- <div
                style="
                  position: absolute;
                  top: 24px;
                  right: 24px;
                  background: rgba(33, 150, 243, 0.9);
                  backdrop-filter: blur(10px);
                  padding: 12px 24px;
                  border-radius: 10px;
                  box-shadow: 0 4px 20px rgba(33, 150, 243, 0.4);
                "
              >
                <v-icon size="20" color="white" style="margin-right: 8px">mdi-chart-line</v-icon>
                <span style="font-weight: 700; font-size: 0.95rem; text-transform: uppercase; letter-spacing: 0.5px"> Transformación </span>
              </div> -->

              <!-- Info del Cliente -->
              <!-- <div
                style="
                  background: linear-gradient(to top, rgba(0, 0, 0, 0.95) 0%, rgba(0, 0, 0, 0.7) 60%, transparent 100%);
                  padding: 100px 32px 40px;
                "
              >
                <v-container>
                  <v-row justify="center">
                    <v-col cols="12" md="10" lg="8">
                       <h3 style="font-size: 2rem; font-weight: 700; margin-bottom: 12px; text-align: center">{{ transformacion.nombre }}</h3>
                       <p style="opacity: 0.9; margin-bottom: 24px; font-size: 1.1rem; line-height: 1.6; text-align: center">
                        {{ transformacion.descripcion }}
                      </p>
                      <div style="display: flex; gap: 16px; flex-wrap: wrap; justify-content: center">
                        <div
                          style="
                            background: rgba(33, 150, 243, 0.2);
                            border: 1px solid rgba(33, 150, 243, 0.4);
                            padding: 12px 24px;
                            border-radius: 10px;
                            backdrop-filter: blur(10px);
                            display: flex;
                            align-items: center;
                          "
                        >
                          <v-icon size="20" color="blue" style="margin-right: 10px">mdi-calendar-clock</v-icon>
                          <span style="font-size: 1rem; font-weight: 600">{{ transformacion.tiempo }}</span>
                        </div>
                        <div
                          v-if="transformacion.peso"
                          style="
                            background: rgba(33, 150, 243, 0.2);
                            border: 1px solid rgba(33, 150, 243, 0.4);
                            padding: 12px 24px;
                            border-radius: 10px;
                            backdrop-filter: blur(10px);
                            display: flex;
                            align-items: center;
                          "
                        >
                          <v-icon size="20" color="blue" style="margin-right: 10px">mdi-trending-up</v-icon>
                          <span style="font-size: 1rem; font-weight: 600">{{ transformacion.peso }}</span>
                        </div>
                      </div>
                    </v-col>
                  </v-row>
                </v-container>
              </div> -->
            </div>
          </v-carousel-item>
        </v-carousel>
      </div>

      <!-- CTA -->
      <v-row justify="center" style="margin-top: 64px" class="fade-in" :class="{ visible: transformacionesVisible }">
        <v-col cols="12" md="6">
          <div
            style="
              background: rgba(33, 150, 243, 0.1);
              border: 1px solid rgba(33, 150, 243, 0.2);
              border-radius: 16px;
              padding: 40px;
              text-align: center;
            "
          >
            <v-icon size="48" color="blue" style="margin-bottom: 16px; opacity: 0.8">mdi-trophy-variant</v-icon>
            <h3 style="font-size: 1.5rem; font-weight: 700; margin-bottom: 12px">¿Listo para tu propia transformación?</h3>
            <p style="color: #b0b0b0; margin-bottom: 24px; font-size: 1rem">Únete a las personas que ya están logrando sus objetivos</p>
            <v-btn
              href="#planes"
              color="blue"
              size="x-large"
              class="minimal-btn"
              style="text-transform: none; font-weight: 600; letter-spacing: 0"
            >
              <v-icon left>mdi-rocket-launch</v-icon>
              Comenzar Ahora
            </v-btn>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'TransformacionesSection',
  data() {
    return {
      transformacionesVisible: true,
      currentSlide: 0,
      transformaciones: [
        {
          nombre: "",
          descripcion: "Ganancia de masa muscular.",
          tiempo: "12 semanas",
          peso: "-8kg de grasa",
          imagen: "/assets/imgs/transformacion1.jpg",
        },
        {
          nombre: "",
          descripcion: "Recomposición corporal",
          tiempo: "20 semanas",
          peso: "-10kg / +4kg músculo",
          imagen: "/assets/imgs/transformacion3.jpg",
        },
        {
          nombre: "",
          descripcion: "Disminución de porcentaje de grasa",
          tiempo: "24 semanas",
          peso: "-12kg de grasa",
          imagen: "/assets/imgs/transformacion4.jpg",
        },
        {
          nombre: "",
          descripcion: "Ganancia de masa muscular.",
          tiempo: "16 semanas",
          peso: "+6kg de músculo",
          imagen: "/assets/imgs/transformacion2.jpg",
        },
        {
          nombre: "",
          descripcion: "perdida de peso",
          tiempo: "24 semanas",
          peso: "-12kg de grasa",
          imagen: "/assets/imgs/transformacion5.jpg",
        },
        {
          nombre: "",
          descripcion: "Disminución de porcentaje de grasa",
          tiempo: "24 semanas",
          peso: "-12kg de grasa",
          imagen: "/assets/imgs/transformacion6.jpeg",
        },
        {
          nombre: "",
          descripcion: "Disminución de porcentaje de grasa",
          tiempo: "20 semanas",
          peso: "-10kg / +4kg músculo",
          imagen: "/assets/imgs/transformacion7.jpeg",
        },
      ],
    }
  },
  mounted() {
    const observer = new IntersectionObserver(
      ([entry]) => { if (entry.isIntersecting) this.transformacionesVisible = true },
      { threshold: 0 }
    )
    observer.observe(this.$el)
  },
  methods: {
    nextSlide() {
      this.currentSlide = (this.currentSlide + 1) % this.transformaciones.length
    },
    prevSlide() {
      this.currentSlide = this.currentSlide === 0 ? this.transformaciones.length - 1 : this.currentSlide - 1
    },
  },
}
</script>
