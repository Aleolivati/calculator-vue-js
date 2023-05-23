<script setup>
    const props = defineProps(['getSignal', 'eventNumberA', 'eventNumberB']) ;

</script>

<template>
    <div class="row d-flex justify-content-center align-items-center mt-4 mb-4">
        <div class="col-md-2 d-flex justify-content-end">
            <input class="input__number" type="number" required @keyup="props.eventNumberA" />
        </div>
        <div class="col-md-1 d-flex justify-content-center display-2">
            <span> {{ props.getSignal }}</span>
        </div>
        <div class="col-md-2 d-flex justify-content-start">
            <input class="input__number" type="number" required @keyup="props.eventNumberB" />
        </div>
    </div>
</template>

<style scoped>
.input__number {
    width: 100px;
    height: 100px;
    font-size: 40px;
    text-align: center;
}
</style>