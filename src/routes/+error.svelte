<script>
  import { page } from '$app/stores';
</script>

<main class="error-container">
  <div class="error-box">
    <div class="error-content">
      <h1>4<span class="zero">0</span>4</h1>
      <p class="message">Oops! Page Not Found</p>
      <p class="description">
        The page you're looking for doesn't exist or has been moved.
      </p>
      <a href="/" class="home-button">
        <i class="fas fa-home"></i>
        Return Home
      </a>
    </div>
  </div>
</main>

<style>
  @import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css');

  .error-container {
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    padding: 1rem;
  }

  .error-box {
    background: rgba(255, 255, 255, 0.95);
    backdrop-filter: blur(10px);
    border-radius: 16px;
    padding: 3rem;
    width: 100%;
    max-width: 500px;
    text-align: center;
    box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
  }

  .error-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1.5rem;
  }

  h1 {
    font-size: 5rem;
    font-weight: 700;
    color: #1a1a1a;
    margin: 0;
    letter-spacing: 0.5rem;
  }

  .zero {
    color: #667eea;
    animation: pulse 2s infinite;
  }

  .message {
    font-size: 1.5rem;
    color: #1a1a1a;
    margin: 0;
  }

  .description {
    color: #666;
    font-size: 1rem;
    max-width: 80%;
    margin: 0 auto;
  }

  .home-button {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    text-decoration: none;
    padding: 1rem 2rem;
    border-radius: 8px;
    font-weight: 500;
    transition: all 0.3s;
    margin-top: 1rem;
  }

  .home-button:hover {
    transform: translateY(-2px);
    box-shadow: 0 4px 12px rgba(102, 126, 234, 0.2);
  }

  @keyframes pulse {
    0% { opacity: 1; }
    50% { opacity: 0.5; }
    100% { opacity: 1; }
  }

  @media (max-width: 480px) {
    h1 {
      font-size: 4rem;
    }

    .message {
      font-size: 1.2rem;
    }

    .error-box {
      padding: 2rem;
    }
  }
</style>