<script>
  let quantity = $state(2);
  let price = $state(10);

  let total = $derived(price * quantity);

  function updatePrice() {
    price += 5; // Perbarui price
  }

  function updateQuantity() {
    quantity += 1; // Perbarui quantity
  }
</script>

<h1>Contoh kasus menggunakan derived</h1>

<p>Price: {price}</p>
<p>Quantity: {quantity}</p>
<p>Total: {total}</p>

<button onclick={updatePrice}>Increase Price</button>
<button onclick={updateQuantity}>Increase Quantity</button>
