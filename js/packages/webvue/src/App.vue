<template>
    <button>Connect</button>
    <img alt="Plush Society logo" src="./assets/plush1.jpg">
    <HelloWorld msg="Welcome to the Plush Society" />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import {getPhantomWallet} from '@solana/wallet-adapter-wallets'
import {initWallet} from '@solana/wallet-adapter-vue'
export default {
  name: 'App',
  components: {
    HelloWorld
  },
  setup() {
    const wallets = [
      getPhantomWallet(),
    ]

    initWallet({
      wallets: [wallets], autoConnect: true
    })
    return {
      wallets
    }
  }
}
</script>
