<template>
    <v-container max-width="98%">
        <v-row>
            <v-col cols="12" md="3">
                <span class="text-h7">Categoria <span class="text-red">*</span></span>
                <v-select :items="categories" variant="solo" flat bg-color="white" />
            </v-col>
            <v-col cols="12" md="3">
                <span class="text-h7">Sub-Categoria <span class="text-red">*</span></span>
                <v-select :items="categories" variant="solo" flat bg-color="white" />
            </v-col>
            <v-col cols="12" md="6">
                <span class="text-h7">Produto</span>
                <v-text-field 
                    variant="solo"
                    flat 
                    bg-color="white" 
                    class="produto-input"
                />
            </v-col>
        </v-row>
        <div style="margin-top: -30px;">
            <v-row>
                <v-col cols="12" md="2">
                    <span class="text-h7">Preço Mínimo</span>
                    <v-text-field label="Menor que" variant="solo" flat bg-color="white" />
                </v-col>
                <v-col cols="12" md="2">
                    <span class="text-h7">Preço Máximo</span>
                    <v-text-field label="Maior que" variant="solo" flat bg-color="white" />
                </v-col>
                <v-col cols="12" md="2">
                    <v-row>
                        <v-checkbox 
                        label="Preço a vista" 
                        color="#3B4256"
                        base-color="#3B4256"
                        />
                    </v-row>
                    <v-row>
                        <v-checkbox 
                        style="margin-top: -40px;"
                        label="Parcelado" 
                        color="#3B4256"
                        base-color="#3B4256"
                        />
                    </v-row>
                </v-col>
                <v-col cols="12" md="4">
                    <v-row>
                        <v-col cols="5">
                            <div style="display: flex; flex-direction: column; align-items: center; justify-content: center;">
                                <span class="text-h7" style="color: #3B4256; font-weight: 600;">Melhor Desconto</span>
                            </div>
                            <div style="display: flex; justify-content: center;">   
                                <v-switch hide-details inset color="#3B4256" base-color="#3B4256"></v-switch>
                            </div>
                        </v-col>    
                        <v-col cols="6">
                            <div style="display: flex; flex-direction: column; align-items: center; justify-content: center;">
                                <span class="text-h7" style="color: #3B4256; font-weight: 600;">Melhor Preço</span>
                            </div>
                            <div style="display: flex; justify-content: center;">
                                <v-switch inset color="#3B4256" base-color="#3B4256"></v-switch>
                            </div>
                        </v-col>
                    </v-row>
                </v-col>
            </v-row>
        </div>
        </v-container>
    </template>

<script lang="ts" setup>
import { ref } from 'vue'
const categories = ref(['Item 1', 'Item 2', 'Item 3'])
</script>
<style lang="scss" scoped>
:deep(.v-checkbox) {
    .v-label {
        color: #3B4256 !important;
        opacity: 1 !important;
    }
}

:deep(.v-switch) {
    .v-switch__track {
        opacity: 1 !important;
    }
    .v-switch__thumb {
        background-color: white !important;
        color: white !important;
    }
    .v-selection-control__input {
        .v-switch__thumb {
            background-color: white !important;
        }
    }
}

:deep(.produto-input) {
    .v-field {
        height: 75px !important;
    }
    .v-field__input {
        padding-top: 12px !important;
        padding-bottom: 12px !important;
    }
}

span {
    color: gray;
}
</style>
