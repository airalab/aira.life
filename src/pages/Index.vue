<template>
  <Layout>
    <div class="wrapper">
      <div class="steps">
        <svg class="dot step1 dot1" xmlns="http://www.w3.org/2000/svg" width="19" height="19" viewBox="0 0 19 19">
          <circle id="Ellipse_1777" data-name="Ellipse 1777" cx="9.5" cy="9.5" r="9.5" fill="#fff"/>
        </svg>
        <svg class="lines step1 line1" xmlns="http://www.w3.org/2000/svg" width="3" height="44" viewBox="0 0 3 44">
          <line id="Line_392" data-name="Line 392" y2="44" transform="translate(1.5)" fill="none" stroke="#fff"
                stroke-width="3"/>
        </svg>
        <svg class="dot step2 dot2" xmlns="http://www.w3.org/2000/svg" width="19" height="19" viewBox="0 0 19 19">
          <circle id="Ellipse_1777" data-name="Ellipse 1777" cx="9.5" cy="9.5" r="9.5" fill="#fff"/>
        </svg>
        <svg class="lines step2 line2" xmlns="http://www.w3.org/2000/svg" width="3" height="44" viewBox="0 0 3 44">
          <line id="Line_392" data-name="Line 392" y2="44" transform="translate(1.5)" fill="none" stroke="#fff"
                stroke-width="3"/>
        </svg>
        <svg class="dot step3 dot3" xmlns="http://www.w3.org/2000/svg" width="19" height="19" viewBox="0 0 19 19">
          <circle id="Ellipse_1777" data-name="Ellipse 1777" cx="9.5" cy="9.5" r="9.5" fill="#fff"/>
        </svg>
        <svg class="lines step3 line3" xmlns="http://www.w3.org/2000/svg" width="3" height="44" viewBox="0 0 3 44">
          <line id="Line_392" data-name="Line 392" y2="44" transform="translate(1.5)" fill="none" stroke="#fff"
                stroke-width="3"/>
        </svg>
        <svg class="dot step4 dot4" xmlns="http://www.w3.org/2000/svg" width="19" height="19" viewBox="0 0 19 19">
          <circle id="Ellipse_1777" data-name="Ellipse 1777" cx="9.5" cy="9.5" r="9.5" fill="#fff"/>
        </svg>
        <svg class="lines step4 line4" xmlns="http://www.w3.org/2000/svg" width="3" height="44" viewBox="0 0 3 44">
          <line id="Line_392" data-name="Line 392" y2="44" transform="translate(1.5)" fill="none" stroke="#fff"
                stroke-width="3"/>
        </svg>
        <svg class="dot step5 dot5" xmlns="http://www.w3.org/2000/svg" width="19" height="19" viewBox="0 0 19 19">
          <circle id="Ellipse_1777" data-name="Ellipse 1777" cx="9.5" cy="9.5" r="9.5" fill="#fff"/>
        </svg>
        <svg class="lines step5 line5" xmlns="http://www.w3.org/2000/svg" width="3" height="44" viewBox="0 0 3 44">
          <line id="Line_392" data-name="Line 392" y2="44" transform="translate(1.5)" fill="none" stroke="#fff"
                stroke-width="3"/>
        </svg>
      </div>
      <div class="content-wrapper">
        <div class="filler_1 flex-col" id="block1">
          <div class="small-wrapper">
            <div>
              Build economic interaction between human-robot and robot-robot
            </div>
            <div class="buttons">
              <a href="https://www.youtube.com/watch?v=1AEmpKReDzE">
                <PlayButton></PlayButton>
              </a>
              <a href="https://blog.aira.life/blockchain-as-refinery-for-industrial-iot-data-873b320a6ff0">
                <MoreButton></MoreButton>
              </a>
            </div>
            <div class="svg-wrapper-smart-contract">
              <SmartContract></SmartContract>
            </div>
          </div>
        </div>
        <div class="filler_1" id="block2">
          <div class="small-wrapper">Connect robots under decentralized computer’s control</div>
          <div class="small-wrapper buttons solo-play-button">
            <a href="https://www.youtube.com/watch?v=V_3rcP2Duv0">
              <PlayButton></PlayButton>
            </a>
          </div>
          <div></div>
          <div>
            <VavesBottom></VavesBottom>
          </div>
        </div>
        <div class="filler_1" id="block3">
          <div class="small-wrapper">
            We support Ethereum and Polkadot/Substrate
          </div>
          <div>
            <CoinsAndIdeas></CoinsAndIdeas>
          </div>
        </div>
        <div class="filler_1" id="block4">
          <div class="small-wrapper">AIRA
            <i>is opensource</i>
            client in
            Robonomics Network
          </div>
          <div class="small-wrapper buttons">
            <a>
              <PlayButton></PlayButton>
            </a>
            <a href="">
              <MoreButton></MoreButton>
            </a>
          </div>
          <div>
            <Robot></Robot>
            <GitAndRobonomics></GitAndRobonomics>
          </div>
        </div>
        <div class="filler_1" id="block5">
          <Ethereum></Ethereum>
        </div>
        <div class="filler_1 hidden" id="block6">qwerty</div>
      </div>
      <div class="code-snippet">
        <CodeSample></CodeSample>
      </div>
    </div>
  </Layout>
</template>

<script>
import CodeSample from "~/components/CodeSample";
import SmartContract from "~/assets/icons/SmartContract";
import VavesBottom from "~/assets/icons/VavesBottom";
import PlayButton from "~/assets/icons/PlayButton";
import MoreButton from "~/assets/icons/MoreButton";
import CoinsAndIdeas from "~/assets/icons/CoinsAndIdeas";
import Ethereum from "../assets/icons/Ethereum";
import Robot from "../assets/icons/Robot";
import GitAndRobonomics from "../assets/icons/GitAndRobonomics";

export default {
  name: 'Index',
  components: {
    CodeSample,
    SmartContract,
    VavesBottom,
    PlayButton,
    MoreButton,
    CoinsAndIdeas,
    Ethereum,
    Robot,
    GitAndRobonomics
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
      let scrollDirection = window.scrollY > this.scrollTop ? 'down' : 'up'
      this.scrollTop = window.scrollY
      let blocks = [...document.getElementsByClassName('filler_1')]
      let lines = [...document.getElementsByClassName('lines')]
      let dots = [...document.getElementsByClassName('dot')]

      let active = blocks.filter(v => ((window.scrollY - v.offsetTop + blocks[0].offsetTop) / v.offsetHeight) * 100 > -40)
      let inactive = blocks.filter(v => ((window.scrollY - v.offsetTop + blocks[0].offsetTop) / v.offsetHeight) * 100 <= -40)
      active.map((item, index) => {
        if (index + 1 === active.length) {
          lines[index].setAttribute('class', 'lines active')
          dots[index].setAttribute('class', 'dot active')
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
                blocks[index + 1].setAttribute('class', 'filler_1')
                blocks[index] && blocks[index].setAttribute('class', 'filler_1 hidden')
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
            if (window.scrollY - v.offsetTop + blocks[0].offsetTop > -100 && window.scrollY - v.offsetTop + blocks[0].offsetTop < 200) {
              if (blocks[index - 1]) {
                this.autoScrollLock = true
                blocks[index - 1].setAttribute('class', 'filler_1')
                v && v.setAttribute('class', 'filler_1 hidden')
                window.scrollTo({
                  top: this.scrollTop - (window.scrollY - v.offsetTop) - blocks[index - 1].offsetHeight - blocks[0].offsetTop - (v.offsetTop - (blocks[index - 1].offsetTop + blocks[index - 1].offsetHeight)),
                  behavior: 'smooth'
                })
                setTimeout(() => {
                  this.autoScrollLock = false
                  this.scrollTop = window.scrollY
                }, 600)
              }
            }
          }
        })
      }
    },
  },
  created() {
    window.addEventListener('scroll', this.handleScroll)
  },
  destroyed() {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>

<style>

a {
  margin-right: 20px;
  display: block;
  text-decoration: none;
}

.solo-play-button {
  margin-top: 50px;
}

.buttons {
  display: flex;
  justify-content: flex-end;
  align-items: center;
}

.buttons a:first-child {
  margin-top: 4px;
}

.svg-wrapper-smart-contract {
  transform: scale(1.2);
  margin-left: 90px;
  margin-top: 40px;
}

.filler_1 {
  height: 700px;
  /*border: 1px solid white;*/
  opacity: 1;
  visibility: visible;
  transition: all 1s;
}

.hidden {
  transition: all 1s;
  opacity: 0;
  /*visibility: hidden;*/
}

.filler_1:last-child {
  margin-bottom: 200px;
}

.wrapper {
  margin-top: 70px;
  width: 100vw;
  z-index: 15;
  display: flex;
}

.steps {
  margin-left: 70px;
  width: 100px;
  /*border: 1px solid black;*/
  min-height: 400px;
  position: fixed;

  display: flex;
  align-items: center;
  flex-direction: column;
  gap: 10px;
}

.content-wrapper {
  /*border: 1px solid black;*/
  margin-left: 200px;
  width: 650px;
  color: white;
  font-family: Roboto, sans-serif;
  font-size: 40pt;
  font-weight: 300;
}

.small-wrapper {
  width: 550px;
}

.code-snippet {
  position: fixed;
  /*top: */
  margin-top: -100px;
  right: 150px;
}

.flex-col {
  display: flex;
  flex-direction: column;
}

.dot, .lines {
  margin-bottom: 10px;
  opacity: 0.5;
  transition: all .7s;
}

.active {
  opacity: 1;
  transition: all .7s;
}

.dot1, .line1 {
  opacity: 1;
}

.dot2 {
  transform: translateX(10px) translateY(5px);
  transition: all .7s;
  /*opacity: 0.5;*/

}

.line2 {
  transform: translateX(-5px) rotate(-30deg) translateY(-13px);
  transition: all .7s;
  /*opacity: 0.5;*/
}

.dot3 {
  transform: translateX(-10px);
  transition: all .7s;
  /*opacity: 0.5;*/
}

.line3 {
  transform: translateX(9px) translateY(-15px) rotate(70deg);
  transition: all .7s;
  /*opacity: 0.5;*/
}

.dot4 {
  transform: translateX(10px);
  transition: all .7s;
  /*opacity: 0.5;*/
}

.line4 {
  transform: translateY(-10px) rotate(-50deg) translateY(-20px) translateX(5px);
  transition: all .7s;
  /*opacity: 0.5;*/
}

.dot5 {
  transform: translateX(-15px);
  transition: all .7s;
  /*opacity: 0.5;*/
}

.line5 {
  transform: translateX(15px) rotate(45deg) translateX(-20px) translateY(-15px);
  transition: all .7s;
  /*opacity: 0.5;*/
}

</style>
