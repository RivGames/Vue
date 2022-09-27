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

      'message': 'hello',
      'name': 'John',
      'surname': 'Red',
      'amount': 50,
      'price': 2,
      'isVisible': true,
      'isVisible1': true,
      'text1': 'default',
      'isAdmin': true,
      'day': 2,
      'age': 17,
      'items': [1, -2, 3, -4, 5],
      'arr': ['x', 'y', 'z'],
      'users_salaries': {
        user1: '100$',
        user2: '200$',
        user3: '300$',
      },
      'products': [
        {
          name: 'product1',
          price: 100,
          quantity: 5
        },
        {
          name: 'product2',
          price: 200,
          quantity: 4
        },
        {
          name: 'product3',
          price: 300,
          quantity: 3
        },
      ],
      products1: [
        {
          id: 1,
          name: 'product1',
        },
        {
          id: 2,
          name: 'product2',
        },
        {
          id: 3,
          name: 'product3',
        },
      ],

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

    'test': function () {
      alert(1);
    },
    'show': function () {
      return this.isVisible = true;
    },
    'hide': function () {
      this.isVisible = false;
    },
    'show_hide': function () {
      this.isVisible = !this.isVisible;
    },
    'toggle1': function () {
      this.text1 = 'text';
      this.isVisible = !this.isVisible;
    },

  },
  filters: {
    'uppercase': function (str) {
      return str.toUpperCase();
    },
    'lowercase': function (str) {
      return str + '1';
    },
  },
  computed: {
    full: function () {
      return this.name + ' ' + this.surname + '!';
    },
    cost: function () {
      return this.amount * this.price;
    }
  }
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

  <!--  <p>{{ 321.132001320120 | toFix}}</p>-->
  <!--  <p>{{full}}</p>-->
  <!--  <p>{{cost}}</p>-->
  <!--  <button @click="cost">{{amount = 2}}</button>-->
  <!--  <a @click.prevent="" href="https://google.com">google</a>-->
  <!--  <button @click.once="test">test</button>-->

  <!--  <button @click="show">show</button>-->
  <!--  <button @click="hide">hide</button>-->
  <!--  <button @click="show_hide">show/hide</button>-->
  <!--  <p v-if="isVisible">text</p>-->
  <!--  <button @click="toggle1">{{isVisible ? 'text':'default'}}</button>-->
  <!--    <p v-if="isAdmin">+++</p>-->
  <!--    <p v-else>-&#45;&#45;</p>-->
  <!--    <p v-if="day === 1">Monday</p>-->
  <!--    <p v-if="day === 2">Tuesday</p>-->
  <!--    <p v-if="day === 3">Wednesday</p>-->
  <!--    <p v-if="day === 4">Thursday</p>-->
  <!--    <p v-if="day === 5">Friday</p>-->
  <!--    <p v-if="day === 6">Saturday</p>-->
  <!--    <p v-if="day === 7">Sunday</p>-->
  <!--    <p v-if="age < 18">a Little programming genius :)</p>-->
  <!--    <p v-else-if="age >= 18 && age < 25">However not bad1</p>-->
  <!--    <p v-else>Too</p>-->
  <!--  <p v-show="isVisible1">test</p>-->
  <!--  <template v-if="isVisible">-->
  <!--    <button @click="hide">hide</button>-->
  <!--    <p>1</p>-->
  <!--    <p>2</p>-->
  <!--    <p>3</p>-->
  <!--  </template>-->
  <ul>
    <li v-for="elem in items">{{ elem }}</li>
  </ul>
  <!--  <div v-for="elem in items">{{elem}}</div>-->
  <ul>
    <li v-for="(key,elem) in arr">{{ elem }}</li>
  </ul>
  <ul>
    <li v-for="(key,elem,index) in users_salaries">{{ elem }} {{ key }} {{ index + 1 }}</li>
  </ul>
  <template v-for="(elem) in items">
    <div>
      <p>{{ elem }}</p>
      <hr>
      <p class="divider"></p>
    </div>
  </template>
  <table v-for="product in products">
    <tr>
      <td>Name of product:{{ product.name }}</td>
      <td>Price:{{ product.price }}</td>
      <td>Qty:{{ product.quantity }}</td>
    </tr>
  </table>
  <p v-for="num in 30">{{ num }}</p>
  <ul>
    <template v-for="item in items">
      <li v-if="item > 0">{{ item }}</li>
    </template>
  </ul>
  <ul>
    <li v-for="product in products1" >{{product.name}}</li>
  </ul>
</template>
