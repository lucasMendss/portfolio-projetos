<script setup>
defineProps({
  image: {
    type: String,
    required: true
  },
  title: {
    type: String,
    required: true
  },
  url: {
    type: String,
    required: true
  }
})
</script>

<template>
  <article class="certification">
    <img :src="image" :alt="`Imagem da certificação ${title}`" />

    <h3>{{ title }}</h3>

    <a
      :href="url"
      target="_blank"
      rel="noopener noreferrer"
    >
      Exibir credencial
    </a>
  </article>
</template>

<style scoped>
.certification {
  flex: 0 1 220px;
  width: 220px;
  padding: 16px;
  border: 1px solid var(--border);
  border-radius: 8px;
  background: var(--surface);
  box-shadow: var(--shadow);
  text-align: center;
}

.certification img {
  width: 100%;
  aspect-ratio: 1;
  object-fit: cover;
  display: block;
  margin-bottom: 16px;
}

.certification h3 {
  margin: 0 0 12px;
  color: var(--text-h);
  font-family: var(--sans);
  font-size: 1rem;
  line-height: 1.35;
}

.certification a {
  color: var(--accent);
  font-size: 0.9rem;
}
</style>