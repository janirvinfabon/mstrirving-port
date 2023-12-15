<template>
  <div class="max-w-7xl m-center pt-48">
    <div
      class="skills text-center mt-10"
      data-aos="fade-up"
      data-aos-delay="100"
      data-aos-duration="800"
    >
      <h2 class="text-5xl dark:text-white">Skills</h2>
      <span class="f-gray text-sm dark:text-white">My Technical Level</span>
    </div>
    <div class="skill-details flex mt-20 flex-col lg:flex-row lg:gap-10">
      <div
        data-aos="fade-down"
        data-aos-duration="1000"
        data-aos-delay="200"
        class="lg:w-1/3 md:w-96 md:m-auto md:mb-16 card bg-white drop-shadow-2xl dark:bg-slate-800"
        v-for="(skill, skill_key) in skills" :key="skill_key"
      >
        <h2 class="pt-7 pl-5 flex items-center">
          <font-awesome-icon
            class="fa-2xl pr-3 f-blue w-20"
            :icon="['fas', skill.logo]"
          />
          <div class="flex flex-col">
            <h2 class="text-xl dark:text-white">{{skill.name}}</h2>
            <span class="text-sm f-gray dark:text-white"
              >{{skill.desc}}</span
            >
          </div>
        </h2>
        <div
          class="description grid grid-cols-4 gap-4 m-auto lg:px-10 px-5 pt-10"
        >
          <div class="p-1 card-mini" v-for="(stack, key) in skill.tech_stacks" :key="key"
          >
            <img
              :src="stack.logo"
              class="h-14"
              :alt="stack.name"
            />
            <span class="dark:text-white">{{stack.name}}</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  setup() {
    return {};
  },

  data() {
    return {
      skills: [
        {
          name: "Frontend Developer",
          desc: "More than " + (Number(new Date().getFullYear()) - 2017) + " years",
          logo: "code",
          tech_stacks: [
            {
              name: "HTML5",
              logo: "https://upload.wikimedia.org/wikipedia/commons/thumb/6/61/HTML5_logo_and_wordmark.svg/130px-HTML5_logo_and_wordmark.svg.png"
            },
            {
              name: "CSS",
              logo: "https://upload.wikimedia.org/wikipedia/commons/thumb/d/d5/CSS3_logo_and_wordmark.svg/120px-CSS3_logo_and_wordmark.svg.png"
            },
            {
              name: "JavaScript",
              logo: "https://upload.wikimedia.org/wikipedia/commons/thumb/6/6a/JavaScript-logo.png/600px-JavaScript-logo.png?20120221235433"
            },
            {
              name: "Boostrap",
              logo: "https://seeklogo.com/images/B/bootstrap-logo-3C30FB2A16-seeklogo.com.png"
            },
            {
              name: "VueJS",
              logo: "https://seeklogo.com/images/V/vuejs-logo-17D586B587-seeklogo.com.png"
            },
            {
              name: "OS",
              logo: "https://media-exp1.licdn.com/dms/image/C560BAQFs9sLsIuJjCQ/company-logo_200_200/0/1519856179274?e=2159024400&v=beta&t=EsgMcxU-uBB1DtgW4uD6K-0n9OjOBp-JhKQi7r9tX_A"
            }
          ]
        },
        {
          name: "Backend Developer",
          desc: "More than " + (Number(new Date().getFullYear()) - 2017) + " years",
          logo: "code-branch",
          tech_stacks: [
            {
              name: "AWS",
              logo: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRK_A4ygFZawvqLFvYUYfssFpgwAfCGZ7Xs_Ka4hDnmgA&s",
            },
            {
              name: "PHP",
              logo: "https://cdn-icons-png.flaticon.com/512/5968/5968332.png"
            },
            {
              name: "Python",
              logo: "https://1.bp.blogspot.com/-X5OBU37Ims4/XQexxebsV0I/AAAAAAAAD80/PlMIGUQBY3YwRugZNLvdRaI2Pw_g0jIlgCLcBGAs/s1600/Python%2BProgramming%2BLogo.png"
            },
            {
              name: "C#",
              logo: "https://iconape.com/wp-content/png_logo_vector/c.png"
            },
            {
              name: "CodeIgniter",
              logo: "https://cdn3.iconfinder.com/data/icons/social-media-2169/24/social_media_social_media_logo_codeigniter-512.png"
            },
            {
              name: "Oracle",
              logo: "https://download.logo.wine/logo/Oracle_Corporation/Oracle_Corporation-Logo.wine.png"
            },
            {
              name: "MySQL",
              logo: "https://www.freepnglogos.com/uploads/logo-mysql-png/logo-mysql-mysql-logo-png-images-are-download-crazypng-21.png"
            },
            {
              name: "PostgreSQL",
              logo: "https://gdm-catalog-fmapi-prod.imgix.net/ProductLogo/ffc47c45-e0ba-4c50-8684-9ab688fad82f.png?auto=format&q=50&fit=fill"
            }
          ]
        },
        {
            name: "Others",
            desc: "Acquired Skills",
            logo: "brain",
            tech_stacks: [
            {
              name: "Git",
              logo: "https://seeklogo.com/images/G/github-logo-5F384D0265-seeklogo.com.png"
            },
            {
              name: "Jira",
              logo: "https://cdn.icon-icons.com/icons2/2699/PNG/512/atlassian_jira_logo_icon_170511.png"
            },
            {
              name: "Confluence",
              logo: "https://seeklogo.com/images/C/confluence-logo-D9B07137C2-seeklogo.com.png"
            },
            {
              name: "CICD",
              logo: "https://www.mabl.com/hubfs/CICDBlog.png"
            },
            {
              name: "SEO",
              logo: "https://thumbs.dreamstime.com/b/seo-logo-magnifying-glass-search-engine-optimization-blue-yellow-red-green-color-98240334.jpg"
            },
            {
              name: "Jmeter",
              logo: "https://www.devopsschool.com/blog/wp-content/uploads/2022/03/Jmeter.png"
            },
            {
              name: "Figma",
              logo: "https://cdn.sanity.io/images/599r6htc/localized/46a76c802176eb17b04e12108de7e7e0f3736dc6-1024x1024.png?w=670&h=670&q=75&fit=max&auto=format"
            },
            {
              name: "ClickUp",
              logo: "https://th.bing.com/th/id/OIP.McPGCOUTuzebecT0Jv0wZAHaHa?rs=1&pid=ImgDetMain"
            }
          ]
        }
      ]
    };
  },
};
</script>