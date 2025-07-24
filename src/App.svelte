<script>
  let audience = "";
  let struggle = "";
  let transformation = "";
  let format = "";
  let irresistible = "";

  $: generatedPrompt = `
Create a ${format} for ${audience} who are struggling with ${struggle}.
Help them achieve ${transformation} in a way that feels exciting and irresistible.
Make sure it includes ${irresistible}.

Use a warm, clear, and motivating tone.
Format it for easy delivery as a digital product.
Make the reader feel seen and empowered.
  `;

  function copyToClipboard() {
    navigator.clipboard.writeText(generatedPrompt)
      .then(() => alert("✅ Prompt copied to clipboard!"))
      .catch(err => alert("❌ Failed to copy. Please try again."));
  }
</script>

<main>
  <img src="/logo.png" alt="So Pretty Logo" class="logo" />

  <h1>🎯 Irresistible Digital Product Prompt Builder</h1>
  <p class="intro">Fill out the fields below to generate a powerful ChatGPT prompt for your product idea:</p>

  <label>
    1. Who is your audience or niche?
    <input bind:value={audience} placeholder="e.g. Christian moms, Etsy sellers" />
  </label>

  <label>
    2. What are they struggling with right now?
    <input bind:value={struggle} placeholder="e.g. feeling overwhelmed, low sales" />
  </label>

  <label>
    3. What transformation do you want to help them achieve?
    <input bind:value={transformation} placeholder="e.g. peace, more confidence, sales" />
  </label>

  <label>
    4. What format do you want to deliver it in?
    <input bind:value={format} placeholder="e.g. printable planner, swipe file, email challenge" />
  </label>

  <label>
    5. What would make this product absolutely irresistible?
    <input bind:value={irresistible} placeholder="e.g. fast results, bonus templates, beautiful design" />
  </label>

  <h2>✨ Your ChatGPT Prompt</h2>
  <pre>{generatedPrompt}</pre>

  <button on:click={copyToClipboard}>📋 Copy to Clipboard</button>
</main>

<style>
  main {
    max-width: 700px;
    margin: auto;
    padding: 2em;
    background-color: #f6c8cc;
    font-family: 'Segoe UI', sans-serif;
    border-radius: 12px;
    box-shadow: 0 0 15px rgba(0,0,0,0.05);
  }

  .logo {
    display: block;
    max-width: 200px;
    margin: 0 auto 1.5em auto;
  }

  h1 {
    text-align: center;
    color: #5bb0ba;
    font-size: 1.75em;
    margin-bottom: 0.5em;
  }

  .intro {
    text-align: center;
    color: #333;
    margin-bottom: 1.5em;
  }

  label {
    display: block;
    margin: 1.2em 0 0.5em 0;
    color: #c15b78;
    font-weight: 600;
  }

  input {
    display: block;
    width: 100%;
    padding: 0.6em;
    font-size: 1em;
    border: 2px solid #5bb0ba;
    border-radius: 8px;
    background-color: #ebf5f7;
  }

  pre {
    white-space: pre-wrap;
    background: white;
    padding: 1em;
    border-radius: 10px;
    border: 1px solid #ccc;
    font-size: 0.95em;
    margin-top: 1.5em;
  }

  button {
    background-color: #c15b78;
    color: white;
    border: none;
    padding: 0.8em 1.2em;
    margin-top: 1em;
    font-size: 1em;
    border-radius: 6px;
    cursor: pointer;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }

  button:hover {
    background-color: #a84562;
  }
</style>

