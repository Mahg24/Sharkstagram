<script>
  export let icons;
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
      <img src="public/assets/icons/{icons.Like}.svg" alt=""/>
      <img src="public/assets/icons/{icons.Comment}.svg" alt="" />
      <img src="public/assets/icons/{icons.Send}.svg" alt="" />

    </div>
  </div>
</div>

<style>
  
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
