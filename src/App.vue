<template>
  <div>
    <HeaderLayout fonts="nexon" />
    <SliderSection attr="nexon type" />
    <ImageSection attr="section nexon type" layout="container" />
    <ImgTextSection attr="section nexon brown type" layout="container" />
    <CardSection attr="section nexon type" layout="container" />
    <BannerSection attr="nexon type" />
    <TextSection attr="section nexon type" layout="container" />
    <FooterLayout attr="nexon section brown type" layout="container" />
  </div>
</template>

<script>
import HeaderLayout from "./components/layout/HeaderLayout.vue";
import SliderSection from "./components/section/SliderSection.vue";
import ImageSection from "./components/section/ImageSection.vue";
import ImgTextSection from "./components/section/ImgTextSection.vue";
import FooterLayout from "./components/layout/FooterLayout.vue";
import CardSection from "./components/section/CardSection.vue";
import BannerSection from "./components/section/BannerSection.vue";
import TextSection from "./components/section/TextSection.vue";

export default {
  name: "App",
  components: {
    HeaderLayout,
    FooterLayout,
    ImageSection,
    ImgTextSection,
    SliderSection,
    CardSection,
    BannerSection,
    TextSection,
  },
};
</script>
