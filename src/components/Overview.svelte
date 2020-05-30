<script>
  import overviewData from './overview-data.js';
</script>

<style>
  h1 {
    font-size: 25px;
    color: var(--text-tl);
  }

  h3 {
    font-size: 16px;
    color: var(--text);
  }

  section {
    padding-top: 32px;
    padding-bottom: 40px;
    margin: 0 auto;
  }

  .data {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    column-gap: 2.5em;
    row-gap: 2em;
    padding-top: 10px;
  }

  .items {
    background-color: var(--card);
    border-radius: 5px;
    padding: 15px 30px;
    cursor: pointer;
  }
  .items span {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .items .logo {
    height: 25px;
  }
  .items h2 {
    font-size: 36px;
    margin: 12px 0 8px;
  }
  .items p {
   margin-left: 4px;
   font-weight: 700;
   color: hsl(163, 72%, 41%);
  }

  .items:hover {
    background-color: var(--hover);
  }

  .likes-fb p, .likes-yt p, .total-views p {
    color: hsl(356, 69%, 56%);
  }

  @media screen and (max-width: 1200px) {
    .data {
      grid-template-columns: repeat(3, 1fr);
    }
  }
 @media screen and (max-width: 900px) {
    .data {
      grid-template-columns: repeat(2, 1fr);
    }
  }
 @media screen and (max-width: 576px) {
    .data {
      grid-template-columns: 1fr;
      row-gap: 25px;
    }
  }
</style>

<section class="container">
  <h1>Overview - Today</h1>
  <div class="data">
    {#each overviewData as item}
      <div class="items {item.class}">
        <span>
          <h3>{item.name}</h3>
          <img class="logo" src={item.logo} alt="logo">
        </span>
        <span>
          <h2>{item.num}</h2>
          <span>
            <img src={item.icon} alt="icon">
            <p>{item.percent}</p>
          </span>
        </span>
      </div>
    {/each}
  </div>
</section>