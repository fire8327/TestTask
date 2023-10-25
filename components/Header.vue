<template>
    <header class="grid-container py-7 text-[#1D1D1D] relative" ref="height">
        <div class="flex items-center gap-12 justify-between">
            <NuxtLink to="/">
                <img src="/images/header/logo.png" alt="">
            </NuxtLink>
            <div class="flex items-center gap-8 max-xl:flex-col bg-white max-xl:h-screen max-xl:absolute max-xl:w-full max-xl:left-0 max-xl:z-40 transition-transform duration-500" :class="isMenuShow ? 'max-xl:top-full' : 'max-xl:top-0 max-xl:-translate-y-full'"> 
                <div class="xl:hidden w-full h-0.5 bg-[#000000]/10"></div> 
                <div class="flex items-center gap-6 max-md:flex-col">
                    <HeaderDropdown v-for="dropdown in dropdowns" v-bind="dropdown"/>
                </div>
                <div class="xl:hidden w-full h-0.5 bg-[#000000]/10"></div> 
                <div class="flex max-md:flex-col max-md:gap-4 xl:items-center gap-2.5 max-xl:order-first">
                    <div class="flex items-center gap-4 py-2 px-4 rounded-lg bg-[#F6F6F6]">
                        <p class="shrink-0">Заработано</p>
                        <p class="shrink-0 text-[#E71616]">0 руб.</p>
                    </div>
                    <div class="flex items-center gap-4 py-2 px-4 rounded-lg bg-[#F6F6F6]">
                        <p class="shrink-0">К выплате</p>
                        <p class="shrink-0 text-[#34B846]">1500 руб.</p>
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
                    <div class="relative group">
                        <button @click="isProfileDown = !isProfileDown" v-on-click-outside="closeProfile" class="relative rounded-lg w-10 h-10 flex items-center justify-center transition-colors duration-300" :class="isProfileDown ? 'bg-[#1F75A8]' : 'bg-[#F6F6F6]'">
                            <Icon name="material-symbols:person" class="text-2xl transition-colors duration-300" :class="isProfileDown ? 'text-white' : 'text-[#1D1D1D]'"/>
                            <span class="absolute rounded-full flex items-center justify-center bg-black w-5 h-5 -top-2 -right-2">
                                <Icon name="ph:gift" class="text-white text-sm"/>
                            </span>
                        </button>
                        <div class="absolute z-50 top-[calc(100%+10px)] shadow-[3px_2px_16px_0px_rgba(0,0,0,0.10)] w-fit flex flex-col rounded-lg transition-all duration-500 bg-white max-xl:left-1/2 max-xl:-translate-x-1/2 right-0" :class="{'hidden' : !isProfileDown}">
                            <NuxtLink @click="closeProfile" class="transition-all duration-500 hover:bg-gray-200 px-4 py-1.5 first:rounded-t-lg last:rounded-b-lg">Профиль</NuxtLink>
                            <NuxtLink @click="closeProfile" class="transition-all duration-500 hover:bg-gray-200 px-4 py-1.5 first:rounded-t-lg last:rounded-b-lg">Зар.плата</NuxtLink>
                            <NuxtLink to="/login" @click="closeProfile" class="transition-all duration-500 hover:bg-gray-200 px-4 py-1.5 first:rounded-t-lg last:rounded-b-lg border-t border-[#D1CFD7] text-[#34B846]">Войти</NuxtLink>
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
    import { vOnClickOutside } from '@vueuse/components'

    const dropdowns = [
        {
            title: "Отчёты",
            contents: [
                {
                    link: "/workers",
                    title: "Сотрудники"
                },
                {
                    link: "/statuses",
                    title: "Статусы"
                },
                {
                    link: "/tasks",
                    title: "Задачи"
                }
            ]
        },
        {
            title: "Операции",
            contents: [
                {
                    link: "/workers",
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
    const isProfileDown = ref(false)
    function closeProfile() {
        isProfileDown.value = false
    }


    const height = ref()
    const header = useHeader()
    onMounted(() => {
        header.height = height.value.clientHeight
        window.addEventListener("resize", () => {
            header.height = height.value.clientHeight
        })
    })    

    const isMenuShow = ref()
    const nuxtApp = useNuxtApp()
    nuxtApp.hook('page:start', () => {
        isMenuShow.value = false
    })
    
</script>