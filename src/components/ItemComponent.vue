<template>
    <div class="flex flex-col bg-slate-300 w-2/3 rounded-xl">
      <div class="text-center bg-slate-400 rounded-t-xl mb-2">{{ name }}</div>
      <div class="px-4"> {{ value }} </div>
      <button 
      @click="$emit('editItem')"
      class="border-2 w-1/2 py-1 my-1 mx-auto border-slate-400 rounded-xl md:w-1/4"
      >
      Редактировать описание
      </button>
    </div>
  </template>
  
  <script>
  export default {
    emits: ['editItem'],
    props: {
      name: {
        type: String,
        required: true 
      },
      value: {
        type: String,
        required: true
      }
    }
  }
  </script>