
 
  <head>
    <meta charset="utf-8" />
    <title>details-menu demo</title>
    <style>
      details-menu {
        background: white;
        border: 1px solid;
        display: block;
        padding: 4px;
        width: 200px;
      }
      button,
      label[tabindex] {
        font-family: inherit;
        font-size: inherit;
        display: block;
        background: none;
        border: 0;
        width: 100%;
        text-align: left;
        padding: 0;
      }
      [aria-disabled="true"] {
        color: gray;
      }
    </style>
  </head>
  <body>
    <h1>Examples</h1>
    <h2>Base examples</h2>

    <details>
      <summary>Best robot: <span data-menu-button>Unknown</span></summary>
      <details-menu>
        <button type="button" role="menuitem" data-menu-button-text>Hubot</button>
        <button type="button" role="menuitem" data-menu-button-text>Bender</button>
        <button type="button" role="menuitem" data-menu-button-text>BB-8</button>
      </details-menu>
    </details>

    <details>
      <summary>Best robot: <span data-menu-button>Unknown</span></summary>
      <details-menu>
        <label tabindex="0" role="menuitemradio" data-menu-button-text>
          <span><input type="radio" name="robot" /> Hubot</span>
        </label>
        <label tabindex="0" role="menuitemradio" data-menu-button-text>
          <span><input type="radio" name="robot" /> Bender</span>
        </label>
        <label tabindex="0" role="menuitemradio" data-menu-button-text>
          <span><input type="radio" name="robot" /> BB-8</span>
        </label>
      </details-menu>
    </details>

    <details>
      <summary>Favorite robots</summary>
      <details-menu>
        <label tabindex="0" role="menuitemcheckbox"><input type="checkbox" name="robot" /> Hubot</label>
        <label tabindex="0" role="menuitemcheckbox"><input type="checkbox" name="robot" /> Bender</label>
        <label tabindex="0" role="menuitemcheckbox"><input type="checkbox" name="robot" /> BB-8</label>
      </details-menu>
    </details>

    <details>
      <summary data-menu-button>Favorite robots</summary>
      <details-menu>
        <button type="submit" name="robot" value="Hubot" role="menuitemradio" data-menu-button-text>Hubot</button>
        <button type="submit" name="robot" value="Bender" role="menuitemradio" data-menu-button-text>Bender</button>
        <button type="submit" name="robot" value="BB-8" role="menuitemradio" data-menu-button-text>BB-8</button>
      </details-menu>
    </details>

    <h2>`aria-disabled="true" example</h2>
    <p>menu items with <code>aria-disabled="true"</code> should be keyboard navigable</p>
    <details>
      <summary data-menu-button autofocus>Least favorite robots</summary>
      <details-menu>
        <input type="text" autofocus />
        <button name="robot" value="Hubot" aria-disabled="true" role="menuitemradio" data-menu-button-text>Hubot</button>
        <button name="robot" value="Bender" role="menuitemradio" data-menu-button-text>Bender</button>
        <button name="robot" value="BB-8" role="menuitemradio" data-menu-button-text>BB-8</button>
      </details-menu>
    </details>

    <h2>Autofocus example</h2>
    <p><code>summary</code> may have <code>autofocus</code> so it's the initially focused element in the page.</p>
    <p>
      Then any focusable element inside the popup can declare autofocus too, so it gets focus when the popup is opened.
    </p>

    <details>
      <summary data-menu-button autofocus>Autofocus picker</summary>
      <details-menu>
        <input type="text" autofocus />
        <button type="submit" name="robot" value="Hubot" role="menuitemradio" data-menu-button-text>Hubot</button>
        <button type="submit" name="robot" value="Bender" role="menuitemradio" data-menu-button-text>Bender</button>
        <button type="submit" name="robot" value="BB-8" role="menuitemradio" data-menu-button-text>BB-8</button>
      </details-menu>
    </details>

    <script type="text/javascript">
      document.addEventListener('details-menu-selected', e => console.log(e))
    </script>
    <!-- <script type="module" src="../dist/index.js"></script> -->
    <script type="module" src="https://unpkg.com/@github/details-menu-element@latest?module"></script>
  </body>
</html>

