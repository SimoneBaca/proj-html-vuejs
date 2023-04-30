<template>
    <!-- Leading Organisations -->
    <div class="lead-organisations">

        <h2 class="marketing-title">Marketing Resources:Insider Advice on How to increase Online Sales
             <a class="marketing-button" href="#">
                Explore all Resources
            </a>
             </h2>
        <div class="organisation-col">

            <!-- Singol Card -->
            <div v-for="(organisation, index) in organisation" :key="index" class="single-card">

                <!-- Imagine -->
                <img :src="organisation.thumb" :alt="organisation.alt">

                <!-- Title -->
                <h3>{{ organisation.title }}</h3>

                <!-- Benefits -->
                <div>{{ organisation.benefit }}</div>
                <span>{{ organisation.subBenefit }}</span>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    name: "MarketingResources",
    data: function () {
        return {
            organisation: [
                {

                    alt: 'thumb organisation',
                    title: 'Marketing Tips and Tricks For your Website',

                },
                {

                    alt: 'thumb organisation',
                    title: 'How to Write Stunning Blog Post Titles',

                },
                {

                    alt: 'thumb organisation',
                    title: 'Techniques to Reduce Facebook Ads Spend',

                },
            ]
        }
    }
}
</script>


<style lang="scss" scoped>
@import '../style/variable.scss';


.lead-organisations {
    text-align: left;

    .organisation-col {
        display: flex;
        justify-content: space-around;

        .single-card {
            padding-top: 100px;
            text-align: left;
            width: 300px;

            h3 {
                font-size: 20px;

            }

            h3::after {
                content: "";
                margin-top: 20px;
                width: 100%;
                display: block;
            }

            div {
                font-size: 25px;
                font-weight: bold;
            }

            span {
                font-size: 18px;
            }
        }
    }

    .marketing-title {
        font-size: 40px;
        width: 600px;
        padding: 2rem;
        margin-left: 35px;

    }

    .marketing-button {
        background-color: $primary-color;
        color: white;
        padding: 15px 35px;
        border-radius: 8px;
        font-size: 15px;
        margin-right: 20px;

    }
}
</style>