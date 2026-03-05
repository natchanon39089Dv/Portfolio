<script setup>
import { ref } from 'vue'

const name = ref("")
const email = ref("")
const message = ref("")
const sent = ref(false)

function submitForm(){
  // For class project: simple frontend submit
  sent.value = true
  name.value = ""
  email.value = ""
  message.value = ""
  setTimeout(() => (sent.value = false), 2500)
}
</script>

<template>
  <section class="container container-narrow py-5" id="contact">
    <div class="card-clean p-4 p-md-5">
      <div class="d-flex justify-content-between flex-wrap gap-3 align-items-start">
        <div>
          <h2 class="section-title mb-1">Customer Support (Contact)</h2>
          <p class="small-muted mb-0">Send a message like requesting a product demo.</p>
        </div>
        <div class="d-flex gap-2">
          <a class="btn btn-outline-dark btn-clean" href="#" title="GitHub">
            <i class="bi bi-github"></i>
          </a>
          <a class="btn btn-outline-dark btn-clean" href="#" title="Facebook">
            <i class="bi bi-facebook"></i>
          </a>
          <a class="btn btn-outline-dark btn-clean" href="#" title="Email">
            <i class="bi bi-envelope"></i>
          </a>
        </div>
      </div>

      <hr />

      <form class="row g-3" @submit.prevent="submitForm">
        <div class="col-md-6">
          <label class="form-label">Name</label>
          <input class="form-control" v-model="name" required placeholder="Your name" />
        </div>
        <div class="col-md-6">
          <label class="form-label">Email</label>
          <input class="form-control" v-model="email" required type="email" placeholder="you@email.com" />
        </div>
        <div class="col-12">
          <label class="form-label">Message</label>
          <textarea class="form-control" v-model="message" required rows="4" placeholder="Write something..."></textarea>
        </div>
        <div class="col-12 d-flex gap-2 align-items-center">
          <button class="btn btn-dark btn-clean px-4" type="submit">
            Send <i class="bi bi-send ms-1"></i>
          </button>
          <span v-if="sent" class="text-success">
            <i class="bi bi-check-circle me-1"></i> Sent!
          </span>
        </div>
      </form>
    </div>
  </section>
</template>