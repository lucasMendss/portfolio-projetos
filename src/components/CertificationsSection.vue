<script setup>
import Certification from './Certification.vue'

import precisePromptsLogo from '../assets/certifications/craft-precise-prompts-for-ai-models.png'
import googleLogo from '../assets/certifications/google-logo.jpg'
import coddyLogo from '../assets/certifications/coddy.png'

const certifications = [
    {
        title: 'Craft Precise Prompts for AI Models',
        image: precisePromptsLogo,
        url: 'https://www.credly.com/earner/earned/badge/d1869793-081d-416d-b482-afd5a32118d3'
    },
    {
        title: 'Fundamentos do Suporte de TI',
        image: googleLogo,
        url: 'https://www.linkedin.com/safety/go/?url=https%3A%2F%2Fwww.coursera.org%2Faccount%2Faccomplishments%2Fverify%2FCB19MQ3LY2H7&urlhash=ZnwH&mt=r0NZdi3ezOQh8IwjLMrLV1TnjFTNpU5bGgLfkgMVudMrCdr7gCuqHzAVjyM0zI2K1WTV0cP6kf-g43JuQH4sU-F2mEz0&isSdui=true&lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_certifications_details%3BBEwzZb7AQBe8JRUotnaCgA%3D%3D'
    },
    {
        title: 'Java Fundamentals',
        image: coddyLogo,
        url: 'https://www.linkedin.com/safety/go/?url=https%3A%2F%2Fcoddy.tech%2Fcertifications%2FbeSjAp-java-jx1zAL&urlhash=lBdX&mt=G9U-KwBpJMGZWFXiFp7x_Ll0lKfLBejFnR1iQwdccQfin9SFS3q4aYeo_h7P4FYY_krD6TE-fV1jmPvpOh8pkPCNQbx8&isSdui=true&lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_certifications_details%3BU5tfiJq2SMexw2H%2FeDRkIg%3D%3D'
    },
    {
        title: 'Java Logic & Flow',
        image: coddyLogo,
        url: 'https://www.linkedin.com/safety/go/?url=https%3A%2F%2Fcoddy.tech%2Fcertifications%2FbeSjAp-java-LqwkcT&urlhash=1SFj&mt=PRefExZ00AZH2bVo1K14PnGKGO_enVfWVboGJVDoqOiETNQ4zxShsn3hkpsbEno9pUIawrUFQUC9owZoIL2t4W3B1XpZ&isSdui=true&lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_certifications_details%3BU5tfiJq2SMexw2H%2FeDRkIg%3D%3D'
    }
]
</script>

<template>
    <section id="certificacoes" class="certifications">
        <h2>Certificações</h2>

        <div class="certifications-list">
            <Certification v-for="certification in certifications" :key="certification.title" v-bind="certification" />
        </div>
    </section>
</template>

<style lang="css" scoped>
.certifications-list {
    display: flex;
    flex-wrap: wrap;
    gap: 24px;
    justify-content: center;
    align-items: stretch;
}
</style>