<template>
    <div class="absolute w-full h-screen z-50 inset-0 flex items-center justify-center text-[#1D1D1D] bg-white">
        <FormKit type="form" form-class="flex flex-col items-center gap-12 w-full md:w-1/2 xl:w-1/3 px-[15px] sm:px-5" @submit="login" :actions="false">
            <img src="/images/header/logo.png" alt="" class="w-fit">
            <div class="flex flex-col gap-6 w-full">
                <FormKit v-model="user.username" type="text" validation="required|length:5" :validation-messages="{ length: 'Поле Логин должно содержать не менее 5 символов' }" inner-class="w-full" input-class="w-full rounded-lg border-[0.6px] border-[#C3C3C3] py-4 px-7" message-class="text-[#E71616]" wrapper-class="flex flex-col gap-3" label="Логин" placeholder="Введите ваш логин"/>
                <FormKit v-model="user.password" type="password" :validation-messages="{ length: 'Поле Пароль должно содержать не менее 5 символов' }" validation="required|length:5" inner-class="w-full" input-class="w-full rounded-lg border-[0.6px] border-[#C3C3C3] py-4 px-7" message-class="text-[#E71616]" wrapper-class="flex flex-col gap-3" label="Пароль" placeholder="Введите ваш пароль"/>
            </div>
            <FormKit type="submit" outer-class="w-full" wrapper-class="w-full" input-class="w-full text-white rounded-lg bg-[#1F75A8] font-medium py-3.5 text-center">Войти</FormKit>
        </FormKit>   
    </div>
</template>

<script setup>   
    const authStore = useAuthStore()
    const authenticateUser = authStore.authenticateUser

    const user = ref({
        username: "kminchelle",
        password: "0lelplR"
    })
    const router = useRouter()    
    
    const login = async () => {
        await authenticateUser(user.value)
        if (authStore.authenticated) {
            router.push('/')
        }
    }
</script>