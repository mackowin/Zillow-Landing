<template>
    <!-- Start Footer Area -->
    <footer class="footer-area bg-f7fafd">
        <div class="container">
            <div class="row">
                <div class="col-lg-3 col-md-6 col-sm-6">
                    <div class="single-footer-widget">
                        <div class="logo">
                            <a href="/">
                                <img width="120px" src="../resources/doorhacker-logo.png"/>
                            </a>
                        </div>
                        <p style="font-weight: 600">Find cash flow on Zillow</p>
                        <p>Get rents in one click and screen properties with the highest returns</p>
                    </div>
                </div>

                <div class="col-lg-3 col-md-6 col-sm-6">
                    <div class="single-footer-widget pl-5">
                        <h3>Company</h3>
                        <ul class="list">
                            <li><a href="/"  v-scroll-to="'#solutions'">Solutions</a></li>
                            <li><a href="/"  v-scroll-to="'#pricing'">Pricing</a></li>
                        </ul>
                    </div>
                </div>

                <div class="col-lg-3 col-md-6 col-sm-6">
                    <div class="single-footer-widget">
                        <h3>Support</h3>
                        <ul class="list">
                            <li><a href="/RE_Terms_of_Service.pdf">Terms of Service</a></li>
                            <li><a href="/RE_Privacy_Policy.pdf">Privacy Policy</a></li>
                            <li><a href="/RE_Website_Terms_and_Conditions.pdf">Terms and Conditions</a></li>
                            
                            <li><a href="/" v-scroll-to="'#contact'" >Contact Us</a></li>
                        </ul>
                    </div>
                </div>



                <div class="col-lg-12 col-md-12">
                    <div class="copyright-area">
                        <p>Copyright &copy;2023 Doorhacker. All Rights Reserved</p>
                    </div>
                </div>
            </div>
        </div>

        <img src="../../../assets/img/map.png" class="map" >
        <div class="shape1"><img src="../../../assets/img/shape1.png" ></div>
        <div class="shape8 rotateme"><img src="../../../assets/img/shape2.svg" ></div>

        <back-to-top bottom="50px" right="50px">
            <div class="go-top"><feather type="arrow-up"></feather></div>
        </back-to-top>
    </footer>
    <!-- End Footer Area -->
</template>

<script>
import BackToTop from 'vue-backtotop'
export default {
    name: 'FooterTemplate',
    components: { BackToTop }
}
</script>
