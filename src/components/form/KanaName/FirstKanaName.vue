<script setup>
import { ref } from "vue";
import { useFormStore } from "@/stores/form";

const props = defineProps(["firstKanaName"]);

const formStore = useFormStore();
const formFirstKanaName = ref(props.firstKanaName);

const updateFirstKanaName = (event) => {
  formStore.firstKanaName = event.target.value;
};
</script>

<template>
  <div class="name name-margin">
    <label class="name-label">セイ</label>
    <input v-model="formFirstKanaName" @input="updateFirstKanaName" class="name-input"/>
  </div>
</template>
