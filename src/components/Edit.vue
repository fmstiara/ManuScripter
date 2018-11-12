<template>
    <div id = "index" v-on="setUserData()">
      <el-container>
        <el-aside>
          <SideMenu />
        </el-aside>
        <el-main>
          edit
        </el-main>
      </el-container>
    </div>
</template>

<script>
import SideMenu from './SideMenu.vue'

const firebase = require('firebase')
let binding = {
  name: 'Index',
  components: {
    SideMenu
  },
  data: function () {
    return {
      user: {
        id: 'user-id',
        name: 'hoge',
        imageSrc: 'url'
      },
      manuscripts: []
    }
  },
  methods: {
    setUserData: (_id, _name, _iamgeSrc) => {
      firebase.auth().onAuthStateChanged((user) => {
        console.log(user)
        this.id = user.uid
        this.name = user.displayName
        this.imageSrc = user.photoURL
      })
    }
  }
}
export default binding
</script>

<style>
</style>
