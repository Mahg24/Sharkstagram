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
    onHover:onHover,
    onLeave:onLeave
  };
  function onHover(item) 
  {
    if (!icons[item].includes("-active")) {
      icons[item] += "-active";
    }else
    {
      icons[item]=icons[item].replace("-active","");
    }
      
      // icons.Home += "-active";
      // icons.Send += "-active";
      // icons.Like += "-active";
      // icons.Comment += "-active";
  }
  function onLeave(item)
  {
    icons[item].replace("-active","");
  }
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
  :global(html) {
    box-sizing: border-box;
    font-size: 16px;
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
