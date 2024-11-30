<template>
    <div>
        <v-card flat style="background-color: white;" height="400">
            <v-img src="https://images7.kabum.com.br/produtos/fotos/550417/placa-de-video-rtx-4060-o8g-v2-gaming-ats-asus-nvidia-geforce-8gb-gddr6-dlss-ray-tracing-g-sync-90yv0jm2-m0na00_1719508167_g.jpg"
             height="52%"/>
            <v-card-title style="display: block;">
                <div class="product-title-wrapper">
                    <span class="product-title">Placa de Vídeo RTX 4060 8G V2 Gaming ATS OC ASUS NVIDIA GeForce, 8GB GDDR6,...</span>
                </div>
                <v-row>
                    <span class="product-price">R$ 1.199,99</span>
                </v-row>
                <v-row>
                    <span class="product-10x">À vista no PIX <br> ou até 10x de R$ 258,82 no cartão</span>
                </v-row>
            </v-card-title>
        </v-card>
    </div>
</template>

<style scoped>
.product-title-wrapper {
    width: 100%;
    max-height: 3.6em; /* Aproximadamente 2 linhas */
    overflow: hidden;
}

.product-title {
    color: #3B4256;
    font-weight: bold;
    font-size: 0.9em;
    line-height: 1.8em;
    display: block;
    width: 100%;
    white-space: normal;
    word-wrap: break-word;
}

:deep(.v-card-title) {
    padding: 16px;
    display: block !important;
    width: 100% !important;
}

.product-price {
    color: #FF6500;
    font-weight: bold;
    font-size: 1.4em;
    margin-left: 10px;
}

.product-10x {
    color: #3B4256;
    opacity: 0.5;
    font-weight: bold;
    font-size: 0.8em;
    margin-left: 10px;
}
</style>

<script setup lang="ts">

</script>
