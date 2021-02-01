<template>
  <div class="container">
    <v-row>
      <v-col class="text-center">
        <div class="scottish-title">
          <h1>{{ title }}</h1>
        </div>
        <img src="../assets/scottish.png" alt="logo-scottish" class="mb-5" />
        <blockquote class="blockquote">
          &#8220;Voici la liste des match pour aujourd'hui&#8221;
          <section>
            <small>
              <em>Match</em>
            </small>
          </section>
        </blockquote>
      </v-col>
    </v-row>
  </div>
</template>
<script>
export default {
  data() {
    return {
      title: "The Scottish league !",
    };
  },
  mounted() {
    axios
      .get(
        "	https://soccer.sportmonks.com/api/v2.0/teams/search/__SEARCH__?api_token=yxFYUOxWYSq2MWX38WtapABIocABgjQmRtbQnnz1o7Qii2Zeeu7TstK3UUSz"
      )
      .then((reponse) => (this.foot = reponse.data));
  },
};
</script>
<style scoped>
.container {
  background-color: white;
}
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