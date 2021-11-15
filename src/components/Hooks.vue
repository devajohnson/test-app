<template>
  <p>I am text inside the component.</p>
</template>

 

<script>

export default {

  data(){
    return
  },

  mounted() {

    console.log(this.$el.textContent) // I'm text inside the component.

  }

}

</script>