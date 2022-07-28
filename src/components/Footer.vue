<template>
  <footer
    class="footer xl:grid-cols-5 grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4 sm:mx-8 lg:mx-16 my-10 py-10 border-t-2"
  >
    <div class="">
      <h3 class="font-bold text-xl mb-4">Funiro.</h3>
      <div class="text-gray-600">
        <p class="leading-normal mb-4">
          Worldwide furniture store since 2020. We sell over 1000+ branded products on our website
        </p>
        <p class="mb-4 flex gap-2">
          <img :src="pin" alt="pin" />
          <span>Sawojajar Malang, Indonesia</span>
        </p>
        <p class="mb-4 flex gap-2">
          <img :src="phone" alt="phone" />
          +6289 456 3455
        </p>
        <p class="mb-4"><a href="#">www.funiro.com</a></p>
      </div>
    </div>
    <div class="menu">
      <h3 class="font-bold text-xl mb-4">Menu</h3>
      <div class="text-gray-600 space-y-4">
        <p class="">Products</p>
        <p>Rooms</p>
        <p>Inspirations</p>
        <p>About Us</p>
        <p>Terms & Policy</p>
      </div>
    </div>
    <div class="account">
      <h3 class="font-bold text-xl mb-4">Account</h3>
      <div class="text-gray-600 space-y-4">
        <p>My Account</p>
        <p>Checkout</p>
        <p>My Cart</p>
        <p>My catalog</p>
      </div>
    </div>
    <div class="stay">
      <h3 class="font-bold text-xl mb-4">Stay Connected</h3>
      <div class="text-gray-600 space-y-4">
        <p>Facebook</p>
        <p>Instagram</p>
        <p>Twitter</p>
      </div>
    </div>
    <div class="stayUpdate">
      <h3 class="font-bold text-xl mb-4">Stay Updated</h3>
      <div class="p">
        <div class="flex">
          <input class="bg-gray-200 py-1 px-3 outline-none w-[85%]" type="email" placeholder="Enter your email" />
          <div class="bg-orange-600 px-1 flex justify-center items-center w-[15%]">
            <img class="" :src="sendMessage" alt="sendMessage" />
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import sendMessage from "../assets/Vector.svg";
import pin from "../assets/Pin 24px.svg";
import phone from "../assets/Phone 24px.svg";

export default {
  name: "Footer",
  data() {
    return {
      sendMessage: sendMessage,
      pin: pin,
      phone: phone,
    };
  },
};
</script>

<style scoped></style>
