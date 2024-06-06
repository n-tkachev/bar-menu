<script setup>
import { reactive } from 'vue'

const menu = reactive([
  {
    title: 'MOJITO',
    price: '7.5€',
    consist: 'Rum, lime, mint, soda'
  },
  {
    title: 'CINDY DOLLAR',
    price: '8€',
    consist: 'Rum, Malibu, raspberry, pineapple juice'
  },
  {
    title: 'MAI TAI',
    price: '8€',
    consist: 'Rum, triple sec, amaretto, pineapple juice'
  },
  {
    title: 'PINA COLADA',
    price: '8€',
    consist: 'Rum, pineapple juice, Malibu, cream'
  },
  {
    title: 'DAIQUIRI',
    price: '7€',
    consist: 'Rum, lemon, sugar'
  },
  {
    title: 'DUNE',
    price: '7.50€',
    consist: 'Rum, vanilla, orange juice, egg white, triple sec'
  },
  {
    title: 'NO SUGAR',
    price: '8€',
    consist: 'Gin, prosecco, grapefruit, mint, lime, ginger'
  },
  {
    title: 'FRENCH 75',
    price: '7€',
    consist: 'Gin, prosecco, lime'
  },
  {
    title: 'CLOVER CLUB',
    price: '7.50€',
    consist: 'Gin, raspberry, egg white, lemon'
  },
  {
    title: 'PALOMA',
    price: '7.5€',
    consist: 'Tequila, grapefruit, soda'
  },
  {
    title: 'MARGARITA',
    price: '7€',
    consist: 'Tequila, triple sec, lime'
  },
  {
    title: 'SEX ON THE BEACH',
    price: '7.50€',
    consist: 'Vodka, peach, pineapple juice, grenadine'
  },
  {
    title: 'ESPRESSO MARTINI',
    price: '7.50€',
    consist: 'Vodka, Kahlua, espresso'
  },
  {
    title: 'WHITE RUSSIAN',
    price: '7€',
    consist: 'Vodka, Kahlua, cream'
  },
  {
    title: 'MOSCOW MULE',
    price: '7.50€',
    consist: 'Vodka, triple sec, ginger, mint, lime'
  },
  {
    title: 'WHISKEY SOUR',
    price: '7.50€',
    consist: 'Bourbon, Angostura, egg white, lemon, sugar'
  },
  {
    title: 'MANHATTAN',
    price: '7€',
    consist: 'Bourbon, Martini Rosso, Angostura'
  },
  {
    title: 'OLD FASHIONED',
    price: '7€',
    consist: 'Bourbon, Angostura, cane sugar'
  },
  {
    title: 'LYNCHBURG LEMONADE',
    price: '7.50€',
    consist: 'Jack Daniels, triple sec, lemon, sugar, egg white, soda'
  },
  {
    title: 'APEROL SPRITZ',
    price: '7.50€',
    consist: 'Aperol, prosecco, soda'
  },
  {
    title: 'NEGRONI',
    price: '7.50€',
    consist: 'Gin, Martini Rosso, Campari'
  },
  {
    title: 'BELLINI',
    price: '7€',
    consist: 'Peach liqueur, prosecco'
  }
])

const alcohol = reactive([
  { title: 'Bombay', price: '3.50€' },
  { title: 'Olmeca', price: '3€' },
  { title: 'Havana Club', price: '3€' },
  { title: 'Brugal Añejo', price: '5€' },
  { title: 'Absolut', price: '3€' },
  { title: 'Jim Beam', price: '4€' },
  { title: 'Jameson', price: '3€' },
  { title: 'Jack Daniel’s', price: '3€' },
  { title: 'Monkey Shoulder', price: '5€' },
  { title: 'Jägermeister', price: '2.50€' },
  { title: 'Amaretto', price: '2.50€' },
  { title: 'Malibu', price: '2.50€' },
  { title: 'Baileys', price: '2.50€' },
  { title: 'Absent', price: '3.50€' },
  { title: 'Campari', price: '2.50€' },
  { title: 'Martini Rosso', price: '2.50€' },
  { title: 'Martini Bianco', price: '2.50€' },
  { title: 'Martini Extra', price: '2.50€' },
  { title: 'Prosecco', price: '5€' }
])

const coffee = reactive([
  {
    title: 'Espresso',
    price: '1.5€'
  },
  {
    title: 'Cappuccino',
    price: '2.5€'
  },
  {
    title: 'Latte',
    price: '3€'
  },
  {
    title: 'Raf',
    price: '4€'
  },
  {
    title: 'Ice coffee',
    price: '3.5€'
  },
])

const lemonades = reactive([
  { title: 'Aranchata', price: '4€' },
  { title: 'Raspberry Passionfruit', price: '4€' },
  { title: 'Watermelon Mango', price: '4€' },
])
</script>

<template>
  <div class="flex flex-col gap-5 px-5 py-10">
    <h1 class="mb-5">Cocktail Menu</h1>

    <div v-for="item in menu" :key="item.title">
      <h2 class="font-bold">{{ item.title }} <span class="text-yellow-500">{{ item.price }}</span></h2>
      <p>{{ item.consist }}</p>
    </div>

    <h3 class="font-medium text-[40px] py-5">Alcohol</h3>

    <div class="grid grid-cols-2 gap-5">
      <div v-for="item in alcohol" :key="item.title">
        <p class="font-bold">{{ item.title }} <span class="text-yellow-500">{{ item.price }}</span></p>
      </div>
    </div>

    <div class="grid grid-cols-2 gap-5">
      <div>
        <h3 class="font-medium text-[40px] py-5">Lemonade</h3>
        <div v-for="item in lemonades" :key="item.title">
          <p class="font-bold">{{ item.title }} <span class="text-yellow-500">{{ item.price }}</span></p>
        </div>
        <div class="font-bold mt-6">FRESH JUICE - <span class="text-yellow-500">3.50€</span></div>
      </div>
      <div>
        <h3 class="font-medium text-[40px] py-5">Coffee</h3>
        <div v-for="item in coffee" :key="item.title">
          <p class="font-bold">{{ item.title }} <span class="text-yellow-500">{{ item.price }}</span></p>
        </div>
      </div>

    </div>


  </div>
</template>
