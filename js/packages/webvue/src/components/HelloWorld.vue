<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p> Minting coming soon </p>
  </div>
</template>

<script>
import {WalletConnectButton} from "@solana/wallet-adapter-vue-ui";
import {WalletMultiButton} from "@solana/wallet-adapter-vue-ui";
import {WalletProvider} from "@solana/wallet-adapter-vue";
import {WalletModal} from "@oyster/common";
export default {
  name: 'HelloWorld',
  components: {
    WalletConnectButton,
    WalletMultiButton,
    WalletProvider,
    WalletModal
  },
  props: {
    msg: String
  },
  setup(props) {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
