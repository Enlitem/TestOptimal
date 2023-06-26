<template>
  <div
    class="w-full flex justify-around items-center h-16 bg-cyan-600 text-white text-xl mb-5"
  >
    OPTIMAL CITY Technologies Тестовое задание
  </div>
  <div class="px-5">
    <div v-if="!isEdit">
      <item-component
        v-for="(item, index) in data"
        :key="index"
        :name="item.name"
        :value="item.value"
        @editItem="edit(index)"
        class="mb-3 mx-auto"
      />
    </div>
    <div v-else class="flex flex-col bg-slate-300 w-2/3 rounded-xl m-auto">
      <div class="px-2 py-2 bg-slate-400 rounded-t-xl mb-2">
        Вы редактируете элемент "{{ data[selectedItem].name }}"
      </div>
      <input
        type="text"
        v-model="data[selectedItem].value"
        class="bg-slate-300 border-2 border-slate-400 mx-2 px-4 rounded-xl"
      />
      <button
        @click="changeValue"
        class="px-2 py-2 border-2 w-1/2 my-1 mx-auto border-slate-400 rounded-xl md:w-1/4"
      >
        Сохранить изменения
      </button>
    </div>
  </div>
</template>

<script>
import ItemComponent from "./components/ItemComponent.vue";

export default {
  components: { ItemComponent },
  data() {
    return {
      data: [
        { name: "name1", value: "value1" },
        { name: "name2", value: "value2" },
        { name: "name3", value: "value3" },
        { name: "name4", value: "value4" },
        { name: "name5", value: "value5" },
        { name: "name6", value: "value6" },
        { name: "name7", value: "value7" },
        { name: "name8", value: "value8" },
        { name: "name9", value: "value9" },
        { name: "name10", value: "value10" },
        { name: "name11", value: "value11" },
        { name: "name12", value: "value12" },
        { name: "name13", value: "value13" },
        { name: "name14", value: "value14" },
        { name: "name15", value: "value15" },
        { name: "name16", value: "value16" },
        { name: "name17", value: "value17" },
        { name: "name18", value: "value18" },
        { name: "name19", value: "value19" },
        { name: "name20", value: "value20" },
        { name: "name21", value: "value21" },
        { name: "name22", value: "value22" },
        { name: "name23", value: "value23" },
      ],
      isEdit: false,
      selectedItem: -1,
    };
  },
  methods: {
    edit(index) {
      this.isEdit = true;
      this.selectedItem = index;
    },
    changeValue() {
      this.isEdit = false;
      this.selectedItem = -1;
    },
  },
};
</script>