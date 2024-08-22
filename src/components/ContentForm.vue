<script setup>
const props = defineProps(['recording1', 'recording2'])
</script>
<template>
    <div class="row">
        <div class="col-10">
            <form class="form-control p-3 ms-4 bg-dark">
                <label>Número 1</label>
                <input class="ms-3" @keyup="props.recording1" type="number" name="" id="input1">
                <label class="ms-3">Número 2</label>
                <input class="ms-3" @keyup="props.recording2" type="number" name="" id="">
            </form>
        </div>
    </div>
</template>
<style scoped>
form {
    color: #fff;
    font-weight: bold;
}
</style>