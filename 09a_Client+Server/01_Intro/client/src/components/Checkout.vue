<template>
  <div>
    <h2>Checkout</h2>
    Your total is CHF {{ cartTotal.toFixed(2) }}.
    <b-button style="background-color: #333333" variant="primary" v-show="cartTotal > 0" @click="checkout">Checkout</b-button>
  </div>
</template>

<script>
import {mapGetters} from 'vuex';

export default {
  name: 'Cart',
  computed: mapGetters(['cartTotal']),
  methods: {
    checkout() {
      alert('Ihre Bestellung wurde getätigt. Danke für den Einkauf.');
    }
  }
}
</script>

