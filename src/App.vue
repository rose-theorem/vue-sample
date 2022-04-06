<template>
  <div class="container mt-3">
    <div class="grid">
      <div class="row">
        <div class="col">
          <p class="h3 text-success fw-bold">App Component</p>
          <p class="fst-italic">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officia reprehenderit cumque molestiae maiores consectetur ea deserunt nam adipisci, at minima quidem commodi iste quo est eaque provident quaerat nihil qui?</p>
        </div>
      </div>
    </div>
    <greetting/>
    <counter/>
    <register/>
    <auth-user/>
 </div>
</template>

<script>
import Greetting from './components/Greetting.vue'
import counter from './components/counter.vue'
import Register from './components/Register.vue'
import AuthUser from './components/AuthUser.vue'
export default {
  components: { Greetting, counter, Register, AuthUser }
}
</script>

<style>
  @import "./styles.css";
</style>
