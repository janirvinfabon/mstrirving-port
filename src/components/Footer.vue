<template>
  <div class="bg-gray-900 h-20 flex justify-center items-center">
    <a
      class="text-neutral-500 font-light cursor-pointer dark:text-white"
      href="https://portfolio.mstrirving.com"
    >
      &copy; mstrirving {{ current_year }}
    </a>
  </div>
  <button id="btn-top" @click="scrollToTop">
    <span>
      <font-awesome-icon class="w-4" :icon="['fas', 'arrow-up']"
      />
    </span>
  </button>
</template>
<script>

const scrollFunction = () => {
      const btn_top = document.getElementById("btn-top");
      if (document.body.scrollTop > 20 || document.documentElement.scrollTop > 20) {
          btn_top.style.display = "block";
      } else {
          btn_top.style.display = "none";
      }
  }

window.onscroll = function() { scrollFunction() };

export default {
  data() {
    return {
      current_year: new Date().getFullYear()
    };
  },
  methods: {
    scrollToTop() {
      window.scrollTo({ top: 0, left: 0, behavior: 'smooth' });
    },
  },
};
</script>

<style scoped>
#btn-top {
  position: fixed;
  bottom: 30px;
  float: right;
  left: 95%;
  font-size: 12px;
  background-color: var(--blue);
  color: var(--white);
  padding: 10px;
  border-radius: 4px;
  text-align: center;
  font-size: 1.35rem;
}

#btn-top:hover {
  transform: scale(1.2);
}

@media (max-width: 575px){
  #btn-top {
    left: 85%;
  }
}
</style>
