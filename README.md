# **GreatPages Whatsapp Float**

<a href="https://www.buymeacoffee.com/claitonllemes" target="_blank" rel="noopener noreferrer"><img src="https://user-images.githubusercontent.com/99222756/210368404-216273fb-c930-453e-b32b-e3614872eba3.png" width="100%"/></a><br>

## **Configurações**
O código abaixo adiciona um botão flutuante do Whatsapp a uma página na plataforma Greatpages. Copie e cole no menu de configurações da página.

<br><a href="https://www.buymeacoffee.com/claitonllemes" target="_blank" rel="noopener noreferrer"><img src="https://user-images.githubusercontent.com/99222756/210372197-a1d41894-8acc-470b-ac38-2bd1ee0a4ed9.png" width="100%"/></a><br>

```Html
<!-- Whatsapp Float for Greatpages v. 2.0.0 - Ⓒ Copyright 2023 Claiton Lemes. -->

<a target="_blank" href="https://wa.me/550000000000" class="float">
  <svg class="icon">
    <path
      d="M.33,48.33,3.06,35.62A23.67,23.67,0,0,1,0,24,24.06,24.06,0,0,1,24.12,0h0a23.95,23.95,0,1,1,0,47.89,24.33,24.33,0,0,1-11-2.61ZM13.7,41.08l.67.36a20.3,20.3,0,0,0,9.74,2.49A20,20,0,1,0,4,24a19.78,19.78,0,0,0,2.89,10.3l.41.68L5.52,43Z" />
    <path
      d="M34.67,31.75C34.22,33,32,34.21,31,34.31S30,35.12,24.5,33s-9-7.77-9.27-8.13S13,21.92,13,19.27a6.08,6.08,0,0,1,1.89-4.5,2,2,0,0,1,1.45-.67c.36,0,.72.05,1,.05s.77-.18,1.22.9,1.54,3.72,1.67,4a1,1,0,0,1,.05.95,3.53,3.53,0,0,1-.54.89c-.28.32-.58.71-.82.95s-.55.56-.24,1.09a16.48,16.48,0,0,0,3,3.73,14.93,14.93,0,0,0,4.37,2.68c.54.26.86.22,1.17-.14s1.36-1.58,1.72-2.12.72-.45,1.22-.26,3.17,1.47,3.71,1.74.9.41,1,.63A4.4,4.4,0,0,1,34.67,31.75Z" />
  </svg>
</a>

<style>
  :root {
    --icon-color: #ffffff;
    --gradient-normal: #2ECC71, #27AE5F;
    --gradient-hover: #2ECC71, #2ECC71;
    --pulse-color: #2ECC71;
  }

  .icon {
    width: 48px;
    height: 48px;
    transform: scale(0.6) translate(20%, 20%);
    fill: var(--icon-color);
  }

  .float {
    position: fixed;
    cursor: pointer;
    width: 60px;
    height: 60px;
    bottom: 30px;
    right: 30px;
    transition: background 2s;
    background: linear-gradient(45deg, var(--gradient-normal));
    border-radius: 50px;
    z-index: 9000;
  }

  .float:hover {
    background: linear-gradient(45deg, var(--gradient-hover));
  }

  .float:hover .icon {
    fill: var(--icon-color);
  }
</style>

<script>
  const floatBtn = document.querySelector('.float');

  function pulseAnimation() {
    const animation = floatBtn.animate(
      [
        { boxShadow: `0 0 0 0 var(--pulse-color)` },
        { boxShadow: `0 0 0 20px rgba(0, 200, 0, 0)` },
      ],
      {
        duration: 2000,
        easing: 'ease-out',
        iterations: Infinity,
      }
    );

    animation.addEventListener('iteration', (event) => {
      if (event.elapsedTime > 0) {
        floatBtn.style.boxShadow = '0 0 0 0 var(--pulse-color)';
      }
    });
  }

  pulseAnimation();
</script>
```
