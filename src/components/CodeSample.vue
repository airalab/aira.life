<template>
  <div class="wrapper">
    <div class="header">
      <div class="buttons">
        <svg class="day" xmlns="http://www.w3.org/2000/svg" width="13" height="13" viewBox="0 0 13 13">
          <g class="header-button" id="Ellipse_1774" data-name="Ellipse 1774" fill="var(--snippet-buttons)" stroke="#707070" stroke-width="1">
            <circle cx="6.5" cy="6.5" r="6.5" stroke="none"/>
            <circle cx="6.5" cy="6.5" r="6" fill="none"/>
          </g>
        </svg>
        <svg class="day" xmlns="http://www.w3.org/2000/svg" width="13" height="13" viewBox="0 0 13 13">
          <g class="header-button" id="Ellipse_1774" data-name="Ellipse 1774" fill="var(--snippet-buttons)" stroke="#707070" stroke-width="1">
            <circle cx="6.5" cy="6.5" r="6.5" stroke="none"/>
            <circle cx="6.5" cy="6.5" r="6" fill="none"/>
          </g>
        </svg>
        <svg class="day" xmlns="http://www.w3.org/2000/svg" width="13" height="13" viewBox="0 0 13 13">
          <g class="header-button" id="Ellipse_1774" data-name="Ellipse 1774" fill="var(--snippet-buttons)" stroke="#707070" stroke-width="1">
            <circle cx="6.5" cy="6.5" r="6.5" stroke="none"/>
            <circle cx="6.5" cy="6.5" r="6" fill="none"/>
          </g>
        </svg>

      </div>
      <div class="title">AUTONOMOUS INTELLIGENT ROBOT AGENT</div>
    </div>
    <div class="content">
      <div class="download">
        <p>Download <a href="https://github.com/airalab/aira/releases">AIRA distribution (x86_64 || AArch64) -></a></p>
        <p>or build it from source:</p>
      </div>
      <div class="code">
        $ curl https://nixos.org/nix/install | sh <br/>
        $ git clone —recursive https://github.com/airalab/aira && cd aira<br/>
        $ make<br/>
      </div>
      <a class="docs" href="https://wiki.robonomics.network/docs/aira-overview/">Documentation -></a>
    </div>
  </div>
</template>

<script>
export default {
  name: "CodeSample"
}
</script>

<style scoped>

@media screen and (min-width: 1440px) and (max-width: 1700px){

  .wrapper {
    width: 500px;
    background-color: #171F24;
  }

}

@media screen and (max-width: 1065px) {

  .wrapper {
    width: 650px;
    max-height: 400px;
    transition: all .5s;
  }

  .wrapper .content {
    margin-top: 10px;
    margin-left: 30px;
    transition: all .5s;
    width: calc(100% - 60px);
  }

  .wrapper .docs {
    margin-top: 10px;
  }

}

@media screen and (max-height: 670px) {
  .content .download p {
    margin-block-start: 5px;
    margin-block-end: 5px;
    transition: all .7s;
  }
  .content .download p:last-child {
    margin-block-end: 15px;
    transition: all .7s;
  }
  .content .code {
    padding-top: 15px;
    padding-bottom: 15px;
    transition: all .7s;
  }
  div.wrapper {
    height: 320px;
    transition: all .7s;
  }
}

div {
  font-family: Roboto, sans-serif;
}

.wrapper {
  transition: all .5s;
  margin-top: 80px;
  border: 1px solid var(--snippet-border);
  background-color: var(--secondary);
  width: 900px;
  height: 470px;
  box-shadow: 20px 20px 0 var(--main);
  display: flex;
  flex-direction: column;
  color: var(--gray-inverted)
}

.header {
  transition: all .5s;
  width: 100%;
  height: 60px;
  background-color: var(--gray);
  display: flex;
  align-items: center;
}

.header-button {
  transition: all .5s;
}

.buttons {
  align-items: center;
  margin-left: 20px;
}

.title {
  margin-left: 90px;
  font-weight: 300;
  font-size: 20pt;
}

svg.day, svg.night {
  transform: scale(1.5);
  margin: 10px;
}

.night {
  display: none;
}

.content {
  margin-left: 135px;
  margin-top: 20px;
  /*border: 1px solid black;*/
  width: calc(100% - 200px);

  font-size: 18pt;
  font-weight: 600;
}

.download {
  font-weight: 600;
}

a {
  transition: all .5s;
  color: var(--main);
  text-decoration: none;
  display: inline;
}

.code {
  transition: all .5s;
  background-color: var(--gray);
  padding: 30px 30px 30px 10px;
  font-family: Roboto Mono, sans-serif;
  font-weight: 400;
  font-size: 11pt;
  color: var(--secondary-inverted)
}

.docs {
  display: block;
  margin-top: 50px;
}

</style>