<template>
  <div id="login">
    <el-card>
      <div>
        <h5>ManuScripterにようこそ</h5>
        <button v-on:click="login()">Googleアカウントでログイン</button>
      </div>
    </el-card>
  </div>
</template>

<script>
const firebase = require('firebase')
const provider = new firebase.auth.GoogleAuthProvider()

const config = require('./_firebase_config.js')
console.log(config)

firebase.initializeApp(config)

export default {
  name: 'Login',
  methods: {
    login: function () {
      firebase.auth().signInWithPopup(provider).then(
        _result => {
          this.$router.push('index')
        })
    }
  }
}

</script>
