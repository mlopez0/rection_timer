<template>

  <p> Reaction Time -> {{ score}} </p>
  <p> This is the ranking of your click: {{rank}} </p>

  

</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if(this.score < 300){
            this.rank = 'Fast fingers'
        } else if (this.score < 500) {
            this.rank = 'Rapid reflexes'
        } else {
            this.rank = 'Snail pace'
        }
    }


}
</script>

<style>

</style>