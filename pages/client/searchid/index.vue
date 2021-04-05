<template>
    <div class="container">
        <div class="row">
            <div class="col-md-12">
                <form action="" class="search-id">
                    <label for="">ID</label>
                    <v-text-field class="search-input"
                        label="コードを入力してください"
                        :rules="rules"
                        hide-details="auto"
                    ></v-text-field>
                    <v-btn
                        class="ma-2"
                        :loading="loading4"
                        :disabled="loading4"
                        color="info"
                        @click="loader = 'loading4'"
                    >
                        小切手
                        <template v-slot:loader>
                        <span class="custom-loader">
                        <v-icon light>mdi-cached</v-icon>
                        </span>
                        </template>
                    </v-btn>
                </form>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data: function() {
        return {
            title: '123'
        }
    }
}
</script>

<style scoped>
    @import "~/assets/checkid.scss";
    .search-id {
        padding: 20px;
        width: 80%;
        margin: 0 auto;
        border: 5px solid black;
        min-height: 300px;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .search-input {
        border: 1px solid #CCC;
        margin: 0 20px;
        padding: 16px;
        width: 60%;
    }
</style>
