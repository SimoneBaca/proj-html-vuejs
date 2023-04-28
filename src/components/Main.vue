<script>
import SingleRowBenefit from "./SingleRowBenefit.vue";
import BrandsWeWork from "./BrandsWeWork.vue";

export default {
  name: "Main", 
  components: {
    SingleRowBenefit,
    BrandsWeWork,
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
        ]
    }
  }
}
</script>


<template>
    <main class="container">

<SingleRowBenefit v-for="(benefits, index) in benefits" :key="index" :benefitsArray="benefits" />
<BrandsWeWork />
</main>
</template>

<style lang="scss" scoped>
</style>