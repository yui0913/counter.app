<template>
  <div class="count">
    <h1>This is an count page</h1>
    <p>{{ count }}</p>
    <p>
    <button @click = "increment">+</button>
    <button @click = "decrement">-</button>
    </p>
  </div>
</template>

<script>
export default {
    data(){
        return{

        }
    },
    methods:{
        increment(){
            this.$store.commit('increment')
        },
        decrement(){
            this.$store.commit('decrement')
        }
    },
    computed:{
        count(){
        return this.$store.getters.count
        }
    }
}
</script>