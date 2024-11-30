# Sistema Web de Análise de Preços de Produtos de Hardware da Kabum

Este é um sistema web desenvolvido para análise de preços dos produtos de hardware disponíveis no site [www.kabum.com.br](https://www.kabum.com.br). O sistema apresenta os preços em gráficos interativos, permitindo ao usuário visualizar a evolução dos preços ao longo do tempo e comparar os preços mais baixos dos produtos.

## Tecnologias Utilizadas

### Frontend
- **Vue.js 3**: Framework JavaScript para construção de interfaces de usuário reativas.
- **TypeScript**: Linguagem de programação baseada em JavaScript, com tipagem estática.
- **Vuetify**: Framework de componentes baseado no Material Design para Vue.js.
- **ApexCharts**: Biblioteca para a criação de gráficos interativos e dinâmicos.

### Backend
- **Selenium**: Ferramenta utilizada para fazer web scraping e extrair os preços dos produtos da página da Kabum.
- **Supabase**: Plataforma de banco de dados como serviço que armazena as informações coletadas pelo Selenium.
- **Python (Pandas)**: Utilizado para análise de dados e filtragem das informações coletadas.
- **FastAPI**: Framework para a construção de APIs rápidas e eficientes em Python, utilizado para comunicar os dados processados para o frontend.

## Funcionalidades

- **Dashboard interativo**: A interface do sistema exibe gráficos com os preços mais baixos e a linha do tempo dos preços dos produtos.
  ![image](https://github.com/user-attachments/assets/6487c25d-4d54-4f21-a5cb-5b3042b87dd0)

- **Web Scraping**: Utilização do Selenium para capturar os dados de preços de produtos diretamente do site Kabum.
- **Armazenamento e Análise de Dados**: Os dados de preços extraídos são armazenados em um banco de dados Supabase. Um script Python, utilizando a biblioteca Pandas, realiza os filtros e análises para passar as informações filtradas para o frontend via FastAPI.
- **Visualização de Gráficos**: Os gráficos exibem a evolução dos preços dos produtos ao longo do tempo e comparam os preços mais baixos encontrados.

## Como Executar o Projeto

### Pré-requisitos

- **Node.js**: Para rodar o frontend.
- **Python 3.x**: Para o backend e análise de dados.
- **Banco de Dados Supabase**: Para armazenar as informações de preços.
- **NPM ou Yarn**: Para gerenciar as dependências do frontend.

### Passo a Passo

#### 1. Clone o Repositório

```bash
git clone https://github.com/GALI3600/Kabum_dashboard.git
cd Kabum_dashboard


