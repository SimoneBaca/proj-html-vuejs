<template>
     <div class="container brands-area">

        <h2 class="title-section">Some Brands We Work With</h2>
        <p class="p-section">Quisque aliquet, libero consequat elementum convallis</p>
       
        <ul class="brands-list">
            <li v-for="(brands, index) in brands" :key="index">
                <img :src="brands.thumb" :alt="brands.alt">
            </li>
        </ul>
    </div>
</template>


<script>
export default {
    name: "BrandsWeWork", 
    data: function() {
        return {
            brands: [
                {
                    name: 'abstract',
                    alt: 'logo abstract'
                },
                {
                    name: 'cglobal',
                    alt: 'logo cglobal'
                },
                {
                    name: 'next',
                    alt: 'logo next'
                },
                {
                    name: 'hemisferio',
                    alt: 'logo hemisferio'
                },
                {
                    name: 'spaces',
                    alt: 'logo spaces'
                },
                {
                    name: 'digitalbox',
                    alt: 'logo digitalbox'
                }
            ]
        }
    }
}
</script>


<style lang="scss" scoped>
@import '../style/commons.scss';
.brands-area {
    padding-top: 200px;
    text-align: center;

    p {
        padding-top: 20px;
    }
    ul {
        padding-top: 60px;
        display: flex;
        justify-content: center;
        li {
            padding: 0 30px;
            img {
                width: 140px;
            }
        }
    }
}
</style>