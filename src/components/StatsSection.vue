<template>
  <section style="background: #141414; padding: 80px 0">
    <v-container>
      <v-row class="fade-in justify-center" :class="{ visible: statsVisible }">
        <v-col cols="6" md="3" class="text-center" v-for="stat in stats" :key="stat.label">
          <div class="stat-number gradient-text">{{ stat.number }}</div>
          <div style="opacity: 0.6; margin-top: 8px; font-size: 0.95rem; font-weight: 500">{{ stat.label }}</div>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'StatsSection',
  data() {
    return {
      statsVisible: true,
      stats: [
        { number: "8+", label: "Competencias" },
        { number: "3", label: "Certificaciones" },
        { number: "7+", label: "Años Experiencia" },
      ],
    }
  },
  mounted() {
    const observer = new IntersectionObserver(
      ([entry]) => { if (entry.isIntersecting) this.statsVisible = true },
      { threshold: 0 }
    )
    observer.observe(this.$el)
  },
}
</script>
