<template>
    <nav id="navbar" class="navbar is-transparent is-fixed-top">
      <div class="navbar-brand columns is-mobile">
        <a class="navbar-item is-left is-spaced" href="https://www.automotivelinux.org/">
          <img class="menubar-icon-img"
               src="~/assets/agl_logo.png" alt="AGL Logo Image">
        </a>
        <a class="nabvar-item is-left is-spaced"
           href="https://github.com/automotive-grade-linux/docs-agl"
           target="_blank">
          <img class="menubar-icon-img"
               src="~/assets/github-icon.jpg" alt="Github Icon Image"
               width="28" height="28">
        </a>
        <a class="nabvar-item is-left is-spaced"
           href="https://gerrit.automotivelinux.org/gerrit"
           target="_blank">
          <img class="menubar-icon-img"
               src="~/assets/Gerrit_icon.svg.png" alt="Gerrit Icon Image"
               width="28" height="28">
        </a>

        <div class="navbar-burger burger is-spaced"
             data-target="menu-item-list"
             @click="toggle(burger)"
             :class="{'is-active': burger.isActive}">
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>
    
      <div id="menu-item-list" class="navbar-menu"
            :class="{'is-active': burger.isActive}">
        <div class="navbar-start">
          <div class="navbar-item has-dropdown is-hoverable container-fluid">
            <a class="navbar-link is-active" target="_blank" href="https://wiki.automotivelinux.org/">
              Wiki
            </a>
            <div class="navbar-dropdown is-boxed is-right">
              <a class="navbar-item " target="_blank" href="https://wiki.automotivelinux.org/agl-sat/">
                System Architecture Team
              </a>
              <a class="navbar-item " target="_blank" href="https://wiki.automotivelinux.org/eg-app-fw/">
                App Framework and Security
              </a>
              <a class="navbar-item " target="_blank" href="https://wiki.automotivelinux.org/eg-connectivity/">
                Connectivity
              </a>
              <a class="navbar-item " target="_blank" href="https://wiki.automotivelinux.org/eg-ciat/">
                Continuous Intergration and Test
              </a>
              <a class="navbar-item " target="_blank" href="https://wiki.automotivelinux.org/eg-ic/">
                Instrument Cluster
              </a>
              <a class="navbar-item " target="_blank" href="https://wiki.automotivelinux.org/eg-navi/">
                Navigation
              </a>
              <a class="navbar-item " target="_blank" href="https://wiki.automotivelinux.org/eg-rhsa/">
                Reference Hardware System Architecture
              </a>
              <a class="navbar-item " target="_blank" href="https://wiki.automotivelinux.org/eg-speech/">
                Speech
              </a>
              <a class="navbar-item " target="_blank" href="https://wiki.automotivelinux.org/eg-requirements-specification/">
                System Spec
              </a>
              <a class="navbar-item " target="_blank" href="https://wiki.automotivelinux.org/eg-ui-graphics/">
                UI and Graphics
              </a>
              <a class="navbar-item " target="_blank" href="https://wiki.automotivelinux.org/eg-v2c/">
                Vehicle to Cloud
              </a>
              <a class="navbar-item " target="_blank" href="https://wiki.automotivelinux.org/eg-virt/">
                Virtualization
              </a>
              <hr class="navbar-divider">
              <div class="navbar-item">
                <div>
                  <p class="is-size-6-desktop">
                    <small><strong class="has-text-info">
                      view all
                    </strong></small>
                  </p>
                </div>
              </div>
              </div>
            </div>
          </div>
          <div class="navbar-end">
            <div class="navbar-item">
              <div class="field is-grouped">
                <p class="control">
                  <a class="bd-tw-button button"
                     data-social-network="Twitter"
                     data-social-action="tweet"
                     target="_blank"
                     href="https://twitter.com/intent/tweet?text=Tweet by My Electron App">
                    <span class="icon">
                      <i class="fab fa-twitter" aria-hidden="true"></i>
                    </span>
                    <span>Tweet</span>
                  </a>
                </p>
                <p class="control">
                  <a class="button is-primary">
                    <span class="icon">
                      <i class="fas fa-download" aria-hidden="true"></i>
                    </span>
                    <span>Download</span>
                  </a>
                </p>
              </div>
          </div>
        </div>
      </div>
    </nav>
</template>

<script>
import { mapMutations } from 'vuex'

export default {
    computed: {
        burger () {
            return this.$store.state.burger
        }
    },
    methods: {
        toggle (e) {
            this.$store.commit('burger/toggle')
        },
        reset (e) {
            this.$store.commit('burger/reset')
        },
        ...mapMutations({
            toggle: 'burger/toggle',
            reset: 'burger/reset'
        })
    }
}
</script>

<style>
.navbar-item {
  text-align: bottom;
  justify-content: left;
  align-items: left;
}

.navbar-burger {
  display: flex;
  text-align: bottom;
  justify-content: right;
  align-items: right;
}
</style>
