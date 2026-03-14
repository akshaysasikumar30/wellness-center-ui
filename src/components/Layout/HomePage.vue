<template>
    <div>
        <Navbar />
        <Hero />
        <Accomodations />
        <EventSpace />
        <Restaurent />
        <Spa />
        <Wellness />
        <Activities />
        <Footer />
    </div>
</template>

<script>    
    import Navbar from '../Views/Navbar.vue';
    import Hero from '../Views/Hero.vue';
    import Accomodations from '../Views/Accomodations.vue';
    import EventSpace from '../Views/EventSpace.vue';
    import Restaurent from '../Views/Restaurent.vue';
    import Spa from '../Views/Spa.vue';
    import Wellness from '../Views/Wellness.vue';
    import Activities from '../Views/Activities.vue';
    import Footer from '../Views/Footer.vue';
    
    export default {
        name: 'HomePage',
        components: {
            Navbar,
            Hero,
            Accomodations,
            EventSpace,
            Restaurent,
            Spa,
            Wellness,
            Activities,
            Footer
        }
    }
</script>

<style scoped>
</style>