<template>
  <v-container>
    <!-- ROW: normal -->
    <v-layout row>
      <v-flex cyan>Flex</v-flex>
      <v-flex pink>Flex</v-flex>
    </v-layout>

    <!-- ROW: grow, shrink -->
    <v-layout row>
      <v-flex grow cyan>Grow Flex</v-flex>
      <v-flex shrink pink>Shrink Flex</v-flex>
    </v-layout>

    <!-- Row: grow, shrink, grow -->
    <v-layout row>
      <v-flex grow cyan>Grow Flex</v-flex>
      <v-flex shrink pink>Shrink Flex</v-flex>
      <v-flex grow cyan>Grow Flex</v-flex>
    </v-layout>

    <!-- ROW: shrink, grow, shrink -->
    <v-layout row>
      <v-flex shrink pink>Shrink Flex</v-flex>
      <v-flex grow cyan>Grow Flex</v-flex>
      <v-flex shrink pink>Shrink Flex</v-flex>
    </v-layout>

    <!-- ROW: shrink, grow, shrink (w/ padding) -->
    <v-layout row>
      <v-flex shrink pink pa-2>Shrink Flex</v-flex>
      <v-flex grow cyan pa-2>Grow Flex</v-flex>
      <v-flex shrink pink pa-2>Shrink Flex</v-flex>
    </v-layout>

    <!-- ROW: grow, grow, grow -->
    <v-layout row>
      <v-flex grow cyan>Grow Flex</v-flex>
      <v-flex grow cyan>Grow Flex</v-flex>
      <v-flex grow cyan>Grow Flex</v-flex>
    </v-layout>

    <!-- ROW: shrink, shrink, shrink -->
    <v-layout row>
      <v-flex shrink pink>Shrink Flex</v-flex>
      <v-flex shrink pink>Shrink Flex</v-flex>
      <v-flex shrink pink>Shrink Flex</v-flex>
    </v-layout>
  </v-container>
</template>

<style scoped>
.layout {
  margin-bottom: 5px;
}

.flex {
  font-weight: bold;
}
</style>

