<script>
  import CircleContainer from "./components/circle-container.svelte";
</script>

<main>
  <div id="title">
    <img src="images/logo.png" alt="Logo" />
    <h1>HOSPITAL MATASANOS</h1>
  </div>
  <CircleContainer
    src="images/interrogacion.png"
    size="35px"
    background="linear-gradient(rgb(251, 100, 0), rgb(0, 119, 182))"
    opacityImg="1"
	position="absolute"
	left="100%"
	top="50%"
	transform="translate(-100%, -25%)"
  />
  <div id="loginContainer">
    <article class="credentials">
      <h3>INICIAR SESION</h3>
      <div id="user">
        <h5>Usuario:</h5>
        <input id="inputUser" type="text" />
      </div>
      <div id="password">
        <h5>Contraseña:</h5>
        <input id="inputPassword" type="password" />
      </div>
      <button id="loginButton">INICIAR</button>
      <p>¿Problemas para iniciar sesion? <a href="help">Necesito ayuda</a></p>
    </article>
    <article class="account">
      <h3>Ultima Sesion Iniciada</h3>
      <CircleContainer
        src="images/fotoPerfil.png"
        size="200px"
        background="rgb(0, 119, 182)"
        opacityImg="0.3"
      />
      <h4>Nombre de la Cuenta</h4>
      <div id="passwordAccount">
        <input id="inputPasswordAccount" type="password" />
        <h5>CONTRASEÑA</h5>
      </div>
      <button id="accountButton">INICIAR</button>
    </article>
  </div>
</main>

<style>
  main {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
    margin: auto;
    position: relative;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }

  #title {
    display: flex;
    align-items: center;
    color: black;
    position: absolute;
    top: 30px;
    left: 50px;
  }

  #title img {
    width: 10%;
    height: 10%;
  }

  #loginContainer {
    display: flex;
    align-items: center;
    height: 650px;
    width: 1200px;
    background: linear-gradient(white, rgb(0, 119, 182));
    border-radius: 20px 20px 0px 0px;
    position: absolute;
    top: 175px;
  }

  .credentials {
    margin: 25px;
    height: 92%;
    width: 30%;
    background: linear-gradient(rgb(3, 4, 94), rgb(2, 62, 138));
    color: white;
    border-radius: 15px;
  }

  .credentials h3 {
    font-weight: 100;
    font-size: 25px;
  }

  .credentials h5 {
    font-weight: 100;
    font-size: 15px;
  }

  #user {
    padding-left: 30px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  #inputUser {
    width: 200px;
    margin-left: 15px;
    background: none;
    border: none;
    border-bottom: 1px solid;
    border-color: white;
    color: white;
    outline: none;
  }

  #password {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  #inputPassword {
    width: 200px;
    margin-left: 15px;
    background: none;
    border: none;
    border-bottom: 1px solid;
    border-color: white;
    color: white;
    outline: none;
  }

  #loginButton {
    position: relative;
    left: 30%;
    background-color: #0f468f;
    color: white;
    border-radius: 5px;
    border: none;
    cursor: pointer;
    background: linear-gradient(#0f468f, #03045e);
  }
  #loginButton:hover {
    background: linear-gradient(#165ebd, #060892);
  }

  .credentials p {
    font-size: 10px;
    position: relative;
    left: 30%;
    transform: translate(-20%);
  }
  .account {
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 80%;
    width: 60%;
    margin-left: 20px;
    border-left: solid;
    border-right: solid;
    border-image: linear-gradient(
      to bottom,
      rgb(0, 119, 182),
      rgb(255, 255, 255)
    );
    border-image-slice: 1;
  }

  h3 {
    font-weight: 250;
    font-size: 25px;
  }
  h4 {
    font-weight: 200;
    font-size: 20px;
  }

  #passwordAccount {
    display: flex;
    flex-direction: column;
    outline: none;
  }
  #passwordAccount h5 {
    position: relative;
    top: -25%;
  }

  #inputPasswordAccount {
    width: 200px;
    background: none;
    border: none;
    border-bottom: 1px solid;
    border-color: white;
    color: white;
    outline: none;
    text-align: center;
  }

  #accountButton {
    background: linear-gradient(#0f468f, #03045e);
    color: white;
    border-radius: 5px;
    border: none;
    cursor: pointer;
  }
  #accountButton:hover {
    background: linear-gradient(#165ebd, #060892);
  }
</style>
