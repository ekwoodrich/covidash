<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer" app clipped>
      <v-list dense>
        <v-list-item link>
          <v-list-item-action>
            <v-icon>mdi-view-dashboard</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Dashboard</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app clipped-left>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-side-icon>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          x="0px"
          y="0px"
          width="32"
          height="32"
          viewBox="0 0 171 171"
          style=" fill:#000000;"
        >
          <g
            fill="none"
            fill-rule="nonzero"
            stroke="none"
            stroke-width="1"
            stroke-linecap="butt"
            stroke-linejoin="miter"
            stroke-miterlimit="10"
            stroke-dasharray
            stroke-dashoffset="0"
            font-family="none"
            font-weight="none"
            font-size="none"
            text-anchor="none"
            style="mix-blend-mode: normal"
          >
            <path d="M0,171.98863v-171.98863h171.98863v171.98863z" fill="none" />
            <g fill="#ffffff">
              <path
                d="M154.96875,101.41992c1.33594,-5.76123 1.92041,-11.71728 1.78125,-17.61767c-0.11133,-4.70361 -0.72363,-9.43506 -1.80908,-14.1665l-13.86036,3.25635c0.41748,1.80908 0.72364,3.646 0.97412,5.48291h-7.23633c-1.22461,-8.43311 -4.53662,-16.17041 -9.40722,-22.71094l5.09326,-5.09326c1.11328,1.44727 2.22656,2.92237 3.20069,4.48096l12.05127,-7.62598c-5.67773,-8.96191 -13.44287,-16.67139 -22.48828,-22.32129l-7.54248,12.0791c1.61425,1.00195 3.17285,2.14306 4.70361,3.31201l-5.09326,5.09326c-6.54053,-4.87061 -14.27783,-8.18262 -22.71094,-9.40723v-7.2085c1.83692,0.22266 3.646,0.50098 5.45508,0.91846l3.14502,-13.88819c-10.29785,-2.33789 -21.76464,-2.22656 -30.97705,-0.0835l-0.83496,0.167l3.45117,13.83252c1.83691,-0.41748 3.67383,-0.6958 5.51074,-0.91846v7.18066c-8.43311,1.22461 -16.17041,4.53662 -22.71094,9.40723l-5.09326,-5.09326c1.44727,-1.14111 2.9502,-2.25439 4.50879,-3.22852l-7.59814,-12.05127c-8.96192,5.6499 -16.69922,13.41504 -22.34912,22.43261l12.0791,7.57031c1.00195,-1.61425 2.11523,-3.14502 3.28418,-4.64795l5.09326,5.09326c-4.87061,6.54053 -8.18262,14.27783 -9.40723,22.71094h-7.18066c0.22266,-1.83691 0.47314,-3.70166 0.89063,-5.51074l-13.88819,-3.14502c-1.30811,5.7334 -1.89258,11.60596 -1.75342,17.50635c0.11133,4.67578 0.72364,9.40722 1.75342,13.91602v0.13916l13.91602,-3.14502c-0.41748,-1.83692 -0.72364,-3.67383 -0.97412,-5.51075h7.23633c1.22461,8.43311 4.53662,16.17041 9.40723,22.71094l-5.09326,5.09326c-1.14111,-1.4751 -2.25439,-2.97803 -3.25635,-4.56445l-12.05127,7.57031c5.6499,8.98975 13.38721,16.72705 22.43262,22.40478l7.57031,-12.0791c-1.61426,-1.00195 -3.11719,-2.11523 -4.62012,-3.25635l5.09326,-5.09326c6.5127,4.8706 14.27783,8.18261 22.71094,9.40722v7.2085c-1.86475,-0.22266 -3.72949,-0.52881 -5.53858,-0.94629l-3.17285,13.88819c5.73339,1.33594 11.63379,1.92041 17.56201,1.75342c4.70361,-0.11133 9.43505,-0.6958 13.83252,-1.69775h0.05566l-2.97802,-13.94385c-1.80909,0.41748 -3.646,0.69581 -5.51075,0.91846v-7.18067c8.46094,-1.22461 16.19825,-4.53662 22.71094,-9.40722l5.09326,5.09326c-1.4751,1.16895 -3.00586,2.28223 -4.59228,3.28418l7.57031,12.05127c8.98974,-5.62207 16.72705,-13.38721 22.40478,-22.40478l-12.05127,-7.57031c-1.00195,1.55859 -2.11523,3.08936 -3.25635,4.56445l-5.09326,-5.09326c4.8706,-6.54053 8.18261,-14.27783 9.40722,-22.71094h7.18067c-0.22266,1.86475 -0.50098,3.75733 -0.91846,5.59424zM49.875,85.5c0,-3.92431 3.20069,-7.125 7.125,-7.125c3.92431,0 7.125,3.20069 7.125,7.125c0,3.92431 -3.20069,7.125 -7.125,7.125c-3.92431,0 -7.125,-3.20069 -7.125,-7.125zM64.125,114c-3.92431,0 -7.125,-3.20069 -7.125,-7.125c0,-3.92431 3.20069,-7.125 7.125,-7.125c3.92431,0 7.125,3.20069 7.125,7.125c0,3.92431 -3.20069,7.125 -7.125,7.125zM64.125,71.25c-3.92431,0 -7.125,-3.20069 -7.125,-7.125c0,-3.92431 3.20069,-7.125 7.125,-7.125c3.92431,0 7.125,3.20069 7.125,7.125c0,3.92431 -3.20069,7.125 -7.125,7.125zM85.5,121.125c-3.92431,0 -7.125,-3.20069 -7.125,-7.125c0,-3.92431 3.20069,-7.125 7.125,-7.125c3.92431,0 7.125,3.20069 7.125,7.125c0,3.92431 -3.20069,7.125 -7.125,7.125zM85.5,92.625c-3.92431,0 -7.125,-3.20069 -7.125,-7.125c0,-3.92431 3.20069,-7.125 7.125,-7.125c3.92431,0 7.125,3.20069 7.125,7.125c0,3.92431 -3.20069,7.125 -7.125,7.125zM85.5,64.125c-3.92431,0 -7.125,-3.20069 -7.125,-7.125c0,-3.92431 3.20069,-7.125 7.125,-7.125c3.92431,0 7.125,3.20069 7.125,7.125c0,3.92431 -3.20069,7.125 -7.125,7.125zM106.875,57c3.92431,0 7.125,3.20069 7.125,7.125c0,3.92431 -3.20069,7.125 -7.125,7.125c-3.92431,0 -7.125,-3.20069 -7.125,-7.125c0,-3.92431 3.20069,-7.125 7.125,-7.125zM106.875,114c-3.92431,0 -7.125,-3.20069 -7.125,-7.125c0,-3.92431 3.20069,-7.125 7.125,-7.125c3.92431,0 7.125,3.20069 7.125,7.125c0,3.92431 -3.20069,7.125 -7.125,7.125zM114,92.625c-3.92431,0 -7.125,-3.20069 -7.125,-7.125c0,-3.92431 3.20069,-7.125 7.125,-7.125c3.92431,0 7.125,3.20069 7.125,7.125c0,3.92431 -3.20069,7.125 -7.125,7.125z"
              />
            </g>
          </g>
        </svg>
      </v-toolbar-side-icon>
      <v-toolbar-title>covidash</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <v-container class="fill-height" fluid>
        <v-row>
          <CovidChart :chart-data="cases" v-bind:width="1000"></CovidChart>
        </v-row>
        <v-row>
          <v-col cols="12" sm="4">
            <v-card class="pa-2" outlined tile>
              <v-card-title>Total Cases</v-card-title>
              <v-card-text>{{current.totalCases.toLocaleString()}}</v-card-text>
            </v-card>
          </v-col>
          <v-col cols="12" sm="4">
            <v-card class="pa-2" outlined tile>
              <v-card-title>Total Deaths</v-card-title>
              <v-card-text>{{current.totalDeaths.toLocaleString()}}</v-card-text>
            </v-card>
          </v-col>
          <v-col cols="12" sm="4">
            <v-card class="pa-2" outlined tile>
              <v-card-title>Current Hospitalized</v-card-title>
              <v-card-text>{{current.currentHospitalized.toLocaleString()}}</v-card-text>
            </v-card>
          </v-col>
        </v-row>

        <v-row>
          <v-col cols="12" sm="4">
            <v-card class="pa-2" outlined tile>
              <v-card-title>New Cases</v-card-title>
              <v-card-text>{{current.newCases.toLocaleString()}}</v-card-text>
            </v-card>
          </v-col>
          <v-col cols="12" sm="4">
            <v-card class="pa-2" outlined tile>
              <v-card-title>New Deaths</v-card-title>
              <v-card-text>{{current.newDeaths.toLocaleString()}}</v-card-text>
            </v-card>
          </v-col>
          <v-col cols="12" sm="4">
            <v-card class="pa-2" outlined tile>
              <v-card-title>New Hospitalized</v-card-title>
              <v-card-text>{{current.newHospitalized.toLocaleString()}}</v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>

    <v-footer app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
      <a href="https://github.com/ekwoodrich/covidash">View on Github</a>
    </v-footer>
  </v-app>
</template>

<script>
import CovidChart from "./components/CovidChart";

export default {
  components: {
    CovidChart
  },
  props: {
    source: String
  },
  data: () => ({
    drawer: null,
    cases: null,
    current: {
      totalCases: null,
      newCases: null,
      totalDeaths: null,
      newDeaths: null,
      currentHospitalized: null,
      newHospitalized: null
    }
  }),
  created() {
    this.$vuetify.theme.dark = true;
  },
  mounted: function() {
    console.log("mounted");
    this.loadHistorical();
    this.loadCurrent();
  },
  methods: {
    loadHistorical: function() {
      console.log("loading historical data...");
      fetch("https://covidtracking.com/api/v1/us/daily.json")
        .then(response => response.json())
        .then(data => {
          let recentCases = data.slice(0, 200).reverse();
          console.log(recentCases);
          this.cases = {
            labels: recentCases.map(day => day.date),
            datasets: [
              {
                label: "Daily Positive",
                backgroundColor: "#f87979",
                data: recentCases.map(day => day.positiveIncrease)
              }
            ]
          };
        });
    },
    loadCurrent: function() {
      console.log("loading current data...");
      fetch("https://covidtracking.com/api/v1/us/current.json")
        .then(response => response.json())
        .then(data => {
          this.current.newCases = data[0].positiveIncrease;
          this.current.totalCases = data[0].positive;
          this.current.newDeaths = data[0].deathIncrease;
          this.current.totalDeaths = data[0].death;
          this.current.currentHospitalized = data[0].hospitalizedCurrently;
          this.current.newHospitalized = data[0].hospitalizedIncrease;
        });
    }
  }
};
</script>
