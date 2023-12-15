<template>
  <div class="max-w-7xl m-center pt-20 pb-20">
    <div
      class="about-me text-center mt-10 md:mt-32"
      data-aos="fade-up"
      data-aos-delay="100"
      data-aos-duration="800"
    >
      <h2 class="text-5xl dark:text-white">About Me</h2>
      <span class="f-gray text-sm dark:text-white">Personal</span>
    </div>
    <div
      class="details flex mt-20 md:flex-col-reverse lg:flex-row flex-col-reverse"
    >
      <div
        class="image lg:w-3/6 mt-12 lg:m-auto"
        data-aos="fade-right"
        data-aos-delay="500"
        data-aos-duration="500"
      >
        <img
          class="w-11/12 rounded-md drop-shadow-lg m-auto lg:m-0"
          src="../assets/img/profile/1.jpg"
          alt=""
        />
      </div>
      <div
        class="information lg:w-3/6 flex flex-col"
        data-aos="fade-right"
        data-aos-delay="1200"
        data-aos-duration="500"
      >
        <div
          class="cover-letter f-gray text-lg pb-7 dark:text-white text-center lg:text-left md:justify-center lg:justify-start"
        >
        {{about}}
        </div>
        <div
          class="summary-experience flex text-center justify-center lg:justify-start"
        >
          <div :class="info.class" class="mr-5 w-2/12" v-for="(info, key) in data" :key="key">
            <h2 class="text-3xl f-dark-blue font-extrabold dark:text-blue-500">
              {{info.title}}
            </h2>
            <span class="text-sm f-gray dark:text-white"
              >{{info.desc}}</span
            >
          </div>
        </div>
        <div class="resume pt-10">
          <button class="btn-accent flex items-center m-auto lg:m-0">
            <a
              :href="resume_link"
              target="_blank"
            >
              Download CV&nbsp;
              <span
                ><font-awesome-icon
                  class="w-4"
                  :icon="['fas', 'arrow-circle-down']"
              /></span>
            </a>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

const numberOfYears = String(Number(new Date().getFullYear()) - 2017);

export default {
  setup() {
    return {};
  },

  data() {
    return {
      about: "Hi 👋, my name is Irvin. A seasoned software developer with " + numberOfYears + " years of experience in the field. Currently using my skills to create an innovative solutions using the latest technologies. I am particularly proficient in utilizing the AWS Serverless framework in my projects, and I constantly strive to expand my knowledge and skills.",
      resume_link: "https://drive.google.com/file/d/1-7RAcI86iM0e4F71QxxRnZMtFYEIVTWB/view?usp=drive_link",
      data: [
        {
          title: numberOfYears.padStart(2, '0') + "+",
          desc: "Years of Experience",
          class: "years-exp"
        },
        {
          title: "15+",
          desc: "Completed projects",
          class: "projects"
        },
        {
          title: "03+",
          desc: "Companies Worked",
          class: "companies-worked"
        }
      ]
    }
  }
}
</script>