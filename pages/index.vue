<template>
<div class="div">
  <div class="container">
  <Hero/>
  <LargeCardDisplay 
    v-for="cardInfo in largeCardInfo"
    :key="cardInfo.id"
    :cardsSection="cardInfo"
  />
  <SmallCardDisplay 
    v-for="cardInfo in smallCardSections"
    :key="cardInfo.id"
    :cardsSection="cardInfo"
  />
  </div>
</div>
</template>

<script>
import { largeCardSections, smallCardSections } from "@/api-data/data.js"
import LargeCardDisplay from '../components/LargeCardDisplay.vue'
export default {
  layout: '@/layout/default',
  components: { LargeCardDisplay },
  data(){
    return{
      largeCardInfo: largeCardSections,
      smallCardSections: smallCardSections
    
    }
  }
}
</script>

<style>

</style>
