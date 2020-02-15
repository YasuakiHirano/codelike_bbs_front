<template>
  <v-layout>
    <v-row justify="center">
      <v-col cols="10">
        <v-form ref="form" lazy-validation>
          <v-text-field v-model="title" label="タイトル" required></v-text-field>
          <v-text-field v-model="name" label="名前" required></v-text-field>
          <v-textarea v-model="description" label="説明文" required></v-textarea>
          <v-text-field v-model="password" type="password" label="パスワード" required></v-text-field>
          <v-row justify="center">
            <v-col cols="4">
              <v-btn color="secondary" block @click="reset">
                <span class="white--text">クリア</span>
              </v-btn>
            </v-col>
            <v-col cols="4">
              <v-btn color="primary" block @click="reset">
                <span class="white--text">登録</span>
              </v-btn>
            </v-col>
          </v-row>
        </v-form>
      </v-col>
    </v-row>
  </v-layout>
</template>

<script>
export default {
  data () {
    return {
      title: '',
      description: '',
      password: '',
      name: ''
    }
  },
  methods: {
    reset () {
      this.$refs.form.reset()
    },
  },
}
</script>
