<template>
    <div class="container" >
        <div class="row">
            <div class="col-md-6">
                <div class="card shadow-lg">
                    <div class="card-body">
                        <div class="h3">Hello<span class="fw-bold">{{this.msg}}</span></div>
                        <button class="btn btn-success m-1" @click=" greet(', good morning')">Good Morning</button>
                        <button class="btn btn-warning m-1" @click="greet(', good afternoon')">Good Afternoon</button>
                        <button class="btn btn-danger m-1" @click="greet(', good evening')">Good Evening</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'NewGreeting',
  data: function () {
    return {
      msg: ''
    }
  },
  methods: {
    greet: function (value) {
      this.msg = value
    }
  }
}
</script>

<style scoped>
div.container {
    margin-bottom: 2em;
}
</style>
