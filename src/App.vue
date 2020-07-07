<template>
    <div id="app">
        <nav class="flex items-center justify-between flex-wrap bg-teal-500 p-6">
            <div class="flex items-center flex-shrink-0 text-white mr-6">
                <span class="font-semibold text-xl tracking-tight">Blumenau Convid19 Evolução</span>
            </div>
        </nav>

        <div class="p-5 mx-auto">
            <confirmed-cases></confirmed-cases>
        </div>
    </div>

<!--  morte: 05/05 - 1  -->
<!--  morte: 07/05 - 2  -->
<!--  morte: 10/05 - 3  -->
<!--  morte: 28/05 - 4  -->
<!--  morte: 11/06 - 5  -->
</template>

<script>
    import ConfirmedCases from "./components/ConfirmedCases";

    export default {
        name: 'App',
        components: {
            ConfirmedCases
        }
    }
</script>
