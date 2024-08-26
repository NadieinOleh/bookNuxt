<template>
    <Header />
    <main>
        <slot />
    </main>
    <Footer />
</template>


<script>
import Header from '../components/Header/Header.vue'
import Footer from '../components/Footer/Footer.vue'
</script>