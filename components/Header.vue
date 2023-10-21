<template>
    <header class="grid-container py-7 text-[#1D1D1D] relative">
        <div class="flex items-center gap-16 justify-between">
            <NuxtLink to="/">
                <img src="/images/header/logo.png" alt="">
            </NuxtLink>
            <div class="flex items-center gap-8 max-xl:flex-col bg-white max-xl:h-screen max-xl:absolute max-xl:w-full max-xl:left-0 max-xl:z-40 transition-transform duration-500" :class="isMenuShow ? 'max-xl:top-full' : 'max-xl:top-0 max-xl:-translate-y-full'"> 
                <div class="xl:hidden w-full h-0.5 bg-[#000000]/10"></div> 
                <div class="flex items-center gap-10 max-md:flex-col">
                    <HeaderDropdown v-for="dropdown in dropdowns" v-bind="dropdown"/>
                </div>
                <div class="xl:hidden w-full h-0.5 bg-[#000000]/10"></div> 
                <div class="flex max-md:flex-col max-md:gap-4 xl:items-center gap-2.5 max-xl:order-first">
                    <div class="flex items-center gap-6 py-2 px-4 rounded-lg bg-[#F6F6F6]">
                        <p>Заработано</p>
                        <p class="text-[#E71616]">0 руб.</p>
                    </div>
                    <div class="flex items-center gap-6 py-2 px-4 rounded-lg bg-[#F6F6F6]">
                        <p>К выплате</p>
                        <p class="text-[#34B846]">1500 руб.</p>
                    </div>
                </div>
                <div class="flex items-center gap-5">
                    <div class="relative rounded-lg bg-[#F6F6F6] w-10 h-10 flex items-center justify-center">
                        <Icon name="material-symbols:notifications-active-rounded" class="text-2xl"/>
                        <div class="absolute rounded-full flex items-center justify-center bg-black w-5 h-5 -top-2 -right-2">
                            <p class="text-white text-sm">9</p>
                        </div>
                    </div>
                    <div class="relative rounded-lg bg-[#F6F6F6] w-10 h-10 flex items-center justify-center">
                        <Icon name="material-symbols:help" class="text-2xl"/>
                    </div>
                    <div class="relative rounded-lg bg-[#F6F6F6] w-10 h-10 flex items-center justify-center">
                        <Icon name="material-symbols:person" class="text-2xl"/>
                        <div class="absolute rounded-full flex items-center justify-center bg-black w-5 h-5 -top-2 -right-2">
                            <Icon name="ph:gift" class="text-white text-sm"/>
                        </div>
                    </div>
                </div>            
            </div>
            <button @click="isMenuShow = !isMenuShow" class="flex flex-col justify-between w-[26px] transition-[height] ease-linear duration-100 xl:hidden" :class="isMenuShow ? 'h-5' : 'h-3.5'">
                <span :class="{'rotate-45' : isMenuShow}" class="w-full h-0.5 bg-[#1D1D1D] rounded-[1px] origin-[0] transition-transform ease-linear duration-500"></span>
                <span :class="{'opacity-0' : isMenuShow}" class="w-full h-0.5 bg-[#1D1D1D] rounded-[1px] transition-opacity ease-linear duration-500"></span>
                <span :class="{'-rotate-45' : isMenuShow}" class="w-full h-0.5 bg-[#1D1D1D] rounded-[1px] origin-[0] transition-transform ease-linear duration-500"></span>
            </button>
        </div>
    </header>
</template>

<script setup>
    const isMenuShow = ref(false)
    const dropdowns = [
        {
            title: "Отчёты",
            contents: [
                {
                    link: "/",
                    title: "Сотрудники"
                },
                {
                    link: "/",
                    title: "Статусы"
                },
                {
                    link: "/",
                    title: "Операции"
                }
            ]
        },
        {
            title: "Операции",
            contents: [
                {
                    link: "/",
                    title: "Сотрудники"
                },
                {
                    link: "/",
                    title: "Статусы"
                },
                {
                    link: "/",
                    title: "Операции"
                }
            ]
        },
        {
            title: "Склад",
            contents: [
                {
                    link: "/",
                    title: "Сотрудники"
                },
                {
                    link: "/",
                    title: "Статусы"
                },
                {
                    link: "/",
                    title: "Операции"
                }
            ]
        },
        {
            title: "Справочник",
            contents: [
                {
                    link: "/",
                    title: "Сотрудники"
                },
                {
                    link: "/",
                    title: "Статусы"
                },
                {
                    link: "/",
                    title: "Операции"
                }
            ]
        }
    ]
</script>