<template>
  <div>
    <!-- Navbar minimalista -->
    <v-app-bar app class="minimal-navbar" elevation="0" height="70">
      <v-container class="d-flex align-center">
        <div class="d-flex align-center">
          <img src="/assets/imgs/FRLogo.png" height="50" width="70" />
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
        <v-spacer></v-spacer>
        <div class="d-none d-md-flex" style="gap: 32px">
          <a
            href="#inicio"
            style="text-decoration: none; color: #fff; font-weight: 500; opacity: 0.8; transition: opacity 0.3s"
            @mouseover="$event.target.style.opacity='1'"
            @mouseleave="$event.target.style.opacity='0.8'"
            >Inicio</a
          >
          <a
            href="#sobre-mi"
            style="text-decoration: none; color: #fff; font-weight: 500; opacity: 0.8; transition: opacity 0.3s"
            @mouseover="$event.target.style.opacity='1'"
            @mouseleave="$event.target.style.opacity='0.8'"
            >Sobre Mí</a
          >
          <!-- <a
            href="#trayectoria"
            style="text-decoration: none; color: #fff; font-weight: 500; opacity: 0.8; transition: opacity 0.3s"
            @mouseover="$event.target.style.opacity='1'"
            @mouseleave="$event.target.style.opacity='0.8'"
            >Trayectoria</a
          > -->
          <a
            href="#planes"
            style="text-decoration: none; color: #fff; font-weight: 500; opacity: 0.8; transition: opacity 0.3s"
            @mouseover="$event.target.style.opacity='1'"
            @mouseleave="$event.target.style.opacity='0.8'"
            >Planes</a
          >
          <a
            href="#transformaciones"
            style="text-decoration: none; color: #fff; font-weight: 500; opacity: 0.8; transition: opacity 0.3s"
            @mouseover="$event.target.style.opacity='1'"
            @mouseleave="$event.target.style.opacity='0.8'"
            >Transformaciones</a
          >
          <a
            href="#contacto"
            style="text-decoration: none; color: #fff; font-weight: 500; opacity: 0.8; transition: opacity 0.3s"
            @mouseover="$event.target.style.opacity='1'"
            @mouseleave="$event.target.style.opacity='0.8'"
            >Contacto</a
          >
        </div>
        <!-- Mobile Menu Button -->
        <v-btn icon class="d-md-none" @click="drawer = !drawer" style="margin-left: 8px">
          <v-icon>mdi-menu</v-icon>
        </v-btn>
      </v-container>
    </v-app-bar>

    <v-navigation-drawer
      v-model="drawer"
      temporary
      location="right"
      class="minimal-navbar"
      style="background: rgba(10, 10, 10, 0.98) !important; backdrop-filter: blur(20px)"
    >
      <v-list style="padding-top: 60px">
        <v-list-item v-for="item in menuItems" :key="item.title" :href="item.link" @click="drawer = false" style="margin-bottom: 8px">
          <template v-slot:prepend>
            <v-icon color="blue" style="margin-right: 16px">{{ item.icon }}</v-icon>
          </template>
          <v-list-item-title style="font-weight: 500; font-size: 1.1rem"> {{ item.title }} </v-list-item-title>
        </v-list-item>
      </v-list>

      <template v-slot:append>
        <div style="padding: 20px; border-top: 1px solid rgba(255, 255, 255, 0.1)">
          <v-btn
            href="https://wa.me/526221562893"
            target="_blank"
            color="green-darken-1"
            block
            prepend-icon="mdi-whatsapp"
            style="margin-bottom: 12px"
          >
            WhatsApp
          </v-btn>
          <v-btn href="https://instagram.com/fernandoruelas03" target="_blank" color="pink-darken-1" block prepend-icon="mdi-instagram">
            Instagram
          </v-btn>
        </div>
      </template>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  name: 'AppNavbar',
  data() {
    return {
      drawer: false,
      menuItems: [
        { title: "Inicio", link: "#inicio", icon: "mdi-home" },
        { title: "Sobre Mí", link: "#sobre-mi", icon: "mdi-account" },
        { title: "Transformaciones", link: "#transformaciones", icon: "mdi-trophy" },
        { title: "Planes", link: "#planes", icon: "mdi-clipboard-text" },
        { title: "Contacto", link: "#contacto", icon: "mdi-phone" },
      ],
    }
  },
}
</script>
