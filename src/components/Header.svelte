<script>
  let styles = { darkMode: true };

  function toggle() {
    styles.darkMode = !styles.darkMode;
    window.document.body.classList.toggle('dark-mode');
  };

  toggle();
</script>

<style>
  header {
    display: grid;
    grid-template-columns: 1fr 140px;
    background-color: var(--top-bg);
    padding-top: 35px;
    padding-bottom: 160px;
    border-bottom-left-radius: 25px;
    border-bottom-right-radius: 25px;
    box-shadow: var(--shadow);
  }

  h1 {
    margin: 0;
  }

  p {
    font-weight: 700;
  }

  .followers {
    margin-top: 5px;
  }

  .toggle {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  
  label {
    height: 25px;
    width: 50px;
    background: var(--toggle);
    box-sizing: border-box;
    border-radius: 20px;
    padding: 3px 3.5px;
    cursor: pointer;
  }
  label::before {
    content: "";
    display: block;
    width: 19px;
    height: 19px;
    background-color: var(--top-bg);
    border-radius: 50%;
    transform: var(--transform);
    transition: .3s;
  }

  @media screen and (max-width: 768px) {
    header {
      grid-template-columns: 1fr;
    }

    .toggle {
      margin-top: 10px;
      padding-top: 10px;
      border-top: var(--border-top);
    }
  }
</style>

<header class="container">
  <div>
    <h1>Social Media Dashboard</h1>
    <p class="followers">Total Followers: 23,004</p>
  </div>
  <div class="toggle">
    <p>Dark Mode</p>
    <label on:click={toggle}></label>
  </div>
</header>