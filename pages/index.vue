<script lang="ts">
import { NuxtImg } from '#build/components';
import MainMenu from '~/components/MainMenu.vue';
import Logo from '~/components/Logo.vue';
import Slideshow from '~/components/Slideshow.vue';
import MenuItems from '~/components/MenuItems.vue';
import ProductsGrid from '~/components/ProductsGrid.vue';
import Footer from '~/components/Footer.vue';




definePageMeta({
    layouts:'default  ',
})
</script>
<template>
  <div>
    <logo />
    <MainMenu />
    <Slideshow />
    <MenuItems/>
    <ProductsGrid/>
    <Footer/>
  </div>
</template>





