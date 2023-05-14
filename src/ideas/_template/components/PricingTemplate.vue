<template>
    <!-- Start Pricing Area -->
    <section class="pricing-area ptb-80" style="background: #F9F6F6">
        <SectionFour id="pricing"/>
        <div class="container">
            <div class="section-title">
                <h2>Pricing Plans</h2>
                <div class="bar"></div>
                <div class="paragraph">
                    <p>Try Doorhacker DEMO for <a href="#" style="font-weight: 600">FREE</a>.</p>
                </div>
            </div>

            <div class="row">
                <div class="col-lg-6 col-md-6 col-sm-6">
                    <div class="pricing-table">
                        <div class="pricing-header">
                            <h3>DEMO</h3>
                        </div>

                        <div class="price">
                            <span><sup></sup>FREE<span></span></span>
                        </div>

                        <div class="pricing-features">
                            <ul>
                                <li class="active">30 properties analyzed</li>
                                <li class="active">30 properties per excel export</li>
                                <li class="active">Request additional cities</li>
                                <li>Sorting by price, rent, and returns</li>
                                <li>Edit rent inputs (*** to come)</li>
                            </ul>
                        </div>

                        <div class="pricing-footer">
                            <a href="#" class="btn btn-primary">TRY DEMO</a>
                        </div>
                    </div>
                </div>

                <div class="col-lg-6 col-md-6 col-sm-6">
                    <div class="pricing-table active-plan">
                        <div class="pricing-header">
                            <h3>Pro Plan</h3>
                        </div>

                        <div class="price">
                            <span><sup></sup>$29<span> monthly</span></span>
                        </div>

                        <div class="pricing-features">
                            <ul>
                                <li class="active">800 properties analyzed</li>
                                <li class="active">800 properties per excel export</li>
                                <li class="active">City requests prioritiezed</li>
                                <li class="active">Sorting by price, rent, and returns</li>
                                <li class="active">Edit rent inputs (*** to come)</li>
                            </ul>
                        </div>

                        <div class="pricing-footer">
                            <a href="https://buy.stripe.com/14kcON0E18b0byE3ce" class="btn btn-primary">UPGRADE</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>


        <div class="shape7"><img src="../../../assets/img/shape4.svg" ></div>
    </section>
    <!-- End Pricing Area -->
</template>

<script>
export default {
    name: 'PricingTemplate'
}
</script>
