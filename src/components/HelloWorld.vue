<template>
  <div>
    <p>{{ messege }}</p>
    <!-- 二重括弧内はjavascriptの動き -->
    <p>{{ number + 3 }}</p>

    <!-- javascriptの関数が実行できる（単一の式のみ） -->
    <p>{{ sayHi() }}</p>

    <!-- vから始まる属性を"ディレクティブ"と呼ぶ -->
    <p v-text="messege"></p>

    <!-- 属性の値をデータに対応付ける -->
    <a v-bind:href="url">ここからアクセス</a>
    <!-- 省略もできる -->
    <a :href="url">ここからアクセス</a>
  </div>
</template>

<script>
export default {
  data() {
    return {
      messege: "こんにちわ！",
      number: 3,
      url: "https://www.yahoo.co.jp/",
    };
  },
  methods: {
    sayHi: function () {
      //インスタンス内のプロパティにアクセスする場合にthisを使う
      this.messege = "Hey に変更";
    },
  },
};
</script>
