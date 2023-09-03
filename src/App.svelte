<!-- App.svelte -->
<script>
  import PriceCard from './lib/PriceCard.svelte';

  const products = [
    {
      title: 'Normal',
      description: 'Normal pack containes',
      price: 19.99,
      feature1: 'Free Wifi limit 1 day',
      feature2: 'Online Video',
      feature3: 'Free downloads limit 5',
      feature4:'Free clicks limit 5',
    },
    {
      title: 'Premium',
      description: 'Premium pack containes',
      price: 119.99,
      feature1: 'Unlimited Wifi',
      feature2: 'Unlimited Online Video',
      feature3: 'Unlimited Free downloads',
      feature4:'Unlimited Free clicks',
    },
  ];
</script>

<div class="app">
  {#each products as product (product.title)}
    <PriceCard
      title={product.title}
      description={product.description}
      price={product.price}
      feature1={product.feature1}
      feature2={product.feature2}
      feature3={product.feature3}
      feature4={product.feature4}

    />
  {/each}
</div>

<style>
  /* Add your app-level CSS styles here */
  .app {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
  }
</style>
