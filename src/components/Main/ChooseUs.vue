<template>
 <div class="md:w-11/12 mx-auto py-10">
    
    <div class="text-center mb-10">
      <h2 class="text-2xl font-bold mb-2">Why Choose Us?</h2>
      <p class="text-gray-500">Lorem ipsum dolor sit amet consectetur. Habitant ut elementum</p>
    </div>
 
    <div class="flex flex-col px-4 md:flex-row justify-center gap-6">
      <div 
        v-for="item in choice" 
        :key="item.header" 
        class="bg-[#FFF8F4] rounded-lg p-6 border  md:w-1/3 text-center">
        
    
        <div class="flex justify-center mb-4">
          <img :src="item.img" :alt="item.header" class="h-16 w-16">
        </div>
        
 
        <h3 class="text-xl font-semibold mb-2">{{ item.header }}</h3>
        <p class="text-gray-500">{{ item.body }}</p>
      </div>
    </div>
  </div>

</template>

<script>
import img1 from "@/assets/images/Maskgroup1.png"
import img2 from "@/assets/images/Maskgroup2.png"
import img3 from "@/assets/images/Maskgroup3.png"
export default {
    data(){
        return{
            choice:[
                {img:img1, header:'Serve Healthy Food', body:'Lorem ipsum dolor sit amet consectetur. Habitant ut elementum'},
                {img:img2, header:'Best Quality', body:'Lorem ipsum dolor sit amet consectetur. Habitant ut elementum'},
                {img:img3, header:'Fast Delivery', body:'Lorem ipsum dolor sit amet consectetur. Habitant ut elementum'},
            ]
        }
    }
}
</script>

<style>

</style>