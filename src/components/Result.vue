<script setup>
    const props = defineProps(['result'])
</script>

<template>
    <div class="row d-flex justify-content-center">
        <div class="col-md-5 d-flex justify-content-center">
            <span class="display-3 border border-white border-5 p-4 mb-4">{{ props.result }}</span>
        </div>
    </div>
</template>