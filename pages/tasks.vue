<template>    
    <div class="relative overflow-x-auto shadow-[0px_0px_13px_-7px_black] rounded-xl my-12">        
        <table class="w-full text-left rounded-xl overflow-hidden">
            <thead>
                <tr class="uppercase text-sm text-gray-600 bg-gray-100 border-b border-[#D1CFD7]">
                    <th class="p-4">Id</th>
                    <th class="p-4">Имя</th>
                    <th class="p-4">Количество</th>
                    <th class="p-4">Цена</th>
                    <th class="p-4">Обновлено</th>
                </tr>
            </thead>
            <tbody class="font-normal">
                <tr v-for="task in tasks.data" class="transition-colors duration-300 hover:bg-gray-100">
                    <th class="py-2 px-4">{{ task.id }}</th>
                    <th class="py-2 px-4">{{ task.packname }}</th>
                    <th class="py-2 px-4">{{ task.qty }}</th>
                    <th class="py-2 px-4">{{ task.price }}</th>
                    <th class="py-2 px-4">{{ task.updatetime }}</th>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script setup>
    /* const { data: workers, error: workersError } = await useFetch(``) */
    const tasks = ref(
        {
    "status": "ok",
    "data": [
        {
            "id": 3041704,
            "positionid": "variant_dd2bb68f-3ffa-11ed-0a80-090d0011b847",
            "date": "2023-07-26 15:55:00",
            "supplyid": "06824d14-2c7d-11ee-0a80-0f1b001199cf",
            "qty": 300,
            "price": 106.8128,
            "packprice": 1.75,
            "packname": "Легкая (без пакета). Упаковать в пакет + Наклеить наклейку + Уложить в коробку",
            "updatetime": "2023-10-23 16:45:32",
            "status": 1,
            "done": 0
        },
        {
            "id": 4244400,
            "positionid": "variant_d7206fad-b6bf-11ed-0a80-0bdb000042b6",
            "date": "2023-07-28 09:28:00",
            "supplyid": "89a54875-2f6b-11ee-0a80-0e8c002b867c",
            "qty": 300,
            "price": 100.4264,
            "packprice": 1.75,
            "packname": "Легкая (без пакета). Упаковать в пакет + Наклеить наклейку + Уложить в коробку",
            "updatetime": "2023-10-23 16:45:32",
            "status": 1,
            "done": 0
        },
        {
            "id": 13813659,
            "positionid": "variant_d7206fad-b6bf-11ed-0a80-0bdb000042b6",
            "date": "2023-08-20 14:44:00",
            "supplyid": "3d11fcac-4018-11ee-0a80-13e20033ee23",
            "qty": 200,
            "price": 0,
            "packprice": 1.75,
            "packname": "Легкая (без пакета). Упаковать в пакет + Наклеить наклейку + Уложить в коробку",
            "updatetime": "2023-10-23 16:45:32",
            "status": 1,
            "done": 0
        },
        {
            "id": 33685751,
            "positionid": "variant_fcf3f986-1192-11ed-0a80-01770032fb66",
            "date": "2023-09-25 14:02:00",
            "supplyid": "4e0f91e4-5c5c-11ee-0a80-1072000f2b57",
            "qty": 300,
            "price": 204.013,
            "packprice": 1.75,
            "packname": "Легкая (без пакета). Упаковать в пакет + Наклеить наклейку + Уложить в коробку",
            "updatetime": "2023-10-23 16:45:32",
            "status": 1,
            "done": 0
        },
        {
            "id": 41704590,
            "positionid": "variant_f5b1fa03-b804-11ed-0a80-10c600069385",
            "date": "2023-10-05 15:26:00",
            "supplyid": "91faf29d-637a-11ee-0a80-088f00118e0d",
            "qty": 100,
            "price": 811.04,
            "packprice": 2.45,
            "packname": "Средняя (без пакета). Упаковать в пакет + Наклеить наклейку + Уложить в коробку",
            "updatetime": "2023-10-23 16:45:32",
            "status": 1,
            "done": 0
        },
        {
            "id": 58353422,
            "positionid": "variant_f01e6d22-be74-11ed-0a80-0860006b21dd",
            "date": "2023-10-21 11:04:00",
            "supplyid": "f97d6eaa-717a-11ee-0a80-015c0030002e",
            "qty": 50,
            "price": 0,
            "packprice": 0.45,
            "packname": "Наклеить наклейку + Уложить в коробку",
            "updatetime": "2023-10-23 16:45:32",
            "status": 1,
            "done": 0
        },
        {
            "id": 58353424,
            "positionid": "variant_efdfc069-be74-11ed-0a80-0860006b2196",
            "date": "2023-10-21 11:04:00",
            "supplyid": "f97d6eaa-717a-11ee-0a80-015c0030002e",
            "qty": 70,
            "price": 0,
            "packprice": 0.45,
            "packname": "Наклеить наклейку + Уложить в коробку",
            "updatetime": "2023-10-23 16:45:32",
            "status": 1,
            "done": 0
        },
        {
            "id": 58354081,
            "positionid": "variant_fff542b6-b696-11ed-0a80-005b005f8c73",
            "date": "2023-10-21 11:06:00",
            "supplyid": "1fc91bb3-717b-11ee-0a80-015c003008f1",
            "qty": 300,
            "price": 0,
            "packprice": 1.75,
            "packname": "Легкая (без пакета). Упаковать в пакет + Наклеить наклейку + Уложить в коробку",
            "updatetime": "2023-10-23 16:45:32",
            "status": 1,
            "done": 0
        },
        {
            "id": 58354082,
            "positionid": "variant_ffec1fe1-b696-11ed-0a80-005b005f8c67",
            "date": "2023-10-21 11:06:00",
            "supplyid": "1fc91bb3-717b-11ee-0a80-015c003008f1",
            "qty": 200,
            "price": 0,
            "packprice": 1.75,
            "packname": "Легкая (без пакета). Упаковать в пакет + Наклеить наклейку + Уложить в коробку",
            "updatetime": "2023-10-23 16:45:32",
            "status": 1,
            "done": 0
        },
        {
            "id": 58355416,
            "positionid": "variant_0f27ed13-590d-11ee-0a80-02d900040582",
            "date": "2023-10-21 11:07:00",
            "supplyid": "501a9525-717b-11ee-0a80-10320032002a",
            "qty": 50,
            "price": 0,
            "packprice": 1.75,
            "packname": "Легкая (без пакета). Упаковать в пакет + Наклеить наклейку + Уложить в коробку",
            "updatetime": "2023-10-23 16:45:32",
            "status": 1,
            "done": 0
        },
        {
            "id": 58355417,
            "positionid": "variant_0f2e0f02-590d-11ee-0a80-02d90004058d",
            "date": "2023-10-21 11:07:00",
            "supplyid": "501a9525-717b-11ee-0a80-10320032002a",
            "qty": 50,
            "price": 0,
            "packprice": 1.75,
            "packname": "Легкая (без пакета). Упаковать в пакет + Наклеить наклейку + Уложить в коробку",
            "updatetime": "2023-10-23 16:45:32",
            "status": 1,
            "done": 0
        },
        {
            "id": 58355418,
            "positionid": "variant_0f1ae91c-590d-11ee-0a80-02d90004056c",
            "date": "2023-10-21 11:07:00",
            "supplyid": "501a9525-717b-11ee-0a80-10320032002a",
            "qty": 50,
            "price": 0,
            "packprice": 1.75,
            "packname": "Легкая (без пакета). Упаковать в пакет + Наклеить наклейку + Уложить в коробку",
            "updatetime": "2023-10-23 16:45:32",
            "status": 1,
            "done": 0
        },
        {
            "id": 58355419,
            "positionid": "variant_0f20d516-590d-11ee-0a80-02d900040577",
            "date": "2023-10-21 11:07:00",
            "supplyid": "501a9525-717b-11ee-0a80-10320032002a",
            "qty": 50,
            "price": 0,
            "packprice": 1.75,
            "packname": "Легкая (без пакета). Упаковать в пакет + Наклеить наклейку + Уложить в коробку",
            "updatetime": "2023-10-23 16:45:32",
            "status": 1,
            "done": 0
        },
        {
            "id": 58355420,
            "positionid": "variant_b2d6ae23-590d-11ee-0a80-14cc00045002",
            "date": "2023-10-21 11:07:00",
            "supplyid": "501a9525-717b-11ee-0a80-10320032002a",
            "qty": 50,
            "price": 0,
            "packprice": 0.45,
            "packname": "Наклеить наклейку + Уложить в коробку",
            "updatetime": "2023-10-23 16:45:32",
            "status": 1,
            "done": 0
        }
    ]
}
    )
</script>