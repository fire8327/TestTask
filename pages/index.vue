<template>
    <div class="absolute w-full h-full z-50 inset-0 flex items-center justify-center text-[#1D1D1D] bg-white">
        <div class="flex flex-col items-center gap-12 w-full md:w-1/2 xl:w-1/3 px-[15px] sm:px-5">
            <img src="/images/header/logo.png" alt="" class="w-fit">
            <div class="flex flex-col gap-6 w-full">
                <div class="flex flex-col gap-3">
                    <p class="font-medium">Логин</p>
                    <input type="text" class="w-full rounded-lg border-[0.6px] border-[#C3C3C3] py-4 px-7" placeholder="Введите ваш логин">
                </div>
                <div class="flex flex-col gap-3">
                    <p class="font-medium">Пароль</p>
                    <input type="text" class="w-full rounded-lg border-[0.6px] border-[#C3C3C3] py-4 px-7" placeholder="Введите ваш пароль">
                </div>
            </div>
            <NuxtLink to="/workers" class="w-full text-lg text-white rounded-lg bg-[#1F75A8] font-medium py-3.5 text-center">Войти</NuxtLink>
        </div>   
    </div>
</template>

<script setup>    

</script>