<template>
  <div>
    <nav :class="[isSticky ? stickyClass : '']">
      <div class="navigation-top">
        <div class="container">
          <ul>
            <li>เกี่ยวกับ Foremost</li>
            <li>สำหรับเกษตรโคนม</li>
          </ul>
        </div>
      </div>
      <div class="navigation-bottom mobile">
        <input type="checkbox" name="" id="menu-toggle" />
        <label for="menu-toggle" @click="handleToggleMenu"
          ><span></span><span></span><span></span
        ></label>
        <nuxt-link to="#">
          <img :src="logo" class="logo" alt="" srcset="" />
        </nuxt-link>
        <button>
          <nuxt-link to="#">
            <img :src="cart" alt="" srcset="" />
          </nuxt-link>
        </button>
      </div>
      <div class="navigation-bottom desktop">
        <div class="container">
          <!-- <div> -->
          <nuxt-link to="/">
            <img :src="logo" alt="" srcset="" class="logo" />
          </nuxt-link>
          <!-- </div>
          <div> -->
          <div class="wrapper-link">
            <ul>
              <li><nuxt-link to="#">หน้าแรก</nuxt-link></li>
              <li @click="handleToggleProduct()">
                <nuxt-link to="#" class="drop-down">สินค้าทั้งหมด</nuxt-link>
                <!-- :style="{ left: '30%' }" -->
                <ul
                  :class="[
                    isToggleProduct
                      ? 'toggle all-product active'
                      : 'toggle all-product',
                  ]"
                >
                  <li><nuxt-link to="#">แบรนด์โฟร์โมสต์</nuxt-link></li>
                  <li><nuxt-link to="#">ประเภทของนม</nuxt-link></li>
                  <li><nuxt-link to="#">คุณประโยชน์</nuxt-link></li>
                </ul>
              </li>
              <li @click="handleTogglePromotion()">
                <nuxt-link to="#" class="drop-down"
                  >โปรโมชั่นและร้านค้า</nuxt-link
                >
                <ul
                  :class="[
                    isTogglePromotion
                      ? 'toggle promotion active'
                      : 'toggle promotion',
                  ]"
                >
                  <li><nuxt-link to="#">โปรโมชั่น</nuxt-link></li>
                  <li><nuxt-link to="#">ร้านค้าออนไลน์</nuxt-link></li>
                </ul>
              </li>
              <li><nuxt-link to="#">กิจกรรม</nuxt-link></li>
              <li><nuxt-link to="#">แหล่งความรู้</nuxt-link></li>
            </ul>
          </div>
          <!-- </div>
          <div> -->
          <button-general name="สั่งซื้อออนไลน์" :shadow="false" />
          <!-- </div> -->
        </div>
      </div>

      <div :class="[isMenuActive ? 'menu active' : 'menu']">
        <ul>
          <li><nuxt-link to="#">หน้าแรก</nuxt-link></li>
          <li @click="handleToggleProduct()">
            <nuxt-link to="#" class="drop-down">สินค้าทั้งหมด</nuxt-link>
            <!-- :style="{ left: '30%' }" -->
            <ul
              :class="[
                isToggleProduct
                  ? 'toggle all-product active'
                  : 'toggle all-product',
              ]"
            >
              <li><nuxt-link to="#">แบรนด์โฟร์โมสต์</nuxt-link></li>
              <li><nuxt-link to="#">ประเภทของนม</nuxt-link></li>
              <li><nuxt-link to="#">คุณประโยชน์</nuxt-link></li>
            </ul>
          </li>
          <li @click="handleTogglePromotion()">
            <nuxt-link to="#" class="drop-down">โปรโมชั่นและร้านค้า</nuxt-link>
            <ul
              :class="[
                isTogglePromotion
                  ? 'toggle promotion active'
                  : 'toggle promotion',
              ]"
            >
              <li><nuxt-link to="#">โปรโมชั่น</nuxt-link></li>
              <li><nuxt-link to="#">ร้านค้าออนไลน์</nuxt-link></li>
            </ul>
          </li>
          <li><nuxt-link to="#">กิจกรรม</nuxt-link></li>
          <li><nuxt-link to="#">แหล่งความรู้</nuxt-link></li>
        </ul>
      </div>
    </nav>
    <section class="section-1">
      <!-- Desktop -->
      <img :src="banner" alt="" srcset="" class="banner-desktop" />
      <div class="wrapper-desktop">
        <img
          :src="imgNew"
          alt=""
          srcset=""
          class="img-new desktop"
          ref="imgNewRef"
        />
        <img
          :src="imgNew2"
          alt=""
          srcset=""
          class="img-foremost desktop"
          ref="foremostRef"
        />
        <img
          :src="imgNew3"
          alt=""
          srcset=""
          class="img-coffee desktop"
          ref="coffeeRef"
        />
        <img
          :src="imgTagline"
          alt=""
          srcset=""
          class="img-tagline desktop"
          ref="taglineRef"
        />
      </div>

      <!-- Mobile -->
      <img :src="bannerMobile" alt="" srcset="" class="banner-mobile" />
    </section>
    <section class="section-2">
      <div class="container">
        <div class="wrapper-container">
          <h1 ref="text1Ref">
            รู้หรือไม่...กลิ่นหอมของกาแฟ จะช่วยให้ร่างกายรู้สึกสดชื่นขึ้น?
          </h1>
          <h1 class="white" ref="text2Ref">หากคุณรู้สึก</h1>
          <div class="wrapper">
            <ul class="container-btn" ref="listsRef">
              <li><nuxt-link to="#">ง่วงนอนทุกเช้า</nuxt-link></li>
              <li><nuxt-link to="#">สมองไม่แล่นเมื่อต้องประชุม</nuxt-link></li>
              <li><nuxt-link to="#">รู้สึกไม่สดใสยามบ่าย</nuxt-link></li>
            </ul>
          </div>
          <h1 ref="text3Ref">
            ใหม่ โฟร์โมสต์ คอฟฟี่ ลาเต้ ผสานกาแฟโรบัสต้าและนมโคคุณภาพ
          </h1>
        </div>

        <!-- Desktop -->
        <img
          :src="splashDesktop"
          alt=""
          srcset=""
          class="desktop splash"
          ref="splashDesktopRef"
        />
        <img
          :src="milkDesktop"
          alt=""
          srcset=""
          class="desktop milk"
          ref="milkDesktopRef"
        />
        <img
          :src="imgSmellGood"
          alt=""
          srcset=""
          class="smellgood"
          ref="smellGoodRef"
        />

        <!-- Mobile -->
        <img
          :src="splashMobile"
          alt=""
          srcset=""
          class="mobile splash"
          ref="splashMobileRef"
        />
        <img
          :src="milkMobile"
          alt=""
          srcset=""
          class="mobile milk"
          ref="milkMobileRef"
        />
      </div>
    </section>
    <section class="section-3">
      <div class="container">
        <div class="wrapper-tagline">
          <img
            src="~/assets/image/title-3.png"
            alt=""
            srcset=""
            ref="title3Ref"
          />
        </div>
        <div class="wrapper-circle" ref="circleRef">
          <div class="container-circle circle coffee-2">
            <img src="~/assets/image/circle-1.png" alt="" srcset="" />
          </div>
          <div class="container-circle circle coffee-1">
            <img src="~/assets/image/circle-2.png" alt="" srcset="" />
          </div>
          <div class="container-circle circle coffee-3">
            <img src="~/assets/image/circle-3.png" alt="" srcset="" />
          </div>
        </div>
        <img
          src="~/assets/image/coffee-bg-desktop-1.png"
          alt=""
          srcset=""
          class="splash-desktop"
        />
        <div class="container-video-1">
          <div class="wrapper-iframe video-1" ref="video1Ref">
            <iframe
              src="https://www.youtube.com/embed/DKZvfQnnytk"
              title="YouTube video player"
              frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
            ></iframe>
          </div>
        </div>
        <div class="wrapper-btn" ref="btnRef">
          <button-capsule
            v-for="item in dataButton"
            :key="item.id"
            :img="item.img"
            :title="item.title"
            :text="item.text"
            @click.native="handleCopy(item.title, item.text)"
          />
        </div>
        <div class="container-video">
          <div class="wrapper-iframe" ref="video2Ref">
            <iframe
              src="https://www.youtube.com/embed/DKZvfQnnytk"
              title="YouTube video player"
              frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
            ></iframe>
          </div>
        </div>

        <div class="container-wrapper">
          <div class="wrapper" ref="clickRef">
            <img src="~/assets/image/title-online.png" alt="" srcset="" />
            <button-general name="คลิกเลย!" :shadow="true" />
          </div>
          <div class="wrapper-row" ref="badgeRef">
            <div class="row">
              <badge
                v-for="item in clientsTop"
                :key="item.id"
                :img="item.img"
                :link="item.link"
                :position="item.position"
              />
            </div>
            <div class="row">
              <badge
                v-for="item in clientsBottom"
                :key="item.id"
                :img="item.img"
                :link="item.link"
                :size="item.size"
              />
            </div>
          </div>
        </div>
      </div>
      <img
        src="~/assets/image/coffee-bg-desktop-2.png"
        alt=""
        srcset=""
        class="coffee-bg-desktop"
      />
    </section>
  </div>
</template>

<script>
// Images
import banner from "~/assets/image/banner-plain.jpg";
import bannerMobile from "~/assets/image/banner-mobile-plain.png";
import logo from "~/assets/image/logo.png";
import cart from "~/assets/image/icon-cart.png";
// section 2 img
import milkMobile from "~/assets/image/milk-mobile.png";
import splashMobile from "~/assets/image/splash-mobile.png";
import splashDesktop from "~/assets/image/splash-desktop.png";
import milkDesktop from "~/assets/image/milk-desktop.png";
import imgSmellGood from "~/assets/image/title-2.png";

import imgNew from "~/assets/image/banner-text-1.png";
import imgNew2 from "~/assets/image/banner-text-2.png";
import imgNew3 from "~/assets/image/banner-text-3.png";
import imgTagline from "~/assets/image/tagline.png";

// Component
import Badge from "../components/Badge.vue";

// Library
import gsap from "gsap";
import ScrollTrigger from "gsap/dist/ScrollTrigger";
import Vue from "vue";
import VueClipboard from "vue-clipboard2";

Vue.use(VueClipboard);
gsap.registerPlugin(ScrollTrigger);

export default {
  components: { Badge },
  data() {
    return {
      bannerMobile,
      banner,
      imgNew,
      imgNew2,
      imgNew3,
      imgTagline,
      milkMobile,
      splashMobile,
      splashDesktop,
      milkDesktop,
      imgSmellGood,
      cart,
      logo,
      isToggleProduct: false,
      isTogglePromotion: false,
      isMenuActive: false,
      dataButton: [
        {
          id: 1,
          img: "cap-1.png",
          title: "ขยับร่างกายระหว่างวัน",
          text: `ลุกหรือเดินทุก 2 ชม.
          เพื่อให้ระบบไหลเวียนเลือด 
          ทำงานได้ดี`,
        },
        {
          id: 2,
          img: "cap-2.png",
          title: "ฟังเพลงสบายๆ",
          text: `หันมาฟังเพลงคลาสสิค 
          หรือเสียงธรรมชาติ 
          ช่วยให้ผ่อนคลายมากขึ้น`,
        },
        {
          id: 3,
          img: "cap-3.png",
          title: "พักสายตาเป็นระยะ",
          text: `เลี่ยงจากหน้าจอคอมฯ 
          หยุดพักสายตาครั้งละ 15 นาที 
          ทุก 2 ชม.`,
        },
        {
          id: 4,
          img: "cap-4.png",
          title: `เติมพลังความสดชื่น 
          ด้วยความหอมของกาแฟ`,
          text: `ดื่มด่ำความหอมและรสชาติกาแฟ 
          พร้อมประโยชน์ของนม ให้ความสดชื่น
          และได้ประโยชน์ทั้งวัน`,
        },
      ],

      clientsTop: [
        { id: 1, img: "logo-lazada.png", link: "#" },
        { id: 2, img: "logo-shopee.png", link: "#" },
        { id: 3, img: "logo-jd.png", link: "#", position: "50% 20%" },
      ],

      clientsBottom: [
        { id: 1, img: "logo-bigc.png", link: "#", size: "50%" },
        { id: 2, img: "logo-makro.png", link: "#" },
        { id: 3, img: "logo-lotus.png", link: "#" },
        { id: 4, img: "logo-tops.jpeg", link: "#" },
      ],

      isSticky: false,
      stickyClass: "is_sticky",
      code: "vueIsBetterThanPBJ",
      supportsCB: false,
      message: "",
    };
  },
  //   created() {
  //     if(navigator.clipboard) {
  //       this.supportsCB = true;
  //     }
  //   },
  methods: {
    handleToggleProduct() {
      this.isToggleProduct = !this.isToggleProduct;
      this.isTogglePromotion = false;
    },
    handleTogglePromotion() {
      this.isTogglePromotion = !this.isTogglePromotion;
      this.isToggleProduct = false;
    },
    handleScroll() {
      this.scrollPosition = window.scrollY;
    },

    handleCopy(title, text) {
      let tmp = title + " " + text;
      console.log(tmp);
      this.$copyText(tmp).then(
        function (e) {
          alert("Copied");
          console.log(e);
        },
        function (e) {
          alert("Can not copy");
          console.log(e);
        }
      );
    },
    handleToggleMenu() {
      this.isMenuActive = !this.isMenuActive;
      console.log(this.isMenuActive);
    },
  },
  async mounted() {
    window.addEventListener("scroll", () => {
      if (window.innerWidth > 768 && window.scrollY > 31) {
        this.isSticky = true;
      } else {
        this.isSticky = false;
      }
    });

    // Animation
    // gsap.from()
    await this.$nextTick(() => {
      // banner
      gsap
        .timeline()
        .from(this.$refs.imgNewRef, {
          duration: 0.6,
          opacity: 0,
          x: -50,
          ease: "circ.inOut",
        })
        .from(this.$refs.foremostRef, {
          delay: 0.2,
          duration: 0.8,
          opacity: 0,
          x: -50,
          ease: "circ.inOut",
        })
        .from(
          this.$refs.coffeeRef,
          {
            duration: 0.8,
            opacity: 0,
            x: 50,
            ease: "circ.inOut",
          },
          "-=.8"
        )
        .from(this.$refs.taglineRef, {
          duration: 2,
          opacity: 0,
          y: -50,
          ease: "elastic.inOut(1,0.3)",
        })
        .from(this.$refs.taglineRef, {
          delay: 0.4,
          duration: 1.2,
          y: 0,
          yoyo: true,
          repeat: -1,
          ease: "bounce.in",
        });

      // section 2
      const tl2 = gsap.timeline({
        scrollTrigger: {
          trigger: this.$refs.listsRef,
          start: "top 70%",
          //   markers: true,
        },
      });

      tl2
        .from(this.$refs.text1Ref, {
          duration: 0.8,
          opacity: 0,
          y: 50,
          ease: "circ.inOut",
        })
        .from(
          this.$refs.text2Ref,
          {
            duration: 0.8,
            opacity: 0,
            // y: 50,
            ease: "circ.in",
          },
          "-=0.4"
        )
        .from(this.$refs.listsRef.querySelectorAll("li"), {
          duration: 1.6,
          stagger: 0.4,
          opacity: 0,
          y: 50,
          ease: "bounce.out",
        })
        .from(
          this.$refs.text3Ref,
          {
            duration: 0.8,
            opacity: 0,
            x: 50,
            ease: "circ.out",
          },
          "-=0.4"
        );

      if (window.innerWidth > 992) {
        const bgTimeline = gsap.timeline({
          scrollTrigger: {
            trigger: this.$refs.splashDesktopRef,
            start: "top 30%",
            //   markers: true,
          },
        });
        bgTimeline
          .from(
            this.$refs.splashDesktopRef,
            {
              duration: 0.8,
              opacity: 0,
              x: -50,
              ease: "circ.out",
            },
            "-=0.4"
          )
          .from(
            this.$refs.milkDesktopRef,
            {
              duration: 0.8,
              opacity: 0,
              scale: 1.2,
              ease: "circ.out",
            },
            "-=0.4"
          )
          .from(
            this.$refs.smellGoodRef,
            {
              duration: 2,
              opacity: 0,
              scale: 0.7,
              ease: "elastic.inOut(1,0.3)",
            },
            "-=0.4"
          );
      } else {
        const bgTimeline = gsap.timeline({
          scrollTrigger: {
            trigger: this.$refs.splashDesktopRef,
            start: "top center",
            //   markers: true,
          },
        });
        bgTimeline
          .from(
            this.$refs.splashMobileRef,
            {
              duration: 0.8,
              opacity: 0,
              x: -50,
              ease: "circ.out",
            },
            "-=0.4"
          )
          .from(
            this.$refs.milkMobileRef,
            {
              duration: 0.8,
              opacity: 0,
              scale: 1.2,
              ease: "circ.out",
            },
            "-=0.4"
          )
          .from(
            this.$refs.smellGoodRef,
            {
              duration: 2,
              opacity: 0,
              scale: 0.7,
              ease: "elastic.inOut(1,0.3)",
            },
            "-=0.4"
          );
      }

      //   section 3
      const tl3 = gsap.timeline({
        scrollTrigger: {
          trigger: this.$refs.title3Ref,
          start: "top center",
          //   markers: true,
        },
      });

      tl3.from(this.$refs.title3Ref, {
        duration: 0.8,
        opacity: 0,
        scale: 0.7,
        ease: "bounce.out",
      });

      const circleTl = gsap.timeline({
        scrollTrigger: {
          trigger: this.$refs.circleRef,
          start: "top center",
          //   markers: true,
        },
      });

      circleTl.from(
        this.$refs.circleRef.querySelectorAll(".container-circle"),
        {
          duration: 0.6,
          scale: 0.8,
          opacity: 0,
          stagger: 0.4,
          ease: "circ.inOut",
        }
      );
    });

    const video1Tl = gsap.timeline({
      scrollTrigger: {
        trigger: this.$refs.video1Ref,
        start: "top center",
        // markers: true,
      },
    });

    video1Tl.from(this.$refs.video1Ref, {
      duration: 1,
      scale: 0.8,
      opacity: 0,
      ease: "bounce.out",
    });

    const btnTl = gsap.timeline({
      scrollTrigger: {
        trigger: this.$refs.btnRef,
        start: "top center",
        // markers: true,
      },
    });

    btnTl.from(this.$refs.btnRef.querySelectorAll(".button-capsule"), {
      duration: 0.6,
      scale: 0.8,
      opacity: 0,
      stagger: 0.2,
      ease: "circ.inOut",
    });

    const video2Tl = gsap.timeline({
      scrollTrigger: {
        trigger: this.$refs.video2Ref,
        start: "top center",
        // markers: true,
      },
    });

    video2Tl.from(this.$refs.video2Ref, {
      duration: 1,
      scale: 1.2,
      opacity: 0,
      ease: "bounce.out",
    });

    const clickTl = gsap.timeline({
      scrollTrigger: {
        trigger: this.$refs.clickRef,
        start: "top center",
        // markers: true,
      },
    });

    clickTl.from(this.$refs.clickRef, {
      duration: 0.6,
      scale: 0.8,
      opacity: 0,
      ease: "circ.inOut",
    });

    const badgeTl = gsap.timeline({
      scrollTrigger: {
        trigger: this.$refs.badgeRef,
        start: "top center",
        // markers: true,
      },
    });
    badgeTl.from(this.$refs.badgeRef.querySelectorAll(".badge"), {
      duration: 0.6,
      scale: 0.8,
      //   stagger: .2,
      opacity: 0,
      ease: "circ.inOut",
    });
    // console.log(this.$refs.badgeRef.querySelectorAll(".badge"));
  },
};
</script>