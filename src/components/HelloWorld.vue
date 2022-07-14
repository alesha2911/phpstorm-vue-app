<template>
  <div class="hello">
    <h1> create project:{{authorCreateProject}}</h1>
    <div v-for="student in students" v-bind:key="student.id">
      <h3>{{student.name}}</h3>
      <p>{{student.age}}</p>
      <p v-if="defineComingAgeStudent(student.age)">Студент совершеннолетний</p>
        <p v-else> Не совершеннолетний</p>
      <ul>
        <li v-for="(stack,key) in student.stacks" :key="key"> {{stack}}</li>
      </ul>
    </div>

   <!-- <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">babel</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank" rel="noopener">eslint</a></li>
    </ul>
    <h3>Essential Links</h3>
    <ul>
      <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>
      <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li><a href="https://router.vuejs.org" target="_blank" rel="noopener">vue-router</a></li>
      <li><a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a></li>
      <li><a href="https://github.com/vuejs/vue-devtools#vue-devtools" target="_blank" rel="noopener">vue-devtools</a></li>
      <li><a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">awesome-vue</a></li>
    </ul>-->
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
  methods: {
    /**
     *
     * @param age Number student age
     * @returns {boolean}
     */
    defineComingAgeStudent(age) {
      return age > 17;
    }
  },
  data() {
    return {
      authorCreateProject: 'Alex Prokopenko',
      students: [
        {
          id: 1,
          name: 'Alex Prokopenko',
          age: 21,
          stacks: ['PHP', 'OctoberCms', 'Laravel', 'html', 'css', 'less', 'git', 'composer', 'yarn', 'vue', 'VueX']
        },
        {
          id: 2,
          name: 'Semin',
          age: 21,
          stacks: ['html'],
        },
        {
          id: 3,
          name: 'Mamut Racality',
          age: 16,
          stacks: ['css', 'html']
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
  color: #42b983;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
</style>
