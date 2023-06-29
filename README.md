# Hugo Shortcodes

Some [shortcodes][hugo_shortcodes] for [Hugo][], which you can add to
your website as a [Hugo Module][hugo_mods] :sparkles:

## Install

1. Enable modules in your repository (**skip this step** if you already
   have a `go.mod` file in your repo):

   ```bash
   hugo mod init github.com/$username/$reponame
   ```

2. Add this module to your website by adding it to your `config.toml`:

   ```toml
   [module]
     [[module.imports]]
       path = "github.com/afiorillo/hugo-shortcodes"
   ```

3. Run Hugo. This will download the latest version of the module.

   ```bash
   hugo server -v -D
   ```

## Update

You can update this module with:

```bash
hugo mod get -u github.com/afiorillo/hugo-shortcodes
```

Or you can update **all** modules defined in your `config.toml` with:

```bash
hugo mod get -u
```

## Override

You can override a shortcode by adding a file with the same name as the one you want to replace in your own shortcode directory (`layouts/shortcodes` for example).

## Modules

### calculator.html

[`calculator.html`][calculator] is useful for representing bread and dough recipes in an interactive way.

Example:

```go
{{< calculator >}}
ingredients:
- name: Bread Flour
  percent: 100
- name: Water
  percent: 70
- name: Instant Yeast
  percent: 1
- name: Sale
  percent: 1
{{< /calculator >}}
```

Demo: https://0x6166.com/pizza/

## Credits

This README borrows heavily from [tohn/hugo-shortcodes].
It's a nice model for easily distributed shortcodes.

[Hugo]: https://gohugo.io
[hugo_mods]: https://gohugo.io/hugo-modules/
[hugo_shortcodes]: https://gohugo.io/content-management/shortcodes/
[calculator]: ./layouts/shortcodes/calculator.html
[tohn/hugo-shortcodes]: https://github.com/tohn/hugo-shortcodes