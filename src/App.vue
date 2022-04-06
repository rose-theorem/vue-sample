<template>
  <div class="container mt-3">
    <div class="grid">
      <div class="row">
        <div class="col">
          <p class="h3 text-success fw-bold">App Csfadsfomponent</p>
          <p class="fst-italic">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officia reprehenderit cumque molestiae maiores consectetur ea deserunt nam adipisci, at minima quidem commodi iste quo est eaque provident quaerat nihil qui?</p>
        </div>
      </div>
    </div>
    <counter />
 </div>

</template>

<script>
import counter from './components/counter.vue'
export default {
  components: { counter }
}
</script>

<style>
  @import "./styles.css";
</style>
