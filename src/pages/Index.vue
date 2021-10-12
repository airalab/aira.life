<template>
  <Layout>
    <div class="wrapper">
      <div class="steps">
        <g-link class="dot step1 dot1" @click.native="goToStep(1)"></g-link>
        <svg class="lines step1 line1" @click="goToStep(1)" xmlns="http://www.w3.org/2000/svg" width="3" height="44" viewBox="0 0 3 44">
          <line id="Line_392" data-name="Line 392" y2="44" transform="translate(1.5)" fill="none" stroke="#fff"
                stroke-width="3"/>
        </svg>
        <g-link class="dot step2 dot2" @click.native="goToStep(2)"></g-link>
        <svg class="lines step2 line2" @click="goToStep(2)" xmlns="http://www.w3.org/2000/svg" width="3" height="44" viewBox="0 0 3 44">
          <line id="Line_392" data-name="Line 392" y2="44" transform="translate(1.5)" fill="none" stroke="#fff"
                stroke-width="3"/>
        </svg>
        <g-link class="dot step3 dot3" @click.native="goToStep(3)"></g-link>
        <svg class="lines step3 line3" @click="goToStep(3)" xmlns="http://www.w3.org/2000/svg" width="3" height="44" viewBox="0 0 3 44">
          <line id="Line_392" data-name="Line 392" y2="44" transform="translate(1.5)" fill="none" stroke="#fff"
                stroke-width="3"/>
        </svg>
        <g-link class="dot step4 dot4" @click.native="goToStep(4)"></g-link>
        <svg class="lines step4 line4" @click="goToStep(4)" xmlns="http://www.w3.org/2000/svg" width="3" height="44" viewBox="0 0 3 44">
          <line id="Line_392" data-name="Line 392" y2="44" transform="translate(1.5)" fill="none" stroke="#fff"
                stroke-width="3"/>
        </svg>
        <g-link class="dot step5 dot5" @click.native="goToStep(5)"></g-link>
        <svg class="lines step5 line5"  @click="goToStep(5)" xmlns="http://www.w3.org/2000/svg" width="3" height="44" viewBox="0 0 3 44">
          <line id="Line_392" data-name="Line 392" y2="44" transform="translate(1.5)" fill="none" stroke="#fff"
                stroke-width="3"/>
        </svg>
      </div>
      <div class="inner-wrapper">
        <div class="content-wrapper">
          <div class="block-content-wrapper flex-col" id="block1">
            <div class="small-wrapper">
              <div class="text-wrapper">
                Build economic<br/> interaction between <br/> human-robot and <br/> robot-robot
              </div>
              <div>
                <div class="buttons">
                  <g-link href="https://www.youtube.com/watch?v=1AEmpKReDzE">
                    <PlayButton></PlayButton>
                  </g-link>
                  <a href="https://blog.aira.life/blockchain-as-refinery-for-industrial-iot-data-873b320a6ff0">
                    <MoreButton></MoreButton>
                  </a>
                </div>
                <div class="svg-wrapper-smart-contract">
                  <SmartContract></SmartContract>
                </div>
              </div>
            </div>
          </div>
          <div class="block-content-wrapper hidden" id="block2">
            <div class="small-wrapper">Connect robots under <br/> decentralized <br/> computer’s control</div>
            <div>
              <div class="small-wrapper buttons solo-play-button">
                <a href="https://www.youtube.com/watch?v=V_3rcP2Duv0">
                  <PlayButton></PlayButton>
                </a>
              </div>
              <div>
                <g-image src="~/assets/pngs/slide-2.png"/>
              </div>
            </div>
          </div>
          <div class="block-content-wrapper hidden" id="block3">
            <div class="small-wrapper">
              We support Ethereum and Polkadot/Substrate
            </div>
            <div class="coins-and-ideas">
              <CoinsAndIdeas></CoinsAndIdeas>
            </div>
          </div>
          <div class="block-content-wrapper hidden" id="block4">
            <div class="small-wrapper">AIRA<br/>
              <span>is <a href="https://github.com/airalab/aira/releases" class="crossover-bottom">opensource</a> </span><br/>
              <span>client in </span><br/>
              <a href="https://robonomics.network" class="crossover-bottom">Robonomics Network</a>
            </div>
            <div>
              <div class="small-wrapper buttons margins-robonomics-network-buttons">
                <a href="https://www.youtube.com/watch?v=FpogdoXOnPA">
                  <PlayButton></PlayButton>
                </a>
                <a href="https://blog.aira.life/airalab-group-positioning-and-partners-cfdedd20a96e">
                  <MoreButton></MoreButton>
                </a>
              </div>
              <div class="robot-and-git-and-robonomics">
                <div>
                  <Robot class="robot"></Robot>
                </div>
                <div>
                  <GitAndRobonomics class="git-and-robonomics-margins"></GitAndRobonomics>
                </div>
              </div>
            </div>
          </div>
          <div class="block-content-wrapper hidden" id="block5">
            <div>View <a href="https://wiki.robonomics.network/docs/aira-overview/" class="crossover-bottom">WIKI</a>
              and
              <br/>
              try ARIA
            </div>
            <div class="drone-and-margin">
              <DroneAndHumanIllustration></DroneAndHumanIllustration>
            </div>
          </div>
        </div>
        <div class="code-snippet">
          <CodeSample></CodeSample>
        </div>
      </div>
    </div>
  </Layout>
</template>

<script>
import CoinsAndIdeas from "~/assets/icons/CoinsAndIdeas";
import CodeSample from "~/components/CodeSample";
import SmartContract from "~/assets/icons/SmartContract";
import PlayButton from "~/assets/icons/PlayButton";
import MoreButton from "~/assets/icons/MoreButton";
import Robot from "../assets/icons/Robot";
import GitAndRobonomics from "../assets/icons/GitAndRobonomics";
import DroneAndHumanIllustration from "../assets/icons/DroneAndHumanIllustration";

export default {
  name: 'Index',
  components: {
    CoinsAndIdeas,
    CodeSample,
    SmartContract,
    PlayButton,
    MoreButton,
    Robot,
    GitAndRobonomics,
    DroneAndHumanIllustration
  },
  data() {
    return {
      scrollTop: 0,
      autoScrollLock: false
    }
  },
  metaInfo: {
    title: 'Build economic interaction between human-robot and robot-robot'
  },
  methods: {
    handleScroll(event) {
      if (process.isClient) {
        let scrollDirection = window.scrollY > this.scrollTop ? 'down' : 'up'
        this.scrollTop = window.scrollY
        let blocks = [...document.getElementsByClassName('block-content-wrapper')]
        let lines = [...document.getElementsByClassName('lines')]
        let dots = [...document.getElementsByClassName('dot')]

        let active = blocks.filter(v => ((window.scrollY - v.offsetTop + blocks[0].offsetTop) / v.offsetHeight) * 100 > -40)
        let inactive = blocks.filter(v => ((window.scrollY - v.offsetTop + blocks[0].offsetTop) / v.offsetHeight) * 100 <= -40)
        active.map((item, index) => {
          if (index + 1 === active.length) {
            lines[index].setAttribute('class', 'lines active_el')
            dots[index].setAttribute('class', 'dot active_el')
          } else {
            lines[index].setAttribute('class', 'lines')
            dots[index].setAttribute('class', 'dot')
          }
        })
        inactive.map((item, index) => {
          lines[index + active.length] && lines[index + active.length].setAttribute('class', `lines step${index + active.length + 1} line${index + active.length + 1}`)
          dots[index + active.length] && dots[index + active.length].setAttribute('class', `dot step${index + active.length + 1} dot${index + active.length + 1}`)
        })
        if (!this.autoScrollLock) {
          blocks.map((v, index) => {
            if (scrollDirection === 'down') {
              if (window.scrollY - v.offsetTop + blocks[0].offsetTop > 75 && window.scrollY - v.offsetTop + blocks[0].offsetTop < 200) {
                if (blocks[index + 1]) {
                  this.autoScrollLock = true
                  blocks[index + 1].setAttribute('class', 'block-content-wrapper')
                  blocks[index] && blocks[index].setAttribute('class', 'block-content-wrapper hidden')
                  window.scrollTo({
                    top: this.scrollTop + blocks[index].offsetHeight - (window.scrollY - blocks[index].offsetTop) - blocks[0].offsetTop + (blocks[index + 1].offsetTop - (v.offsetTop + v.offsetHeight)),
                    behavior: 'smooth'
                  })
                  setTimeout(() => {
                    this.autoScrollLock = false
                    this.scrollTop = window.scrollY
                  }, 500)
                }
              }
            }
            if (scrollDirection === 'up') {
              if (window.scrollY - v.offsetTop + blocks[0].offsetTop > -250 && window.scrollY - v.offsetTop + blocks[0].offsetTop < -30) {
                if (blocks[index - 1]) {
                  this.autoScrollLock = true
                  blocks[index - 1].setAttribute('class', 'block-content-wrapper')
                  v && v.setAttribute('class', 'block-content-wrapper hidden')
                  window.scrollTo({
                    top: this.scrollTop - (window.scrollY - v.offsetTop) - blocks[index - 1].offsetHeight - blocks[0].offsetTop - (v.offsetTop - (blocks[index - 1].offsetTop + blocks[index - 1].offsetHeight)),
                    behavior: 'smooth'
                  })
                  setTimeout(() => {
                    window.scrollTo({
                      top: this.scrollTop - (window.scrollY - v.offsetTop) - blocks[index - 1].offsetHeight - blocks[0].offsetTop - (v.offsetTop - (blocks[index - 1].offsetTop + blocks[index - 1].offsetHeight)),
                      behavior: 'smooth'
                    })
                    setTimeout(() => {
                      this.autoScrollLock = false
                      this.scrollTop = window.scrollY
                    }, 600)
                  }, 500)
                }
              }
            }
          })
        }
      }
    },
    goToStep(step) {
      let blocks = [...document.getElementsByClassName('block-content-wrapper')]
      this.autoScrollLock = true
      blocks[step - 1].setAttribute('class', 'block-content-wrapper')
      blocks.map((item, index) => {
        if (index !== step - 1) {
          item.setAttribute('class', 'block-content-wrapper hidden')
        }
      })
      window.scrollTo({
        top: blocks[step - 1].offsetTop - blocks[0].offsetTop,
        behavior: 'smooth'
      })
      setTimeout(() => this.autoScrollLock = false, 600)

    }
  },
  created() {
    if (process.isClient) {
      window.addEventListener('scroll', this.handleScroll)
    }
  },
  destroyed() {
    if (process.isClient) {
      window.removeEventListener('scroll', this.handleScroll)
    }
  }
}
</script>

<style>

@media screen and (min-width: 1630px) {
  #block1 .svg-wrapper-smart-contract {
    transform: scale(1.5);
    transition: .5s;
  }

  #block3 .coins-and-ideas {
    transform: scale(1.5) translateX(70px) translateY(-50px);
    transition: .5s;
  }

  #block4 .robot {
    transform: scale(1.5) translateX(50px) translateY(50px);
    transition: .5s;
  }

  #block4 .git-and-robonomics-margins {
    transform: scale(1.5) translateX(-50px) translateY(25px);
    transition: .5s;
  }

  #block5 .drone-and-margin {
    transform: scale(1.5) translateX(100px);
    transition: .5s;
  }
}

@media screen and (min-width: 1630px) and (max-width: 1800px) {
  .wrapper .code-snippet {
    transform: translateX(-50px) scale(0.8);
    width: 700px;
    transition: all .5s;
  }
}

@media screen and (min-width: 1065px) and (max-width: 1630px) {
  div {
    transition: all .5s !important;
  }

  span {
    transition: all .5s !important;
  }

  .code-snippet {
    transform: translateY(235px) translateX(calc(-50% + 100px)) scale(0.8);
    width: 700px;
    transition: all .5s;
  }

  .content-wrapper {
    width: 100vw;
  }

  .text-wrapper {
    width: 500px;
  }

  #block1 .small-wrapper {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: 80vw;
  }

  #block1 .svg-wrapper-smart-contract {
    margin-right: 100px;
    margin-left: 0;
  }

  .text-wrapper ~ div {
    margin-top: -100px;
  }

  #block2 {
    display: flex;
    flex-direction: row;
  }

  #block2 .buttons {
    margin-top: -100px;
  }

  #block2 .solo-play-button ~div img {
    width: calc(100vw - 600px);
    margin-top: -30px;
    max-width: 800px;
    margin-left: 50px;
    transition: .5s;
  }

  #block3 {
    width: 80vw;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }

  #block3 .coins-and-ideas {
    margin-top: -100px;
  }

  #block4 {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: 90vw;
  }

  #block4 .small-wrapper {
    width: 500px;
  }

  #block4 .robot-and-git-and-robonomics .robot {
    margin-right: 200px;
    margin-top: -100px;
    transition: all .5s;
  }

  .robot-and-git-and-robonomics {
    display: flex;
    flex-direction: column;
  }

  #block4 .git-and-robonomics-margins {
    margin: 0;
    top: 250px;
    left: calc(-75vw);
    transition: all .5s;
  }

  #block5 {
    width: 1000px;
    height: 750px;
    display: flex;
    flex-direction: row;
  }

  #block5 :first-child {
    width: 300px;
  }

  #block5 .drone-and-margin {
    margin-top: -80px;
    margin-left: 150px;
  }
}

@media screen and (min-width: 1250px) and (max-width: 1440px) {
  #block4.block-content-wrapper  .git-and-robonomics-margins {
    left: -100px;
    top: 130px;
    transition: all .5s;
  }
}

@media screen and (min-width: 1065px) and (max-width: 1250px) {
  .slot-wrapper .code-snippet {
    transform: translateY(235px) translateX(calc(-40% + 120px)) scale(0.8);
    transition: all .5s;
  }

  #block2 .solo-play-button ~div img {
    width: calc(100vw - 600px);
    margin-top: 50px;
    max-width: 700px;
    margin-left: 50px;
    transition: .5s;
  }

  #block4 .git-and-robonomics-margins {
    margin: 0;
    top: 400px;
    left: -850px;
    transition: all .5s;
  }

  #block4 .small-wrapper {
    width: 500px;
  }
  #block4 .robot-and-git-and-robonomics .robot {
    margin-right: 150px;
  }

  #block4 .margins-robonomics-network-buttons {
    margin-left: -35px;
  }
}

@media screen and (min-width: 1065px) and (max-width: 1250px) and (min-height: 900px) {
  .slot-wrapper .code-snippet {
    transform: translateY(300px) translateX(calc(-40% + 120px)) scale(0.8);
    transition: all .5s;
  }
}

@media screen and (min-width: 1065px) and (max-width: 1250px) and (min-height: 700px) and (max-height: 900px) {
  .slot-wrapper .code-snippet {
    transform: translateY(250px) translateX(calc(5%)) scale(0.7);
    transition: all .5s;
  }
}

@media screen and (min-width: 550px) and (max-width: 1065px) {

  .slot-wrapper .code-snippet {
    transform: translateY(435px) translateX(calc(50%)) scale(calc(0.7));
    margin-right: calc(50% - 100px);
    transition: all .5s;
  }
  .wrapper .steps {
    margin-left: 15px;
    margin-top: -50px;
    transform: scale(0.75);
    transition: all .5s;
  }

  .inner-wrapper .content-wrapper {
    margin-left: 120px;
    max-width: calc(100% - 150px);
    width: inherit;
    transition: all .5s;
  }

  .content-wrapper .small-wrapper {
    max-width: 100%;
    width: 100%;
  }

  #block1 .svg-wrapper-smart-contract {
    margin-left: calc(40vw - 200px);
    margin-top: -20px;
    transition: all .5s;
  }
  #block2 .solo-play-button {
    margin-top: 0;
    transition: all .5s;
  }

  #block2 .solo-play-button ~div img {
    width: calc(100vw - 200px);
    margin-top: -40px;
    max-width: 730px;
    margin-left: -50px;
    transition: .5s;
  }

  #block3 .coins-and-ideas {
    display: flex;
    justify-content: center;
    margin-top: 10px;
    transition: all .5s;
  }

  #block4 br:not(:first-child) and #block4 br:not(:last-child) {
    display: none;
  }

  #block4 .margins-robonomics-network-buttons {
    width: inherit;
  }

  #block4 .robot-and-git-and-robonomics {
    margin-top: -40px;
    transition: all .5s;
  }

  #block4 .robot-and-git-and-robonomics .git-and-robonomics-margins {
    left: calc(90vw - 600px);
    top: 40px;
    transition: all .5s;
  }

  #block5 .drone-and-margin {
    margin-top: 20px;
    display: flex;
    justify-content: center;
    transition: all .5s;
  }
}

@media screen and (min-width: 650px) and (max-width: 700px) {
  .slot-wrapper .wrapper .code-snippet {
    transform: translateY(380px) translateX(calc(40% - 150px)) scale(calc(0.55));
    margin-right: 0;
    transition: all .5s;
  }

  .inner-wrapper .content-wrapper {
    margin-left: 120px;
    transition: all .5s;
  }
}

@media screen and (min-width: 550px) and (max-width: 700px) {
  .wrapper .inner-wrapper .content-wrapper {
    max-width: calc(100%);
    margin-left: 0;
    transition: all .5s;
  }
  .slot-wrapper .code-snippet {
    transform: translateY(380px) translateX(calc(40% - 100px)) scale(calc(0.55));
    transition: all .5s;
    margin-right: 0;
  }

  .content-wrapper .block-content-wrapper {
    transition: all .5s;
    max-width: 100%;
    width: calc(100% - 100px);
    margin-left: 90px;
    transform: scale(0.8) translateX(calc(-50% + 240px)) translateY(-80px);
    /*transform: scale(0.8) translateX(calc(-50% + 250px));*/
  }

  .small-wrapper {
    max-width: calc(100% - 50px);
    transition: all .5s;
  }

  #block2 .buttons ~div {
    margin-left: -150px;
    margin-top: -30px;
    transition: all .5s;
  }

  #block2 .solo-play-button ~div img {
    width: calc(100vw - 10px);
    max-width: 700px;
    margin-top: 0;
    margin-left: 100px;
    transition: .5s;
  }

  #block4 .robot-and-git-and-robonomics {
    margin-top: -30px;
    transition: all .5s;
  }

  #block4 .robot-and-git-and-robonomics .git-and-robonomics-margins {
    left: 20px;
    top: 50px;
    transition: all .5s;
  }
}


/*@media screen and (max-width: 1065px) {*/
@media screen and (max-width: 550px) {
  .wrapper {

    flex-direction: column;
    transition: all .5s;
  }

  .wrapper .steps {
    margin-top: -40px;
    min-height: 0;
    width: 100vw;
    position: fixed;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-start;
    margin-left: 40px;
    transition: all .5s;
  }

  .inner-wrapper .code-snippet {
    transition: all .5s;
    transform: scale(0.5);
    width: 100vw;
    right: 70px;
    margin-top: 200px;
  }

  .code-snippet .wrapper {
    width: 650px;
    height: 450px;
    transition: all .5s;
  }

  .code-snippet .wrapper .header {
    min-height: 60px;
    justify-content: center;
    align-items: center;
    transition: all .5s;
  }

  .code-snippet .wrapper .title {
    margin: 0;
    transition: all .5s;
  }

  .code-snippet .wrapper .buttons {
    pointer-events: none;
    opacity: 0;
    display: none;
    transform: scale(0);
    transition: all .5s;
  }

  .inner-wrapper .content-wrapper {
    margin-left: 0;
    transition: all .5s;
    align-items: center;
  }

  .inner-wrapper .content-wrapper .block-content-wrapper {
    transform: scale(0.7);
    margin: -15% 0 0 -15%;
    transition: all .5s;
    transition-delay: .2s;
  }

  .block-content-wrapper .buttons {
    display: flex;
    justify-content: flex-start;
    margin-top: 20px;
    transition: all .5s;
  }

  .steps .dot {
    margin-left: 0;
    width: 30px;
    height: 30px;
    background-color: white;
    border-radius: 50%;
    transition: all .5s;
    margin-right: 25px;
  }

  .dot.dot1, .dot.dot2, .dot.dot3, .dot.dot4, .dot.dot5 {
    width: 30px;
    height: 30px;
    transform: scale(1);
    transition: all .5s;
  }

  .lines {
    display: none;
    transition: all .5s;
  }

  #block2 .small-wrapper.buttons.solo-play-button {
    margin-left: 40px;
  }

  #block2 .solo-play-button ~div img {
    width: calc(100vw + 50px);
    max-width: 500px;
    margin-left: 50px;
    transition: .5s;
  }

  #block3 .small-wrapper {
    transition: all .5s;
    width: 70%;
  }

  #block3.block-content-wrapper .coins-and-ideas {
    margin-top: 50px;
    transition: all .5s;
  }

  #block4 .block-content-wrapper .small-wrapper {
    width: 100%;
  }

  #block4 .robot-and-git-and-robonomics {
    pointer-events: none;
    margin-left: 50px;
    margin-top: -20px;
    transition: all .5s;
  }

  #block4 .robot-and-git-and-robonomics .git-and-robonomics-margins {
    transition: all .5s;
    left: 0;
    top: 0;
  }

  #block5.block-content-wrapper .drone-and-margin {
    margin-top: 50px;
    transition: all .5s;
    margin-left: 80px;
  }

}

a {
  margin-right: 20px;
  display: block;
  text-decoration: none;
  color: white;
}

.inner-wrapper {
  width: 100vw;
  z-index: 15;
  display: flex;
}

.crossover-bottom {
  display: inline;
  background-color: transparent;
  position: relative;
}

.crossover-bottom::before {
  border-top: 10px solid #6CEEFF;
  content: "";
  margin: 0 auto; /* this centers the line to the full width specified */
  position: absolute; /* positioning must be absolute here, and relative positioning must be applied to the parent */
  top: calc(50% + 10px);
  left: 0;
  right: 0;
  bottom: 0;
  width: 100%;
  z-index: -1;
}

.coins-and-ideas {
  margin-top: 200px;
}

.solo-play-button {
  margin-top: 50px;
}

.solo-play-button ~div img {
  margin-left: -100px;
  max-width: 1000px;
  transition: all .5s;
  margin-right: -16px;
}

.buttons {
  display: flex;
  justify-content: flex-end;
  align-items: center;
}

.buttons a:first-child {
  margin-top: 4px;
}

#block2 .buttons a :first-child {
  margin-right: 100px;
  transition: .5s all;
}

.robot-and-git-and-robonomics {
  display: flex;
  flex-direction: row;
}

.robot-and-git-and-robonomics :nth-child(2) {
  pointer-events: none;
}

.git-and-robonomics-margins {
  position: relative;
  left: 420px;
  top: 200px;
}

.margins-robonomics-network-buttons {
  margin-top: 0;
  margin-left: 35px;
}

.drone-and-margin {
  margin-top: 150px;
}

.svg-wrapper-smart-contract {
  transform: scale(1.2);
  margin-left: 90px;
  margin-top: 40px;
}

.block-content-wrapper {
  height: 700px;
  opacity: 1;
  visibility: visible;
  transition: all .5s;
  transition-delay: .3s;
}

.hidden {
  transition: all .2s;
  opacity: 0;
  pointer-events: none;
}

.block-content-wrapper:last-child {
  height: 750px;
}

.wrapper {
  width: 100vw;
  z-index: 15;
  display: flex;
}

.steps {
  margin-left: 70px;
  width: 100px;
  min-height: 400px;
  position: fixed;
  display: flex;
  align-items: center;
  flex-direction: column;
  z-index: 25;
}

.content-wrapper {
  margin-left: 200px;
  width: 650px;
  color: white;
  font-family: "Yeseva One", sans-serif;
  font-size: 34pt;
  font-weight: 300;
}

.small-wrapper {
  width: 600px;
}

.code-snippet {
  position: fixed;
  margin-top: -100px;
  right: 100px;
  transition: all .5s;
}

.flex-col {
  display: flex;
  flex-direction: column;
}

.dot {
  height: 20px;
  width: 20px;
  border-radius: 50%;
  margin-left: 20px;
  background-color: white;
  cursor: pointer;
}

.dot, .lines {
  margin-bottom: 20px;
  opacity: 0.5;
  transition: all .5s;
}

.active_el {
  opacity: 1;
  transition: all .5s;
}

.dot1, .line1 {
  opacity: 1;
}

.dot2 {
  transform: translateX(10px) translateY(5px);
  transition: all .5s;
}

.line2 {
  transform: translateX(-5px) rotate(-30deg) translateY(-13px);
  transition: all .5s;
}

.dot3 {
  transform: translateX(-10px);
  transition: all .5s;
}

.line3 {
  transform: translateX(9px) translateY(-15px) rotate(70deg);
  transition: all .5s;
}

.dot4 {
  transform: translateX(10px);
  transition: all .5s;
}

.line4 {
  transform: translateY(-10px) rotate(-50deg) translateY(-20px) translateX(5px);
  transition: all .5s;
}

.dot5 {
  transform: translateX(-15px);
  transition: all .5s;
}

.line5 {
  transform: translateX(15px) rotate(45deg) translateX(-20px) translateY(-15px);
  transition: all .5s;
}

</style>
