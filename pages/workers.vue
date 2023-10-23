<template>    
    <div class="relative overflow-x-auto shadow-[0px_0px_13px_-7px_black] rounded-xl my-12">        
        <table class="w-full text-left rounded-xl overflow-hidden">
            <thead>
                <tr class="uppercase text-sm text-gray-600 bg-gray-100 border-b border-[#D1CFD7]">
                    <th class="p-4">Id</th>
                    <th class="p-4">Фото</th>
                    <th class="p-4">Имя</th>
                    <th class="p-4">Логин</th>
                    <th class="p-4">Телефон</th>
                    <th class="p-4">Email</th>
                    <th class="p-4">Группа</th>
                </tr>
            </thead>
            <tbody class="font-normal">
                <tr v-for="worker in workers.data" class="transition-colors duration-300 hover:bg-gray-100">
                    <th class="py-2 px-4">{{ worker.id }}</th>
                    <th class="py-2 px-4"><Icon name="material-symbols:emoji-people" class="text-2xl"/></th>
                    <th class="py-2 px-4">{{ worker.name }}</th>
                    <th class="py-2 px-4">{{ worker.username }}</th>
                    <th class="py-2 px-4">{{ worker.phone }}</th>
                    <th class="py-2 px-4">{{ worker.email }}</th>
                    <th class="py-2 px-4">{{ worker.usergroup }}</th>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script setup>
    /* const { data: workers, error: workersError } = await useFetch(``) */
    const workers = ref(
        {
    "status": "ok",
    "data": [
        {
            "id": 1,
            "groupid": 1,
            "username": "admin",
            "name": "Роман Никандров",
            "email": "chnry@yandex.ru",
            "photo": "avatar.jpeg",
            "phone": "+7(927)865-33-55",
            "last_activity": "2023-10-23 13:33:39",
            "created_at": "2022-03-28 12:06:22",
            "updated_at": "2023-10-23 13:33:39",
            "usergroup": "Администратор"
        },
        {
            "id": 2,
            "groupid": 6,
            "username": "pack1",
            "name": "Юлия",
            "email": "",
            "photo": "avatar.png",
            "phone": "",
            "last_activity": "2023-08-25 14:19:04",
            "created_at": "2022-03-28 12:06:22",
            "updated_at": "2023-08-25 14:19:04",
            "usergroup": "Упаковщик с отгрузкой"
        },
        {
            "id": 3,
            "groupid": 2,
            "username": "Elsayed",
            "name": "Саид",
            "email": "",
            "photo": "avatar.png",
            "phone": "",
            "last_activity": "2023-07-17 15:34:35",
            "created_at": "2022-03-28 12:06:22",
            "updated_at": "2023-07-17 15:34:35",
            "usergroup": "Кладовщик"
        },
        {
            "id": 4,
            "groupid": 3,
            "username": "pack3",
            "name": "Махмуд",
            "email": "",
            "photo": "avatar.png",
            "phone": "",
            "last_activity": "2023-09-29 11:08:11",
            "created_at": "2022-03-28 12:06:22",
            "updated_at": "2023-09-29 11:08:11",
            "usergroup": "Упаковщик"
        },
        {
            "id": 5,
            "groupid": 2,
            "username": "roman",
            "name": "Роман Васильев",
            "email": "",
            "photo": "avatar.png",
            "phone": "",
            "last_activity": "2023-10-23 16:24:59",
            "created_at": "2022-03-28 12:06:22",
            "updated_at": "2023-10-23 16:24:59",
            "usergroup": "Кладовщик"
        },
        {
            "id": 6,
            "groupid": 3,
            "username": "pack4",
            "name": "Ая",
            "email": "",
            "photo": "avatar.png",
            "phone": "",
            "last_activity": "2023-07-17 14:46:31",
            "created_at": "2022-03-28 12:06:22",
            "updated_at": "2023-10-21 01:32:08",
            "usergroup": "Упаковщик"
        },
        {
            "id": 7,
            "groupid": 1,
            "username": "admin2",
            "name": "Tatyana",
            "email": "",
            "photo": "avatar.png",
            "phone": "",
            "last_activity": "2023-10-22 17:07:39",
            "created_at": "2022-03-28 12:06:22",
            "updated_at": "2023-10-22 17:07:39",
            "usergroup": "Администратор"
        },
        {
            "id": 8,
            "groupid": 3,
            "username": "olga1",
            "name": "Малькова Ольга",
            "email": null,
            "photo": "avatar.png",
            "phone": null,
            "last_activity": "2023-07-21 17:20:37",
            "created_at": "2023-07-21 08:09:06",
            "updated_at": "2023-07-21 17:20:37",
            "usergroup": "Упаковщик"
        },
        {
            "id": 9,
            "groupid": 3,
            "username": "viktoria1",
            "name": "Григорьева Виктория",
            "email": null,
            "photo": "avatar.png",
            "phone": null,
            "last_activity": "2023-10-10 18:37:32",
            "created_at": "2023-07-21 08:09:56",
            "updated_at": "2023-10-10 18:37:32",
            "usergroup": "Упаковщик"
        },
        {
            "id": 10,
            "groupid": 3,
            "username": "maria1",
            "name": "Падышева Мария",
            "email": null,
            "photo": "avatar.png",
            "phone": null,
            "last_activity": "2023-09-30 13:53:47",
            "created_at": "2023-07-21 08:10:51",
            "updated_at": "2023-09-30 13:53:51",
            "usergroup": "Упаковщик"
        },
        {
            "id": 11,
            "groupid": 3,
            "username": "nosova",
            "name": "Носова Татьяна Владимировна",
            "email": null,
            "photo": "avatar.png",
            "phone": null,
            "last_activity": "2023-10-05 15:53:42",
            "created_at": "2023-10-03 15:31:13",
            "updated_at": "2023-10-05 15:53:42",
            "usergroup": "Упаковщик"
        },
        {
            "id": 12,
            "groupid": 3,
            "username": "grishina",
            "name": "Гришина Анна Сергеевна",
            "email": null,
            "photo": "avatar.png",
            "phone": null,
            "last_activity": "2023-10-05 15:47:28",
            "created_at": "2023-10-04 08:41:58",
            "updated_at": "2023-10-05 15:47:28",
            "usergroup": "Упаковщик"
        },
        {
            "id": 13,
            "groupid": 5,
            "username": "larionova",
            "name": "Ларионова Татьяна Анатольевна",
            "email": null,
            "photo": "avatar.png",
            "phone": null,
            "last_activity": "2023-10-23 16:28:47",
            "created_at": "2023-10-10 09:18:29",
            "updated_at": "2023-10-23 16:28:47",
            "usergroup": "Старший упаковщик"
        },
        {
            "id": 14,
            "groupid": 5,
            "username": "shteynikova",
            "name": "Штейникова Юлия Николаевна",
            "email": null,
            "photo": "avatar.png",
            "phone": null,
            "last_activity": "2023-10-23 16:26:17",
            "created_at": "2023-10-13 08:05:59",
            "updated_at": "2023-10-23 16:26:17",
            "usergroup": "Старший упаковщик"
        }
    ]
}
    )
</script>