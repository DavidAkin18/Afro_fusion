<template>
  <div class="p-4 w-full text-center mx-auto md:w-11/12">
    <h2 class="pb-12 font-bold text-3xl">Testimonials</h2>
    <div class="flex flex-col relative rounded-2xl md:w-2/5 p-4 py-6 border mx-auto bg-[#FFF8F4] items-center mt-12 shadow-inner" style="box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25) inset;">
        <div v-for="item in items" :key="item.name">
            <div class="text-center flex items-center justify-center absolute -top-16 left-1/3">
                <img :src="item.avatar" :alt="item.name" class="">
            </div>
            <div class="pt-6">
                <h4 class="font-bold text-xl">{{ item.name }}</h4>
                <p class="leading-6 text-[#848484] text-base">{{ item.body }}</p>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
import img1 from '@/assets/images/iiiii.svg'
export default {
    data(){
        return{
            items:[
                {name:'Awee John', avatar:img1, body:'Lorem ipsum dolor sit amet consectetur. Gravida congue viverra arcu arcu. Ac fringilla egestas duis a at tincidunt lectus tristique. Venenatis interdum tortor posuere phasellus vitae faucibus. Varius pellentesque egestas at nunc.'}
            ]
        }
    }
}
</script>

<style>

</style>