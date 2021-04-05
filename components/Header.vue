<template>
   <div class="container topmenu">
    <div class="wrapHeader">
        <div class="headerLeft">
          <nuxt-link to="/">
               <img src="@/static/common/images/kowa_logo.svg" alt="kowa">
          </nuxt-link>
        </div>
        <div class="headerRight">
            <div class="navBar">
              <nuxt-link class="headerLink" to="/client/checkid">
                キャンペーンの資料請求に進む
              </nuxt-link>
              <nuxt-link class="headerLink" to="/client/searchid">
                   IDを検索
              </nuxt-link>
            </div>
        </div>
    </div>
</div>
</template>
<script>
export default {
    
}
</script>
<style lang="scss">
  @import "~/assets/header.scss";
</style>