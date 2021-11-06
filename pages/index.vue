<template>
  <div>
    <nav>
      <div class="navigation-top">
        <div class="container">
          <ul>
            <li>เกี่ยวกับ Foremost</li>
            <li>สำหรับเกษตรโคนม</li>
          </ul>
        </div>
      </div>
      <div class="navigation-bottom mobile">
        <label for=""><span></span><span></span><span></span></label>
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
              <li><nuxt-link to="#">สินค้าทั้งหมด</nuxt-link></li>
              <li><nuxt-link to="#">โปรโมชั่นและร้านค้า</nuxt-link></li>
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
    </nav>
    <section class="banner">
      <img :src="banner" alt="" srcset="" class="banner-desktop" />
      <img :src="bannerMobile" alt="" srcset="" class="banner-mobile" />
    </section>
    <section class="middle">
      <div class="container">
        <div class="wrapper-container">
          <h1>
            รู้หรือไม่...กลิ่นหอมของกาแฟ จะช่วยให้ร่างกายรู้สึกสดชื่นขึ้น?
          </h1>
          <h1 class="white">หากคุณรู้สึก</h1>
          <div class="wrapper">
            <ul class="container-btn">
              <li><nuxt-link to="#">ง่วงนอนทุกเช้า</nuxt-link></li>
              <li><nuxt-link to="#">สมองไม่แล่นเมื่อต้องประชุม</nuxt-link></li>
              <li><nuxt-link to="#">รู้สึกไม่สดใสยามบ่าย</nuxt-link></li>
            </ul>
          </div>
          <h1>ใหม่ โฟร์โมสต์ คอฟฟี่ ลาเต้ ผสานกาแฟโรบัสต้าและนมโคคุณภาพ</h1>
        </div>
        <img :src="splashDesktop" alt="" srcset="" class="desktop splash" />
        <img :src="milkDesktop" alt="" srcset="" class="desktop milk" />
        <img :src="splashMobile" alt="" srcset="" class="mobile splash" />
        <img :src="milkMobile" alt="" srcset="" class="mobile milk" />
      </div>
    </section>
    <section class="section-3">
      <div class="container">
        <div class="wrapper-tagline">
          <img src="~/assets/image/title-3.png" alt="" srcset="" />
        </div>
        <div class="wrapper-circle">
          <img
            src="~/assets/image/circle-1.png"
            class="circle"
            alt=""
            srcset=""
          />
          <img
            src="~/assets/image/circle-2.png"
            class="circle"
            alt=""
            srcset=""
          />
          <img
            src="~/assets/image/circle-3.png"
            class="circle"
            alt=""
            srcset=""
          />
        </div>
        <img
          src="~/assets/image/coffee-bg-desktop-1.png"
          alt=""
          srcset=""
          class="splash-desktop"
        />
        <div class="container-video-1">
          <div class="wrapper-iframe video-1">
            <iframe
              src="https://www.youtube.com/embed/DKZvfQnnytk"
              title="YouTube video player"
              frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
            ></iframe>
          </div>
        </div>
        <div class="wrapper-btn">
          <button-capsule
            v-for="item in dataButton"
            :key="item.id"
            :img="item.img"
            :title="item.title"
            :text="item.text"
          />
        </div>
        <div class="container-video">
          <div class="wrapper-iframe">
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
          <div class="wrapper">
            <img src="~/assets/image/title-online.png" alt="" srcset="" />
            <button-general name="คลิกเลย!" :shadow="true" />
          </div>
          <div class="wrapper-row">
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
import banner from "~/assets/image/banner.jpg";
import bannerMobile from "~/assets/image/banner-mobile.png";
import logo from "~/assets/image/logo.png";
import cart from "~/assets/image/icon-cart.png";
import milkMobile from "~/assets/image/milk-mobile.png";
import splashMobile from "~/assets/image/splash-mobile.png";
import splashDesktop from "~/assets/image/splash-desktop.png";
import milkDesktop from "~/assets/image/milk-desktop.png";

import imgNew from "~/assets/image/banner-text-1.png";
import imgNew2 from "~/assets/image/banner-text-2.png";
import imgNew3 from "~/assets/image/banner-text-3.png";

import Badge from "../components/Badge.vue";
export default {
  components: { Badge },
  data() {
    return {
      bannerMobile,
      banner,
      imgNew,
      imgNew2,
      imgNew3,
      milkMobile,
      splashMobile,
      splashDesktop,
      milkDesktop,
      cart,
      logo,
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
    };
  },
};
</script>