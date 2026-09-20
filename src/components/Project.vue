<script setup>
defineProps({
  name: {
    type: String,
    required: true
  },
  description: {
    type: String,
    required: true
  },
  technologies: {
    type: Array,
    default: () => []
  },
  repositoryUrl: {
    type: String,
    default: ''
  },
  demoUrl: {
    type: String,
    default: ''
  }
})
</script>

<template>
  <article class="project">
    <h2>{{ name }}</h2>

    <p>{{ description }}</p>

    <p v-if="technologies.length">
      <strong>Tecnologias:</strong>
      {{ technologies.join(', ') }}
    </p>

    <p v-if="repositoryUrl">
      <strong>Repositório e documentação: </strong>
      <a :href="repositoryUrl" target="_blank" rel="noopener noreferrer">
        Acessar repositório
      </a>
    </p>

    <p v-if="demoUrl">
      <strong>Página web: </strong>
      <a :href="demoUrl" target="_blank" rel="noopener noreferrer">
        Acessar aplicação
      </a>
    </p>
  </article>
</template>

<style lang="css" scoped>
.project {
  min-height: 100%;
  padding: 26px;
  border: 1px solid var(--border);
  border-radius: 10px;
  background: var(--surface);
  box-shadow: var(--shadow);
}

.project h2 {
  margin-bottom: 12px;
  color: var(--text-h);
  font-size: 1.45rem;
}

.project p {
  margin-bottom: 16px;
}

.project p:last-child {
  margin-bottom: 0;
}

.project a {
  display: inline-block;
  margin-top: 4px;
}
</style>