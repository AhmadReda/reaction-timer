<template>
  <p>This score is {{reactionTime}} ms</p>
  <p class="rank">{{rank}}</p>
</template>

<script>
export default {
    props:['reactionTime'],
    data(){
        return{
            rank:null
        }
    },
    mounted(){
        if(this.reactionTime < 250){
            this.rank = 'Ninja Fingers'
        }else if(this.reactionTime < 400){
            this.rank = 'Rapid Reflexes'
        }else{
            this.rank = 'Snail Pace...'
        }
    }
}
</script>

<style>
.rank {
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
}
</style>