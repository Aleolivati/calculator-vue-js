<script setup>
    const props = defineProps(['eventFilter'])
</script>

<template>
    <div class="row d-flex justify-content-center align-items-center">
        <div class="col-md-5 d-flex justify-content-end">
            <h3>Selecione a operação:</h3>
        </div>
        <div class="col-md-4 d-flex justify-content-start">
            <select class="w-50 text-center h4" @change="props.eventFilter">
                <option value="add">+</option>
                <option value="subtract">-</option>
                <option value="multiply">x</option>
                <option value="divide">/</option>
            </select>
        </div>
    </div>
    <hr>
</template>