<script setup>
import FrontendLayout from '@/Layouts/Frontend.vue';
import { Head, Link } from '@inertiajs/vue3';
import Hero from '@/Components/Frontend/Hero.vue';
import Promote from '@/Components/Frontend/Promote.vue';
import About from '@/Components/Frontend/About.vue';
import Skills from '@/Components/Frontend/Skills.vue';
import Portfolio from '@/Components/Frontend/Profolio.vue';
import Services from '@/Components/Frontend/Services.vue';
import ContactMe from '@/Components/Frontend/ContactMe.vue';

defineProps({
    skills: Object,
    projects: Object
});

</script>

<template>
    <Head title="My Portfolio" />
    <FrontendLayout>
        <!-- Hero Primary -->
        <Hero />
        <!-- Promote tail-100 -->
        <Promote />
        <!-- About Secondary -->
        <About />
        <!-- Skills tail-100 -->
        <Skills :skills="skills" />
        <!-- Portfolio primary -->
        <Portfolio :projects="projects" :skills="skills" />
        <!-- Services secondary -->
        <Services />
        <!-- Contact primary -->
        <ContactMe />
    </FrontendLayout>
</template>


