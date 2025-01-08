## Tailwind CSS Language Variant Plugin

This Tailwind CSS plugin adds a new variant called `lang-{language}` that can be used to style elements based on their language. This can be useful for creating multilingual websites or applications.

## Installation

1. Install the plugin using npm or Yarn:

    ```bash
    # Using npm
    npm install -D @ganmahmud/tailwindcss-language-variant
    ```
    ```bash
    # Using Yarn
    yarn add -D @ganmahmud/tailwindcss-language-variant
    ```
2. Add the plugin to your `tailwind.config.js` file. Add as many languages as you like using the `languages` option in theme configuration.

    ```js
    // tailwind.config.js
    module.exports = {
      theme: {
        languages: ['bn', 'en', 'hr'],
      },
      plugins: [
        require('@ganmahmud/tailwindcss-language-variant'),
      ],
    }
    ```
3. The plugin needs a `lang` attribute in your HTML tag to work. You can then use the `lang-{language}` variant in your HTML like this:

    ```html
    <html lang="bn">
      <body>
        <h1 class="lang-bn:font-bold">Hello world!</h1>
      </body>
    </html>
    ```

    This will result in the following CSS:
    
    ```css
    [lang="bn"] .lang-bn\:font-bold {
        font-weight: 700;
    }
    ```

    ## Changelog
    -  `1.0.1`: Fixed languge config type issue
    -  `1.0.0`: Initial release 
