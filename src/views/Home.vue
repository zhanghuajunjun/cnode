
<template>
 <div>
   <child-one></child-one>
   <child-two></child-two>
 </div>
</template>

<script>
 import ChildOne from '../components/ChildOne';
 import ChildTwo from '../components/ChildTwo';
 export default {
   name: '',
   props: {},
   data () {
     return {

     }
   },
   components: {
     ChildOne,
     ChildTwo
   },
   methods: {

   },
   mounted() {

   },
   watch: {

   },
   computed: {

   }
 }
</script>

<style scoped lang='scss'>

</style>