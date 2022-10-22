<template>
    <div class="mensagem-container" v-if="show">
        <p>{{ msg }}</p>
    </div>
</template>

<script>
    export default{
        name: 'Message',
        props:{
            msg: String
        },
        watch:{
            msg:function(){
                this.show = true
                setTimeout(()=> this.show = false, 3000)
            }
        },
        data(){
            return{
                show: false
            }
        }
    }
</script>

<style scoped>

    .mensagem-container{
        color: #004085;
        background-color: #CCE5FF;
        border: 2px solid #B8DAFF;
        border-radius: 5px;
        padding: 10px;
        max-width: 400px;
        margin: 30px auto;
    }
    
</style>