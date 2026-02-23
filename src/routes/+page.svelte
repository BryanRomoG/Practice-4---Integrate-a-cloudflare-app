<script>
  // Simulación simple de IA generando mensaje dinámico
  let hora = new Date().getHours();

  function saludoIA() {
    if (hora < 12) return "Buenos días";
    if (hora < 19) return "Buenas tardes";
    return "Buenas noches";
  }

  const mensajeIA = `
    Esta aplicación fue modificada utilizando Inteligencia Artificial 🤖.
    El contenido fue generado dinámicamente según la hora actual.
  `;
</script>

<svelte:head>
  <title>Practice 4 - Cloudflare + IA</title>
  <meta name="description" content="Proyecto desplegado en Cloudflare con modificaciones usando IA">
</svelte:head>

<main>
  <h1>🚀 Practice 4 - Cloudflare Deployment</h1>
  <h2>{saludoIA()}, Bryan 👋</h2>

  <div class="card">
    <p>{mensajeIA}</p>
    <p><strong>Hora actual:</strong> {new Date().toLocaleTimeString()}</p>
  </div>

  <footer>
    <p>Proyecto desarrollado con SvelteKit + Cloudflare Workers</p>
  </footer>
</main>

<style>
  main {
    font-family: Arial, sans-serif;
    text-align: center;
    padding: 2rem;
    background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
    min-height: 100vh;
    color: white;
  }

  h1 {
    font-size: 2.5rem;
  }

  h2 {
    margin-bottom: 2rem;
    color: #00ffd5;
  }

  .card {
    background: rgba(255, 255, 255, 0.1);
    padding: 2rem;
    border-radius: 12px;
    backdrop-filter: blur(10px);
    width: 60%;
    margin: auto;
  }

  footer {
    margin-top: 3rem;
    font-size: 0.9rem;
    opacity: 0.8;
  }
</style>