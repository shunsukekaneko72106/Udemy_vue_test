<template>
  <div>
    <p>{{ messege }}</p>
    <!-- 二重括弧内はjavascriptの動き -->
    <p>{{ number + 3 }}</p>

    <!-- javascriptの関数が実行できる -->
    <p>{{ sayHi() }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      messege: "こんにちわ！",
      number: 3,
    };
  },
  methods: {
    sayHi: function () {
      return "hi!";
    },
  },
};
</script>
