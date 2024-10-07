<script>
    import Modal from "$lib/Modal.svelte";

    let showModal = false;
</script>


<main>
  <section class="intro-section">
      <h1>School Projects</h1>
      <p>
        Welcome to my page about me, you can have a look @ the projects i've made and besides that it is a sort of play/testground for applying new techniques i've learned by myself throughout this education. 
      </p>
  </section>
  <section class="map-section">
    <button on:click={() => (showModal = true)}>
      <svg width="115" height="89" viewBox="0 0 95 69" fill="none">
        <path d="M36 6H90C92.7614 6 95 8.23858 95 11V18H36V6Z" fill="#373535"/>
        <path d="M0 5C0 2.23858 2.23858 0 5 0H25C36.0457 0 45 8.95431 45 20V20H0V5Z" fill="#373535"/>
        <rect y="11.6538" width="95" height="57.3462" rx="5" fill="#545252"/>
      </svg>
      <span>Projects</span>
    </button>
  </section>
  <Modal bind:showModal>
         <!-- Passing videos into the slots -->
    <video slot="video-1" width="300" controls>
      <source src="Jackboys-test.mp4" type="video/mp4">
      Your browser does not support the video tag.
  </video>
  
  <video slot="video-2" width="300" controls>
      <source src="Jackboys-test.mp4" type="video/mp4">
      Your browser does not support the video tag.
  </video>
  
  <video slot="video-3" width="300" controls>
      <source src="Jackboys-test.mp4" type="video/mp4">
      Your browser does not support the video tag.
  </video>
  </Modal>
</main>

<style>

  main{
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .intro-section {
      display: flex;
      flex-direction: column;
      text-align: center;
      margin: 0% 10% 3em 10%;
      gap: .8em;
  }

  .map-section{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  button{
    background: inherit;
    border: none;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1em;
  }

  button:hover {
    background-color: rgba(68, 66, 66, 0.222);
    border-radius: 1em;
  }

  span {
    font-size: 1em;
    font-weight: 600;
    color: #FFFFFF;
  }

  /* #region Media queries */ 

  @media(min-width: 892px){
      .intro-section {
        margin: 0% 25% 3em 25%;
    }
  }

  @media(min-width: 1048px){
    h1 {
      font-size: var(--heading-lg);
    }
  }

  @media(min-width: 1280px){
    .intro-section {
        margin: 0% 30% 3em 30%;
    }
  }


  /* #endregion */ 
</style>