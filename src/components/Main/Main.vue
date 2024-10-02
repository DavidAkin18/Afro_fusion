<template>
  <SectionOne />
  <Categories />
  <ChooseUs/>
  <About />
  <Menu />
  <Meet />
  <Testimonial />
</template>

<script>
import About from './About.vue';
import Categories from './Categories.vue';
import ChooseUs from './ChooseUs.vue';
import Meet from './Meet.vue';
import Menu from './Menu.vue';
import SectionOne from './SectionOne.vue';
import Testimonial from './Testimonial.vue';

export default {
components:{
    SectionOne,
    Categories,
    ChooseUs,
    About,
    Menu,
    Meet,
    Testimonial
}
}
</script>

<style>
body{
  background-color: #FEF9F4
}
</style>