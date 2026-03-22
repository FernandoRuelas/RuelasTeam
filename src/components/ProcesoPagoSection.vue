<template>
  <section id="comoComenzamos" style="background: #000; padding: 100px 0; position: relative; overflow: hidden;">
    <!-- Fondo decorativo -->
    <div style="
      position: absolute; inset: 0;
      background: radial-gradient(ellipse 80% 60% at 50% 50%, rgba(33,150,243,0.07) 0%, transparent 70%);
      pointer-events: none;
    "></div>

    <v-container style="position: relative; z-index: 1;">
      <!-- Encabezado -->
      <div class="text-center mb-12">
        <div style="
          display: inline-flex; align-items: center; gap: 10px;
          background: rgba(33,150,243,0.1);
          border: 1px solid rgba(33,150,243,0.25);
          border-radius: 100px;
          padding: 8px 22px;
          margin-bottom: 28px;
        ">
          <v-icon size="16" color="blue">mdi-information-outline</v-icon>
          <span style="color: #64b5f6; font-size: 0.82rem; font-weight: 600; letter-spacing: 1.5px; text-transform: uppercase;">Proceso de Inicio</span>
        </div>
        <h2 style="font-size: clamp(2rem, 5vw, 3rem); font-weight: 800; letter-spacing: -1px; margin-bottom: 16px;">
          <span class="gradient-text">¿Cómo Empezamos?</span>
        </h2>
        <p style="color: rgba(255,255,255,0.5); font-size: 1.05rem; max-width: 520px; margin: 0 auto; line-height: 1.7;">
          Una vez que elijas tu plan, el proceso es simple. Sigue estos pasos y en cuestión de horas estarás en camino a tu transformación.
        </p>
      </div>

      <!-- Steps -->
      <v-row justify="center" style="margin-bottom: 56px;">
        <v-col cols="12" lg="10">
          <div style="display: flex; flex-direction: column; gap: 0;">

            <!-- Paso 1 -->
            <div style="display: flex; gap: 24px; align-items: flex-start; padding: 32px 0; border-bottom: 1px solid rgba(255,255,255,0.06);">
              <div style="flex-shrink: 0; display: flex; flex-direction: column; align-items: center;">
                <div style="
                  width: 52px; height: 52px;
                  background: linear-gradient(135deg, #1565c0, #2196f3);
                  border-radius: 14px;
                  display: flex; align-items: center; justify-content: center;
                  font-size: 1.3rem; font-weight: 800; color: #fff;
                  box-shadow: 0 8px 24px rgba(33,150,243,0.3);
                ">1</div>
              </div>
              <div style="flex: 1; padding-top: 8px;">
                <div style="display: flex; align-items: center; gap: 12px; margin-bottom: 8px;">
                  <v-icon color="blue" size="20">mdi-credit-card-outline</v-icon>
                  <h3 style="font-size: 1.2rem; font-weight: 700; color: #fff;">Realiza el pago de tu plan</h3>
                </div>
                <p style="color: rgba(255,255,255,0.55); line-height: 1.7; font-size: 0.97rem; margin: 0;">
                  Selecciona el plan que mejor se adapte a tus objetivos y realiza el pago. Recibirás un correo de confirmación con tu comprobante —
                  <span style="color: rgba(255,255,255,0.75);">puede demorar unos minutos en llegar</span>, así que ten paciencia.
                </p>
              </div>
            </div>

            <!-- Paso 2 -->
            <div style="display: flex; gap: 24px; align-items: flex-start; padding: 32px 0; border-bottom: 1px solid rgba(255,255,255,0.06);">
              <div style="flex-shrink: 0; display: flex; flex-direction: column; align-items: center;">
                <div style="
                  width: 52px; height: 52px;
                  background: linear-gradient(135deg, #1565c0, #2196f3);
                  border-radius: 14px;
                  display: flex; align-items: center; justify-content: center;
                  font-size: 1.3rem; font-weight: 800; color: #fff;
                  box-shadow: 0 8px 24px rgba(33,150,243,0.3);
                ">2</div>
              </div>
              <div style="flex: 1; padding-top: 8px;">
                <div style="display: flex; align-items: center; gap: 12px; margin-bottom: 8px;">
                  <v-icon color="blue" size="20">mdi-whatsapp</v-icon>
                  <h3 style="font-size: 1.2rem; font-weight: 700; color: #fff;">Envía tu comprobante por WhatsApp</h3>
                </div>
                <p style="color: rgba(255,255,255,0.55); line-height: 1.7; font-size: 0.97rem; margin: 0 0 16px 0;">
                  Una vez que tengas el comprobante, envíalo directamente a mi WhatsApp junto con:
                </p>
                <div style="display: flex; flex-direction: column; gap: 8px;">
                  <div style="display: flex; align-items: center; gap: 10px;">
                    <div style="width: 6px; height: 6px; background: #2196f3; border-radius: 50%; flex-shrink: 0;"></div>
                    <span style="color: rgba(255,255,255,0.7); font-size: 0.93rem;">Tu <strong style="color:#fff;">nombre completo</strong></span>
                  </div>
                  <div style="display: flex; align-items: center; gap: 10px;">
                    <div style="width: 6px; height: 6px; background: #2196f3; border-radius: 50%; flex-shrink: 0;"></div>
                    <span style="color: rgba(255,255,255,0.7); font-size: 0.93rem;">El <strong style="color:#fff;">plan que adquiriste</strong></span>
                  </div>
                </div>

                <!-- WhatsApp CTA inline -->
                <a
                  href="https://wa.me/526221562893"
                  target="_blank"
                  style="
                    display: inline-flex; align-items: center; gap: 10px;
                    margin-top: 20px;
                    background: rgba(37,211,102,0.12);
                    border: 1px solid rgba(37,211,102,0.3);
                    color: #4caf50;
                    padding: 10px 20px;
                    border-radius: 10px;
                    text-decoration: none;
                    font-weight: 600; font-size: 0.9rem;
                    transition: all 0.2s ease;
                  "
                  onmouseover="this.style.background='rgba(37,211,102,0.2)'; this.style.transform='translateY(-1px)'"
                  onmouseleave="this.style.background='rgba(37,211,102,0.12)'; this.style.transform='translateY(0)'"
                >
                  <v-icon size="18">mdi-whatsapp</v-icon>
                  6221562893
                </a>
              </div>
            </div>

            <!-- Paso 3 -->
            <div style="display: flex; gap: 24px; align-items: flex-start; padding: 32px 0;">
              <div style="flex-shrink: 0;">
                <div style="
                  width: 52px; height: 52px;
                  background: linear-gradient(135deg, #1565c0, #2196f3);
                  border-radius: 14px;
                  display: flex; align-items: center; justify-content: center;
                  font-size: 1.3rem; font-weight: 800; color: #fff;
                  box-shadow: 0 8px 24px rgba(33,150,243,0.3);
                ">3</div>
              </div>
              <div style="flex: 1; padding-top: 8px;">
                <div style="display: flex; align-items: center; gap: 12px; margin-bottom: 8px;">
                  <v-icon color="blue" size="20">mdi-clipboard-check-outline</v-icon>
                  <h3 style="font-size: 1.2rem; font-weight: 700; color: #fff;">¡Listo! Comenzamos tu proceso</h3>
                </div>
                <p style="color: rgba(255,255,255,0.55); line-height: 1.7; font-size: 0.97rem; margin: 0;">
                  Después de confirmar tu pago, te enviaré el <span style="color:#fff; font-weight:600;">formulario de evaluación inicial</span> y te explicaré paso a paso cómo llevaremos el seguimiento de tu proceso. Todo está diseñado para que tu experiencia sea clara, ordenada y efectiva desde el primer día.
                </p>
              </div>
            </div>

          </div>
        </v-col>
      </v-row>

      <!-- Card destacada resumen -->
      <v-row justify="center">
        <v-col cols="12" md="8">
          <div style="
            background: linear-gradient(135deg, rgba(21,101,192,0.15) 0%, rgba(33,150,243,0.08) 100%);
            border: 1px solid rgba(33,150,243,0.25);
            border-radius: 20px;
            padding: 36px 40px;
            display: flex;
            align-items: center;
            gap: 24px;
            flex-wrap: wrap;
          ">
            <div style="
              width: 56px; height: 56px; flex-shrink: 0;
              background: rgba(33,150,243,0.15);
              border-radius: 16px;
              display: flex; align-items: center; justify-content: center;
            ">
              <v-icon size="28" color="blue">mdi-shield-check-outline</v-icon>
            </div>
            <div style="flex: 1; min-width: 200px;">
              <p style="font-weight: 700; font-size: 1.05rem; color: #fff; margin-bottom: 6px;">Tu proceso es nuestra prioridad</p>
              <p style="color: rgba(255,255,255,0.5); font-size: 0.93rem; line-height: 1.6; margin: 0;">
                Pago → Comprobante por WhatsApp → Formulario inicial → Seguimiento personalizado.
                Simple, transparente y sin complicaciones.
              </p>
            </div>
            <v-btn
              href="https://wa.me/526221562893"
              target="_blank"
              color="blue"
              variant="flat"
              class="minimal-btn"
              style="text-transform: none; font-weight: 600; letter-spacing: 0; flex-shrink: 0;"
            >
              <v-icon left size="18">mdi-whatsapp</v-icon>
              Contactar
            </v-btn>
          </div>
        </v-col>
      </v-row>

    </v-container>
  </section>
</template>

<script>
export default {
  name: 'ProcesoPagoSection',
}
</script>
