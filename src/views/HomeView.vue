<template>
  <v-app id="home">
    <!-- Sayfanın header kısmı -->
    <NavBar/>
    <v-container fluid>
    <!-- Safanın en üst kısmı head  -->
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative" class="mt-16">
              <h1 class="text-grey">Merhaba,</h1>
              <h1 class="text-white">Benim Adım Hatice</h1>
              <span class="text-grey">Mobile Developer</span><br />

              <v-btn tile dark class="text-purple mt-8" variant="outlined">
                İletişime Geç
              </v-btn>
            </div>
          </v-col>
          <v-col cols="2">
            <div
              style="
                position: absolute;
                z-index: 9999;
                bottom: 0;
                margin-left: auto;
                margin-right: auto;
                left: 0;
                right: 0;
                text-align: center;
              "
              class="mt-16"
              >
              <v-icon>fas fa-angle-double-down</v-icon>
            </div>
          </v-col>
          <v-col cols="5">
            <div style="position: relative; z-index: 9999" class="mt-16">
              <v-img src='assets\mobile-dev.png' contain max-height="300"/>
            </div>
          </v-col>
        </v-row>
      </div> 
      <!-- Hakkımda kolunu -->
      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class="egg">
              <v-img src='assets\mobile-dev.png' contain max-height="300"/>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h1>Hakkımda</h1><br>
              <div style="width: 120px;"> </div>
              <h4 class="mt-n4"> Mobile Uygulama Geliştiricisi</h4>
              <p class="text-grey">Lorem Ipsum is simply dummy text of the printing and typesetting industry.
                 Lorem Ipsum has been the industry</p> 
                 <p class="text-grey">Lorem Ipsum is simply dummy text of the printing and typesetting industry.
                 Lorem Ipsum has been the industry Lorem Ipsum is simply dummy text of the printing and typesetting industry.
                 Lorem Ipsum has been the industr</p>
                 <v-btn tile dark class="text-purple mt-8" variant="outlined">
                Devamını yükle
              </v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <!-- Liste şeklinde cartlerın bulunduğu kısım -->
      <v-col cols="12" class="imgHover">
        <v-row class="fill-height" align="center" justify="center">
          <template v-for="(item, i) in items" :key="i">
            <v-col cols="12" md="4">
              <v-hover v-slot="{ isHovering, props }">
                <v-card
                  :elevation="isHovering ? 12 : 2"
                  :class="{ 'on-hover': isHovering }"
                  v-bind="props"
                >
                  <v-img :src="item.img" height="225px" cover> </v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
      </v-col> 
      <!-- <div class="text-center mt-4">
        <h1> Ne Yapıyorum</h1>
              <v-img src='assets\mobile-dev.png' contain max-height="300"/>
     </div>
     <v-col cols="12" id="services"> 
              <div class="d-flex justify-center mb-6"> 
                 <v-btn tile dark class="text-purple mt-8" > Tümü </v-btn>
                 <v-btn tile dark class="text-purple mt-8" variant="tonal"> Web Tasarım </v-btn>
                 <v-btn tile dark class="text-purple mt-8" variant="tonal"> Fotoğraflar </v-btn>
                 <v-btn tile dark class="text-purple mt-8" variant="tonal"> Mobil Tasarım</v-btn> 
            </div>
       </v-col>
       <v-col cols="12" id="imgHover"> 
        <v-row class="fill-height" align="center" justify="center"> 
              <template  v-for="(item,i) in items" :key="i" > 
                <v-col cols="12" md="4"> 
              <v-hover v-slot="{ isHovering,props } ">  
                 <v-card   :elevation="isHovering?12:2" :class="{ 'on-hover':isHovering } " v-bind="props"> 
                  <v-img src="item.img" height="225px" cover/>
                 </v-card> 
              </v-hover>
          </v-col>
          </template>
        </v-row>
        </v-col> -->
        <v-col cols="12" sm="12"> 
          <div class="d-flex justify-center mb-6"> 
                 <v-btn tile dark class="text-purple mt-8" variant="outlined"> DAha Fazla </v-btn> 
            </div>
        </v-col>
        <v-col cols="12" id="biog">
        <div class="hire">
          <v-row>
            <v-col cols="12" sm="8">
              <h1 class="mt-9">Hire me for your awesome project</h1>
              <p class="text-grey">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Quod
                itaque, eaque molestiae deleniti, earum voluptate eos id dicta
                at, blanditiis
              </p>
            </v-col>
            <v-col cols="12" sm="4">
              <v-btn color="#FBDF7E" class="mt-15">Hire Me</v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
      
        <!-- Sayfanın en alt kısmında yer alan konum telefon mail form ksımının bulunduğu containerı -->
        <v-col cols="12" sm="12" class="px-16" id="contact">
        <v-row>
          <v-col cols="12" sm="4">
            <div class="child">
              <h1>Contact info.</h1>
              <v-btn
                icon="fas fa-map-marker-alt"
                color=""
                class="mt-10"
                variant="outlined"
              ></v-btn
              ><br />
              <span class="text-caption">Your Street SYO,yourArea Dream </span
              ><br />
              <v-btn
                icon="fas fa-phone-alt"
                color=""
                class="mt-10"
                variant="outlined"
              ></v-btn
              ><br />
              <span class="text-caption">00235 - 6521 </span> <br />
              <span class="text-caption">00235 - 6521 </span> <br />
              <v-btn
                icon="fas fa-envelope"
                color=""
                class="mt-10"
                variant="outlined"
              ></v-btn
              ><br />
              <span class="text-caption">aaeideapro@gmail.com </span> <br />
              <span class="text-caption">aaeideapro@gmail.com </span> <br />
            </div>
          </v-col>
          <v-col cols="12" sm="8">
            <h1 class="mt-8">Send your message</h1>
            <v-divider></v-divider>
            <span class="text-caption"
              >Lorem ipsum dolor sit amet consectetur adipisicing elit. Sunt
              fugiat officia, odio eaque exercitationem libero nesciunt placeat,
              repellat obcaecati sed tenetur! Est labore aliquam amet
              consequatur necessitatibus fugit obcaecati facilis!</span
            >
            <v-row class="mt-10">
              <v-col cols="12" sm="6">
                <v-text-field
                  label="Name"
                  persistent-hint
                  variant="outlined"
                ></v-text-field>
              </v-col>
              <v-col cols="12" sm="6">
                <v-text-field
                  label="Phone No"
                  persistent-hint
                  variant="outlined"
                ></v-text-field>
              </v-col>
            </v-row>
            <v-textarea
              label="Message"
              persistent-hint
              variant="outlined"
            ></v-textarea>
            <v-btn tile dark class="text-purple mt-8" variant="outlined">
                Gönder
              </v-btn>
          </v-col>
        </v-row>
      </v-col>
    </v-container> 
    <!-- Footer componenti -->
    <FooterView />
  </v-app>
</template>

<script>
import { defineComponent } from 'vue';

// Components 
import NavBar from '@/components/NavBar.vue';
import FooterView from "../components/FooterView.vue";

export default defineComponent({
  name: 'HomeView',
  setup() {
    return {
      slider2: 50,

      items: [
        {
          img: "i3.jpg",
        },
        {
          img: "i4.jpg",
        },
        {
          img: "i5.jpg",
        },
        {
          img: "i6.jpeg",
        },
        {
          img: "i9.jpg",
        },
        {
          img: "i8.jpg",
        },
      ],
    };
  },
  components: { 
    NavBar,
    FooterView
  },
});
</script>
<style scoped >
.v-container {
  padding: 16px 0 16px 0;
}

.head {
  position: relative;
  text-align: center;
  padding: 12px;
  margin-bottom: 6px;
  height: 400px;
  width: 100%;
  color: white;
}
.head:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, 6deg);
}
.head:after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, -6deg);
}
.egg{
  display: block;
  margin-left: 100px;
  margin-top: 0x;
 width: 356px;
 height: 300px;
 background-color: rgb(226, 189, 246);
 border-radius:  50%  50%  50%  50%   /  60%  60%  40%   0% 

}

.first{
padding: 2rem 2rem;
text-align: center;
 width:  100%;
 height: 260px; 
}
.first{
padding: 2rem 2rem;
text-align: center;
 width:  100%;
 height: 260px; 
}

.child{
display: inline-block;
padding: 2rem 1rem;
vertical-align: middle;
text-align: center;
margin-right: 8px;
}

.imgHover{
padding: 0 200px;
}

.pre {
  width: 100%;
  height: 380px;
  text-align: center;
  padding: 0 200px;
  background-color: #f5f5f5;
}
.hire {
  width: 100%;
  height: 200px;
  padding: 0 200px;
  background-color: #e9e9e9;
  margin-top: -24px;
}
</style>