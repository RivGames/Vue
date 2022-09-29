<script>
import User from './components/User.vue';
export default {
  components:{
    Test
  },
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

      // 'name': 'John',
      // 'surname': 'Red',
      // 'amount': 50,
      // 'price': 2,
      // 'isVisible': true,
      // 'isVisible1': true,
      // 'text1': 'default',
      // 'isAdmin': true,
      // 'day': 2,
      // 'age': 17,
      // 'items': [1, -2, 3, -4, 5],
      // 'arr': ['x', 'y', 'z'],
      // 'users_salaries': {
      //   user1: '100$',
      //   user2: '200$',
      //   user3: '300$',
      // },
      // 'products': [
      //   {
      //     name: 'product1',
      //     price: 100,
      //     quantity: 5
      //   },
      //   {
      //     name: 'product2',
      //     price: 200,
      //     quantity: 4
      //   },
      //   {
      //     name: 'product3',
      //     price: 300,
      //     quantity: 3
      //   },
      // ],
      // products1: [
      //   {
      //     id: 1,
      //     name: 'product1',
      //   },
      //   {
      //     id: 2,
      //     name: 'product2',
      //   },
      //   {
      //     id: 3,
      //     name: 'product3',
      //   },
      // ],
      // 'testArr': [1, 2, 3, 4, 5],
      // 'someClass': 'someClass',
      // 'taskClasses': {
      //   done: true,
      //   selected: false,
      //   default: true,
      // },
      // 'taskClasses1': {
      //   hidden: false,
      // },
      // 'isActive': true,
      // 'message': 'hello',
      // 'number':0,
      'res': 0,
      'number1': 0,
      'number2': 0,
      'FIO': '',
      'name': '',
      'patronymic': '',
      'surname': '',
      'textarea': '',
      'arr': [],
      'checked': false,
      'languages': [],
      'choice': '',
      'selected': '',
      'makeYears': function () {
        let result = [];
        for (let i = 1950; i < (new Date).getFullYear(); i++) {
          result.push(i);
        }
        return result;
      },
      'months': ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
      'days': [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31],
      'years': [this.makeYears()],
      'isDisable':true,

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

    // 'test': function () {
    //   alert(1);
    // },
    // 'show': function () {
    //   return this.isVisible = true;
    // },
    // 'hide': function () {
    //   this.isVisible = false;
    // },
    // 'show_hide': function () {
    //   this.isVisible = !this.isVisible;
    // },
    // 'toggle1': function () {
    //   this.text1 = 'text';
    //   this.isVisible = !this.isVisible;
    // },
    // 'add': function () {
    //   this.testArr.push(this.testArr[this.testArr.length - 1] + 1);
    // },
    // 'removeFirst': function () {
    //   this.testArr[0] = '';
    // },
    // 'removeLast': function () {
    //   this.testArr.pop();
    // },
    // 'removePreLast': function () {
    //   this.testArr[this.testArr.length - 2] = '';
    // },
    // 'reverseArr': function () {
    //   this.testArr.reverse();
    // },
    // 'setShow': function () {
    //   this.taskClasses1.hidden = true;
    // },
    // 'setHide': function () {
    //   this.taskClasses1.hidden = false;
    // },
    // 'setToggle': function () {
    //   this.taskClasses1.hidden = !this.taskClasses1.hidden;
    // }
    'toSquare': function () {
      this.res = this.number1 ** 2;
    },
    'sum': function () {
      this.res = this.number1 + this.number2;
    },
    'sqrt': function () {
      this.res = Math.sqrt(this.number1);
    },
    'doSomeMagick': function () {
    },
    'parseFIO': function () {
      let arr = this.FIO.split(' ');
      this.name = arr[0];
      this.patronymic = arr[1];
      this.surname = arr[2];
    },
    'magick': function () {
      this.arr = this.textarea.split(' ');
    }
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
    },

  }
}
</script>

<template>
  <!--    <div :class="name">-->
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
  <!--  <ul>-->
  <!--    <li v-for="elem in items">{{ elem }}</li>-->
  <!--  </ul>-->
  <!--  &lt;!&ndash;  <div v-for="elem in items">{{elem}}</div>&ndash;&gt;-->
  <!--  <ul>-->
  <!--    <li v-for="(key,elem) in arr">{{ elem }}</li>-->
  <!--  </ul>-->
  <!--  <ul>-->
  <!--    <li v-for="(key,elem,index) in users_salaries">{{ elem }} {{ key }} {{ index + 1 }}</li>-->
  <!--  </ul>-->
  <!--  <template v-for="(elem) in items">-->
  <!--    <div>-->
  <!--      <p>{{ elem }}</p>-->
  <!--      <hr>-->
  <!--      <p class="divider"></p>-->
  <!--    </div>-->
  <!--  </template>-->
  <!--  <table v-for="product in products">-->
  <!--    <tr>-->
  <!--      <td>Name of product:{{ product.name }}</td>-->
  <!--      <td>Price:{{ product.price }}</td>-->
  <!--      <td>Qty:{{ product.quantity }}</td>-->
  <!--    </tr>-->
  <!--  </table>-->
  <!--  <p v-for="num in 30">{{ num }}</p>-->
  <!--  <ul>-->
  <!--    <template v-for="item in items">-->
  <!--      <li v-if="item > 0">{{ item }}</li>-->
  <!--    </template>-->
  <!--  </ul>-->
  <!--  <ul>-->
  <!--    <li v-for="product in products1" >{{product.name}}</li>-->
  <!--  </ul>-->
  <!--  <ul>-->
  <!--    <li v-for="elem in testArr">-->
  <!--      {{elem}}-->
  <!--    </li>-->
  <!--  </ul>-->
  <!--  <button @click="add">add</button>-->
  <!--  <button @click="removeLast">removeLast</button>-->
  <!--  <button @click="removeFirst">removeFirst</button>-->
  <!--  <button @click="removePreLast">removePreLast</button>-->
  <!--  <button @click="reverseArr">reverseArr</button>-->
  <!--  <p :class="someClass">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aspernatur at, corporis enim libero pariatur reiciendis. Eius eos maiores minima molestias voluptatum. Atque cupiditate earum praesentium sapiente. Assumenda consectetur et ex.</p>-->
  <!--  <p :class="taskClasses">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aspernatur at, corporis enim libero pariatur reiciendis. Eius eos maiores minima molestias voluptatum. Atque cupiditate earum praesentium sapiente. Assumenda consectetur et ex.</p>-->
  <!--  <p :class="taskClasses1">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aspernatur at, corporis enim libero pariatur reiciendis. Eius eos maiores minima molestias voluptatum. Atque cupiditate earum praesentium sapiente. Assumenda consectetur et ex.</p>-->
  <!--  <button @click="setShow">Show(display)</button>-->
  <!--  <button @click="setHide">Hide(display)</button>-->
  <!--  <button @click="setToggle">Show/Hide</button>-->
  <!--  <p :class="{active: isActive, valid: false}">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Commodi cum deserunt earum, eius enim exercitationem fugiat, fugit iure laudantium libero minus nemo, optio quas reiciendis totam. Atque nisi quasi recusandae.</p>-->
  <!--  <p :style="{'backgroundColor':'blue','color':'yellow','fontSize':'30px'}">I`m a Ukrainian programmer,who will change the world!</p>-->
  <!--  <input v-model="message">-->
  <!--  <p>{{message}}</p>-->
  <!--  <input v-model="number" type="number">-->
  <!--  <p>{{number ** 2}}</p>-->
  <!--  <p>{{ res }}</p>-->
  <!--  <input v-model="number1" type="number">-->
  <!--  <button v-on:click="toSquare">Magick</button>-->
  <!--  <p>{{ res }}</p>-->
  <!--  <input v-model="number1" type="number">-->
  <!--  &lt;!&ndash;  <input v-model="number2" type="number">&ndash;&gt;-->
  <!--  &lt;!&ndash;  <button v-on:click="sum">sum</button>&ndash;&gt;-->
  <!--  <button v-on:click="sqrt">get Square From</button>-->
  <!--  <input v-model="FIO" type="text">-->
  <!--  <button v-on:click="parseFIO">parse your FIO</button>-->
  <!--  <p>{{ name }}</p>-->
  <!--  <p>{{ patronymic }}</p>-->
  <!--  <p>{{ surname }}</p>-->
  <!--  <textarea v-model="textarea"></textarea>-->
  <!--  <button v-on:click="magick">magick</button>-->
  <!--  <ul>-->
  <!--    <li v-for="elem in arr">{{ elem }}</li>-->
  <!--  </ul>-->
  <!--  <input type="checkbox" v-model="checked">-->
  <!--  <p v-if="checked">yes</p>-->
  <!--  <p v-else>nope</p>-->
  <!--  <p>Which languages do you know?</p>-->
  <!--  <p>English</p><input type="checkbox" v-model="languages" value="english">-->
  <!--  <p>Spanish</p><input type="checkbox" v-model="languages" value="spanish">-->
  <!--  <p>Ukrainian</p><input type="checkbox" v-model="languages" value="ukrainian">-->
  <!--  <ul>-->
  <!--    <li v-for="lang in languages">{{ lang }}</li>-->
  <!--  </ul>-->
  <!--  <p>Your native language is:</p>-->
  <!--  <p>Eng</p>-->
  <!--  <input type="radio" name="radio" v-model="choice" value="english">-->
  <!--  <p>Ukr</p>-->
  <!--  <input type="radio" name="radio" v-model="choice" value="ukrainian">-->
  <!--  <p v-if="choice === 'ukrainian'">Добрий день!</p>-->
  <!--  <p v-if="choice === 'english'">Good afternoon!</p>-->
  <p>Where are you come from?</p>
  <select v-model="selected">
    <option value="Ukraine">Ukraine</option>
    <option value="USA">USA</option>
    <option value="England">England</option>
  </select>
  <p>{{ selected }}</p>
  <select>
    <option v-for="year in years">{{year}}</option>
  </select>

</template>
<style>
button {
  background: #222222;
  color: crimson;
}
.someClass {
  color: blue;
}

ul {
  background: aqua;
}

li {
  color: green;
}

.done {
  background: green;
}

.selected {
  background: red;
}

.default {
  text-align: center;
}

p.hidden {
  display: none;
}

p.active {
  background-color: blue;
}

p.valid {
  background-color: seagreen;
}
</style>