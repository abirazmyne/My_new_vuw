<template>
    <HeroArea></HeroArea>
    <ShopInfo></ShopInfo>
    <AllProducts></AllProducts>
    <BrandsArea></BrandsArea>
    <BlogsArea></BlogsArea>


</template>

<script>
    import HeroArea from "@/components/home/HeroArea";
    import AllProducts from "@/components/home/AllProducts";
    import ShopInfo from "@/components/home/ShopInfo";
    import BlogsArea from "@/components/home/BlogsArea";
    import BrandsArea from "@/components/home/BrandsArea";

export default {
  name: 'HomeView',
  components: {HeroArea, AllProducts, ShopInfo, BrandsArea, BlogsArea},

}
</script>
