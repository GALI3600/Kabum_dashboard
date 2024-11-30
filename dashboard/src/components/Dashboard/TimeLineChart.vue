<template>
    <div>
        <v-card flat style="background-color: white;">
            <apexchart
                type="line"
                height="350"
                :options="chartOptions"
                :series="series"
            />
        </v-card>
    </div>
</template>

<script setup lang="ts">
const series = [
    {
        name: 'Preço Pix',
        data: [2050, 2100, 2050, 2100, 2150, 2100]
    },
    {
        name: 'Preço Parcelado',
        data: [2100, 2150, 2100, 2150, 2200, 2150]
    }
]

const chartOptions = {
    chart: {
        type: 'line',
        height: 350,
        toolbar: {
            show: false
        }
    },
    title: {
        text: 'Variação de Preço: Placa de Vídeo RTX 4060 8G V2 Gaming ATS OC ASUS NVIDIA',
        align: 'left',
        style: {
            fontSize: '16px',
            fontWeight: 'bold',
            color: '#3B4256'
        }
    },
    subtitle: {
        text: 'R$ 1.199,99',
        align: 'left',
        style: {
            fontSize: '30px',
            color: '#FF6500'
        }
    },
    stroke: {
        curve: 'smooth',
        width: 2
    },
    colors: ['#FF6500', '#FFC199'],
    dataLabels: {
        enabled: false
    },
    xaxis: {
        categories: ['Jan', 'Feb', 'Mar', 'Apr', 'Mai', 'Jun'],
        labels: {
            style: {
                colors: '#3B4256'
            }
        }
    },
    yaxis: {
        labels: {
            formatter: function (value: number) {
                return `R$ ${value.toFixed(2)}`
            },
            style: {
                colors: '#3B4256'
            }
        }
    },
    legend: {
        position: 'bottom',
        horizontalAlign: 'left',
        labels: {
            colors: '#3B4256'
        }
    },
    tooltip: {
        theme: 'dark',
        y: {
            formatter: function(value: number) {
                return `R$ ${value.toFixed(2)}`
            }
        }
    },
    grid: {
        borderColor: '#e0e0e0',
        strokeDashArray: 5,
    }
}
</script>
