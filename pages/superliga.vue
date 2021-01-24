<template>
  <v-row>
    <v-col class="text-center">
      <img
        src="../assets/danemarkliga.png"
        alt="logo-daemark-liga"
        class="mb-5"
      />
      <blockquote class="blockquote">
        &#8220;Voici la liste des match pour aujourd'hui&#8221;
        <footer>
          <small>
            <em>&mdash;Match</em>
          </small>
          <div class="match">
            {{ foot }}
          </div>
        </footer>
      </blockquote>
    </v-col>
  </v-row>
</template>
<script>
import axios from "axios";
export default {
  data() {
    return {
      foot: "il n'y a pas de match",
    };
  },
  mounted() {
    axios
      .get(
        "	https://soccer.sportmonks.com/api/v2.0/teams/search/__SEARCH__?api_token=yxFYUOxWYSq2MWX38WtapABIocABgjQmRtbQnnz1o7Qii2Zeeu7TstK3UUSz"
      )
      .then((reponse) => (this.foot = reponse.data.plan.name));
  },
};
</script>
<style scoped>
img {
  background-color: coral;
}
</style>