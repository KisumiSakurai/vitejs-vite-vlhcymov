<script setup lang="ts">
const props = defineProps<{
  name: string;
  age: number;
  isAdmin: boolean;
}>();
</script>

<template>
  <section>
    名前：{{ props.name }} 年齢：{{ props.age }}歳 管理者：
    <span v-if="props.isAdmin">はい</span><span v-else>いいえ</span>
  </section>
</template>
