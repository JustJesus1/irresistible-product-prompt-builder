<script>
  let audience = "";
  let struggle = "";
  let transformation = "";
  let format = "";
  let irresistible = "";
</script>

<main style="max-width: 700px; margin: auto; font-family: sans-serif;">
  <h1>🎯 Irresistible Digital Product Prompt Builder</h1>
  <p>Fill out the fields below to generate a powerful ChatGPT prompt for your product idea:</p>

  <label>
    <strong>1. Who is your audience or niche?</strong><br />
    <input bind:value={audience} placeholder="e.g. Christian moms, Etsy sellers" />
  </label>

  <label>
    <strong>2. What are they struggling with right now?</strong><br />
    <input bind:value={struggle} placeholder="e.g. feeling overwhelmed, low sales" />
  </label>

  <label>
    <strong>3. What transformation do you want to help them achieve?</strong><br />
    <input bind:value={transformation} placeholder="e.g. peace, more confidence, sales" />
  </label>

  <label>
    <strong>4. What format do you want to deliver it in?</strong><br />
    <input bind:value={format} placeholder="e.g. printable planner, swipe file, email challenge" />
  </label>

  <label>
    <strong>5. What would make this product absolutely irresistible?</strong><br />
    <input bind:value={irresistible} placeholder="e.g. fast results, bonus templates, beautiful design" />
  </label>

  <hr />

  <h2>✨ Your ChatGPT Prompt</h2>
  <pre style="white-space: pre-wrap; background: #f9f9f9; padding: 1em; border-radius: 8px;">
Create a {format} for {audience} who are struggling with {struggle}.
Help them achieve {transformation} in a way that feels exciting and irresistible.
Make sure it includes {irresistible}.

Use a warm, clear, and motivating tone.
Format it for easy delivery as a digital product.
Make the reader feel seen and empowered.
  </pre>
</main>

<style>
  input {
    display: block;
    width: 100%;
    margin: 0.5em 0 1em 0;
    padding: 0.5em;
    font-size: 1em;
  }
  label {
    display: block;
    margin-top: 1em;
  }
</style>
