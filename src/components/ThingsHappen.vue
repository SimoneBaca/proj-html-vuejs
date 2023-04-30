<script>

import ExpertConsultant from "./Expertconsultant.vue";

export default {
    name: "Jumbotron",
    components: {
        ExpertConsultant,
    },
}
</script>

<template>
    <div class="jumbotron">
        <div class="container">
            <div class="content">
                <!-- Area Text -->
                <div class="area-text">
                    <h2>Let's Make Things Happen</h2>
                    <p>Curabitur ac leo nunc.Vestibulum et mauris vel ante finibus maximus nec ut leo.Integer consectetur.
                    </p>
                    <hr>
                    <p>"The team at Avada Marketing Consultant is fabulous.They helped us unlock our potential online and
                        offline. We have experienced year on year growth due to their progressive approach."</p>
                        <p>George Anderson</p>
                        <div class="ceo">Digitalbox CEO</div>
                       
                </div>
                <!-- Expert consultant -->
                <div class="expert-consultant">
                    <ExpertConsultant />
                </div>
            </div>
        </div>
    </div>
</template>
 
<style lang="scss" scoped>
@import '../style/variable.scss';

.jumbotron {
    background-color: black;
    background-repeat: no-repeat;
    background-position-y: top;
    background-size: cover;
    height: 700px;
    width: 100%;

    .content {
        padding-top: 120px;
        display: flex;
    }

    .area-text {
        color: white;
        width: 50%;

        h2 {
            font-size: 40px;
            font-weight: bold;
        }

        p {
            font-size: 20px;
            padding: 25px 0;
        }
        .ceo {
            color:gray;

        }

      
        .white-button:hover {
            background-color: rgba(0, 0, 0, 0);
            color: white;
            border: 1px solid white;
        }
    }

    .expert-consultant {
        padding-left: 50px;
        position: relative;
       top:-50px;
       
    }

}
</style>