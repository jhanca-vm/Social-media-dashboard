<script>
  import cardsData from './cards-data.js';
</script>

<style>
  section {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    column-gap: 2.5em;
    margin: 0 auto;
    text-align: center;
    position: relative;
    z-index: 1;
  }

 .card {
   display: flex;
   flex-direction: column;
   align-items: center;
   padding: 25px 0 15px;
   background-color: var(--card);
   border-radius: 5px;
   margin-top: -125px;
   cursor: pointer;
 }
 .card:hover {
   background-color: var(--hover);
 }

 .red-social {
   display: flex;
   align-items: center;
   font-weight: 700;
 }
 .red-social img {
   margin-right: 10px;
   height: 25px;
 }

 .total {
   margin: 12px 0;
 }
 .total h2 {
   margin: 0;
   font-size: 60px;
 }
 .total p {
   margin-top: 4px;
   margin-bottom: 7px;
   font-size: 13.5px;
   text-transform: uppercase;
   letter-spacing: 6px;
 }

 .tracking {
   display: flex;
   align-items: center;
 }
 .tracking img {
   height: 6px;
 }
 .tracking p {
   margin-left: 6px;
   font-weight: 700;
   color: hsl(163, 72%, 41%);
 }

 .facebook {
   border-top: 5px solid hsl(208, 92%, 53%);
 }

 .twitter {
   border-top: 5px solid hsl(203, 89%, 53%);
 }

 .instagram {
   border-top: 5px solid transparent;
   background-clip: padding-box;
   position: relative;
 }
 .instagram::before {
    content: '';
    position: absolute;
    top: 0; right: 0; bottom: 0; left: 0;
    z-index: -1;
    margin: -5px 0 2px;
    border-radius: inherit;
    background: linear-gradient(to right, hsl(37, 97%, 70%), hsl(329, 70%, 58%));
 }

 .youtube {
   border-top: 5px solid hsl(348, 97%, 39%);
 }
 .youtube .tracking p {
   color: hsl(356, 69%, 56%);
 }

 @media screen and (max-width: 1200px) {
   section {
    grid-template-columns: repeat(3, 1fr);
    row-gap: 160px;
   }
 }
 @media screen and (max-width: 900px) {
   section {
    grid-template-columns: repeat(2, 1fr);
    row-gap: 160px;
   }
 }
 @media screen and (max-width: 576px) {
   section {
    grid-template-columns: 1fr;
    row-gap: 150px;
   }
 }
</style>

<section class="container">
  {#each cardsData as item}  
    <div class="card {item.name}">
      <div class="red-social">
        <img src={item.icon} alt={item.name}>
        <p>{item.user}</p>
      </div>
      <div class="total">
        <h2>{item.quantity}</h2>
        <p>{item.of}</p>
      </div>
      <div class="tracking">
        <img src={item.iconTracking} alt="icon">
        <p>{item.tracking}</p>
      </div>
    </div>
  {/each}
</section>