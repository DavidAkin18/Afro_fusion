<template>
    <div class="p-4 md:w-11/12 mx-auto">
        <h1 class="font-bold text-2xl leading-10">Our Menu</h1>
        <div class="flex flex-col  md:flex-row gap-3">
            <div 
                v-for="item in menus" 
                :key="item.name" 
                class="bg-[#FEEEE4] p-3 border rounded-md border-[#BEB7B7] md:w-1/4"
            >
                <div class="flex flex-col items-center md:items-start">
                    <img 
                        :src="item.img" 
                        :alt="item.name" 
                        class="w-full h-full object-cover rounded-md"
                    />
                    <div class="flex  items-center gap-4 md:gap-2 mt-2">
                        <div>
                            <h3 class="font-bold text-base">{{ item.name }}</h3>
                            <p class="flex gap-1 text-base text-[#FD9900]">
                                <img src="../../assets/images/Naira.svg" alt="">
                                {{ item.price }}
                            </p>
                        </div>
                        <div class="p-2 rounded-md bg-[#FD9900]">
                            <img src="../../assets/images/garden_cart.svg" alt="">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import img1 from '@/assets/images/menu1.png'
import img2 from '@/assets/images/menu2.png'
import img3 from '@/assets/images/menu3.png'
import img4 from '@/assets/images/menu4.png'
export default {
    data(){
        return{
            menus:[
                {name:'Nyama Choma', img:img1, price:'10,000'},
                {name:'Nyama Choma', img:img2, price:'10,000'},
                {name:'Nyama Choma', img:img3, price:'10,000'},
                {name:'Nyama Choma', img:img4, price:'10,000'},
            ]
        }
    }
}
</script>

<style>

</style>