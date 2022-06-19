<template>
  <!--
   Using v-for to Loop Over an Array of Strings
  -->
  <div>
    <h1>Looping through arrays (07_Loops.vue)</h1>
    <!-- Backticks -->
    <div v-for="n in 5" :key="`${n}`">
      {{ n }}
    </div>
    <!-- Unordered list -->
    <ul>
      <li v-for="n in 5" :key="n">
        {{ n }}
      </li>
    </ul>
    <!-- Unordered list with an array -->
    <ul>
      <li v-for="(item, n) in interests" :key="n">
        {{ item }}
      </li>
    </ul>
    <!-- Ordered list with objects -->
    <h3>Book:</h3>
    <ol>
      <li v-for="item in books" :key="item">
        {{ item }}
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  data() {
    return {
      interests: ['TV', 'Games', 'Sports', 'Programming Vue'],
      books: [
          {
            title: 'Schachnovelle',
            author: 'Stefan Zweig',
            publishedAt: '19xy-04-10'
          },{
            title: 'Ready Player One',
            author: 'Ernest Clien',
            publishedAt: '20xx-04-10'
          },
      ]
    }
  },
}
</script>

<style lang="scss" scoped>
li {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  color: #2c3e50;
  margin-top: 10px;
}

h1 {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
