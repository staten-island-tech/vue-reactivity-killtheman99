<script setup>
import TheWelcome from "../components/TheWelcome.vue";
const cart = [
  {
    id: 1,
    name: "Hershey",
    image: "https://images.heb.com/is/image/HEBGrocery/000740766-1",
    price: 5,
  },

  {
    id: 2,
    name: "lipton-soup",
    image:
      "https://i5.walmartimages.com/asr/0f775896-f961-486f-acfc-baf14377084c_1.14a0791085b77162940f4825efcebdc3.jpeg",
    price: 3,
  },
  {
    id: 3,
    name: "choco-chip cookies",
    image:
      "https://i5.walmartimages.com/asr/5902e3f2-960b-4b11-ade6-a77274955633.55663977ef35ff08c3e814b59e6b8d65.jpeg",
    price: 6,
  },
  {
    id: 4,
    name: "chicken",
    image:
      "https://cdn.mos.cms.futurecdn.net/BX7vjSt8KMtcBHyisvcSPK-1200-80.jpg",
    price: 50,
  },

  {
    id: 5,
    name: "milk",
    image:
      "https://images.immediate.co.uk/production/volatile/sites/30/2020/02/Glass-and-bottle-of-milk-fe0997a.jpg",
    price: 2,
  },
  {
    id: 6,
    name: "cow",
    image:
      "https://upload.wikimedia.org/wikipedia/commons/8/8c/Cow_%28Fleckvieh_breed%29_Oeschinensee_Slaunger_2009-07-07.jpg",
    price: 200,
  },
];

function makecart() {
  document.cart.innerHTML = "";
  cart
    .filter((item) => item.image)
    .foreach((item) => {
      cart.insertAdjacentHTML(
        "beforeend",
        `<div class="flex">
  <img class="img" src=${item.image}
  <p>${item.name}</p>
  </div>`
      );
    });
}
makecart();
</script>

<template>
  <main>
    <section class="cart"></section>
  </main>
</template>
