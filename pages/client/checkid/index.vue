<template>
  <div class="container">
    <div class="wrapContent">
      <h2 class="titleCheckId">糖尿病進展予防プログラム</h2>
      <!--      <form method="POST" action="{{ route('post.checkid') }}">-->
      <div class="wrapInputCheckId">
        <label class="control-label col-3 col-sm-2 col-md-2 col-lg-2 laybel">ID入力:</label>
        <div class=" col-8 col-sm-6 col-md-5 col-lg-5">
          <v-text-field class="inPutCheckId"
            label="コードを入力してください"
            :rules="rules"
            hide-details="auto"
          ></v-text-field>
        </div>
      </div>
      <h5>
        ID：圧着はがきにてお送りさせて頂いた、各種アプリ登録用ID

      </h5>
      <v-btn
        class="ma-2"
        :loading="loading4"
        :disabled="loading4"
        color="info"
        @click="loader = 'loading4'"
      >
        次へ
        <template v-slot:loader>
        <span class="custom-loader">
          <v-icon light>mdi-cached</v-icon>
        </span>
        </template>
      </v-btn>
      <!--      </form>-->
    </div>
  </div>
</template>
<script>
export default {
  data: () => ({
    rules: [
      value => !!value || 'IDを入力してください',
      v => (v && v.length <= 10) || '長すぎる',
    ],
  }),
}
</script>
<style lang="scss">
@import "~/assets/checkid.scss";
</style>
