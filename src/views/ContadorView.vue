<template>
<!--En el view tambien debe tener un div para los compoenntes que los contengan-->
<div>
    <Contador/>
</div>
</template>

<script>
import Contador from '@/components/Contador.vue'
export default {
    components: {
        Contador
    },
}
</script>

<style>

</style>