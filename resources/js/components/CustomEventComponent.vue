<template>
  <div class="section">
    <div class="container">
      <h1 class="title">
        E12 Component Communication Example #1: Custom Events
      </h1>
      <coupon
        @coupon-applied="onCouponApplied"
      />
      <div
        v-if="couponApplied"
      >
        <p>You applied <strong>{{ coupon }}</strong> coupon!</p>
      </div>
    </div>
  </div>
</template>

<script>
import coupon from "./widgets/Coupon";

export default {
	components: {
		coupon
	},
	data(){
		return {
			couponApplied: false,
			coupon: ''
		}
	},
	methods:{
		onCouponApplied(name){
			this.couponApplied = name.length > 0
			this.coupon = name
		}
	}
}
</script>
