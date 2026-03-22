<template>
  <section id="sobre-mi" style="background: #0a0a0a; padding: 120px 0">
    <v-container>
      <v-row align="center" style="gap: 60px 0">
        <v-col cols="12" md="5" class="fade-in-left" :class="{ visible: sobreMiVisible }">
          <div style="position: relative">
            <div
              style="
                position: absolute;
                inset: -8px;
                background: linear-gradient(135deg, #2196f3, #1565c0);
                border-radius: 16px;
                opacity: 0.15;
                filter: blur(20px);
              "
            ></div>
            <v-img src="/assets/imgs/fernandoRuelas.jpeg" height="500" cover style="border-radius: 16px; position: relative"></v-img>
          </div>
        </v-col>
        <v-col cols="12" md="7" class="fade-in-right" :class="{ visible: sobreMiVisible }">
          <div class="decorative-line" style="margin-left: 0"></div>
          <h2 style="font-size: clamp(2rem, 5vw, 3rem); font-weight: 700; margin-bottom: 32px; letter-spacing: -1px">
            <span class="gradient-text">Sobre Mí</span>
          </h2>
          <div class="text-body-1 text-grey-lighten-2" style="line-height: 1.8">
            <p class="mb-4">
              Soy <span class="font-weight-bold text-white">Fernando Ruelas</span>, entrenador personal y asesor certificado en nutrición
              deportiva y nutrición aplicada al fisiculturismo de manera internacional.
            </p>
            <p class="mb-4">
              Mi experiencia no solo viene de los libros y certificaciones. He vivido cada proceso: desde las etapas de volumen hasta los
              cortes más exigentes para competir en el escenario. Conozco la frustración, el sacrificio, pero sobre todo, la satisfacción de
              lograr resultados reales.
            </p>
            <p class="mb-4">
              A lo largo de mi trayectoria competitiva, he cometido errores que me costaron tiempo, dinero y energía.
              <span class="text-blue font-weight-bold">Mi misión es que tú no tengas que cometerlos</span>. Aprende de mi experiencia y
              acelera tu camino hacia tus objetivos.
            </p>
            <p class="mb-4">
              Con más de 8 competencias en mi haber, certificaciones profesionales y años de estudio constante, combino la ciencia con la
              práctica real para ofrecerte resultados medibles y sostenibles.
            </p>
            <p class="text-blue font-weight-bold font-italic text-h6">
              "No importa dónde estés ahora, lo importante es hacia dónde quieres ir. Yo te llevaré ahí."
            </p>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'SobreMiSection',
  data() {
    return {
      sobreMiVisible: true,
    }
  },
  mounted() {
    const observer = new IntersectionObserver(
      ([entry]) => { if (entry.isIntersecting) this.sobreMiVisible = true },
      { threshold: 0 }
    )
    observer.observe(this.$el)
  },
}
</script>
