<template>
  <v-footer style="background: #0a0a0a; border-top: 1px solid rgba(255, 255, 255, 0.05); padding: 40px 0">
    <v-container>
      <v-row align="center">
        <v-col cols="12" md="4" class="text-center text-md-left">
          <div style="display: flex; align-items: center; justify-content: center; justify-content: md-start">
            <img src="/assets/imgs/FRLogo.png" height="150" width="190" />
            <!-- <div
              style="
                width: 40px;
                height: 40px;
                background: #2196f3;
                border-radius: 8px;
                display: flex;
                align-items: center;
                justify-content: center;
                margin-right: 12px;
              "
            >
              <span style="font-weight: 800; font-size: 18px; letter-spacing: -1px">FR</span>
            </div> -->
            <span style="font-weight: 600; font-size: 18px; letter-spacing: -0.5px">Ruelas Team</span>
          </div>
        </v-col>
        <v-col cols="12" md="4" class="text-center">
          <p style="margin-bottom: 4px; opacity: 0.8; font-size: 0.9rem">© 2026 Fernando Ruelas</p>
          <p style="opacity: 0.5; font-size: 0.85rem">Hermosillo, Sonora</p>
        </v-col>
        <v-col cols="12" md="4" class="text-center text-md-right">
          <v-btn icon href="https://wa.me/526221562893" target="_blank" style="margin-right: 8px">
            <v-icon color="green">mdi-whatsapp</v-icon>
          </v-btn>
          <v-btn icon href="https://instagram.com/fernandoruelas03" target="_blank">
            <v-icon color="pink">mdi-instagram</v-icon>
          </v-btn>
        </v-col>
      </v-row>
    </v-container>
  </v-footer>
</template>

<script>
export default {
  name: 'AppFooter',
}
</script>
