<template>
  <div class="section">
    <div class="container">
      <h1 class="title">
        E10 Practical Component Exercise #2: Modal
      </h1>
      <button
        class="button"
        @click="isVisible = true"
      >
        Show Modal
      </button>
      <modal
        :is-visible="isVisible"
        @closeModal="isVisible = false"
      >
        <h1 class="title">
          Nice title
        </h1>
        <p>Here is the body from the parent</p>
      </modal>
    </div>
  </div>
</template>

<script>
import Modal from "./widgets/Modal";

export default {
	components: {
		Modal
	},
	data(){
		return {
			isVisible: false
		}
	}
}
</script>
