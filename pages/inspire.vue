<template>
  <v-row>
    <v-col class="text-center">
      <img
        src="../assets/danemarkliga.png"
        alt="logo-daemark-liga"
        class="mb-5"
      />
      <blockquote class="blockquote">
        &#8220;il n'y a pas de hasard .&#8221;
        <footer>
          <small>
            <em>&mdash;Flo</em>
          </small>
        </footer>
      </blockquote>
    </v-col>
  </v-row>
</template>
// <script>
import axios from "axios";
export default {
  async asyncData() {
    const api =
      "https://github.com/FlorentVigot?tab=overview&from=2021-01-01&to=2021-01-09";
    const mountains = await axios.get(api).then((response) => {
      return response.data;
    });
  },
};
</script>
<style scoped>
template {
  background-color: #00a86b;
}
</style>