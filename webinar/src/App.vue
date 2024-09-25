<script setup>
import { reactive } from 'vue';
import header from './components/header.vue';

  const estado = reactive({
    operation: '+',
    num1: '',
    num2: ''
  })

  const resultado = ()=> {
    const {operation} = estado
    switch(operation) {
      case'-':
      return parseFloat(estado.num1) - parseFloat(estado.num2)
      case'*':
      return parseFloat(estado.num1) * parseFloat(estado.num2)
      case'/':
      return parseFloat(estado.num1) / parseFloat(estado.num2)
      case'+':
      return parseFloat(estado.num1) + parseFloat(estado.num2)
    }
  }
</script>