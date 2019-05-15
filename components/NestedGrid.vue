<template>
  <v-container grid-list-md>
    <v-layout row wrap white--text>
      <!-- COLUMN -->
      <v-flex xs12 sm6 md4 purple>Purple</v-flex>

      <!-- COLUMN: d-flex required on v-flex if it contains v-layout -->
      <v-flex d-flex xs12 sm6 md3>
        <v-layout row wrap>
          <!-- Row 1: v-flex -->
          <v-flex indigo>Indigo</v-flex>
          <v-flex v-for="n in num" :key="n" black>Black {{ n }}</v-flex>

          <!-- Row 2: v-flex > v-layout > div (BROKEN: doesn't have padding given by .grid-list) -->
          <v-flex xs12 d-flex>
            <v-layout row justify-space-between>
              <div class="indigo">Indigo</div>
              <div v-for="n in num" :key="n" class="black">Black {{ n }}</div>
            </v-layout>
          </v-flex>

          <!-- Row 3: v-flex > v-layout > v-flex -->
          <v-flex xs12 d-flex>
            <v-layout row wrap>
              <v-flex indigo>Indigo</v-flex>
              <v-flex v-for="n in num" :key="n" black>Black {{ n }}</v-flex>
            </v-layout>
          </v-flex>

          <!-- Row 4: v-flex > v-layout > v-flex -->
          <v-flex xs12 d-flex>
            <v-layout row wrap>
              <v-flex v-for="n in num" :key="n" red lighten-2>Red {{ n }}</v-flex>
              <!-- <v-flex :class="'xs' + 12/num" v-for="n in num" :key="n" red lighten-2>Red {{ n }}</v-flex> -->
            </v-layout>
          </v-flex>
        </v-layout>
      </v-flex>

      <!-- COLUMN -->
      <v-flex xs12 sm6 md2 green lighten-2>Green</v-flex>

      <!-- COLUMN -->
      <v-flex xs12 sm6 md3 blue lighten-2>Blue</v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    lorem: `Lorem ipsum dolor sit amet, mel at clita quando. Te sit oratio vituperatoribus, nam ad ipsum posidonium mediocritatem, explicari dissentiunt cu mea. Repudiare disputationi vim in, mollis iriure nec cu, alienum argumentum ius ad. Pri eu justo aeque torquatos.`,
    num: 2
  })
};
</script>
