<template>
  <div>
    <div class="app">
      <p>{{ name }} - {{ age }}</p>
    </div>
  <button @click="changeName('nejah')">change Name</button>
  <button @click="changeAge('30')">change age</button>
  </div>

</template>

<script lang="ts" >
     
import { defineComponent,reactive ,toRefs,ref} from "vue";

export default defineComponent({
  name: 'App',
  components: {},
  setup(){
    //  const state = reactive({
    //    name :'link' ,
    //    age : 23 as string | number
    //  })
    //    return{...toRefs(state)}
     const name = ref('amin')
     const age = ref(27)
    return { name , age}
  },
  // data() {
  //   return {
  //     name: 'Link',
  //     age: 25 as number | string
  //   }
  // },
  methods: {
    changeName(name: string) {
      this.name = name
      return name
    },
    changeAge(age: number | string) {
      this.age = age
      return age
    }
  }
});
</script>

<style></style>
