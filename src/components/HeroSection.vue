<template>
  <section id="inicio" class="hero-section">
    <v-container class="py-16" style="min-height: 100vh; display: flex; align-items: center">
      <v-row justify="center" align="center">
        <v-col cols="12" class="text-center">
          <v-icon size="80" color="blue" class="pulse-animation mb-4">mdi-dumbbell</v-icon>
          <h1 class="text-h2 text-md-h1 font-weight-bold mb-4">Transforma Tu Cuerpo</h1>
          <p class="text-h5 text-md-h4 mb-2 text-grey-lighten-1">Entrenamiento Personalizado con Fernando Ruelas</p>
          <p class="text-h6 mb-8 text-grey">
            Entrenador Personalizado | Asesor certificado en nutrición deportiva y nutricion aplicada al fisicoculturismo
          </p>
          <div class="d-flex flex-column flex-sm-row gap-4 justify-center">
            <v-btn href="#planes" size="x-large" color="blue" class="mr-2 hover-scale" variant="elevated" >
              <v-icon left>mdi-clipboard-text</v-icon>
              Ver Planes
            </v-btn>
            <v-btn href="#contacto" size="x-large" variant="outlined" color="blue" class="hover-scale">
              <v-icon left>mdi-phone</v-icon>
              Contactar
            </v-btn>
          </div>
          <v-icon size="50" color="blue" class="bounce-animation mt-16">mdi-chevron-down</v-icon>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'HeroSection',
}
</script>
