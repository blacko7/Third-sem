<template>
    <header class="header">
      <h1>
        <p>MY-APP</p>
      </h1>
      
    </header>
    <main class="main">
      <form class="form-options" @submit.prevent="handleSelect">
        <select class="select" @change="handleSelect">
          <option value="manual">Manual</option>
          <option value="range">Range</option>
          <option value="word">Word</option>
        </select>
      </form>
      
      <Manual v-if="selected == 'manual'"/>
      <Range v-else-if="selected == 'range'"/>
      <Word v-else/>
    </main>
  </template>
  
  <script>
  //components
  import Manual from "../components/Manual";
  import Range from "../components/Range";
  import Word from "../components/Word";
  
  export default {
    name: "CounterView",
    components: {Manual, Range, Word},
    data(){
      return {
        selected: "manual",
      }
    },
    methods: {
      handleSelect(event) {
        this.selected = event.target.value;
      }
    }
  }
  </script>
