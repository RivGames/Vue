<script>
export default {
  data() {
    return {
      // 'name': 'John',
      // 'surname': 'Smith',
      // 'text': 'page',
      // 'href': 'https://vuejs.org/guide/essentials/application.html',
      // 'num1': 5,
      // 'num2': 39,
      // 'num3': 359,
      // 'num4': 319,
      // 'arr1': ['x', 'y', 'z'],
      // 'arr2': [21, 41, 53],
      // obj: {x: 1, y: 2, z: 3},
      // 'text1': 'hello vue',
      // 'text2': 'hii',
      message:'hello',

    }
  },
  methods: {
    // 'show': function () {
    //   alert(new Date(2022, 8, 26));
    // },
    // 'showMinutes': function () {
    //   alert(new Date(2022, 8, 26).getFullYear());
    // },
    // 'sumNumbers': function () {
    //   alert(this.num1 + this.num3);
    // },
    // 'showDayOfWeek': function (number) {
    //   let date = new Date(2022, 8, number);
    //   if (date.getDay() === 1) {
    //     alert('Monday))))))');
    //   }
    // },
    // 'mainFunc': function (number) {
    //   this.showDayOfWeek(number);
    // },
    // 'getSquare': function (number) {
    //   alert(number ** 2);
    // },
    // 'change': function () {
    //   this.text1 = 'vue the best JavaScript framework in the world!';
    // },
    // 'change1': function () {
    //   this.text2 = 'bla-bla-bla';
    // }

  },
  filters:{
    'uppercase':function(str){
      return str.toUpperCase();
    },
    'lowercase':function(str){
      return str + '1';
    },

  },
}
</script>

<template>
<!--  <div :class="name">-->
<!--    {{ name }}-->
<!--  </div>-->
<!--  <div class="surname">-->
<!--    {{ surname }}-->
<!--  </div>-->
<!--  <a :href="{href}">{{ text }}</a>-->
<!--  <p><strong>{{ num1 ** 2 }}</strong></p>-->
<!--  <p><strong>{{ num2 + num3 + num4 }}</strong></p>-->
<!--  <p><strong>{{ arr1[0] }}</strong></p>-->
<!--  <p><strong>{{ arr2[0] + arr2[1] + arr2[2] }}</strong></p>-->
<!--  <h4>{{ obj['x'] + obj['y'] + obj['z'] }}</h4>-->
<!--  {{ show() }}-->
<!--  <button v-on:click="show">showDate</button>-->
<!--  <button @mouseover="showMinutes">showMinutes</button>-->
<!--  {{ sumNumbers() }}-->
<!--  {{ mainFunc(26) }}-->
<!--  <button @dblclick="getSquare(21)">btn1</button>-->
<!--  <button @mousemove="getSquare(3)">btn2</button>-->
<!--  <button @click="change()">{{ text1 }}</button>-->
<!--  <button @mousemove="change1()">{{ text2 }}</button>-->

</template>
