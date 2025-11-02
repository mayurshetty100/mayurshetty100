<style>
  @keyframes glowPulse {
    0%, 100% { 
      box-shadow: 0 0 20px rgba(0, 212, 255, 0.5), 0 0 40px rgba(102, 126, 234, 0.3);
    }
    50% { 
      box-shadow: 0 0 40px rgba(0, 212, 255, 0.8), 0 0 80px rgba(102, 126, 234, 0.6);
    }
  }
  
  @keyframes starGlow {
    0%, 100% { opacity: 0.4; }
    50% { opacity: 1; }
  }
  
  @keyframes gradientFlow {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
  }
  
  @keyframes slideDown {
    from {
      opacity: 0;
      transform: translateY(-30px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
  
  @keyframes colorShift {
    0% { filter: hue-rotate(0deg); }
    33% { filter: hue-rotate(180deg); }
    66% { filter: hue-rotate(280deg); }
    100% { filter: hue-rotate(360deg); }
  }

  
  .gradient-text {
    background: linear-gradient(90deg, #00d4ff 0%, #764ba2 25%, #ff00ff 50%, #00d4ff 75%, #764ba2 100%);
    background-size: 300% 300%;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    animation: gradientFlow 6s ease infinite;
    display: inline-block;
    font-family: 'Arial Black', sans-serif;
  }
  
  .glow-divider {
    height: 2px;
    background: linear-gradient(90deg, transparent, #00d4ff, #764ba2, #ff00ff, transparent);
    box-shadow: 0 0 20px rgba(0, 212, 255, 0.6), 0 0 40px rgba(255, 0, 255, 0.4);
    margin: 20px 0;
    animation: glowPulse 3s ease-in-out infinite;
  }
  
  .stars {
    position: relative;
  }
  
  .star {
    display: inline-block;
    position: relative;
    animation: starGlow 2s ease-in-out infinite;
  }
</style>

<div align="center">

<div style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); padding: 60px 40px; border-radius: 20px; margin: 20px auto; max-width: 800px; box-shadow: 0 20px 60px rgba(102, 126, 234, 0.4); animation: glowPulse 3s ease-in-out infinite; position: relative; overflow: hidden;">

<!-- Glowing Star Background -->
<div style="position: absolute; top: 10px; left: 20px; font-size: 1.5em; opacity: 0.6; animation: starGlow 2s ease-in-out infinite;">✨</div>
<div style="position: absolute; top: 30px; right: 30px; font-size: 1.2em; opacity: 0.5; animation: starGlow 2.5s ease-in-out infinite;">⭐</div>
<div style="position: absolute; bottom: 20px; left: 40px; font-size: 1.3em; opacity: 0.6; animation: starGlow 2.2s ease-in-out infinite;">💫</div>
<div style="position: absolute; bottom: 30px; right: 50px; font-size: 1.4em; opacity: 0.5; animation: starGlow 2.8s ease-in-out infinite;">✨</div>

<!-- Content -->
<div style="position: relative; z-index: 10;">

<h1 class="gradient-text" style="font-size: 4em; font-weight: 900; margin: 0; text-shadow: 0 4px 20px rgba(0, 0, 0, 0.3); letter-spacing: 2px; animation: slideDown 0.8s ease;">
MAYUR SHETTY
</h1>

<div class="glow-divider"></div>

<img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=28&duration=3000&pause=500&color=00D4FF&center=true&width=700&height=60&lines=Unleash+The+Power+Of+Imagination;Where+creativity+meets+code;Ideas+become+reality" alt="Typing Animation" style="margin: 20px 0; animation: colorShift 9s ease-in-out infinite;" />

<div class="glow-divider"></div>

<p style="font-size: 1.1em; color: #e0e0e0; margin-top: 15px; font-style: italic; animation: slideDown 1.2s ease;">
✨ Where creativity meets code, and ideas become reality ✨
</p>

</div>

</div>

</div>
