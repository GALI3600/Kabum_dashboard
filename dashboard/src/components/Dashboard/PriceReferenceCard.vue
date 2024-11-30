<template>
    <v-card flat style="background-color: white;" class="pa-4">
        <div class="text-subtitle-1 font-weight-bold mb-2" style="color: #3B4256;">
            Referência de preço
        </div>

        <div class="text-h5 font-weight-bold mb-1" style="color: #3B4256;">
            R$ 2.200,00
        </div>
        <div class="text-caption mb-3" style="color: gray;">
            Preço do anúncio
        </div>

        <v-progress-linear
            rounded
            height="15"
            color="#00B4D8"
            :model-value="calculateProgressValue(2200, 2000, 2700)"
            style="background-color: #E9ECEF;"
        ></v-progress-linear>

        <v-row class="mt-4">
            <v-col cols="6">
                <v-card variant="outlined" class="pa-2">
                    <div class="text-subtitle-1 font-weight-bold" style="color: #3B4256;">
                        R$ 2.000,00
                    </div>
                    <div class="text-caption" style="color: gray;">
                        Menor Preço registrado
                    </div>
                </v-card>
            </v-col>
            <v-col cols="6">
                <v-card variant="outlined" class="pa-2">
                    <div class="text-subtitle-1 font-weight-bold" style="color: #3B4256;">
                        R$ 2.700,00
                    </div>
                    <div class="text-caption" style="color: gray;">
                        Maior Preço registrado
                    </div>
                </v-card>
            </v-col>
        </v-row>
    </v-card>
</template>

<script setup lang="ts">
const calculateProgressValue = (current: number, min: number, max: number) => {
    return ((current - min) / (max - min)) * 100;
}
</script>

<style scoped>
:deep(.v-card) {
    border-radius: 8px;
}

:deep(.v-progress-linear) {
    border-radius: 4px;
}

:deep(.v-progress-linear__background) {
    opacity: 1 !important;
}
</style>
