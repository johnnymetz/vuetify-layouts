<template>
  <v-container>
    <v-layout row wrap lime white--text>
      <!-- CUT IN HALF -->
      <v-flex xs6 yellow>
        <v-layout row wrap blue lighten-3>
          <!-- FULL WIDTH: v-flex > v-layout > v-flex -->
          <v-flex xs12>
            <v-layout row wrap>
              <v-flex v-for="i in num" :key="i" text-xs-center blue>
                <div class="m">{{ i }}</div>
              </v-flex>
            </v-layout>
          </v-flex>

          <!-- FULL WIDTH: v-flex > v-layout > div.flex-item (same as above) -->
          <v-flex xs12>
            <v-layout row wrap>
              <div v-for="i in num" :key="i" class="text-xs-center pink darken-2 box flex-item">
                <div class="m">{{ i }}</div>
              </div>
            </v-layout>
          </v-flex>

          <!-- HALF WIDTH: v-flex.xs6 > v-layout > v-flex -->
          <v-flex xs6>
            <v-layout row wrap>
              <v-flex v-for="i in num" :key="i" text-xs-center green darken-2>
                <div class="m">{{ i }}</div>
              </v-flex>
            </v-layout>
          </v-flex>

          <!-- 3/4 WIDTH: fixed width box -->
          <v-flex xs9>
            <v-layout row wrap justify-space-between>
              <div v-for="i in num" :key="i" class="text-xs-center pink darken-2 fixed-width-box">
                <div class="m">{{ i }}</div>
              </div>
            </v-layout>
          </v-flex>
        </v-layout>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      num: 6
    };
  }
};
</script>

<style scoped>
.fixed-width-box {
  width: 20px;
}

.m {
  margin: 5px;
  background-color: darkorange;
}

.flex-item {
  flex: 1 1 auto;
}
</style>

