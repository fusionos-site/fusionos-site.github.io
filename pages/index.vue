
<template>
  <full-page id="fullpage" ref="fullpage" class="fullPage" :options="options">
    <!-- Home section -->
    <section id="home-section" class="section fp-table ">
      <NavBar :parentRefs="$refs" class="absolute top-0 w-full md:mt-5"></NavBar>
      <div class="fp-tableCell">
        <div class="grid items-center grid-cols-2 p-6 mt-10 md:mt-12 md:pl-1/6 xl:mt-16">
          <div class="order-first col-span-2 md:col-span-1 md:order-last">
            <img
              src="../assets/img/heroo.png"
              class="hidden w-64 max-w-md mx-auto md:block lg:w-3/5 card "
            />
        <!--    <img
              src="../assets/img/hero_phones_small.svg"
              class="w-7/12 pb-6 mx-auto md:hidden"
            /> -->
            
          </div>
          <div class="order-last text-justify col-span-2 md:col-span-1 md:order-first">
            <div>
              <h1 class="text-justify text-6xl text-gray-100 font-black text-p-blue">FusionOS</h1>
              <div class="text-black-700 ">
                <span class="font-semibold pb-7">A new experience awaits you</span>
                <p
                  class="pb-2 text-xl"
                >A buttery smooth aftermarket Android™ firmware.</p>
                <p class="pb-4 text-lg">A custom ROM which wants to bring Android Device at first glance, with many additional configurations at your disposal. We aim to provide frequent builds with monthly security patches from the latest aosp sources.</p>
              </div>
              <button
                v-on:click="$refs.fullpage.api.moveSectionDown()"
                class="px-4 py-3 mt-6 font-semibold text-white rounded-full focus:outline-none bg-p-blue hover:bg-blue-700"
              >Learn more</button>
            </div>
          </div>
        </div>
      </div>
      <img
        src="../assets/img/Fusion.png"
        style="width: 80.2rem; transform: translateY(1px);"
        class="bottom-0 left-0 hidden p-absolute md:block"
      />
    </section>
    <!-- Feature section -->
    <section id="feature-section" class="section">
      <div class="grid items-center bg-purple-300 grid-cols-8 row-gap-4 p-12 md:row-gap-40 md:pl-1/6 ">
        <div class="col-span-8 md:col-span-4">
          <div class="inline-block mx-auto ">
            <h1
              class="hidden font-bold text-left text-black md:block md:text-xl lg:text-2xl xl:text-vw-4xl max-text-4xl"
            >
              <p>We've included many</p>
              <p>useful features,</p>
              <p>to help with everyday</p>
              <p>tasks</p>
            </h1>
            <h1 class="text-2xl font-bold text-center text-white sm:text-3xl md:hidden">
              <p>Faster security updates</p>
              <p>features,</p>
              <p>to help with everyday tasks</p>
            </h1>
          </div>
        </div>
        <div class="col-span-8 md:col-span-4">
          <img
            src="../assets/img/features.svg"
            class="w-full mx-auto md:w-80 lg:w-104 xl:w-full xl:px-6 xl:max-w-xl"
          />  
        </div>
        <div class="col-span-8 md:col-span-3">
          <img src="../assets/img/RoutineUpdates2.svg" class="w-full mx-auto md:w-80 lg:w-104 xl:w-full xl:px-16 xl:max-w-xl" />
        </div>
        <div class="col-span-8 md:col-span-4">
          <img src="../assets/img/RoutineUpdates.svg" class="w-full mx-auto md:w-80 lg:w-104 xl:w-full xl:px-16 xl:max-w-xl" />
        </div>
      </div>
    <!--  <img
        src="../assets/img/volpanel.svg"
        style="transform: translateY(1px);"
        class="bottom-0 hidden p-absolute max-h-1/2 left-1/6 md:block md:w-48 lg:w-56 xl:w-64"
      /> -->
    </section>

    <!-- Team section -->
    <section id="team-section" class="section">
      <div class="grid items-center grid-cols-1 pt-3">
        <div class="col-span-6">
          <h1 class="text-4xl font-semibold text-center text-p-yellow md:text-5xl">Meet the team</h1>
        </div>
      </div>
      <div
        class="grid items-center grid-cols-6 gap-3 px-6 pb-6 md:pl-1/8 md:pr-8 md:gap-4 lg:gap-6 lg:pr-1/12"
      >
        <div class="col-span-6">
          <h1 class="text-xl text-center p-6 font-semibold text-left text-white md:text-3xl">Core Team</h1>
        </div>
        <div class="col-span-3 md:col-span-2 ">
          <TeamCard
            name="Sakthivel Nadar"
            role="Founder and Lead Developer"
            :img="require(`@/assets/img/pfp/sakthi.jpg`)"
            github="https://github.com/sparxfusion"
          />
        </div>
        <div class="col-span-3 md:col-span-2">
          <TeamCard
            name="Sreekanth"
            role="Core Developer and Maintainer Relations"
            :img="require(`@/assets/img/pfp/sree.jpg`)"
            github="https://github.com/"
            
          />
        </div>
        <div class="col-span-3 md:col-span-2">
          <TeamCard
            name="Debayan"
            role="Core Developer"
            :img="require(`@/assets/img/pfp/debayan.jpg`)"
            
          />
        </div>
        <div class="col-span-3 md:col-span-2">
          <TeamCard
            name="Sarthak Roy"
            role="Core Developer"
            :img="require(`@/assets/img/pfp/sarthak.jpg`)"
            github="https://github.com/"
            
          />
        </div>
        <div class="col-span-3 md:col-span-2">
          <TeamCard
            name="SriBalaji"
            role="Project manager / Web Dev"
            :img="require(`@/assets/img/pfp/thecloverly.jpg`)"
            github="https://github.com/iamthecloverly"
            instagram="https://instagram.com/iam.sribalaji"
            twitter="https://twitter.com/thecloverly"
          />
        </div>
        
        <div class="col-span-3 md:col-span-2">
          <TeamCard
            name="Aditya Singh"
            role="Maintainer Relations"
            :img="require(`@/assets/img/pfp/aditya.jpg`)"
            github="https://github.com/"
            instagram="https://instagram.com/"
            twitter="https://twitter.com/"
          />
        </div>
        <div class="col-span-3 md:col-span-2">
          <TeamCard
            name="Suyog"
            role="Developer"
            :img="require(`@/assets/img/pfp/kat.webp`)"
            github="https://github.com/"
          />
        </div>
        <div class="col-span-6 md:col-span-2">
          <TeamCard
            name="AmaanCG"
            role="Designer and Animator"
            :img="require(`@/assets/img/pfp/aman.png`)"
            github="https://github.com/"
          />
        </div>
        <div class="col-span-6 md:col-span-2">
          <TeamCard
            name="loxianne"
            role="Designer"
            :img="require(`@/assets/img/pfp/l.webp`)"
            github="https://github.com/"
          />
        </div>
        
  <!--  <div class="col-span-6">
          <h1 class="text-xl font-semibold text-left text-white md:text-3xl">Designers</h1>
        </div>
        <div class="col-span-3 md:col-span-2">
          <TeamCard
            name="Dhruv Gera"
            role=" Web dev"
            :img="require(`@/assets/img/pfp/rishi.webp`)"
            twitter="https://twitter.com/rshbfn"
          />
        </div>
        <div class="col-span-3 md:col-span-2">
          <TeamCard
            name="SriBalaji"
            role="Project manager / Web Dev"
            :img="require(`@/assets/img/pfp/karol.webp`)"
            github="https://github.com/iamthecloverly"
            instagram="https://instagram.com/iam.sribalaji"
            twitter="https://twitter.com/thecloverly"
          />
        </div>
        <div class="col-span-6 md:col-span-2">
          <TeamCard
            name="AmaanCG"
            role="Designer and Animator"
            :img="require(`@/assets/img/pfp/parth.webp`)"
            youtube="https://www.youtube.com/channel/UCkzhkIspDgx1HsUnA2oeUqA"
            github="https://github.com/valvze"
          />
        </div> --> 
        </div>
      <img
        src="../assets/img/team_circle_top.svg"
        style="transform: translateY(-1px);"
        class="top-0 right-0 hidden w-24 p-absolute lg:w-32 md:block"
      />
      <img
        src="../assets/img/team_circle_bottom.svg"
        style="transform: translateY(1px);"
        class="bottom-0 left-0 hidden w-24 p-absolute lg:w-32 md:block"
      />
    </section>
    <!-- Changelog section -->
    <section id="changelog-section" class="section">
      <div class="grid items- grid-cols-1 pt-3">
        <div class="col-span-6">
          <h1
            class="text-xl font-bold p-10 text-black md:text-4xl"
          >What's New?</h1>
        </div>
        <div class="col-span-6">
          <h1 class="text-xl font-semibold text-center text-black md:text-4xl">Coming soon!</h1>
        </div>
        <div class="col-span-6">
          <h1 class="text-lg font-semibold text-center text-black md:text-2xl">
            <p>In the meantime you can check the changelog on github!</p>
          </h1>
        </div>
        <div class="col-span-6">
          <a
            href="https://t.me/fusionos"
            target="_blank"
          >
            <button
              class="px-5 py-3 mt-6 font-semibold text-white rounded-full focus:outline-none bg-p-green hover:bg-green-700"
            >Click here</button>
          </a>
        </div>
      </div>
      <img
        src="../assets/img/k1.png"
        style="width: 11.2rem; transform: translateY(1px);"
        class="bottom-0 left-0 hidden p-absolute md:block"
      />
    </section>
    <!-- Download section -->
    <section id="download-section" class="section">
      <div class="grid items-center grid-cols-1 p-6 mt-3 mb-36 md:mb-96 lg:mb-104">
        <div class="col-span-1">
          <h1
            class="my-6 text-xl font-semibold text-center text-white sm:text-2xl md:text-4xl"
          >Like what you see?</h1>
        </div>
        <div class="col-span-1 mb-6 text-white">
          <p class>Great! Head to our downloads page, grab</p>
          <p>a zip file for your desired device and you</p>
          <p>should be all set. Happy flashing!</p>
        </div>
        <div class="col-span-1">
          <a href="#" target="_blank">
            <button
              class="px-5 py-3 mb-10 font-semibold bg-white rounded-full text-p-blue hover:bg-gray-300"
            >Download</button>
          </a>
        </div>
        <div class="col-span-1">
          <h1
            class="mb-6 text-xl font-semibold text-center text-white sm:text-2xl md:mb-0 md:text-4xl"
          >Don’t see your device on the list?</h1>
        </div>
        <div class="col-span-1 mb-6">
          <UserDevCardMobile class="w-full md:hidden" />
        </div>
        <div class="col-span-1">
          <DevDevCardMobile class="w-full md:hidden" />
        </div>
      </div>
      <div class="bottom-0 flex hidden w-full pb-10 p-absolute md:flex">
        <div class="flex-1">
          <DevCard header="I'm a user" class="w-64 ml-auto mr-12 bg-purple-700 xl:w-96 lg:w-80 xl:mr-20">
            <p
              class="pb-5"
            >Don’t worry, we’re supporting more and more devices as we grow, so there is a chance that in the near future, we’ll support yours too!</p>
            <p>Some developers also build POSP unofficially, so you can search your device’s xda page for one and try it out. We’re not responsible for any bugs you encounter in those builds, though.</p>
          </DevCard>
        </div>
        <div class="flex-1">
          <DevCard header="I'm a developer" class="w-64 ml-12 bg-red-700 xl:ml-20 lg:w-80 xl:w-96">
            <p class="pb-5">
              So you wanna build this ROM by yourself? Great! Fusion-OS is entirely open source, so head out to our
              <a
                href="https://github.com/Fusion-OS/"
                class="font-semibold text-p-yellow"
                target="_blank"
              >GitHub page</a> for instructions and get right to it!
            </p>
            <p>
              Or have you been building Fusion-OS unofficially for some time now and want to become a maintainer? Fill out
              <a
                href="https://t.me/TheCloverly"
                class="font-semibold text-p-yellow"
                target="_blank"
              >this form</a> and we’ll see what we can do!
            </p>
          </DevCard>
        </div>
      </div>
      <div class="bottom-0 w-full bg-blue-900  p-absolute md:h-10 lg:h-12">
        <ul
          class="h-full py-4 pl-5 text-left md:p-0 text-p-black md:items-center md:inline-flex md:flex text-2xs lg:text-xs xl:text-sm"
        >
          <li class="px-1 pb-1 md:pb-0 lg:pr-2 hover:text-p-yellow">
            <a href="https://github.com/iamthecloverly" target="_blank">Website created by SriBalaji</a>
            </li>
          <li class="px-1 py-1 md:py-0 lg:px-2 hover:text-p-yellow">
            <a href="https://t.me/fusionos" target="_blank">Our Telegram channel</a>
          </li>
          <li class="px-1 py-1 md:py-0 lg:px-2 hover:text-p-yellow">
            <a href="https://github.com/Fusion-OS/" target="_blank">Our GitHub</a>
          </li>
          <li class="px-1 py-1 md:py-0 lg:px-2 hover:text-p-yellow">
            <a href="#" target="_blank">View source code</a>
          </li>
          <li class="pt-1 pl-1 md:pt-0 lg:pl-2">© 2021 FusionOS (An Andriod Open Source Project)</li>
        </ul>
      </div>
      <img
        src="../assets/img/k2.png"
        style
        class="top-0 left-0 hidden w-40 p-absolute md:block"
      />
    </section>
  </full-page>
</template>

<script>
import NavBar from "~/components/nav-bar"
import TeamCard from "~/components/team-card";
import DevCard from "~/components/dev-card";
import UserDevCardMobile from "~/components/user-dev-card-mobile";
import DevDevCardMobile from "~/components/dev-dev-card-mobile";
export default {
  data() {
    return {
      options: {
        licenseKey: "&X18O?Q$d9",
        anchors: ["home", "features", "team", "changelog", "download"],
        sectionsColor: ["#ffffff", "#4285f4", "#db4437", "#ffffff", "#4285f4"],
        navigation: true,
        scrollingSpeed: 750,
        navigationPosition: "left",
        autoScrolling: true,
        fitToSection: false,
        recordHistory: false,
        lockAnchors: true
      }
    };
  },
  beforeDestroy() {
    if (typeof window !== "undefined") {
      window.removeEventListener("resize", this.onResize, { passive: true });
    }
  },
  mounted() {
    this.onResize();
    window.addEventListener("resize", this.onResize, { passive: true });
  },
  methods: {
    onResize() {
      this.options.navigation = window.innerWidth > 768;
      if (window.innerWidth < 768 || window.innerHeight < 800)
        this.options.autoScrolling = false;
      else
        this.options.autoScrolling = true;
    }
  },
  components: {
    NavBar,
    TeamCard,
    DevCard,
    UserDevCardMobile,
    DevDevCardMobile
  }
};
</script>

<style>

@media (min-width: 1920px) {
  .max-text-4xl {
    font-size: 2.5rem !important;
  } 
}
</style>
