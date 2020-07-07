<template>
    <div class="flex p-2">
        <div class="flex-grow mr-2">
            <h1 class="font-sans text-4xl mt-10 mb-3">Evolução de Casos Confirmados</h1>
            <area-chart
                    id="area_2"
                    :data="evolution"
                    resize="true"
                    line-colors='[ "#FF6384" ]'
                    grid="true"
                    xkey="data"
                    labels='["Casos"]'
                    ykeys='["casos"]'
                    grid-text-weight="bold">
            </area-chart>
        </div>
        <div class="my-10 flex-none">
            <div class="bg-white rounded overflow-hidden shadow-lg">
                <div class="text-center p-6  border-b">
                    <p class="pt-2 text-lg font-semibold">Último boletim</p>
                    <p class="text-sm font-bold">06/07/2020</p>
                </div>
                <div class="border-b">
                    <div href="#" class="px-4 py-2 hover:bg-gray-100 flex">
                        <div class="text-gray-800">
                            <svg
                                    fill="none"
                                    stroke="currentColor"
                                    strokeLinecap="round"
                                    strokeLinejoin="round"
                                    strokeWidth="0"
                                    viewBox="0 0 20 20"
                                    class="w-5 h-5"
                            >
                                <path d="M15.573,11.624c0.568-0.478,0.947-1.219,0.947-2.019c0-1.37-1.108-2.569-2.371-2.569s-2.371,1.2-2.371,2.569c0,0.8,0.379,1.542,0.946,2.019c-0.253,0.089-0.496,0.2-0.728,0.332c-0.743-0.898-1.745-1.573-2.891-1.911c0.877-0.61,1.486-1.666,1.486-2.812c0-1.79-1.479-3.359-3.162-3.359S4.269,5.443,4.269,7.233c0,1.146,0.608,2.202,1.486,2.812c-2.454,0.725-4.252,2.998-4.252,5.685c0,0.218,0.178,0.396,0.395,0.396h16.203c0.218,0,0.396-0.178,0.396-0.396C18.497,13.831,17.273,12.216,15.573,11.624 M12.568,9.605c0-0.822,0.689-1.779,1.581-1.779s1.58,0.957,1.58,1.779s-0.688,1.779-1.58,1.779S12.568,10.427,12.568,9.605 M5.06,7.233c0-1.213,1.014-2.569,2.371-2.569c1.358,0,2.371,1.355,2.371,2.569S8.789,9.802,7.431,9.802C6.073,9.802,5.06,8.447,5.06,7.233 M2.309,15.335c0.202-2.649,2.423-4.742,5.122-4.742s4.921,2.093,5.122,4.742H2.309z M13.346,15.335c-0.067-0.997-0.382-1.928-0.882-2.732c0.502-0.271,1.075-0.429,1.686-0.429c1.828,0,3.338,1.385,3.535,3.161H13.346z"></path>
                            </svg>
                        </div>
                        <div class="pl-3">
                            <p class="text-sm font-medium text-gray-800 leading-none">3112</p>
                            <p class="text-xs text-gray-500">Casos confirmados</p>
                        </div>
                    </div>
                    <div href="#" class="px-4 py-2 hover:bg-gray-100 flex">
                        <div class="text-green-600">
                            <svg
                                    fill="none"
                                    stroke="currentColor"
                                    strokeLinecap="round"
                                    strokeLinejoin="round"
                                    strokeWidth="1"
                                    viewBox="0 0 24 24"
                                    class="w-5 h-5"
                            >
                                <path d="M14.613,10c0,0.23-0.188,0.419-0.419,0.419H10.42v3.774c0,0.23-0.189,0.42-0.42,0.42s-0.419-0.189-0.419-0.42v-3.774H5.806c-0.23,0-0.419-0.189-0.419-0.419s0.189-0.419,0.419-0.419h3.775V5.806c0-0.23,0.189-0.419,0.419-0.419s0.42,0.189,0.42,0.419v3.775h3.774C14.425,9.581,14.613,9.77,14.613,10 M17.969,10c0,4.401-3.567,7.969-7.969,7.969c-4.402,0-7.969-3.567-7.969-7.969c0-4.402,3.567-7.969,7.969-7.969C14.401,2.031,17.969,5.598,17.969,10 M17.13,10c0-3.932-3.198-7.13-7.13-7.13S2.87,6.068,2.87,10c0,3.933,3.198,7.13,7.13,7.13S17.13,13.933,17.13,10"></path>
                            </svg>
                        </div>
                        <div class="pl-3">
                            <p class="text-sm font-medium text-green-600 leading-none">+ 156</p>
                            <p class="text-xs text-gray-500">Novos casos</p>
                        </div>
                    </div>
                    <div href="#" class="px-4 py-2 hover:bg-gray-100 flex">
                        <div class="text-red-500">
                            <svg
                                    fill="currentColor"
                                    stroke="currentColor"
                                    strokeLinecap="round"
                                    strokeLinejoin="round"
                                    strokeWidth="1"
                                    viewBox="0 0 457.983 457.983"
                                    class="w-5 h-5"
                            >
                                <path d="M250.654 123.777h102.12V167.1h-102.12v253.746h-43.326V167.1h-102.12v-43.323h102.12V37.131h43.326v86.646zm139.252-37.134v117.592h-102.12v253.749H170.197v-253.75H68.077V86.643h102.121V0h117.589v86.643h102.119zm-18.572 18.563H269.22V18.562h-80.454v86.643H86.646v80.458h102.12v253.743h80.454V185.663h102.127v-80.458h-.013z"/>
                            </svg>
                        </div>
                        <div class="pl-3">
                            <p class="text-sm font-medium text-red-500 leading-none">14</p>
                            <p class="text-xs text-gray-500">Mortes Registradas</p>
                        </div>
                    </div>

                    <div href="#" class="px-4 py-2 hover:bg-gray-100 flex">
                        <div class="text-yellow-600">
                            <svg
                                    fill="none"
                                    stroke="currentColor"
                                    strokeLinecap="round"
                                    strokeLinejoin="round"
                                    strokeWidth="1"
                                    viewBox="0 0 24 24"
                                    class="w-5 h-5"
                            >
                                <path stroke="none" d="M0 0h24v24H0z"/>
                                <path d="M13 3a1 1 0 0 1 1 1v4.535l3.928 -2.267a1 1 0 0 1 1.366 .366l1 1.732a1 1 0 0 1 -.366 1.366L16.001 12l3.927 2.269a1 1 0 0 1 .366 1.366l-1 1.732a1 1 0 0 1 -1.366 .366L14 15.464V20a1 1 0 0 1 -1 1h-2a1 1 0 0 1 -1 -1v-4.536l-3.928 2.268a1 1 0 0 1 -1.366 -.366l-1-1.732a1 1 0 0 1 .366 -1.366L7.999 12 4.072 9.732a1 1 0 0 1 -.366 -1.366l1-1.732a1 1 0 0 1 1.366 -.366L10 8.535V4a1 1 0 0 1 1 -1h2z" />
                            </svg>
                        </div>
                        <div class="pl-3">
                            <p class="text-sm font-medium text-yellow-600 leading-none">33</p>
                            <p class="text-xs text-gray-500">Pessoas em UTI</p>
                        </div>
                    </div>

                    <div href="#" class="px-4 py-2 hover:bg-gray-100 flex">
                        <div class="text-blue-600">
                            <svg
                                    fill="none"
                                    stroke="currentColor"
                                    strokeLinecap="round"
                                    strokeLinejoin="round"
                                    strokeWidth="1"
                                    viewBox="0 0 24 24"
                                    class="w-5 h-5"
                            >
                                <path stroke="none" d="M0 0h24v24H0z"/>
                                <path d="M13 3a1 1 0 0 1 1 1v4.535l3.928 -2.267a1 1 0 0 1 1.366 .366l1 1.732a1 1 0 0 1 -.366 1.366L16.001 12l3.927 2.269a1 1 0 0 1 .366 1.366l-1 1.732a1 1 0 0 1 -1.366 .366L14 15.464V20a1 1 0 0 1 -1 1h-2a1 1 0 0 1 -1 -1v-4.536l-3.928 2.268a1 1 0 0 1 -1.366 -.366l-1-1.732a1 1 0 0 1 .366 -1.366L7.999 12 4.072 9.732a1 1 0 0 1 -.366 -1.366l1-1.732a1 1 0 0 1 1.366 -.366L10 8.535V4a1 1 0 0 1 1 -1h2z" />
                            </svg>
                        </div>
                        <div class="pl-3">
                            <p class="text-sm font-medium text-blue-600 leading-none">38</p>
                            <p class="text-xs text-gray-500">Pessoas em Enfermaria</p>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </div>
</template>

<script>
    import Raphael from 'raphael/raphael'
    global.Raphael = Raphael

    import jQuery from 'jquery'
    global.jQuery = jQuery

    import { AreaChart } from 'vue-morris'

    export default {
        name: "ConfirmedCases",
        data() {
            return {
                evolution: [
                    { data: '2020-03-20', casos: 2 },
                    { data: '2020-03-21', casos: 2 },
                    { data: '2020-03-22', casos: 6 },
                    { data: '2020-03-23', casos: 9 },
                    { data: '2020-03-24', casos: 9 },
                    { data: '2020-03-25', casos: 13 },
                    { data: '2020-03-26', casos: 15 },
                    { data: '2020-03-27', casos: 15 },
                    { data: '2020-03-28', casos: 15 },
                    { data: '2020-03-29', casos: 20 },
                    { data: '2020-03-30', casos: 20 },
                    { data: '2020-03-31', casos: 33 },
                    { data: '2020-04-01', casos: 37 },
                    { data: '2020-04-02', casos: 40 },
                    { data: '2020-04-03', casos: 44 },
                    { data: '2020-04-04', casos: 48 },
                    { data: '2020-04-05', casos: 48 },
                    { data: '2020-04-06', casos: 52 },
                    { data: '2020-04-07', casos: 53 },
                    { data: '2020-04-08', casos: 55 },
                    { data: '2020-04-09', casos: 59 },
                    { data: '2020-04-10', casos: 61 },
                    { data: '2020-04-11', casos: 61 },
                    { data: '2020-04-12', casos: 65 },
                    { data: '2020-04-13', casos: 71 },
                    { data: '2020-04-14', casos: 76 },
                    { data: '2020-04-15', casos: 79 },
                    { data: '2020-04-16', casos: 82 },
                    { data: '2020-04-17', casos: 87 },
                    { data: '2020-04-18', casos: 88 },
                    { data: '2020-04-19', casos: 91 },
                    { data: '2020-04-20', casos: 95 },
                    { data: '2020-04-21', casos: 98 },
                    { data: '2020-04-22', casos: 98 },
                    { data: '2020-04-23', casos: 100 },
                    { data: '2020-04-24', casos: 105 },
                    { data: '2020-04-25', casos: 130 },
                    { data: '2020-04-26', casos: 167 },
                    { data: '2020-04-27', casos: 168 },
                    { data: '2020-04-28', casos: 194 },
                    { data: '2020-04-29', casos: 195 },
                    { data: '2020-04-30', casos: 215 },
                    { data: '2020-05-01', casos: 223 },
                    { data: '2020-05-02', casos: 225 },
                    { data: '2020-05-03', casos: 239 },
                    { data: '2020-05-04', casos: 239 },
                    { data: '2020-05-05', casos: 257 },
                    { data: '2020-05-06', casos: 273 },
                    { data: '2020-05-07', casos: 279 },
                    { data: '2020-05-08', casos: 289 },
                    { data: '2020-05-09', casos: 339 },
                    { data: '2020-05-10', casos: 343 },
                    { data: '2020-05-11', casos: 346 },
                    { data: '2020-05-12', casos: 385 },
                    { data: '2020-05-13', casos: 438 },
                    { data: '2020-05-14', casos: 451 },
                    { data: '2020-05-15', casos: 474 },
                    { data: '2020-05-16', casos: 477 },
                    { data: '2020-05-17', casos: 512 },
                    { data: '2020-05-18', casos: 514 },
                    { data: '2020-05-19', casos: 531 },
                    { data: '2020-05-20', casos: 540 },
                    { data: '2020-05-21', casos: 550 },
                    { data: '2020-05-22', casos: 577 },
                    { data: '2020-05-23', casos: 621 },
                    { data: '2020-05-24', casos: 626 },
                    { data: '2020-05-25', casos: 644 },
                    { data: '2020-05-26', casos: 654 },
                    { data: '2020-05-27', casos: 691 },
                    { data: '2020-05-28', casos: 710 },
                    { data: '2020-05-30', casos: 770 },
                    { data: '2020-05-31', casos: 786 },
                    { data: '2020-06-01', casos: 799 },
                    { data: '2020-06-02', casos: 818 },
                    { data: '2020-06-03', casos: 829 },
                    { data: '2020-06-04', casos: 843 },
                    { data: '2020-06-05', casos: 885 },
                    { data: '2020-06-06', casos: 898 },
                    { data: '2020-06-07', casos: 920 },
                    { data: '2020-06-08', casos: 930 },
                    { data: '2020-06-09', casos: 972 },
                    { data: '2020-06-10', casos: 1025 },
                    { data: '2020-06-11', casos: 1036 },
                    { data: '2020-06-12', casos: 1074 },
                    { data: '2020-06-13', casos: 1097 },
                    { data: '2020-06-14', casos: 1110 },
                    { data: '2020-06-15', casos: 1134 },
                    { data: '2020-06-16', casos: 1181 },
                    { data: '2020-06-17', casos: 1248 },
                    { data: '2020-06-18', casos: 1287 },
                    { data: '2020-06-19', casos: 1354 },
                    { data: '2020-06-20', casos: 1402 },
                    { data: '2020-06-21', casos: 1478 },
                    { data: '2020-06-22', casos: 1530 },
                    { data: '2020-06-23', casos: 1667 },
                    { data: '2020-06-24', casos: 1723 },
                    { data: '2020-06-25', casos: 1853 },
                    { data: '2020-06-26', casos: 1956 },
                    { data: '2020-06-27', casos: 2019 },
                    { data: '2020-06-28', casos: 2114 },
                    { data: '2020-06-29', casos: 2277 },
                    { data: '2020-06-30', casos: 2458 },
                    { data: '2020-06-31', casos: 2458 },
                    { data: '2020-07-01', casos: 2576 },
                    { data: '2020-07-02', casos: 2660 },
                    { data: '2020-07-03', casos: 2757 },
                    { data: '2020-07-04', casos: 2892 },
                    { data: '2020-07-05', casos: 2956 },
                    { data: '2020-07-06', casos: 3112 },
                ]
            }
        },
        components: {
            AreaChart
        }
    }
</script>

<style scoped>

</style>
