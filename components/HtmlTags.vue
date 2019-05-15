<template>
  <v-container>
    <!-- Plain H1 -->
    <h1 v-for="i in 2" :key="i">Index {{ i }}</h1>

    <!-- H1 as v-flex -->
    <v-layout>
      <v-flex v-for="i in 2" :key="i" tag="h1">Index {{ i }}</v-flex>
    </v-layout>
  </v-container>
</template>
