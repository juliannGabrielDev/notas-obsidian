---
tags:
  - css
  - efectos
---
<div class="dt-body">
  <label for="dt-toggle-theme" class="dt-theme-button">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"  fill="currentColor"  class="dt-dark icon icon-tabler icons-tabler-filled icon-tabler-brightness-down"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M12 8a4 4 0 1 1 -3.995 4.2l-.005 -.2l.005 -.2a4 4 0 0 1 3.995 -3.8z" /><path d="M12 4a1 1 0 0 1 .993 .883l.007 .127a1 1 0 0 1 -1.993 .117l-.007 -.127a1 1 0 0 1 1 -1z" /><path d="M17 6a1 1 0 0 1 .993 .883l.007 .127a1 1 0 0 1 -1.993 .117l-.007 -.127a1 1 0 0 1 1 -1z" /><path d="M19 11a1 1 0 0 1 .993 .883l.007 .127a1 1 0 0 1 -1.993 .117l-.007 -.127a1 1 0 0 1 1 -1z" /><path d="M17 16a1 1 0 0 1 .993 .883l.007 .127a1 1 0 0 1 -1.993 .117l-.007 -.127a1 1 0 0 1 1 -1z" /><path d="M12 18a1 1 0 0 1 .993 .883l.007 .127a1 1 0 0 1 -1.993 .117l-.007 -.127a1 1 0 0 1 1 -1z" /><path d="M7 16a1 1 0 0 1 .993 .883l.007 .127a1 1 0 0 1 -1.993 .117l-.007 -.127a1 1 0 0 1 1 -1z" /><path d="M5 11a1 1 0 0 1 .993 .883l.007 .127a1 1 0 0 1 -1.993 .117l-.007 -.127a1 1 0 0 1 1 -1z" /><path d="M7 6a1 1 0 0 1 .993 .883l.007 .127a1 1 0 0 1 -1.993 .117l-.007 -.127a1 1 0 0 1 1 -1z" /></svg>
    
      <svg  xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"  fill="currentColor"  class="dt-light icon icon-tabler icons-tabler-filled icon-tabler-moon"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M12 1.992a10 10 0 1 0 9.236 13.838c.341 -.82 -.476 -1.644 -1.298 -1.31a6.5 6.5 0 0 1 -6.864 -10.787l.077 -.08c.551 -.63 .113 -1.653 -.758 -1.653h-.266l-.068 -.006l-.06 -.002z" /></svg>
  </label>
  <input type="checkbox" id="dt-toggle-theme" />
  <h1>Dark Theme</h1>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
</div>

CSS:
```css
:root {
  --font: #1a2e05;
  --bg-main: #f7fee7;
  --bg-secondary: #4d7c0f;
  
  --theme-button-icon: #bef264;
  --icon-light: block;
  --icon-dark: none;
}
:root:has(#dt-toggle-theme:checked) {
  --font: #f7fee7;
  --bg-main: #1a2e05;
  --bg-secondary: #bef264;
  
  --theme-button-icon: #4d7c0f;
  --icon-light: none;
  --icon-dark: block;
}
#dt-toggle-theme {
  display: none;
}
.dt-theme-button {
  background-color: var(--bg-secondary);
  background-position: center;
  background-repeat: no-repeat;
  color: var(--theme-button-icon);
  display: grid;
  place-items: center;
  position: fixed;
  top: 16px;
  right: 16px;
  width: 40px;
  height: 40px;
  border-radius: 8px;
}
.dt-theme-button svg.dt-light {
  display: var(--icon-light);
  width: 24px;
  height: 24px;
}
.dt-theme-button svg.dt-dark {
  display: var(--icon-dark);
  width: 32px;
  height: 32px;
}
.dt-body {
  color: var(--font);
  background-color: var(--bg-main);
  transition: color 300ms, background-color 300ms;
}
```