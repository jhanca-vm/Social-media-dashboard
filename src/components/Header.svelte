<style>
  header {
    display: grid;
    grid-template-columns: 1fr 140px;
    background-color: hsl(225, 100%, 98%);
    padding-top: 30px;
    padding-bottom: 160px;
    border-bottom-left-radius: 25px;
    border-bottom-right-radius: 25px;
    box-shadow: 0px 1px 3px 3px rgba(245,245,245, .9);
    position: relative;
    z-index: -2;
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
  .toggle input {
    display: none;
  }
  .toggle label {
    height: 25px;
    width: 50px;
    background-color: hsl(230, 22%, 74%);
    box-sizing: border-box;
    border-radius: 20px;
    padding: 3px 3.5px;
    cursor: pointer;
  }
  .toggle label::before {
    content: "";
    display: block;
    width: 19px;
    height: 19px;
    background-color: hsl(225, 100%, 98%);
    border-radius: 50%;
    transform: translateX(24px);
  }

  @media screen and (max-width: 768px) {
    header {
      grid-template-columns: 1fr;
    }

    .toggle {
      margin-top: 10px;
      padding-top: 10px;
      border-top: 1px solid hsl(230, 22%, 74%);
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
    <input type="checkbox">
    <label for="checkbox"></label>
  </div>
</header>