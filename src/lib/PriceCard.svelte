<!-- PriceCard.svelte -->

<script>
    // Define component properties
    export let title;
    export let description;
    export let feature1;
    export let feature2;
    export let feature3;
    export let feature4;
    export let price;
</script>

<div class="price-card">
    <div class="header">
        <h2 class="title">{title}</h2>
    </div>
    <div class="body">
        <p class="description">{description}</p>
        <hr>
        <div class="feature">
            <p class="description">{feature1}</p>
            <p class="description">{feature2}</p>
            <p class="description">{feature3}</p>
            <p class="description">{feature4}</p>
        </div>
        <p class="price">${price.toFixed(2)}</p>
    </div>
    <div class="footer">
        <button value="">choose</button>
    </div>
</div>

<style>
    .feature{
        text-align: start;
        padding: 20px;
    }
    /* Attractive CSS styles for the PriceCard */
    .price-card {
        width: 250px;
        margin: 20px;
        background-color: #fff;
        border: 1px solid #ccc;
        border-radius: 12px;
        padding: 16px;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        transition: transform 0.2s ease-in-out;
        cursor: pointer;
        overflow: hidden;
    }

    hr{
        color: #0089a1;
        background-color: #0089a1;
    }
    .price-card:hover {
        transform: scale(1.02);
    }

    .header {
        background-color: #0089a1; /* Green background for the header */
        padding: 10px;
        border-radius: 12px 12px 0 0;
    }

    .title {
        font-size: 24px;
        font-weight: bold;
        margin-bottom: 8px;
        color: #fff; /* White text color */
    }

    .body {
        padding-top: 16px;
    }

    .description {
        font-size: 16px;
        margin-bottom: 6px;
        color: #333;
    }

    .price {
        font-size: 28px;
        font-weight: bold;
        color: #0089a1; /* Green price color */
    }
    .footer button:hover {
        background-color: cadetblue;
    }
</style>
