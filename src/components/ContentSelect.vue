<script setup>
const props = defineProps(['operation'])
</script>
<template>
    <div class="row">
        <div class="col-4">
            <select @change="props.operation" name="Operations" class="form-control p-2 ms-4 bg-dark mt-4 mb-4">
                <option value="sum">Sum</option>
                <option value="subtraction">Subtraction</option>
                <option value="divide">Divide</option>
                <option value="multiply">Multiply</option>
            </select>
        </div>
    </div>
</template>
<style scoped>
select {
    color: #fff;
    font-weight: bold;
}

option {
    color: #fff;
}
</style>