<template>
    <div class="absolute w-full h-full z-50 inset-0 flex items-center justify-center text-[#1D1D1D] bg-white">
        <FormKit type="form" form-class="flex flex-col items-center gap-12 w-full md:w-1/2 xl:w-1/3 px-[15px] sm:px-5" :actions="false">
            <img src="/images/header/logo.png" alt="" class="w-fit">
            <div class="flex flex-col gap-6 w-full">
                <FormKit type="text" validation="required|length:5" inner-class="w-full $remove:max-w-md" input-class="w-full rounded-lg border-[0.6px] border-[#C3C3C3] py-4 px-7" message-class="text-[#E71616]" wrapper-class="flex flex-col gap-3" label="Логин" placeholder="Введите ваш логин"/>
                <FormKit type="password" validation="required|length:5" inner-class="w-full $remove:max-w-md" input-class="w-full rounded-lg border-[0.6px] border-[#C3C3C3] py-4 px-7" message-class="text-[#E71616]" wrapper-class="flex flex-col gap-3" label="Пароль" placeholder="Введите ваш пароль"/>
            </div>
            <NuxtLink to="/workers" class="w-full text-lg text-white rounded-lg bg-[#1F75A8] font-medium py-3.5 text-center">Войти</NuxtLink>
        </FormKit>   
    </div>
</template>

<script setup>    

</script>