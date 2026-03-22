<template>
  <v-app>
    <AppNavbar />
    <v-main style="background: #000">
      <HeroSection />
      <SobreMiSection />
      <StatsSection />
      <VentajasSection />
      <PlanesSection />
      <ProcesoPagoSection />
      <TransformacionesSection />
      <FaqSection />
      <ContactoSection />
    </v-main>
    <AppFooter />
  </v-app>
</template>

<script>
import AppNavbar from './components/AppNavbar.vue'
import HeroSection from './components/HeroSection.vue'
import SobreMiSection from './components/SobreMiSection.vue'
import StatsSection from './components/StatsSection.vue'
import VentajasSection from './components/VentajasSection.vue'
import PlanesSection from './components/PlanesSection.vue'
import ProcesoPagoSection from './components/ProcesoPagoSection.vue'
import TransformacionesSection from './components/TransformacionesSection.vue'
import FaqSection from './components/FaqSection.vue'
import ContactoSection from './components/ContactoSection.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  name: 'App',
  components: {
    AppNavbar,
    HeroSection,
    SobreMiSection,
    StatsSection,
    VentajasSection,
    PlanesSection,
    ProcesoPagoSection,
    TransformacionesSection,
    FaqSection,
    ContactoSection,
    AppFooter,
  },
}
</script>

<style>
</style>
