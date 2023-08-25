<template>
  <HelloWorld/>
  <HomeRaju/>
  <GreetingWorld/>
  <IfElse/>
  <ul>
    <li v-for="item in Profiles" :key="item.name">
      <ChildComponent :data="item" :getData="getDetails" />
    </li>
  </ul>
  <h1>Props Example</h1>
  <h2><StudentsDetails name="Raju"/></h2>
  <h2><TeacherDetails name="Jack"/></h2>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import HomeRaju from './components/HomeRaju.vue';
import GreetingWorld from './components/GreetingWorld.vue';
import IfElse from './components/IfElse.vue';
import ChildComponent from './components/ChildComponent.vue';
import StudentsDetails from './components/StudentsDetails.vue';
import TeacherDetails from './components/TeacherDetails.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    HomeRaju,
    GreetingWorld,
    IfElse,
    ChildComponent,
    StudentsDetails,
    TeacherDetails
},

  methods: {
    getDetails(name){
      alert(name)
    }
  },
  data(){
    return{
      Profiles: [
        {
          name: "Raju",
          age: "24"
        },
        {
          name: "Jack",
          age: "25"
        },
        {
          name: "Miller",
          age: "26"
        }

      ]
    }
  }
}
</script>


