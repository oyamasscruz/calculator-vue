<script setup>
  import { reactive } from 'vue';
  import ContentHeader from './components/ContentHeader.vue';
  import ContentForm from './components/ContentForm.vue';
  import ContentSelect from './components/ContentSelect.vue';


  const recordingNumber = reactive({
    operation: 'sum',
    number1: '',
    number2: '',
  }
)

function recordingOperation() {

  if(recordingNumber.number1 === '') {
    return '';
  }else {
  const {operation} = recordingNumber;
  switch(operation) {
    case 'sum':
      return sum();
    case 'subtraction':
      return sub();
    case 'divide':
      return divi();
    case 'multiply':
      return multi();
  }
}
}

function multi() {
  return recordingNumber.number1 * recordingNumber.number2;
}

function divi() {
  return recordingNumber.number1 / recordingNumber.number2;
}

function sum() {
  return parseFloat(recordingNumber.number1) + parseFloat(recordingNumber.number2);
}

function sub() {
  return recordingNumber.number1 - recordingNumber.number2;
}
</script>

<template>
  <div class="container bg-dark rounded-3">
    <ContentHeader :recording-operation="recordingOperation()"/>
    <ContentForm :recording1="evento => recordingNumber.number1 = evento.target.value" :recording2="evento => recordingNumber.number2 = evento.target.value"/>
    <ContentSelect :operation="evento => recordingNumber.operation = evento.target.value"/>
  </div>
</template>

<style scoped>
.container {
  color: #fff;
}
</style>
