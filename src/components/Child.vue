<template>
    <div>
       Child component
    </div>
</template>

<script>
    export default {
        name: 'childA',
        beforeCreate(){
            console.log('Child beforeCreate()');
        },
        created(){
            console.log('Child created()');
        },
        beforeMount(){
            console.log('child beforeMount()');
        },
        mounted(){
           console.log('Child mounted()');
        },
        beforeUpdate(){
            console.log('child beforeUpdate()');
        },
        updated(){
            console.log('child updated()');
        },
        beforeUnmount(){
            console.log('child beforeUnmount()');
        },
        unmounted(){
            console.log('child unmounted()');
        }
    }
</script>

<style scoped>

</style>