<template>
  <div class="">
    <section class="sec-one   ">
        <div class="px-4 py-10 md:py-20 md:w-11/12 mx-auto w-full md:flex gap-4 flex-row-reverse items-center">
            <div class="md:w-1/2">
                <div class="w-full">
                    <img :src="largeImage" width="inherit" height="inherit" alt="hero" class="md:w-6/6">
                </div>
                <div class="flex p-1 mx-auto w-1/3 gap-1 cursor-pointer">
                    <div v-for="(imgSrc, index) in smallImages" :key="index">
                        <img
                            :src="imgSrc"
                            alt="food image"
                            class="cursor-pointer"
                            @click="changeImage(index)"
                        />
                    </div>
                </div>
            </div>
            <div class="pt-4 md:pt-0 md:w-1/2 md:px-4">
                <h2 class="text-xl md:text-3xl text-center md:text-left font-bold leading-8">Experience the Rich Tapestry of African Flavors</h2>
                <p class="text-lg md:text-xl text-[#818181] leading-8 text-center md:text-left">
                    Immerse yourself in a culinary journey like no other at Afro fusion delight, Our menu is a celebration of the diverse and vibrant tapestry of African flavors.
                </p>
                <div class="flex w-full gap-2 pt-2 text-center items-center justify-center">
                    <button class="border rounded-md p-2 md:w-2/3 bg-[#FD9900] text-[#fff]">EXPLORE OUR MENU</button>
                    <button class="border border-[#FD9900] md:w-1/2  rounded-md p-2 ">CONTACT US</button>
                </div>
            </div>
        </div>
    </section>
  </div>
</template>

<script>
export default {
    data(){
        return{
            largeImage: require('../../assets/images/hero.png'),
            smallImages:[
                require('../../assets/images/foodSmall1.png'),
                require('../../assets/images/foodSmall2.png'),
                require('../../assets/images/foodSmall3.png'),
                require('../../assets/images/foodSmall1.png'),
            ],
            largeImages:[
                require('../../assets/images/food1.png'),
                require('../../assets/images/food2.png'),
                require('../../assets/images/food3.png'),
                require('../../assets/images/food1.png')
            ]

        }
    },
    methods:{
        changeImage(index){
            this.largeImage = this.largeImages[index]
        }
    }
}
</script>

<style scoped>
.sec-one{
    background: url('../../assets/images/Handrawn\ barbecue\ elements.png');
    width: 100%;
    background-position: contain;
    background-size: cover;
    background-repeat: no-repeat;
    min-height: 100%;
}
</style>