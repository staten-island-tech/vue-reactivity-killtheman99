<script>
import { c } from "./array.js";

const DOM = {
  cart: document.getElementById("cart"),
};

function makecart() {
  document.DOM.cart.innerHTML = "";
  c.filter((item) => item.image).foreach((item) => {
    DOM.cart.insertAdjacentHTML(
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
