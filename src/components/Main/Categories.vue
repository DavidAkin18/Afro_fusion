<template>
  <div class="py-6 px-2 md:w-11/12 mx-auto">
   
    <h2 class="text-center text-2xl font-semibold pb-30">
      Categories
    </h2>
    
    <div class="flex flex-col md:flex-row gap-4 px-2 my-20 mb-4 justify-center">
      <div 
        v-for="category in categories"
        :key="category.header"
        class="bg-[#2B1706] text-center rounded-lg shadow-md"
      >
        
        <div class="p-4  h-2/4">
          <img :src="category.img" :alt="category.header" class="w-52 mx-auto md:relative bottom-20">
        </div>
        <div class="p-4 pt-0 text-white">
          <h3 class="font-bold text-lg pb-2">{{ category.header }}</h3>
          <p class="text-sm">{{ category.body }}</p>
        </div>
      </div>
    </div>
    <div class="rounded-lg px-2">
        <img src="../../assets/images/frame.png" alt="">
    </div>
  </div>
</template>

<script>
import cate1 from '@/assets/images/cate1.png'
import cate2 from '@/assets/images/cate2.png'
import cate3 from '@/assets/images/cate3.png'
export default {
    data(){
        return{
            categories:[
                {img:cate1, header:'Afro-Spiced Chicken', body:'Lorem ipsum dolor sit amet consectetur. Habitant ut elementum tempor eget libero sit diam felis..'},
                {img:cate2, header:'Afro-Spiced Chicken', body:'Lorem ipsum dolor sit amet consectetur. Habitant ut elementum tempor eget libero sit diam felis..'},
                {img:cate3, header:'Afro-Spiced Chicken', body:'Lorem ipsum dolor sit amet consectetur. Habitant ut elementum tempor eget libero sit diam felis..'},
            ]
        }
    }
}
</script>

<style>

</style>