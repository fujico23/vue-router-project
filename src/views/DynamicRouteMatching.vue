<template>
  <div>{{ userId }}</div>
</template>

<script>
export default {
  data() {
    return {
      userId: this.$route.query.userId,
      //this.$route.queryは現在のルートに含まれているクエリパラメータ全体を保持しているオブジェクト
      //userIdというキーに対応する値を取得している
    };
  },
};
</script>
