<script>
import SingleRowBenefit from "./SingleRowBenefit.vue";
import BrandsWeWork from "./BrandsWeWork.vue";
import Leads from "./Leads.vue";
import References from "./References.vue";
import Testimonial from "./Testimonial.vue";
import MarketingResources from "./MarketingResources.vue";
import ThingsHappen from "./ThingsHappen.vue";

export default {
  name: "Main", 
  components: {
    SingleRowBenefit,
    BrandsWeWork,
    Leads,
    References,
    Testimonial,
    MarketingResources,
    ThingsHappen,
  },
  data: function() {
    return {
        benefits: [
            {
             
                upTitle: 'Business Growth',
                title: 'Increase Brand Awareness',
                subTitle: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed auctor placerat luctus. Nullam sit amet ante sed orci convallis gravida et at massa.',
                button: 'Get a Consultation',
                isReverse: false
            },
            {
               
                upTitle: 'Investors In People',
                title: 'In-House Sales Training',
                subTitle: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed auctor placerat luctus. Nullam sit amet ante sed orci convallis gravida et at massa.',
                button: 'Get a Consultation',
                isReverse: true
            },
            {
                
                upTitle: 'Social Media Analysis',
                title: 'Harness Your Social Proof',
                subTitle: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed auctor placerat luctus. Nullam sit amet ante sed orci convallis gravida et at massa.',
                button: 'Get a Consultation',
                isReverse: false
            },
        ],
    }
  }
}
</script>


<template>
    <main>

<SingleRowBenefit v-for="(benefits, index) in benefits" :key="index" :benefitsArray="benefits" />
<BrandsWeWork />
<Leads />
<References/>
<Testimonial/>
<MarketingResources />
<ThingsHappen/>
</main>
</template>

<style lang="scss" scoped>
</style>