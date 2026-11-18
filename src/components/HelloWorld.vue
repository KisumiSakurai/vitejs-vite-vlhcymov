<script setup lang="ts">
import UserCard from './UserCard.vue';
import { ref } from 'vue';
const user = {
  name: '佐藤',
  age: 28,
  isAdmin: true,
};

type Product = {
  id: number;
  name: string;
  price: number;
  description?: string;
  status: 'sale' | 'soldout';
};

function getSalePrice(price: number, isSale: boolean): number {
  if (isSale) {
    return price / 2;
  }
  return price;
}

const selectedProduct = ref<Product | null>(null);

selectedProduct.value = {
  id: 1,
  name: 'りんご',
  price: 150,
  status: 'sale',
};

function handleInput(event: Event): void {
  const input = event.target as HTMLInputElement;
  const text = input.value;
}

type User = {
  name: string;
  age: number;
};

function getUserName(user: User): string {
  return user.name;
}
</script>

<template>
  <UserCard :name="user.name" :age="user.age" :isAdmin="user.isAdmin" />
</template>
