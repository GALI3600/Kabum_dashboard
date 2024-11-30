<template>
  <div>
    <Filters />
    <v-container max-width="98%">

      <v-row>
        <v-col cols="12" md="4">
          <BarChart />
        </v-col>
        <v-col cols="12" md="4">
          <PriceReferenceCard />
        </v-col>
        <v-col cols="12" md="4">
          <ProductCard />
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12">
          <TimeLineChart />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script lang="ts" setup>
  //
</script>
