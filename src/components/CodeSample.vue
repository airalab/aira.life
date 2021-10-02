<template>
  <div class="wrapper">
    <div class="header">
      <div class="buttons">
        <svg class="day" xmlns="http://www.w3.org/2000/svg" width="13" height="13" viewBox="0 0 13 13">
          <g id="Ellipse_1774" data-name="Ellipse 1774" fill="#fff" stroke="#707070" stroke-width="1">
            <circle cx="6.5" cy="6.5" r="6.5" stroke="none"/>
            <circle cx="6.5" cy="6.5" r="6" fill="none"/>
          </g>
        </svg>
        <svg class="day" xmlns="http://www.w3.org/2000/svg" width="13" height="13" viewBox="0 0 13 13">
          <g id="Ellipse_1774" data-name="Ellipse 1774" fill="#fff" stroke="#707070" stroke-width="1">
            <circle cx="6.5" cy="6.5" r="6.5" stroke="none"/>
            <circle cx="6.5" cy="6.5" r="6" fill="none"/>
          </g>
        </svg>
        <svg class="day" xmlns="http://www.w3.org/2000/svg" width="13" height="13" viewBox="0 0 13 13">
          <g id="Ellipse_1774" data-name="Ellipse 1774" fill="#fff" stroke="#707070" stroke-width="1">
            <circle cx="6.5" cy="6.5" r="6.5" stroke="none"/>
            <circle cx="6.5" cy="6.5" r="6" fill="none"/>
          </g>
        </svg>

<!--    // Night buttons    -->
        <svg class="night" xmlns="http://www.w3.org/2000/svg" width="13" height="13" viewBox="0 0 13 13">
          <g id="Ellipse_1774" data-name="Ellipse 1774" fill="#171f24" stroke="#707070" stroke-width="1">
            <circle cx="6.5" cy="6.5" r="6.5" stroke="none"/>
            <circle cx="6.5" cy="6.5" r="6" fill="none"/>
          </g>
        </svg>
        <svg class="night" xmlns="http://www.w3.org/2000/svg" width="13" height="13" viewBox="0 0 13 13">
          <g id="Ellipse_1774" data-name="Ellipse 1774" fill="#171f24" stroke="#707070" stroke-width="1">
            <circle cx="6.5" cy="6.5" r="6.5" stroke="none"/>
            <circle cx="6.5" cy="6.5" r="6" fill="none"/>
          </g>
        </svg>
        <svg class="night" xmlns="http://www.w3.org/2000/svg" width="13" height="13" viewBox="0 0 13 13">
          <g id="Ellipse_1774" data-name="Ellipse 1774" fill="#171f24" stroke="#707070" stroke-width="1">
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

div {
  font-family: Roboto, sans-serif;
}
.wrapper {
  transition: all 1s;
  margin-top: 0;
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
  transition: all 1s;
  width: 100%;
  height: 60px;
  background-color: var(--gray);
  display: flex;
  align-items: center;
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
  transition: all 1s;
  color: var(--main);
  text-decoration: none;
  display: inline;
}

.code {
  transition: all 1s;
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