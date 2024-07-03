<template>
  <h2>6. Event Handling v-on:</h2>
  <div class="container">
    <button v-on:click="count++">Increment v-on:click</button>
    <button @:click="decrementCount">Decrement Method @click</button>
    <h3> Count: {{ count }}</h3>
  </div>
  <form @:submit="submitHandler">
    <input type="text" placeholder="Name">
    <input type="text" placeholder="Email">
    <button type="submit">Submit</button>
  </form>
  <button class="butParam" @:click="showMessage('Param from button template')">Pass Parameter</button>
</template>

<script>
export default{
  name: 'EventsComp',
  data() {
    return{ count: 0}
  },

  //METHODS
  methods: {
    decrementCount() {
      this.count--
    },
    submitHandler(e) {
      e.preventDefault()  // Prevents the default form submission behavior ex. reload page, send to server, etc.
      alert('Form Test Handler')
    },
    showMessage(message){
      alert(message)
    }
  }

}
</script>

<style scoped>
.container, form, .butParam {
  margin-left: 20px;
  display: flex;
  align-items: center;          /* Align items vertically in the center */
  justify-content: flex-start;  /* Start from the left */
}
.container button, form input, form button, .butParam  {
  width: 200px;
  box-sizing: border-box;      /* Include padding and border in the element's total width */
}
</style>