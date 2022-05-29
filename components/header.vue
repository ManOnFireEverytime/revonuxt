<template>
        <header class="header revonue-header header-style-3">
            <div id="revonue-sticky-placeholder"></div>
            <div class="revonue-mainmenu">
                <div class="container">
                    <div class="header-navbar">
                        <div class="header-logo">
                            <!-- <a href="index-1.html"><img class="light-version-logo" src="assets/media/logo.svg" alt="logo"></a>
                            <a href="index-1.html"><img class="dark-version-logo" src="assets/media/logo-3.svg" alt="logo"></a>
                            <a href="index-1.html"><img class="sticky-logo" src="assets/media/logo-2.svg" alt="logo"></a> -->
                        </div>
                        <div class="header-action">
                            <ul class="list-unstyled">
                                <li class="header-social-link">
                                    <ul class="social-icon-list list-unstyled">
                                        <!-- <li><a href="https://facebook.com/"><i class="fab fa-facebook-f"></i></a></li>
                                        <li><a href="https://twitter.com/"><i class="fab fa-twitter"></i></a></li>
                                        <li><a href="https://www.linkedin.com/"><i class="fab fa-linkedin-in"></i></a></li>
                                        <li><a href="https://www.behance.net/"><i class="fab fa-behance"></i></a></li>
                                         <li><a href="https://www.behance.net/">Contact Us</a></li> -->
                                    </ul>
                                </li>
                                <li class="header-btn">
                                    <a href="contact.html" class="revonue-btn btn-fill-white">Let's Talk</a>
                                </li>

                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </header>
</template>

<script>
export default {
  name: "AccHeader",
  data () {
    return {
      height: '',
      scrollY: 0,
    }
  },
  computed:{
    mousescroll() {
      if(this.scrollY>50)
      {
        return 'hide';
      }else{
        return '';
      }
    },
  },
  beforeMount () {
    window.addEventListener('scroll', this.handleScroll);
  },

  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll () {
      this.scrollY = window.scrollY;
    }
  },
}
</script>
