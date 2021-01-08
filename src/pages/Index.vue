<template>
  <q-page >
    <div class="heroImages">
      <!-- <q-img v-for="(image,index) in heroImages" :key="index" :src="image.imgaeURL" height="100vh">
        {{image.caption}}
      </q-img> -->
      <q-img src="../assets/heroImage/IMG_20210108_170406.jpg" height="95vh"></q-img>
      <div class="desc">

      <div class="title text-h3 text-center text-white">
        Our price are based on our talents, not your budget.
      </div>
      </div>
    </div>
          <div class="row justify-center">

      <div class=" self-center q-pa-lg">
        <div class="text-h3">
        Our services
        </div>
      </div>
      </div>
    <div class="row">

      <div class="col-3 q-pa-md" v-for="(i,index) in 4" :key="index">
      <q-img src="../assets/heroImage/IMG_20210108_170406.jpg" height="50vh"></q-img>

      </div>
    </div>

    <div class="row">
      <div class="col-6 q-pa-lg">
        <q-img src="../assets/heroImage/IMG_20210108_170406.jpg" height="50vh"></q-img>
      </div>
      <div class="col-6 q-pa-lg">
        <div class="text-h3">
          Tattoo
        </div>
        <div class="text-h5">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Iure velit quas magnam? Assumenda dolorum nemo nisi eius libero ipsa officiis dicta voluptatem ullam autem ab, debitis iste animi explicabo magni.
        </div>
        <q-btn size="medium" label="More Details" color="negative" no-caps></q-btn>
      </div>
    </div>
    <div class="row">
      
      <div class="col-6 q-pa-lg">
        <div class="text-h3">
          Wall painting
        </div>
        <div class="text-h5">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Iure velit quas magnam? Assumenda dolorum nemo nisi eius libero ipsa officiis dicta voluptatem ullam autem ab, debitis iste animi explicabo magni.
        </div>
        <q-btn size="medium" label="More Details" color="negative" no-caps></q-btn>
      </div>
      <div class="col-6 q-pa-lg">
        <q-img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRKdoftEq2hjSIf1zO3dY3djBqbPA2g0eZ8EQ&usqp=CAU" height="50vh"></q-img>
      </div>
    </div>
    <div class="row">
      
      <div class="col-6 q-pa-lg">
        <q-img src="data:image/jpeg;base64,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" height="50vh"></q-img>
      </div>
      <div class="col-6 q-pa-lg">
        <div class="text-h3">
          Wood carving
        </div>
        <div class="text-h5">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Iure velit quas magnam? Assumenda dolorum nemo nisi eius libero ipsa officiis dicta voluptatem ullam autem ab, debitis iste animi explicabo magni.
        </div>
        <q-btn size="medium" label="More Details" color="negative" no-caps></q-btn>
      </div>
    </div>
    <div class="row">
      
      
      <div class="col-6 q-pa-lg">
        <div class="text-h3">
          Customized design
        </div>
        <div class="text-h5">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Iure velit quas magnam? Assumenda dolorum nemo nisi eius libero ipsa officiis dicta voluptatem ullam autem ab, debitis iste animi explicabo magni.
        </div>
        <q-btn size="medium" label="More Details" color="negative" no-caps></q-btn>
      </div>
      <div class="col-6 q-pa-lg">
        <q-img src="https://cdn.shopify.com/s/files/1/1810/7857/products/airbrush-custom-paint-drip-shoes-airbrushbrothers-shoes-custom-spray-paint-design-shirt-hat-shoes-outfit-graffiti-t-shirts-birthday-90s-80s-custom-neon-drip-shoes-15299585310798_600x.jpg?v=1593993250" height="50vh"></q-img>
      </div>
    </div>

  </q-page>
</template>

<script>
import heroImages from '../util/imgUrl.js'

export default {
  name: 'PageIndex',
  data(){
    return{
      heroImages,
    }
  }
}
</script>

<style lang="scss">
.heroImages{
  position:relative;
  .desc{
    position:absolute;
    bottom:0%;
    width:100%;
    padding:25px;
    background: rgba($color: #000000, $alpha: 0.2);
  }
}

</style>