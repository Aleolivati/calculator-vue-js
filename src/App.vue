<script setup>
  import {reactive} from 'vue' ;

  import Header from './components/Header.vue' ;
  import InputNumber from './components/InputNumber.vue' ;
  import SelectOperation from './components/SelectOperation.vue' ;
  import Result from './components/Result.vue' ;

  const status = reactive ({
    signal: '',
    filter: 'add',
    numberA: 0,
    numberB: 0,
  })


  const getSignal = () => {
    const {filter} = status ;

    switch(filter) {
      case 'add':
        return '+' ;
      case 'subtract':
        return '-' ;
      case 'multiply':
        return 'x' ;
      case 'divide':
        return '/' ;
      default:
        return ' ' ;
    }
  }

  const result = () => {
    const {filter} = status ;

    switch(filter) {
      case 'add':
        return parseInt(status.numberA) + parseInt(status.numberB) ;
      case 'subtract':
        return status.numberA - status.numberB ;
      case 'multiply':
        return status.numberA * status.numberB ;
      case 'divide':
        return status.numberA / status.numberB ;
      default:
        return ' ' ;
    }
  }
</script>

<template>
  <div class="container bg-secondary mt-5 rounded-5 w-50">
    <Header />
    <InputNumber :event-number-a="event => status.numberA = event.target.value" :event-number-b="event => status.numberB = event.target.value" :get-signal="getSignal()"/>
    <SelectOperation :event-filter="event => status.filter = event.target.value"/>
    <Result :result="result()"/>
  </div>
</template>