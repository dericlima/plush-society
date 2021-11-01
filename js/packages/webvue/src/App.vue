<template>
  <wallet-provider :wallets="wallets" auto-connect>
    <div>
      <wallet-modal-provider>
        <wallet-multi-button></wallet-multi-button>
      </wallet-modal-provider>
    </div>
    <img alt="Vue logo" src="./assets/plush1.jpg">
    <HelloWorld msg="Welcome to the Plush Society"/>
  </wallet-provider>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import {getPhantomWallet} from '@solana/wallet-adapter-wallets'
export default {
  name: 'App',
  components: {
    HelloWorld
  },
  setup() {
    const wallets = [
      getPhantomWallet(),
    ]
    return {
      wallets
    }
  }
}
</script>
