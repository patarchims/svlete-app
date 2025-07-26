<script>
  let email = '';
  let password = '';

  function handleSubmit() {
    console.log('Login attempt:', { email });
  }
</script>

<main class="login-container">
  <div class="login-box">
    <div class="header">
      <!-- <img src="/logo.png" alt="Logo" class="logo" /> -->
      <h1>Welcome Back</h1>
      <p class="subtitle">Please enter your details to sign in</p>
    </div>
    
    <form on:submit|preventDefault={handleSubmit} class="login-form">
      <div class="form-group">
        <label for="email">Email</label>
        <div class="input-wrapper">
          <i class="fas fa-envelope"></i>
          <input 
            type="email" 
            id="email"
            placeholder="Enter your email"
            bind:value={email}
            required
          />
        </div>
      </div>

      <div class="form-group">
        <label for="password">Password</label>
        <div class="input-wrapper">
          <i class="fas fa-lock"></i>
          <input 
            type="password" 
            id="password"
            placeholder="Enter your password"
            bind:value={password}
            required
          />
        </div>
      </div>



      <button type="submit">Sign In</button>
    </form>
  </div>
</main>

<style>
  @import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css');

  .login-container {
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    padding: 1rem;
  }

  .login-box {
    background: rgba(255, 255, 255, 0.95);
    backdrop-filter: blur(10px);
    border-radius: 16px;
    padding: 2.5rem;
    width: 100%;
    max-width: 450px;
    box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
  }

  .header {
    text-align: center;
    margin-bottom: 2rem;
  }



  h1 {
    color: #1a1a1a;
    font-size: 1.8rem;
    margin-bottom: 0.5rem;
  }

  .subtitle {
    color: #666;
    font-size: 0.9rem;
  }

  .login-form {
    display: flex;
    flex-direction: column;
    gap: 1.2rem;
  }

  .form-group {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
  }

  label {
    color: #4a5568;
    font-size: 0.9rem;
    font-weight: 500;
  }

  .input-wrapper {
    position: relative;
  }

  .input-wrapper i {
    position: absolute;
    left: 1rem;
    top: 50%;
    transform: translateY(-50%);
    color: #a0aec0;
  }

  input {
    width: 100%;
    padding: 0.75rem 1rem 0.75rem 2.5rem;
    border: 1px solid #e2e8f0;
    border-radius: 8px;
    font-size: 1rem;
    transition: all 0.3s;
  }

  input:focus {
    outline: none;
    border-color: #667eea;
    box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1);
  }

  .options {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 0.5rem;
  }

  .remember-me {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    cursor: pointer;
  }

  .forgot-link {
    color: #667eea;
    text-decoration: none;
    font-size: 0.9rem;
  }

  .forgot-link:hover {
    text-decoration: underline;
  }

  button {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 1rem;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    font-size: 1rem;
    font-weight: 500;
    transition: all 0.3s;
  }

  button:hover {
    transform: translateY(-1px);
    box-shadow: 0 4px 12px rgba(102, 126, 234, 0.2);
  }
</style>