<script>
  export let icons;
  import EmojiSelector from 'svelte-emoji-selector';

  let textContent = '😛';

  function onEmoji(event) {
    textContent += event.detail;
  }
</script>

<div class="Card">
  <div class="Card-container">
    <div class="Card-header">
      <div class="Card-user">
        <div class="Card-user-img profile-pic">
          <img src="public/assets/img/profile.jpg" alt="" />
        </div>
        <h2>Shark King</h2>
      </div>
      <div class="Card-settings"><h1>...</h1></div>
    </div>
    <div class="Card-Photo">
      <img src="public/assets/img/shark.jpg" alt="" />
    </div>
    <div class="Card-icons">
      <img src="public/assets/icons/{icons.Like}.svg" class="icons-{icons.Like} cursor-pointer" alt="icons-{icons.Like} "/>
      <img src="public/assets/icons/{icons.Comment}.svg" class="icons-{icons.Comment} cursor-pointer" alt="icons-{icons.Comment}" />
      <img src="public/assets/icons/{icons.Send}.svg" class="icons-{icons.Send} cursor-pointer" alt="icons-{icons.Send}" />
    </div>

    <div class="Card-info">
      <div class="Card-info-username">
        <h3>Shark King</h3>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia beatae possimus nisi ad, quidem sapiente esse explicabo. Atque rem, saepe ea vel nobis cupiditate odit porro cum, sed, provident architecto.</p>
        <a href="/">Ver los 3666 comentarios</a>
      </div>
    </div>
    <div class="Card-comments">
     <form>
  
      <EmojiSelector on:emoji={onEmoji} />
       <button class="Emoji">😛</button>
       <textarea name="" id="" cols="30" rows="10"></textarea>
       <button>Comentar</button>
     </form>
    </div>
  </div>
</div>

<style>
  .Emoji
  {
    font-size:xx-large;
  }
  button
  {
    font-family: 'Montserrat';
    background: transparent;
    border: none;
    cursor: pointer;
    overflow: hidden;
  }
  .Card-comments textarea
  {
    width: 70%;
    height: 30px;
  }
  .Card-comments form
  {
    display: flex;
    align-items: center;
  }
  .Card-info-username a {
    font-size: small;
    color: gray;
  }
  .Card-info-username
  {
    font-size:smaller;
    font-weight:900;
  }
  .Card-header {
    display: flex;
    justify-content: space-between;
  }
  .Card {
    width: 50%;
    background-color: white;
    color: #040b23;
    display: flex;
    padding: 10px;
    margin: 15px auto;
    -webkit-box-shadow: 0px 0px 24px 0px rgba(0,0,0,0.34);
-moz-box-shadow: 0px 0px 24px 0px rgba(0,0,0,0.34);
box-shadow: 0px 0px 24px 0px rgba(0,0,0,0.34);
  }
  .Card-user {
    display: flex;
    align-items: center;
  }
  .Card-user h2 {
    margin: 20px;
  }
  .Card-icons img {
    height: 25px;
  }
  .Card-user-img {
    margin: 10px;
    width: 70px;
    height: 70px;
    border-radius: 50%;
    overflow: hidden;
    border: solid #073f71 5px;
  }
  .Card-user img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  .Card-Photo img {
    width: 100%;
  }
</style>
