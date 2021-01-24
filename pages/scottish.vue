<template>
  <v-row>
    <v-col class="text-center">
      <div class="scottish-title">
        <h1>{{ title }}</h1>
      </div>
      <img src="../assets/scottish.png" alt="logo-scottish" class="mb-5" />
      <blockquote class="blockquote">
        &#8220;Voici la liste des match pour aujourd'hui&#8221;
        <footer>
          <small>
            <em>&mdash;Match</em>
          </small>
        </footer>
      </blockquote>
    </v-col>
  </v-row>
</template>
<script>
export default {
  data() {
    return {
      title: "The Scottish league !",
    };
  },
};
</script>
<style scoped>
img {
  background-color: white;
}
.scottish-title h1 {
  color: rgb(23, 48, 95);
  text-shadow: 1px 1px 1px white;
}
footer {
  background-color: rgb(228, 186, 50);
}
</style>