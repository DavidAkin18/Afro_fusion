<template>
  <div class="bg-[#FFF8F4] border-b-4 w-full shadow-md fixed z-10 top-0 ">
    <div class="h-14 px-2 md:px-4  w-full md:w-11/12 mx-auto flex justify-between items-center">
        <div @click="handleShowItems" class="md:hidden cursor-pointer">
            <i class="ri-menu-line"></i>
        </div>
        <ul ref="menu" class="fixed top-14 left-0 w-60 bg-[#FFF8F4] z-50 flex flex-col gap-4 p-4 md:flex md:static md:flex-row md:gap-3.5 md:bg-transparent md:p-0"
        :class="{ 'hidden': !showItems, 'block': showItems, 'md:flex': true }">
            <li class="hover:underline-offset-2 text-xl hover:border-b-2 border-[#904C1D] pb-1"  v-for="item in items" :key="item.name">
                {{ item.name }}
            </li>
        </ul>
        <h3 class="text-black text-lg md:text-2xl font-semibold">Afro Fusion Delights</h3>
        <div class="flex gap-2 md:gap-4 items-center text-md md:text-xl">
            <i class="ri-search-line"></i>
            <i class="ri-heart-fill"></i>
            <i class="ri-shopping-cart-fill"></i>
            <h3><i class="ri-account-circle-fill pl-1"></i>sign in</h3>
        </div>
    </div>
    <div
      v-if="showItems && screenIsSmall"
      class="fixed inset-0 bg-black opacity-50 z-40"
      @click="closeMenu"
    ></div>
    <!-- <hr class="border-2 "> -->
  </div>
 
</template>

<script>
import { ref } from 'vue';

export default {
    data(){
        return{
            showItems:false,
            items:[
                {name:'home'},
                {name:'blog'},
                {name:'contact'}
            ],
            screenIsSmall: window.innerWidth < 768,
        }
    },
    methods:{
        handleShowItems(){
            if(this.screenIsSmall){
                this.showItems = !this.showItems
            }
        },
        closeMenu() {
            if (this.screenIsSmall) {
                this.showItems = false;
            }
        },
        handleClickOutside(event){
            if(this.showItems && this.$refs.menu && !this.$refs.menu.contains(event.target)){
                this.closeMenu();
            }
        },
        updateScreenSize() {
            this.screenIsSmall = window.innerWidth < 768;
            if (!this.screenIsSmall) {
                this.showItems = false; 
            }
        },
        mounted() {
            document.addEventListener('click', this.handleClickOutside);
            window.addEventListener('resize', this.updateScreenSize);
        },
        beforeUnmount() {
            document.removeEventListener('click', this.handleClickOutside);
            window.removeEventListener('resize', this.updateScreenSize);
        }
    }
}
</script>

<style>

</style>