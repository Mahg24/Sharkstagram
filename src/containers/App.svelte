<script>
  import Header from "../components/Header.svelte";
  import Main from "../components/Main.svelte";
  import Timeline from "../components/Timeline.svelte";
  import Sidebar from "../components/Sidebar.svelte";
  import Status from  "../components/Status.svelte";
  let homeIcon = "home";
  let sendIcon = "send";
  let heartIcon = "like";
  let commentIcon = "comment";
  let icons = {
    Home: homeIcon,
    Send: sendIcon,
    Like: heartIcon,
    Comment: commentIcon,
    Modyfier: handlelogos,
  };
  function handlelogos() {
    if (document.querySelector("#logos").checked) {
      icons.Home += "-sea";
      icons.Send += "-sea";
      icons.Like += "-sea";
      icons.Comment += "-sea";
    } else {
      icons.Home = "home";
      icons.Send = "send";
      icons.Like = "like";
      icons.Comment = "comment";
    }
    
  }
</script>

<Header {icons} />
<Status />
<Main>
  <Timeline {icons} />
  <Sidebar />
</Main>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,400;1,700;1,900&display=swap');

  :global(.cursor-pointer)
  {
    cursor: pointer;
  }
  :global(.icons-home:hover)
  {
    content:url("public/assets/icons/home-active.svg")
  }
  :global(.icons-send:hover)
  {
    content:url("public/assets/icons/send-active.svg")
  }
  :global(.icons-like:hover)
  {
    content:url("public/assets/icons/like-active.svg")
  }
  :global(.icons-comment:hover)
  {
    content:url("public/assets/icons/comment-active.svg")
  }
  
/* asdasdasd */

:global(.icons-home-sea:hover)
  {
    content:url("public/assets/icons/home-sea-active.svg")
  }
  :global(.icons-send-sea:hover)
  {
    content:url("public/assets/icons/send-sea-active.svg")
  }
  :global(.icons-like-sea:hover)
  {
    content:url("public/assets/icons/like-sea-active.svg")
  }
  :global(.icons-comment-sea:hover)
  {
    content:url("public/assets/icons/comment-sea-active.svg")
  }

/* aasdasdda */

  :global(html) {
    box-sizing: border-box;
    font-size: 16px;
    font-family: 'Montserrat', sans-serif;
  }
  :global(body) {
    background-color: #6daebb;
    color: white;
    margin: 0;
    padding: 0;
  }
  :global(.center) {
    justify-content: center;
    align-items: center;
  }

  :global(.profile-pic) {
    width: 90px;
    height: 90px;
    border-radius: 50%;
    overflow: hidden;
    border: solid #073f71 5px;
    cursor: pointer;
  }

  :global(.profile-pic img) {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
</style>
