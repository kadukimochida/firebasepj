<template>
  <div class="register">
    <label>メールアドレス：<input v-model="email" type="email" required /></label>
    <br />
    <label>パスワード：<input v-model="password" type="password" required /></label>
    <br/>
    <NuxtLink to="/">戻る</NuxtLink>
  </div>
</template>

<script>
import firebase from '~/plugins/firebase'
export default {
  data(){
    return {
      email:null,
      password:null,
    }
  },
  methods: {
    register(){
      if (!this.email || !this.password) {
        alert('メールアドレスまたはパスワードが入力されていません')
        return
      }
    },
  },
}
</script>