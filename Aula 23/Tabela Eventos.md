# Tabela de Eventos em JavaScript

|        Evento       |                      Descrição                     |                          Exemplo                           |
|:-------------------:|:--------------------------------------------------:|:----------------------------------------------------------:|
|       `click`       |    Ocorre quando o usuário clica em um elemento.    | `element.addEventListener('click', () => { alert('Clicked!'); });` |
|     `dblclick`      | Ocorre quando o usuário clica duas vezes em um elemento. | `element.addEventListener('dblclick', () => { alert('Double Clicked!'); });` |
|    `mouseover`      | Ocorre quando o ponteiro do mouse passa sobre um elemento. | `element.addEventListener('mouseover', () => { console.log('Mouse Over'); });` |
|     `mouseout`      | Ocorre quando o ponteiro do mouse sai de um elemento. | `element.addEventListener('mouseout', () => { console.log('Mouse Out'); });` |
|    `mousedown`      |   Ocorre quando o botão do mouse é pressionado.    | `element.addEventListener('mousedown', () => { console.log('Mouse Down'); });` |
|     `mouseup`       |    Ocorre quando o botão do mouse é solto.         | `element.addEventListener('mouseup', () => { console.log('Mouse Up'); });` |
|    `mousemove`      | Ocorre quando o ponteiro do mouse se move sobre um elemento. | `element.addEventListener('mousemove', () => { console.log('Mouse Move'); });` |
|     `keydown`       |   Ocorre quando uma tecla é pressionada.           | `document.addEventListener('keydown', (e) => { console.log('Key Down:', e.key); });` |
|      `keyup`        |     Ocorre quando uma tecla é solta.               | `document.addEventListener('keyup', (e) => { console.log('Key Up:', e.key); });` |
|    `keypress`       | Ocorre quando uma tecla é pressionada e solta.     | `document.addEventListener('keypress', (e) => { console.log('Key Press:', e.key); });` |
|      `focus`        |  Ocorre quando um elemento recebe foco.            | `element.addEventListener('focus', () => { console.log('Focused'); });` |
|      `blur`         |  Ocorre quando um elemento perde o foco.           | `element.addEventListener('blur', () => { console.log('Blurred'); });` |
|     `change`        | Ocorre quando o valor de um elemento `<input>` ou `<select>` muda. | `element.addEventListener('change', (e) => { console.log('Changed:', e.target.value); });` |
|     `submit`        |    Ocorre quando um formulário é enviado.          | `form.addEventListener('submit', (e) => { e.preventDefault(); console.log('Form Submitted'); });` |
|      `input`        |  Ocorre quando o valor de um campo de entrada muda. | `input.addEventListener('input', (e) => { console.log('Input Value:', e.target.value); });` |
|     `scroll`        | Ocorre quando a visualização do documento é rolada. | `window.addEventListener('scroll', () => { console.log('Scrolled'); });` |
|     `resize`        | Ocorre quando a janela do navegador é redimensionada. | `window.addEventListener('resize', () => { console.log('Resized'); });` |
|      `load`         |  Ocorre quando a página é completamente carregada.  | `window.addEventListener('load', () => { console.log('Page Loaded'); });` |
|     `unload`        |  Ocorre quando o usuário fecha a página.            | `window.addEventListener('unload', () => { console.log('Page Unloaded'); });` |
|  `contextmenu`      | Ocorre quando o menu de contexto (botão direito) é aberto. | `element.addEventListener('contextmenu', (e) => { e.preventDefault(); console.log('Context Menu Opened'); });` |
