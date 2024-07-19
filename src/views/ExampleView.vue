<template>
  <div class="ExampleView">
    <MdEditor :value="mdvalue" :handle-change="onMdChange" />
    {{ codevalue }}
    <CodeEditor :value="codevalue" :handle-change="onCodeChange" />
  </div>
</template>

<script setup lang="ts">
import { defineComponent, ref } from "vue";
import HelloWorld from "@/components/HelloWorld.vue";
import MdEditor from "@/components/MdEditor.vue";
import CodeEditor from "@/components/CodeEditor.vue"; // @ is an alias to /src

const mdvalue = ref();
const codevalue = ref();

const onMdChange = (v: string) => {
  mdvalue.value = v;
};
const onCodeChange = (v: string) => {
  codevalue.value = v;
};
</script>
