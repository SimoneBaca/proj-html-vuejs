<template>
    <div class="content">
        <div class="container">
            <div class="row-card">
                <!-- Text -->
                <div class="text-area">
                    <h2 class="title-section">
                        We Boost Our Clients' Bottom Line by Optimizing Their Growth Potential.
                    </h2>

                    <p class="p-section">
                        Quisque aliquet, libero consequat elementum convallis, erat risus imperdiet pellentesque sem neque
                        eget.
                    </p>

                    <a class="primary-button" href="#">
                        Why Work With Us
                    </a>
                </div>

                <img src="../assets/images/we-boost-our-clients-600x549.jpg" alt="">

            </div>
            <!-- INFO -->
            <div class="info-text">

                <!-- Col-SX -->
                <div class="text-area">
                    <h2>We Build Relationships</h2>
                    <p>Curabitur ac leo nunc. Vestibulum et mauris vel ante finibus maximus nec ut leo. Integer consectetur
                    </p>

                    <h2>Proprietary Processes</h2>
                    <p>Curabitur ac leo nunc. Vestibulum et mauris vel ante finibus maximus nec ut leo. Integer consectetur
                    </p>
                </div>

                <!-- Col-DX -->
                <div class="info-icons">

                    <!-- Single Icon Area -->
                    <div class="single-icon-area">
                        <img src="../assets/images/aa1.png" alt="">

                        <div class="icon-text">
                            <h2>Accountability</h2>
                            <p>Curabitur ac leo nunc vestibulum</p>
                        </div>
                    </div>

                    <!-- Single Icon Area -->
                    <div class="single-icon-area">
                        <img src="../assets/images/aa2.png" alt="">

                        <div class="icon-text">
                            <h2>Transparency</h2>
                            <p>Curabitur ac leo nunc vestibulum</p>
                        </div>
                    </div>

                    <!-- Single Icon Area -->
                    <div class="single-icon-area">
                        <img src="../assets/images/aa3.png" alt="">

                        <div class="icon-text">
                            <h2>Investment</h2>
                            <p>Curabitur ac leo nunc vestibulum</p>
                        </div>
                    </div>

                </div>
            </div>
            <!-- AWARDS -->
            <div class="awards">
                <h2>Awards</h2>
                <ul class="awards-list">
                    <li v-for="(awards, index) in awards" :key="index">
                        <img :src="awards.thumb" :alt="awards.alt">
                        <span>{{ awards.name }}</span>
                        <span>{{ awards.info }}</span>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name: "References",
    data: function () {
        return {
            awards: [
                {
                    name: 'Winner Seo Master MAGT',
                    info: 'Smart Start Award 2017',
                    alt: 'logo award seo master magt',
                },
                {
                    name: 'Top Social Media Agencies',
                    info: 'Next Partner 2018',
                    alt: 'logo award top social media agencies',
                },
                {
                    name: '10 Fastest Growing Abstract',
                    info: 'Solution Providers 2019',
                    alt: 'logo award 10 fastest growing abstract',
                },
                {
                    name: 'National Excellence Agencie',
                    info: 'Award Winner 2020',
                    alt: 'logo award national excellence agencie',
                },
            ]
        }
    }
}
</script>


<style lang="scss" scoped>
@import '../style/variable';
@import '../style/commons';

.content {
    background-color: #f5f5f7;
    width: 100%;

    .row-card {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 130px 0;

        .text-card {
            padding-right: 150px;
        }

        .p-section {
            padding: 30px 0;
        }

        img {
            border-radius: 10px;
        }
    }

    // INFO
    .info-text {
        display: flex;
        // justify-content: space-around;
        align-items: center;

        .text-area {
            width: 50%;
            padding-right: 130px;

            h2 {
                font-size: 28px;
            }

            p {
                font-size: 20px;
                padding: 20px 0 80px 0;
            }
        }

        .info-icons {
            width: 50%;
            margin-left: 140px;

            .single-icon-area {
                display: flex;
                align-items: center;
                padding-bottom: 40px;

                img {
                    padding-right: 25px;
                }

                h2 {
                    padding-bottom: 20px;
                }
            }
        }
    }

    // AWARDS
    .awards {
        padding-top: 50px;

        h2 {
            text-align: center;
        }

        .awards-list {
            display: flex;

            li {
                display: flex;
                flex-direction: column;
                text-align: center;

                img {
                    width: 160px;
                }

                span {
                    font-size: 18px;
                    padding-bottom: 10px;
                }
            }
        }
    }
}</style>