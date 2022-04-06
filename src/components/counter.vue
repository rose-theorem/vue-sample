<template>
    <div class="container">
        <div class="row">
            <div class="col-md-4">
                <div class="card">
                    <div class="card-body">
                        <div class="h3 display-3">{{this.count}}</div>
                        <button class="btn btn-success m-1" @click="this.incr">Increment</button>
                        <button class="btn btn-warning m-1" @click="this.decr">Decrement</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'CounterNumber',
  data: function () {
    return {
      count: 88
    }
  },
  methods: {
    incr: function () {
      this.count = this.count + 1
    },
    decr: function () {
      this.count = this.count - 1
    }
  }
}
</script>

<style scoped>
div.container {
    margin-bottom: 2em;
}

</style>
