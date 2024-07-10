<template>
  <h2>6. Custom Directives - Create own behavior v-mybehavior</h2>
  <h3 v-format-div="2">Using own Custom Directive vFormatDiv on this header</h3>
  <h3 v-format-div:red>Using Custom Directive Argument</h3>
  <h3 v-format-size>Custom Directive Shorthand on Script</h3>
</template>

<script setup>

const vFormatDiv = {
  mounted:  (myElement, binding) => {
    console.log(myElement)
    myElement.style.fontStyle = 'italic'
    myElement.style.color = 'green'

    //Using Binding
    myElement.style.fontSize = `${binding.value}rem`
    myElement.style.border = `${binding.value}px solid gray`

    //Using arguments
    switch (binding.arg){
      case 'red':
        myElement.style.color = 'red'
        break
      case 'blue':
        myElement.style.color = 'blue'
        break
      default:
        myElement.style.color = "green"
    }
  }
}

//Shorthand
const vFormatSize = (myElement) => (myElement.style.fontSize = '1.5rem')
</script>

<style scoped>
</style>