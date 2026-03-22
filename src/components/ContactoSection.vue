<template>
  <section id="contacto" style="background: #000; padding: 120px 0">
    <v-container>
      <div class="text-center mb-16 fade-in" :class="{ visible: contactoVisible }">
        <div class="decorative-line"></div>
        <h2 style="font-size: clamp(2rem, 5vw, 3rem); font-weight: 700; margin-bottom: 16px; letter-spacing: -1px">
          <span class="gradient-text">Comienza Hoy</span>
        </h2>
        <p style="opacity: 0.6; font-size: 1.1rem">Da el primer paso hacia tu transformación</p>
      </div>

      <!-- Formulario -->
      <v-row justify="center" class="scale-in" :class="{ visible: contactoVisible }">
        <v-col cols="12" md="8">
          <div class="minimal-card" style="padding: 48px; border-radius: 16px">
            <h3 style="font-size: 1.5rem; font-weight: 600; text-align: center; margin-bottom: 32px">Formulario de Contacto</h3>

            <v-text-field
              v-model="formData.nombre"
              label="Nombre"
              variant="outlined"
              color="blue"
              style="margin-bottom: 24px"
              hide-details
            ></v-text-field>

            <v-select
              v-model="formData.plan"
              :items="planesNombres"
              label="Plan de Interés"
              variant="outlined"
              color="blue"
              style="margin-bottom: 24px"
              hide-details
            ></v-select>

            <v-textarea
              v-model="formData.objetivo"
              label="Tu Objetivo"
              variant="outlined"
              color="blue"
              rows="4"
              style="margin-bottom: 32px"
              hide-details
            ></v-textarea>

            <v-btn
              @click="enviarWhatsApp"
              color="blue"
              block
              size="x-large"
              class="minimal-btn"
              :disabled="!formData.nombre || !formData.plan || !formData.objetivo"
              style="text-transform: none; font-weight: 600; letter-spacing: 0; padding: 20px"
            >
              <v-icon left>mdi-send</v-icon>
              Enviar por WhatsApp
            </v-btn>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'ContactoSection',
  data() {
    return {
      contactoVisible: true,
      formData: {
        nombre: '',
        plan: '',
        objetivo: '',
      },
      certificados: [
        { nombre: "Asesor en Nutrición Deportiva", institucion: "FISICOCULTURISMO MEXICO S.C AFILIADO A WABBA INTERNATIONAL" },
        { nombre: "Nutrición Aplicada al Fisiculturismo", institucion: "FISICOCULTURISMO MEXICO S.C AFILIADO A WABBA INTERNATIONAL" },
      ],
      competencias: [
        { nombre: "iniciación", posicion: "1er Lugar", año: 2022 },
        { nombre: "iniciación", posicion: "Campeon absoluto", año: 2022 },
        { nombre: "MR MEXICO", posicion: "1er Lugar juvenil", año: 2022 },
        { nombre: "MR MEXICO", posicion: "3er Lugar categoria abierta", año: 2022 },
        { nombre: "MS y MR Sonora juvenil", posicion: "1do Lugar", año: 2022 },
        { nombre: "MS y MR Sonora juvenil", posicion: "Campeon absoluto", año: 2022 },
        { nombre: "Iniciacion", posicion: "2do lugar", año: 2021 },
        { nombre: "MSS Y MR SONORA juvenil", posicion: "3er Lugar", año: 2021 },
        { nombre: "Iniciacion", posicion: "1er Lugar", año: 2019 },
        { nombre: "MS Y MR SONORA juvenil", posicion: "2do Lugar", año: 2019 },
        { nombre: "CLASICO MSS Y MR SONORA", posicion: "3er Lugar", año: 2019 },
      ],
    }
  },
  computed: {
    planesNombres() {
      return ['Estudiante', 'Estándar', 'Plan de Alimentación', 'Plan de Entrenamiento', 'Preparación Competencia']
    },
  },
  mounted() {
    const observer = new IntersectionObserver(
      ([entry]) => { if (entry.isIntersecting) this.contactoVisible = true },
      { threshold: 0 }
    )
    observer.observe(this.$el)
  },
  methods: {
    enviarWhatsApp() {
      const mensaje = `Hola, me llamo ${this.formData.nombre} y estoy interesado en el plan ${this.formData.plan} con el objetivo de ${this.formData.objetivo}.`
      const url = `https://wa.me/526221562893?text=${encodeURIComponent(mensaje)}`
      window.open(url, "_blank")
    },
  },
}
</script>
