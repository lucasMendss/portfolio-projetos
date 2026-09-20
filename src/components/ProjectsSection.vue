<script setup>
import Project from './Project.vue';

const projects = [
    /*
    {
      name: '',
      description:
        '',
      technologies: [
        
      ],
      repositoryUrl: '',
      demoUrl: ''  
    }
    */
    {
        name: 'SnapClima',
        description:
            'Desenvolvi uma página web que exibe informações sobre o tempo atual de local pesquisado. Hospedei o front-end na Vercel e, com Java, criei a Azure Function que se comunica com a API de tempo da OpenWeather.',
        technologies: [
            'HTML',
            'CSS',
            'JavaScript',
            'Vercel',
            'Java',
            'Azure'
        ],
        repositoryUrl: 'https://github.com/lucasMendss/Snapclima',
        demoUrl: 'https://snapclima-one.vercel.app'
    },

    {
        name: 'Bot de figurinhas para WhatsApp',
        description:
            'Desenvolvi e hospedei na Azure um bot para WhatsApp que converte imagens e GIFs em figurinhas. O processo é ativado quando é enviada uma mídia junto com a legenda "!sticker".',
        technologies: [
            'JavaScript',
            'Node.js',
            'Virtual Machine da Azure',
            'Linux'
        ],
        repositoryUrl: 'https://github.com/lucasMendss/bot-figurinha-whatsapp'
    },

    {
        name: 'API REST de Produtos',
        description:
            'Criei uma API REST com funcionalidades de criação, listagem, atualização e exclusão de produtos.',
        technologies: [
            'Java 17',
            'Spring Boot',
            'Spring Web',
            'SpringDoc OpenAPI UI'
        ],
        repositoryUrl: 'https://github.com/lucasMendss/first-spring-web-rest-api'
    },

    {
        name: 'Gerenciador de Frota',
        description:
            'Aplicação Web que permite criar, atualizar, pesquisar e deletar registros de veículos.',
        technologies: [
            'JavaScript',
            'Vue.js',
            'Node.js',
            'SQLite'
        ],
        repositoryUrl: 'https://github.com/lucasMendss/gerenciador-de-frota',
    },

    {
      name: 'Gerenciador de Aluno',
      description:
        'App desktop para criar, atualizar, pesquisar e deletar cadastros de alunos.',
      technologies: [
        'C#',
        '.NET 8',
        'PostgreSQL',
        'Supabase'  
      ],
      repositoryUrl: 'https://github.com/lucasMendss/gerenciador-de-aluno-windows-desktop',
      demoUrl: ''  
    }
]
</script>

<template>
    <section id="projetos" class="projects">
        <h2>Projetos</h2>

        <Project v-for="project in projects" :key="project.name" v-bind="project" />
    </section>
</template>