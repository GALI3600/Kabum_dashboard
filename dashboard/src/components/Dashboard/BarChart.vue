<template>
    <div>
        <v-card flat style="background-color: white;">

            <apexchart
            type="bar"
            height="400"
            :options="chartOptions"
            :series="series"
            />
        </v-card>
    </div>
</template>

<script setup lang="ts">
const series = [
    {
        name: 'Preço à Vista',
        data: [1299, 1499, 899, 2499, 1799, 999, 3499, 1999, 2999, 1599]
    },
    {
        name: 'Preço a Prazo',
        data: [1499, 1699, 999, 2799, 1999, 1199, 3799, 2199, 3299, 1799]
    }
]

const chartOptions = {
    chart: {
        type: 'bar',
        height: 400,
        toolbar: {
            show: false
        }
    },
    title: {
        text: '10 Melhores Promoções',
        align: 'left',
        style: {
            fontSize: '16px',
            fontWeight: 'bold',
            color: '#3B4256'
        }
    },
    plotOptions: {
        bar: {
            horizontal: false,
            columnWidth: '55%',
            borderRadius: 1
        },
    },
    colors: ['#FF6500', '#FFC199'],
    dataLabels: {
        enabled: false
    },
    xaxis: {
        categories: [
            'iPhone 13',
            'Samsung S21',
            'Xiaomi 12',
            'MacBook Air',
            'PS5',
            'Nintendo Switch',
            'Smart TV 55"',
            'iPad Pro',
            'Dell XPS 13',
            'AirPods Pro'
        ],
        labels: {
            style: {
                colors: '#3B4256'
            }
        }
    },
    yaxis: {
        labels: {
            formatter: function (value: number) {
                return `R$ ${value}`
            },
            style: {
                colors: '#3B4256'
            }
        }
    },
    legend: {
        position: 'top',
        horizontalAlign: 'center',
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
        },
        style: {
            fontSize: '12px',
            fontFamily: undefined
        }
    }
}
</script>
