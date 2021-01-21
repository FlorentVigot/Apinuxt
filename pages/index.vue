<template>
  <div class="container">
    <v-row justify="center" align="center">
      <v-col cols="12" sm="8" md="6">
        <div class="text-center">
          <logo />
          <vuetify-logo />
        </div>
        <v-card>
          <v-card-title class="headline">
            Bienvenue sur Coaching gagnant !
          </v-card-title>
          <v-card-text>
            <h2>Coaching gagnant c'est quoi ?</h2>
            <p>
              Coaching gagnant, c'est un site web, qui regroupe tout les match
              de Superliga, la ligue danoise et la ligue écossaise !
            </p>
          </v-card-text>
          <v-card-actions>
            <v-spacer />
            <v-btn color="dark" nuxt to="/superliga"> Superliga </v-btn>
            <v-btn color="dark" nuxt to="/scottish"> Ligue écossaise </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import Logo from "~/components/Logo.vue";
import VuetifyLogo from "~/components/VuetifyLogo.vue";

export default {
  components: {
    Logo,
    VuetifyLogo,
  },
};
</script>
<style scoped>
.container {
  background-color: white;
}
.v-card {
  background-color: #00a86b;
}
</style>
