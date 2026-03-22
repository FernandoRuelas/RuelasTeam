<template>
  <section
    style="background: linear-gradient(180deg, #000000 0%, #0a1929 50%, #000000 100%); padding: 140px 0; position: relative; overflow: hidden"
  >
    <!-- Elementos decorativos de fondo -->
    <div
      style="
        position: absolute;
        top: 0;
        left: -20%;
        width: 800px;
        height: 800px;
        background: radial-gradient(circle, rgba(33, 150, 243, 0.06) 0%, transparent 70%);
        filter: blur(100px);
      "
    ></div>
    <div
      style="
        position: absolute;
        bottom: 0;
        right: -20%;
        width: 800px;
        height: 800px;
        background: radial-gradient(circle, rgba(33, 150, 243, 0.06) 0%, transparent 70%);
        filter: blur(100px);
      "
    ></div>

    <v-container style="position: relative; z-index: 1; max-width: 1400px">
      <!-- Header de la sección -->
      <div class="text-center mb-16 fade-in" :class="{ visible: ventajasVisible }" style="margin-bottom: 100px !important">
        <div class="decorative-line"></div>
        <h2 style="font-size: clamp(2.5rem, 6vw, 4rem); font-weight: 800; margin-bottom: 32px; letter-spacing: -2px">
          <span class="gradient-text">¿Por Qué Elegirme?</span>
        </h2>
        <p
          style="
            color: rgba(255, 255, 255, 0.7);
            font-size: clamp(1.1rem, 2vw, 1.4rem);
            max-width: 800px;
            margin: 0 auto;
            line-height: 1.8;
            font-weight: 300;
          "
        >
          Un enfoque integral donde combino experiencia real de competencia, respaldo científico y un compromiso genuino con tu transformación
          sostenible
        </p>
      </div>

      <!-- ============================================ -->
      <!-- FILOSOFÍA PRINCIPAL - DESTACADA -->
      <!-- ============================================ -->
      <v-row justify="center" class="mb-16 fade-in" :class="{ visible: ventajasVisible }" style="margin-bottom: 120px !important">
        <v-col cols="12" lg="11">
          <div
            style="
              background: linear-gradient(135deg, rgba(33, 150, 243, 0.08) 0%, rgba(21, 101, 192, 0.04) 100%);
              border-radius: 32px;
              padding: 80px 60px;
              border: 2px solid rgba(33, 150, 243, 0.15);
              position: relative;
              overflow: hidden;
              box-shadow: 0 30px 60px rgba(0, 0, 0, 0.3);
            "
          >
            <!-- Brillo decorativo -->
            <div
              style="
                position: absolute;
                top: -100px;
                right: -100px;
                width: 400px;
                height: 400px;
                background: radial-gradient(circle, rgba(33, 150, 243, 0.15) 0%, transparent 70%);
                filter: blur(60px);
              "
            ></div>

            <div style="position: relative; z-index: 1">
              <div style="display: flex; align-items: center; gap: 24px; margin-bottom: 40px">
                <div
                  style="
                    background: linear-gradient(135deg, #2196f3 0%, #1565c0 100%);
                    width: 80px;
                    height: 80px;
                    border-radius: 20px;
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    box-shadow: 0 10px 30px rgba(33, 150, 243, 0.4);
                  "
                >
                  <v-icon size="45" color="white">mdi-heart-pulse</v-icon>
                </div>
                <h3 style="font-size: clamp(1.8rem, 4vw, 2.8rem); font-weight: 800; color: #fff; letter-spacing: -1px; margin: 0">
                  Mi Filosofía: Balance y Sostenibilidad
                </h3>
              </div>

              <div style="display: grid; gap: 32px">
                <p
                  style="font-size: clamp(1.1rem, 2vw, 1.3rem); line-height: 2; color: rgba(255, 255, 255, 0.9); font-weight: 300; margin: 0"
                >
                  <strong style="color: #64b5f6; font-weight: 600"
                    >El fitness no debe ser una carga en tu vida, sino una parte natural de ella.</strong
                  >
                  Mi enfoque se centra en crear planes que se integren perfectamente con tu rutina diaria, para que puedas mantener resultados
                  a largo plazo sin sacrificar tu vida social, familiar o profesional.
                </p>

                <p
                  style="
                    font-size: clamp(1.05rem, 2vw, 1.25rem);
                    line-height: 2;
                    color: rgba(255, 255, 255, 0.75);
                    font-weight: 300;
                    margin: 0;
                  "
                >
                  No busco clientes que sigan dietas extremas temporales.
                  <strong style="color: #fff"
                    >Busco personas comprometidas que quieran construir un estilo de vida saludable y sostenible.</strong
                  >
                </p>

                <div
                  style="
                    background: rgba(33, 150, 243, 0.1);
                    border-left: 4px solid #2196f3;
                    padding: 28px 32px;
                    border-radius: 12px;
                    margin-top: 16px;
                  "
                >
                  <p
                    style="
                      font-size: clamp(1rem, 2vw, 1.2rem);
                      color: #90caf9;
                      font-weight: 500;
                      margin: 0;
                      font-style: italic;
                      line-height: 1.8;
                    "
                  >
                    <v-icon size="24" color="blue" style="margin-right: 12px">mdi-format-quote-open</v-icon>
                    Se debe mantener una vida equilibrada y los planes que elaboro buscan ayudarte a encontrar ese equilibrio, para que esto
                    se convierta en parte de tu día a día sin que tenga que ser difícil para ti.
                  </p>
                </div>
              </div>
            </div>
          </div>
        </v-col>
      </v-row>

      <!-- ============================================ -->
      <!-- VENTAJA 1: ENTRENAMIENTO PERSONALIZADO -->
      <!-- ============================================ -->
      <v-row align="center" class="mb-16 fade-in-left" :class="{ visible: ventajasVisible }" style="margin-bottom: 140px !important">
        <!-- <v-col cols="12" md="6" class="pr-md-8">
          <div style="position: relative">

            <div style="position: relative; border-radius: 24px; overflow: hidden; box-shadow: 0 40px 80px rgba(0, 0, 0, 0.5)">
              <div
                style="
                  position: absolute;
                  inset: -4px;
                  background: linear-gradient(135deg, #2196f3, #1565c0);
                  border-radius: 24px;
                  opacity: 0.3;
                  filter: blur(20px);
                  z-index: -1;
                "
              ></div>
              <v-img

                src="https://images.unsplash.com/photo-1571019614242-c5c5dee9f50b?w=800&h=600&fit=crop"
                height="500"
                cover
                style="border-radius: 24px"
              >
                <div
                  style="
                    position: absolute;
                    inset: 0;
                    background: linear-gradient(135deg, rgba(33, 150, 243, 0.3) 0%, rgba(21, 101, 192, 0.2) 100%);
                  "
                ></div>
              </v-img>
            </div>
            <div
              style="
                position: absolute;
                bottom: 30px;
                right: 30px;
                background: rgba(0, 0, 0, 0.85);
                backdrop-filter: blur(20px);
                padding: 20px 28px;
                border-radius: 16px;
                border: 1px solid rgba(33, 150, 243, 0.3);
                box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
              "
            >
              <p style="margin: 0; font-size: 0.85rem; color: #90caf9; font-weight: 600; text-transform: uppercase; letter-spacing: 1px">
                100% Personalizado
              </p>
            </div>
          </div>
        </v-col> -->

        <v-col cols="12" md="12" class="pl-md-8">
          <div style="padding: 40px 0">
            <!-- Icono y título -->
            <div style="display: flex; align-items: flex-start; gap: 20px; margin-bottom: 40px">
              <div
                style="
                  background: linear-gradient(135deg, #2196f3 0%, #1565c0 100%);
                  width: 70px;
                  height: 70px;
                  border-radius: 16px;
                  display: flex;
                  align-items: center;
                  justify-content: center;
                  flex-shrink: 0;
                  box-shadow: 0 10px 30px rgba(33, 150, 243, 0.4);
                "
              >
                <v-icon size="36" color="white">mdi-account-heart</v-icon>
              </div>
              <div>
                <h3
                  style="
                    font-size: clamp(1.8rem, 3vw, 2.5rem);
                    font-weight: 800;
                    color: #fff;
                    line-height: 1.2;
                    margin: 0 0 12px 0;
                    letter-spacing: -1px;
                  "
                >
                  Entrenamiento 100% Personalizado
                </h3>
                <div style="width: 80px; height: 4px; background: linear-gradient(90deg, #2196f3, transparent); border-radius: 2px"></div>
              </div>
            </div>

            <!-- Contenido -->
            <div style="display: flex; flex-direction: column; gap: 28px">
              <p
                style="font-size: clamp(1.05rem, 2vw, 1.2rem); line-height: 1.9; color: rgba(255, 255, 255, 0.9); margin: 0; font-weight: 300"
              >
                <strong style="color: #64b5f6; font-weight: 600">Cada persona es completamente diferente:</strong> tu genética, metabolismo,
                horarios, experiencia previa y objetivos son únicos. Por eso, no creo en los planes genéricos que se copian y pegan.
              </p>

              <p
                style="
                  font-size: clamp(1.05rem, 2vw, 1.2rem);
                  line-height: 1.9;
                  color: rgba(255, 255, 255, 0.75);
                  margin: 0;
                  font-weight: 300;
                "
              >
                A partir de un <strong style="color: #fff">formulario inicial detallado y evaluaciones continuas</strong>, diseño un plan
                específico para ti que considera tus limitaciones, disponibilidad de tiempo y equipo de entrenamiento.
                <span style="color: #90caf9">Tu plan evoluciona contigo.</span>
              </p>

              <!-- Feature boxes -->
              <div style="display: grid; gap: 16px; margin-top: 12px">
                <div
                  style="
                    display: flex;
                    align-items: center;
                    gap: 16px;
                    background: rgba(33, 150, 243, 0.06);
                    padding: 18px 24px;
                    border-radius: 12px;
                    border-left: 3px solid #2196f3;
                  "
                >
                  <v-icon size="24" color="blue">mdi-check-circle</v-icon>
                  <span style="font-size: 1.05rem; color: #e0e0e0; font-weight: 400">Evaluación inicial completa</span>
                </div>
                <div
                  style="
                    display: flex;
                    align-items: center;
                    gap: 16px;
                    background: rgba(33, 150, 243, 0.06);
                    padding: 18px 24px;
                    border-radius: 12px;
                    border-left: 3px solid #2196f3;
                  "
                >
                  <v-icon size="24" color="blue">mdi-check-circle</v-icon>
                  <span style="font-size: 1.05rem; color: #e0e0e0; font-weight: 400">Ajustes según tu progreso y respuesta</span>
                </div>
                <div
                  style="
                    display: flex;
                    align-items: center;
                    gap: 16px;
                    background: rgba(33, 150, 243, 0.06);
                    padding: 18px 24px;
                    border-radius: 12px;
                    border-left: 3px solid #2196f3;
                  "
                >
                  <v-icon size="24" color="blue">mdi-check-circle</v-icon>
                  <span style="font-size: 1.05rem; color: #e0e0e0; font-weight: 400">Adaptación a tu estilo de vida y horarios reales</span>
                </div>
              </div>
            </div>
          </div>
        </v-col>
      </v-row>

      <!-- ============================================ -->
      <!-- VENTAJA 2: EXPERIENCIA REAL DE COMPETENCIA -->
      <!-- ============================================ -->
      <v-row align="center" class="mb-16 fade-in-right" :class="{ visible: ventajasVisible }" style="margin-bottom: 140px !important">
        <v-col cols="12" md="6" :order="$vuetify.display.mdAndUp ? 2 : 1" class="pl-md-8">
          <div style="position: relative">
            <div style="position: relative; border-radius: 24px; overflow: hidden; box-shadow: 0 40px 80px rgba(0, 0, 0, 0.5)">
              <div
                style="
                  position: absolute;
                  inset: -4px;
                  background: linear-gradient(135deg, #2196f3, #1565c0);
                  border-radius: 24px;
                  opacity: 0.3;
                  filter: blur(20px);
                  z-index: -1;
                "
              ></div>
              <v-img src="/assets/imgs/fernando_ruelas_trofeos.png" height="500" cover style="border-radius: 24px">
                <div
                  style="
                    position: absolute;
                    inset: 0;
                    background: linear-gradient(135deg, rgba(33, 150, 243, 0.3) 0%, rgba(21, 101, 192, 0.2) 100%);
                  "
                ></div>
              </v-img>
            </div>
            <div
              style="
                position: absolute;
                bottom: 30px;
                left: 30px;
                background: rgba(0, 0, 0, 0.85);
                backdrop-filter: blur(20px);
                padding: 20px 28px;
                border-radius: 16px;
                border: 1px solid rgba(255, 193, 7, 0.3);
                box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
              "
            >
              <p style="margin: 0; font-size: 0.85rem; color: #ffd54f; font-weight: 600; text-transform: uppercase; letter-spacing: 1px">
                <v-icon size="18" color="amber" style="margin-right: 8px">mdi-trophy</v-icon>
                8+ Competencias
              </p>
            </div>
          </div>
        </v-col>

        <v-col cols="12" md="6" :order="$vuetify.display.mdAndUp ? 1 : 2" class="pr-md-8">
          <div style="padding: 40px 0">
            <div style="display: flex; align-items: flex-start; gap: 20px; margin-bottom: 40px">
              <div
                style="
                  background: linear-gradient(135deg, #ffb300 0%, #ff6f00 100%);
                  width: 70px;
                  height: 70px;
                  border-radius: 16px;
                  display: flex;
                  align-items: center;
                  justify-content: center;
                  flex-shrink: 0;
                  box-shadow: 0 10px 30px rgba(255, 179, 0, 0.4);
                "
              >
                <v-icon size="36" color="white">mdi-trophy-variant</v-icon>
              </div>
              <div>
                <h3
                  style="
                    font-size: clamp(1.8rem, 3vw, 2.5rem);
                    font-weight: 800;
                    color: #fff;
                    line-height: 1.2;
                    margin: 0 0 12px 0;
                    letter-spacing: -1px;
                  "
                >
                  Experiencia Real de Competencia
                </h3>
                <div style="width: 80px; height: 4px; background: linear-gradient(90deg, #ffb300, transparent); border-radius: 2px"></div>
              </div>
            </div>

            <div style="display: flex; flex-direction: column; gap: 28px">
              <p
                style="font-size: clamp(1.05rem, 2vw, 1.2rem); line-height: 1.9; color: rgba(255, 255, 255, 0.9); margin: 0; font-weight: 300"
              >
                <strong style="color: #ffd54f; font-weight: 600">No solo lo estudié, lo viví en el escenario.</strong>
                He competido en más de 8 ocasiones, pasando por procesos de volumen extremo, cortes agresivos, peak weeks y todo lo que
                conlleva la preparación de alto nivel.
              </p>

              <p
                style="
                  font-size: clamp(1.05rem, 2vw, 1.2rem);
                  line-height: 1.9;
                  color: rgba(255, 255, 255, 0.75);
                  margin: 0;
                  font-weight: 300;
                "
              >
                Cometí errores costosos que me enseñaron lecciones invaluables: desde sobreentrenamiento hasta errores dietéticos que me
                costaron semanas de progreso. <strong style="color: #fff">Mi misión es que tú evites esos errores</strong> y aceleres tu
                camino hacia tus metas, aprendiendo de mi experiencia práctica.
              </p>

              <div style="display: grid; gap: 16px; margin-top: 12px">
                <div
                  style="
                    display: flex;
                    align-items: center;
                    gap: 16px;
                    background: rgba(255, 179, 0, 0.06);
                    padding: 18px 24px;
                    border-radius: 12px;
                    border-left: 3px solid #ffb300;
                  "
                >
                  <v-icon size="24" color="amber">mdi-medal</v-icon>
                  <span style="font-size: 1.05rem; color: #e0e0e0; font-weight: 400">Múltiples podios y campeonatos absolutos</span>
                </div>
                <div
                  style="
                    display: flex;
                    align-items: center;
                    gap: 16px;
                    background: rgba(255, 179, 0, 0.06);
                    padding: 18px 24px;
                    border-radius: 12px;
                    border-left: 3px solid #ffb300;
                  "
                >
                  <v-icon size="24" color="amber">mdi-lightbulb-on</v-icon>
                  <span style="font-size: 1.05rem; color: #e0e0e0; font-weight: 400">Errores superados que ahora son tu ventaja</span>
                </div>
                <div
                  style="
                    display: flex;
                    align-items: center;
                    gap: 16px;
                    background: rgba(255, 179, 0, 0.06);
                    padding: 18px 24px;
                    border-radius: 12px;
                    border-left: 3px solid #ffb300;
                  "
                >
                  <v-icon size="24" color="amber">mdi-dumbbell</v-icon>
                  <span style="font-size: 1.05rem; color: #e0e0e0; font-weight: 400">Estrategias probadas en competencia de alto nivel</span>
                </div>
              </div>
            </div>
          </div>
        </v-col>
      </v-row>

      <!-- ============================================ -->
      <!-- VENTAJA 3: RESPALDO CIENTÍFICO -->
      <!-- ============================================ -->
      <v-row align="center" class="mb-16 fade-in-left" :class="{ visible: ventajasVisible }" style="margin-bottom: 140px !important">
        <v-col cols="12" md="6" class="pr-md-8">
          <div style="position: relative">
            <div style="position: relative; border-radius: 24px; overflow: hidden; box-shadow: 0 40px 80px rgba(0, 0, 0, 0.5)">
              <div
                style="
                  position: absolute;
                  inset: -4px;
                  background: linear-gradient(135deg, #2196f3, #1565c0);
                  border-radius: 24px;
                  opacity: 0.3;
                  filter: blur(20px);
                  z-index: -1;
                "
              ></div>
              <v-img src="/assets/imgs/certificados.png" height="500" cover style="border-radius: 24px">
                <div
                  style="
                    position: absolute;
                    inset: 0;
                    background: linear-gradient(135deg, rgba(33, 150, 243, 0.3) 0%, rgba(21, 101, 192, 0.2) 100%);
                  "
                ></div>
              </v-img>
            </div>
            <div
              style="
                position: absolute;
                bottom: 30px;
                right: 30px;
                background: rgba(0, 0, 0, 0.85);
                backdrop-filter: blur(20px);
                padding: 20px 28px;
                border-radius: 16px;
                border: 1px solid rgba(76, 175, 80, 0.3);
                box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
              "
            >
              <p style="margin: 0; font-size: 0.85rem; color: #81c784; font-weight: 600; text-transform: uppercase; letter-spacing: 1px">
                <v-icon size="18" color="green" style="margin-right: 8px">mdi-certificate</v-icon>
                Certificado WABBA
              </p>
            </div>
          </div>
        </v-col>

        <v-col cols="12" md="6" class="pl-md-8">
          <div style="padding: 40px 0">
            <div style="display: flex; align-items: flex-start; gap: 20px; margin-bottom: 40px">
              <div
                style="
                  background: linear-gradient(135deg, #4caf50 0%, #2e7d32 100%);
                  width: 70px;
                  height: 70px;
                  border-radius: 16px;
                  display: flex;
                  align-items: center;
                  justify-content: center;
                  flex-shrink: 0;
                  box-shadow: 0 10px 30px rgba(76, 175, 80, 0.4);
                "
              >
                <v-icon size="36" color="white">mdi-school</v-icon>
              </div>
              <div>
                <h3
                  style="
                    font-size: clamp(1.8rem, 3vw, 2.5rem);
                    font-weight: 800;
                    color: #fff;
                    line-height: 1.2;
                    margin: 0 0 12px 0;
                    letter-spacing: -1px;
                  "
                >
                  Respaldo Científico y Certificaciones
                </h3>
                <div style="width: 80px; height: 4px; background: linear-gradient(90deg, #4caf50, transparent); border-radius: 2px"></div>
              </div>
            </div>

            <div style="display: flex; flex-direction: column; gap: 28px">
              <p
                style="font-size: clamp(1.05rem, 2vw, 1.2rem); line-height: 1.9; color: rgba(255, 255, 255, 0.9); margin: 0; font-weight: 300"
              >
                Cuento con
                <strong style="color: #81c784; font-weight: 600"
                  >certificaciones internacionales en nutrición deportiva y nutrición aplicada al fisicoculturismo</strong
                >, respaldadas por FISICOCULTURISMO MEXICO S.C afiliado a WABBA INTERNATIONAL. Combino este conocimiento académico con años de
                estudio continuo y actualización constante.
              </p>

              <p
                style="
                  font-size: clamp(1.05rem, 2vw, 1.2rem);
                  line-height: 1.9;
                  color: rgba(255, 255, 255, 0.75);
                  margin: 0;
                  font-weight: 300;
                "
              >
                No me baso en tendencias ni modas pasajeras.
                <strong style="color: #fff">Cada recomendación que te doy está fundamentada en evidencia científica</strong>, adaptada a la
                práctica real y probada en resultados medibles. Tu progreso se basa en hechos, no en suposiciones.
              </p>

              <div style="display: grid; gap: 16px; margin-top: 12px">
                <div
                  style="
                    display: flex;
                    align-items: center;
                    gap: 16px;
                    background: rgba(76, 175, 80, 0.06);
                    padding: 18px 24px;
                    border-radius: 12px;
                    border-left: 3px solid #4caf50;
                  "
                >
                  <v-icon size="24" color="green">mdi-certificate-outline</v-icon>
                  <span style="font-size: 1.05rem; color: #e0e0e0; font-weight: 400"
                    >Certificaciones internacionales vigentes y actualizadas</span
                  >
                </div>
                <div
                  style="
                    display: flex;
                    align-items: center;
                    gap: 16px;
                    background: rgba(76, 175, 80, 0.06);
                    padding: 18px 24px;
                    border-radius: 12px;
                    border-left: 3px solid #4caf50;
                  "
                >
                  <v-icon size="24" color="green">mdi-book-open-variant</v-icon>
                  <span style="font-size: 1.05rem; color: #e0e0e0; font-weight: 400">Estudio continuo de las últimas investigaciones</span>
                </div>
                <div
                  style="
                    display: flex;
                    align-items: center;
                    gap: 16px;
                    background: rgba(76, 175, 80, 0.06);
                    padding: 18px 24px;
                    border-radius: 12px;
                    border-left: 3px solid #4caf50;
                  "
                >
                  <v-icon size="24" color="green">mdi-flask</v-icon>
                  <span style="font-size: 1.05rem; color: #e0e0e0; font-weight: 400">Métodos basados en evidencia científica sólida</span>
                </div>
              </div>
            </div>
          </div>
        </v-col>
      </v-row>

      <!-- ============================================ -->
      <!-- VENTAJA 4: ACOMPAÑAMIENTO CONSTANTE -->
      <!-- ============================================ -->
      <v-row align="center" class="mb-16 fade-in-right" :class="{ visible: ventajasVisible }" style="margin-bottom: 140px !important">
        <!-- <v-col cols="12" md="6" :order="$vuetify.display.mdAndUp ? 2 : 1" class="pl-md-8">
          <div style="position: relative">
            <div style="position: relative; border-radius: 24px; overflow: hidden; box-shadow: 0 40px 80px rgba(0, 0, 0, 0.5)">
              <div
                style="
                  position: absolute;
                  inset: -4px;
                  background: linear-gradient(135deg, #2196f3, #1565c0);
                  border-radius: 24px;
                  opacity: 0.3;
                  filter: blur(20px);
                  z-index: -1;
                "
              ></div>
              <v-img
                src="https://images.unsplash.com/photo-1517836357463-d25dfeac3438?w=800&h=600&fit=crop"
                height="500"
                cover
                style="border-radius: 24px"
              >
                <div
                  style="
                    position: absolute;
                    inset: 0;
                    background: linear-gradient(135deg, rgba(33, 150, 243, 0.3) 0%, rgba(21, 101, 192, 0.2) 100%);
                  "
                ></div>
              </v-img>
            </div>
            <div
              style="
                position: absolute;
                bottom: 30px;
                left: 30px;
                background: rgba(0, 0, 0, 0.85);
                backdrop-filter: blur(20px);
                padding: 20px 28px;
                border-radius: 16px;
                border: 1px solid rgba(156, 39, 176, 0.3);
                box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
              "
            >
              <p style="margin: 0; font-size: 0.85rem; color: #ce93d8; font-weight: 600; text-transform: uppercase; letter-spacing: 1px">
                <v-icon size="18" color="purple" style="margin-right: 8px">mdi-chat</v-icon>
                Soporte 24/7
              </p>
            </div>
          </div>
        </v-col> -->

        <v-col cols="12" md="12" :order="$vuetify.display.mdAndUp ? 1 : 2" class="pr-md-8">
          <div style="padding: 40px 0">
            <div style="display: flex; align-items: flex-start; gap: 20px; margin-bottom: 40px">
              <div
                style="
                  background: linear-gradient(135deg, #9c27b0 0%, #6a1b9a 100%);
                  width: 70px;
                  height: 70px;
                  border-radius: 16px;
                  display: flex;
                  align-items: center;
                  justify-content: center;
                  flex-shrink: 0;
                  box-shadow: 0 10px 30px rgba(156, 39, 176, 0.4);
                "
              >
                <v-icon size="36" color="white">mdi-message-text</v-icon>
              </div>
              <div>
                <h3
                  style="
                    font-size: clamp(1.8rem, 3vw, 2.5rem);
                    font-weight: 800;
                    color: #fff;
                    line-height: 1.2;
                    margin: 0 0 12px 0;
                    letter-spacing: -1px;
                  "
                >
                  Acompañamiento en Cada Paso
                </h3>
                <div style="width: 80px; height: 4px; background: linear-gradient(90deg, #9c27b0, transparent); border-radius: 2px"></div>
              </div>
            </div>

            <div style="display: flex; flex-direction: column; gap: 28px">
              <p
                style="font-size: clamp(1.05rem, 2vw, 1.2rem); line-height: 1.9; color: rgba(255, 255, 255, 0.9); margin: 0; font-weight: 300"
              >
                <strong style="color: #ce93d8; font-weight: 600">No te dejo solo con un plan esperando milagros.</strong> Estaré contigo
                constantemente para resolver dudas, ajustar tu programa según tu progreso, motivarte en los momentos difíciles y celebrar tus
                logros.
              </p>

              <p
                style="
                  font-size: clamp(1.05rem, 2vw, 1.2rem);
                  line-height: 1.9;
                  color: rgba(255, 255, 255, 0.75);
                  margin: 0;
                  font-weight: 300;
                "
              >
                A través de
                <strong style="color: #fff">seguimiento continuo, formularios de progreso y evaluaciones periódicas</strong>, monitoreo cada
                aspecto de tu transformación. Si algo no funciona, lo ajustamos de inmediato. Si algo está funcionando bien, lo optimizamos
                aún más.
              </p>

              <div style="display: grid; gap: 16px; margin-top: 12px">
                <div
                  style="
                    display: flex;
                    align-items: center;
                    gap: 16px;
                    background: rgba(156, 39, 176, 0.06);
                    padding: 18px 24px;
                    border-radius: 12px;
                    border-left: 3px solid #9c27b0;
                  "
                >
                  <v-icon size="24" color="purple">mdi-clock-fast</v-icon>
                  <span style="font-size: 1.05rem; color: #e0e0e0; font-weight: 400">Respuesta rápida a tus consultas</span>
                </div>
                <div
                  style="
                    display: flex;
                    align-items: center;
                    gap: 16px;
                    background: rgba(156, 39, 176, 0.06);
                    padding: 18px 24px;
                    border-radius: 12px;
                    border-left: 3px solid #9c27b0;
                  "
                >
                  <v-icon size="24" color="purple">mdi-chart-timeline-variant</v-icon>
                  <span style="font-size: 1.05rem; color: #e0e0e0; font-weight: 400">Seguimiento detallado de tu progreso</span>
                </div>
                <div
                  style="
                    display: flex;
                    align-items: center;
                    gap: 16px;
                    background: rgba(156, 39, 176, 0.06);
                    padding: 18px 24px;
                    border-radius: 12px;
                    border-left: 3px solid #9c27b0;
                  "
                >
                  <v-icon size="24" color="purple">mdi-tune</v-icon>
                  <span style="font-size: 1.05rem; color: #e0e0e0; font-weight: 400">Ajustes oportunos cuando los necesites</span>
                </div>
              </div>
            </div>
          </div>
        </v-col>
      </v-row>

      <!-- ============================================ -->
      <!-- VENTAJA 5: RESULTADOS SOSTENIBLES -->
      <!-- ============================================ -->
      <v-row align="center" class="mb-16 fade-in-left" :class="{ visible: ventajasVisible }" style="margin-bottom: 100px !important">
        <v-col cols="12" md="6" class="pr-md-8">
          <div style="position: relative">
            <div style="position: relative; border-radius: 24px; overflow: hidden; box-shadow: 0 40px 80px rgba(0, 0, 0, 0.5)">
              <div
                style="
                  position: absolute;
                  inset: -4px;
                  background: linear-gradient(135deg, #2196f3, #1565c0);
                  border-radius: 24px;
                  opacity: 0.3;
                  filter: blur(20px);
                  z-index: -1;
                "
              ></div>
              <v-img src="/assets/imgs/fernando_ruelas_comida.jpeg" height="500" cover style="border-radius: 24px">
                <div
                  style="
                    position: absolute;
                    inset: 0;
                    background: linear-gradient(135deg, rgba(33, 150, 243, 0.3) 0%, rgba(21, 101, 192, 0.2) 100%);
                  "
                ></div>
              </v-img>
            </div>
            <div
              style="
                position: absolute;
                bottom: 30px;

                background: rgba(0, 0, 0, 0.85);
                backdrop-filter: blur(20px);
                padding: 20px 28px;
                border-radius: 16px;
                border: 1px solid rgba(33, 150, 243, 0.3);
                box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
              "
            >
              <p style="margin: 0; font-size: 0.85rem; color: #64b5f6; font-weight: 600; text-transform: uppercase; letter-spacing: 1px">
                <v-icon size="18" color="blue" style="margin-right: 8px">mdi-infinity</v-icon>
                Largo Plazo
              </p>
            </div>
          </div>
        </v-col>

        <v-col cols="12" md="6" class="pl-md-8">
          <div style="padding: 40px 0">
            <div style="display: flex; align-items: flex-start; gap: 20px; margin-bottom: 40px">
              <div
                style="
                  background: linear-gradient(135deg, #2196f3 0%, #1565c0 100%);
                  width: 70px;
                  height: 70px;
                  border-radius: 16px;
                  display: flex;
                  align-items: center;
                  justify-content: center;
                  flex-shrink: 0;
                  box-shadow: 0 10px 30px rgba(33, 150, 243, 0.4);
                "
              >
                <v-icon size="36" color="white">mdi-trending-up</v-icon>
              </div>
              <div>
                <h3
                  style="
                    font-size: clamp(1.8rem, 3vw, 2.5rem);
                    font-weight: 800;
                    color: #fff;
                    line-height: 1.2;
                    margin: 0 0 12px 0;
                    letter-spacing: -1px;
                  "
                >
                  Enfoque en Resultados Sostenibles
                </h3>
                <div style="width: 80px; height: 4px; background: linear-gradient(90deg, #2196f3, transparent); border-radius: 2px"></div>
              </div>
            </div>

            <div style="display: flex; flex-direction: column; gap: 28px">
              <p
                style="font-size: clamp(1.05rem, 2vw, 1.2rem); line-height: 1.9; color: rgba(255, 255, 255, 0.9); margin: 0; font-weight: 300"
              >
                Mi objetivo
                <strong style="color: #64b5f6; font-weight: 600">no es que bajes 10 kilos en un mes para recuperarlos al siguiente.</strong>
                Busco transformaciones reales y duraderas que puedas mantener a largo plazo sin sufrir en el proceso.
              </p>

              <p
                style="
                  font-size: clamp(1.05rem, 2vw, 1.2rem);
                  line-height: 1.9;
                  color: rgba(255, 255, 255, 0.75);
                  margin: 0;
                  font-weight: 300;
                "
              >
                Creo en la construcción de hábitos saludables, no en restricciones extremas.
                <strong style="color: #fff">Te enseño a entender tu cuerpo</strong>, a tomar decisiones informadas sobre tu alimentación y
                entrenamiento, y a crear un estilo de vida que puedas mantener.
              </p>

              <div style="display: grid; gap: 16px; margin-top: 12px">
                <div
                  style="
                    display: flex;
                    align-items: center;
                    gap: 16px;
                    background: rgba(33, 150, 243, 0.06);
                    padding: 18px 24px;
                    border-radius: 12px;
                    border-left: 3px solid #2196f3;
                  "
                >
                  <v-icon size="24" color="blue">mdi-target</v-icon>
                  <span style="font-size: 1.05rem; color: #e0e0e0; font-weight: 400"
                    >Educación continua para mantener resultados de por vida</span
                  >
                </div>
                <div
                  style="
                    display: flex;
                    align-items: center;
                    gap: 16px;
                    background: rgba(33, 150, 243, 0.06);
                    padding: 18px 24px;
                    border-radius: 12px;
                    border-left: 3px solid #2196f3;
                  "
                >
                  <v-icon size="24" color="blue">mdi-food-apple</v-icon>
                  <span style="font-size: 1.05rem; color: #e0e0e0; font-weight: 400">Hábitos saludables sin restricciones extremas</span>
                </div>
                <div
                  style="
                    display: flex;
                    align-items: center;
                    gap: 16px;
                    background: rgba(33, 150, 243, 0.06);
                    padding: 18px 24px;
                    border-radius: 12px;
                    border-left: 3px solid #2196f3;
                  "
                >
                  <v-icon size="24" color="blue">mdi-calendar-check</v-icon>
                  <span style="font-size: 1.05rem; color: #e0e0e0; font-weight: 400">Transformación real</span>
                </div>
              </div>
            </div>
          </div>
        </v-col>
      </v-row>

      <!-- ============================================ -->
      <!-- VENTAJA 6: APP PERSONALIZADA -->
      <!-- ============================================ -->
      <v-row align="center" class="mb-16 fade-in" :class="{ visible: ventajasVisible }" style="margin-bottom: 140px !important">
        <v-col cols="12" class="text-center mb-8">
          <div style="display: flex; align-items: center; justify-content: center; gap: 20px; margin-bottom: 24px">
            <div
              style="
                background: linear-gradient(135deg, #2196f3 0%, #1565c0 100%);
                width: 70px;
                height: 70px;
                border-radius: 16px;
                display: flex;
                align-items: center;
                justify-content: center;
                flex-shrink: 0;
                box-shadow: 0 10px 30px rgba(33, 150, 243, 0.4);
              "
            >
              <v-icon size="36" color="white">mdi-cellphone-check</v-icon>
            </div>
            <h3
              style="
                font-size: clamp(1.8rem, 3.5vw, 2.8rem);
                font-weight: 800;
                color: #fff;
                letter-spacing: -1px;
                margin: 0;
              "
            >
              Tu Plan Siempre a la Mano
            </h3>
          </div>
          <p
            style="
              font-size: clamp(1.05rem, 2vw, 1.25rem);
              line-height: 1.9;
              color: rgba(255, 255, 255, 0.8);
              max-width: 800px;
              margin: 0 auto 16px;
              font-weight: 300;
            "
          >
            Todos mis clientes tienen acceso a una <strong style="color: #fff">aplicación personalizada</strong> donde subo
            toda su información: rutinas de entrenamiento, plan de nutrición, y
            <strong style="color: #64b5f6">videos de ejemplo de cada ejercicio</strong> para que puedas seguir tu plan
            con total claridad desde cualquier lugar.
          </p>
          <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 16px; margin-top: 24px; margin-bottom: 48px">
            <div style="display: flex; align-items: center; gap: 10px; background: rgba(33,150,243,0.08); padding: 12px 20px; border-radius: 10px; border-left: 3px solid #2196f3">
              <v-icon size="20" color="blue">mdi-dumbbell</v-icon>
              <span style="color: #e0e0e0; font-size: 0.95rem">Rutinas detalladas</span>
            </div>
            <div style="display: flex; align-items: center; gap: 10px; background: rgba(33,150,243,0.08); padding: 12px 20px; border-radius: 10px; border-left: 3px solid #2196f3">
              <v-icon size="20" color="blue">mdi-food-apple</v-icon>
              <span style="color: #e0e0e0; font-size: 0.95rem">Plan nutricional</span>
            </div>
            <div style="display: flex; align-items: center; gap: 10px; background: rgba(33,150,243,0.08); padding: 12px 20px; border-radius: 10px; border-left: 3px solid #2196f3">
              <v-icon size="20" color="blue">mdi-play-circle</v-icon>
              <span style="color: #e0e0e0; font-size: 0.95rem">Videos de ejemplo</span>
            </div>
            <div style="display: flex; align-items: center; gap: 10px; background: rgba(33,150,243,0.08); padding: 12px 20px; border-radius: 10px; border-left: 3px solid #2196f3">
              <v-icon size="20" color="blue">mdi-chart-line</v-icon>
              <span style="color: #e0e0e0; font-size: 0.95rem">Seguimiento de progreso</span>
            </div>
          </div>
        </v-col>

        <!-- Galería de imágenes de la app -->
        <v-col cols="12">
          <v-row justify="center" style="gap: 0">
            <v-col cols="12" sm="6" md="4" v-for="(img, i) in appImagenes" :key="i">
              <div
                style="
                  border-radius: 20px;
                  overflow: hidden;
                  border: 1px solid rgba(33, 150, 243, 0.2);
                  box-shadow: 0 20px 50px rgba(0, 0, 0, 0.4);
                  margin: 8px;
                "
              >
                <v-img :src="img.src" :alt="img.alt" contain>
                  <div
                    style="
                      position: absolute;
                      bottom: 0;
                      left: 0;
                      right: 0;
                      padding: 16px 20px;
                      background: linear-gradient(transparent, rgba(0,0,0,0.8));
                    "
                  >
                    <p style="margin: 0; font-size: 0.9rem; color: rgba(255,255,255,0.9); font-weight: 500">{{ img.alt }}</p>
                  </div>
                </v-img>
              </div>
            </v-col>
          </v-row>
        </v-col>
      </v-row>

      <!-- ============================================ -->
      <!-- CTA FINAL IMPACTANTE -->
      <!-- ============================================ -->
      <v-row justify="center" class="fade-in scale-in" :class="{ visible: ventajasVisible }">
        <v-col cols="12" lg="10">
          <div
            style="
              background: linear-gradient(135deg, rgba(33, 150, 243, 0.15) 0%, rgba(21, 101, 192, 0.08) 100%);
              border-radius: 32px;
              padding: 80px 60px;
              text-align: center;
              border: 2px solid rgba(33, 150, 243, 0.2);
              position: relative;
              overflow: hidden;
              box-shadow: 0 30px 60px rgba(0, 0, 0, 0.3);
            "
          >
            <div
              style="
                position: absolute;
                top: -100px;
                left: 50%;
                transform: translateX(-50%);
                width: 500px;
                height: 500px;
                background: radial-gradient(circle, rgba(33, 150, 243, 0.2) 0%, transparent 70%);
                filter: blur(80px);
              "
            ></div>

            <div style="position: relative; z-index: 1">
              <v-icon size="60" color="blue" style="margin-bottom: 32px; opacity: 0.9">mdi-rocket-launch</v-icon>

              <h3
                style="
                  font-size: clamp(2rem, 4vw, 3.2rem);
                  font-weight: 800;
                  margin-bottom: 24px;
                  color: #fff;
                  letter-spacing: -1px;
                  line-height: 1.2;
                "
              >
                ¿Listo para Comenzar tu Transformación?
              </h3>

              <p
                style="
                  font-size: clamp(1.15rem, 2vw, 1.5rem);
                  color: rgba(255, 255, 255, 0.8);
                  margin-bottom: 16px;
                  line-height: 1.7;
                  font-weight: 300;
                  max-width: 800px;
                  margin-left: auto;
                  margin-right: auto;
                "
              >
                No importa dónde estés ahora, lo importante es hacia dónde quieres ir.
              </p>

              <p style="font-size: clamp(1.3rem, 2.5vw, 1.8rem); color: #64b5f6; margin-bottom: 48px; font-weight: 600; font-style: italic">
                Yo te llevaré ahí con un plan diseñado específicamente para ti.
              </p>

              <v-btn
                href="#planes"
                size="x-large"
                color="blue"
                class="minimal-btn"
                style="
                  text-transform: none;
                  font-weight: 700;
                  letter-spacing: 0;
                  font-size: 1.15rem;
                  box-shadow: 0 15px 40px rgba(33, 150, 243, 0.4);
                "
              >
                <v-icon left size="28">mdi-arrow-right-circle</v-icon>
                Ver Planes y Comenzar Ahora
              </v-btn>
            </div>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'VentajasSection',
  data() {
    return {
      ventajasVisible: true,
      appImagenes: [
        { src: '/assets/imgs/app1.jpg', alt: 'Rutinas de entrenamiento' },
        { src: '/assets/imgs/app2.jpg', alt: 'Videos de ejemplo' },
        { src: '/assets/imgs/app3.jpg', alt: 'Plan nutricional ' },
      ],
      ventajas: [
        {
          icono: "mdi-trending-up",
          titulo: "Eficiencia Comprobada",
          descripcion: "Estrategias probadas que evitan errores costosos y aceleran tus resultados.",
        },
        {
          icono: "mdi-account-heart",
          titulo: "100% Personalizado",
          descripcion: "Planes adaptados a tu vida, objetivos y necesidades específicas.",
        },
        {
          icono: "mdi-chat",
          titulo: "Acompañamiento",
          descripcion: "Estaré contigo en cada paso del camino hacia tu meta.",
        },
        {
          icono: "mdi-trophy",
          titulo: "Experiencia Real",
          descripcion: "Basado en competencia y certificación profesional.",
        },
      ],
    }
  },
  mounted() {
    const observer = new IntersectionObserver(
      ([entry]) => { if (entry.isIntersecting) this.ventajasVisible = true },
      { threshold: 0 }
    )
    observer.observe(this.$el)
  },
}
</script>
