<template >
  <v-app>
    <v-app-bar app color="#003B93" dark>
      <img
        src="./assets/Logo_SNCF.png"
        alt="Logo SNCF"
        width="170px"
        height="60px"
      />
      <v-spacer></v-spacer>
      <h3>
        Evolution et proportion des objets perdus et restitués en France 2020
      </h3>
      <v-spacer></v-spacer>
      <v-btn href="https://github.com/zetu25/ihm" target="_blank" text>
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main class="main">
      <!-- Objets perdus -->
      <v-row justify="center">
        <h2>Objets perdus</h2>
      </v-row>
      <v-row justify="center">
        <v-col cols="auto">
          <lost-object-per-month></lost-object-per-month>
        </v-col>
        <v-divider vertical></v-divider>
        <v-col cols="auto">
          <lost-object></lost-object>
        </v-col>
        <v-divider vertical></v-divider>
        <v-col cols="auto">
          <lost-bar-chart></lost-bar-chart>
        </v-col>
      </v-row>

      <v-spacer></v-spacer>
      <v-divider horizontal></v-divider>
            <!-- Objets retrounés et rendus -->
      <v-row justify="center">
        <h2>Objets retrouvés et rendus à leurs propriétaires</h2>
      </v-row>
      <v-row justify="center">
        <v-col cols="auto">
          <returned-object-per-month></returned-object-per-month>
        </v-col>
        <v-divider vertical></v-divider>
        <v-col cols="auto">
          <returned-object></returned-object>
        </v-col>
        <v-divider vertical></v-divider>
        <v-col cols="auto">
          <returned-bar-chart></returned-bar-chart>
        </v-col>
      </v-row>

      <v-spacer></v-spacer>
      <v-divider horizontal></v-divider>
      <!-- <v-row>
        <v-col cols="6">
          <v-row justify="center">
            <h2>Objets trouvés et restitués</h2>
          </v-row>
          <returned-board></returned-board>
        </v-col>
        <v-col cols="6">
          <v-row justify="center">
            <h2>Déclaration de perte</h2>
          </v-row>
          <lost-board></lost-board>
        </v-col>
      </v-row> -->
      <v-row justify="center">
        <h2>Objets trouvés et restitués</h2>
      </v-row>
      <v-row justify="center">
        <v-col cols="10">
          <returned-board></returned-board>
        </v-col>
      </v-row>
      <v-row justify="center">
        <h2>Déclaration de pertes</h2>
      </v-row>
      <v-row justify="center">
        <v-col cols="10">
          <lost-board></lost-board>
        </v-col>
      </v-row>
    </v-main>
  </v-app>
</template>

<script>
import ReturnedObject from "./components/ReturnedObject.vue";
import ReturnedObjectPerMonth from "./components/ReturnedObjectPerMonth.vue";
import LostObject from "./components/LostObject.vue";
import LostObjectPerMonth from "./components/LostObjectPerMonth.vue";
import LostBarChart from "./components/LostBarChart.vue";
import ReturnedBarChart from "./components/ReturnedBarChart.vue";
import ReturnedBoard from "./components/ReturnedBoard.vue";
import LostBoard from "./components/LostBoard.vue";

export default {
  name: "App",
  components: {
    LostObject,
    LostObjectPerMonth,
    LostBarChart,
    LostBoard,
    ReturnedObject,
    ReturnedObjectPerMonth,
    ReturnedBarChart,
    ReturnedBoard,
  },

};

</script>
<style >
.main {
  /* background-image: url("./assets/background1.jpg"); */
  /* background-size: cover; */
  background-color: #bbf0f3;
  background-image: linear-gradient(315deg, #f6d285 0%, #bbf0f3 74%);
}
</style>
