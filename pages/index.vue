<template>
  <div class="lyt-Content">
    <section class="smpl-Hero">
      <div class="smpl-Hero_Inner">
        <div class="smpl-Hero_Body">
          <h1 class="smpl-Hero_Title">products</h1>
        </div>
      </div>
    </section>

    <div class="flt-Filters">
      <div class="flt-Filters_Inner">
        <div class="flt-Filters_Body">
          <ul class="flt-Filters_Items">
            <li class="flt-Filters_Item"
                v-for="filter in filters">
              <button @click="clickFilter(filter)" class="flt-Filters_Button">{{ filter }}</button>
            </li>
          </ul>
        </div>
      </div>
    </div>

    <div class="lst-List">
      <div class="lst-List_Inner">
        <div class="lst-List_Body">
          <ul class="lst-List_Items">
            <li class="lst-List_Item"
                v-for="(product, index) in products"
                :key="product.id">
              <div class="prd-Card">
                <div class="prd-Card_ImageContainer">
                  <img alt="product image" :src="product.image" class="prd-Card_Image">
                </div>

                <div class="prd-Card_Content">
                  <div class="prd-Card_Prices">
                    <p class="prd-Card_Price prd-Card_Price-original">£{{ Math.round(product.original_price) }}</p>
                    <p class="prd-Card_Price prd-Card_Price-final">£{{ Math.round(product.final_price) }}</p>
                  </div>
                  <h4 class="prd-Card_Title">{{ product.first_header_cart }}</h4>
                  <p class="prd-Card_Text">{{ product.second_header_cart }}</p>

                  <button class="prd-Card_Button">Add to cart</button>
                </div>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import axios from 'axios'

  export default {
    data() {
      return {
        activeClass: 'active',
        activeFilter: 'all',
        currency: '£',
        filters: [
          'all',
          'color',
          'size',
          'tog'
        ]
      }
    },

    asyncData ({ params }) {
      return axios.get('http://localhost:3000/data.json')
        .then((res) => {
          return { products: res.data.data }
        }).catch(err => console.log(err))
    },

    methods: {
      clickFilter (type) {
        console.log(type)
      }
    }
  }
</script>
