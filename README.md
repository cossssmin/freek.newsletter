# freek.dev newsletter template

The HTML email template for the [freek.dev newsletter](https://freek.dev/newsletter), built with [Tailwind CSS](https://tailwindcss.com/) in [Maizzle](https://maizzle.com).

## Features

The original design has been preserved, but code has been refactored:

- it's now responsive, even where `@media` queries aren't supported
    - includes double `<head>` tag, to make it responsive in Yahoo! Android
- fixed broken layout in Outlook 2007-2019 (Windows)
    - inlined CSS (Outlook only uses the first class in a `class=""` attribute)
    - fixed padding, margins, spacers
- accessibility improvements:
    - semantic markup (headings, paragraphs, lists)
    - fully clickable buttons in Outlook
- hover effects on buttons
- code weight reduced to half ([why it matters](https://github.com/hteumeuleu/email-bugs/issues/41))

## Development

Make sure you have the Maizzle CLI installed:

```sh
npm i -g @maizzle/cli
```

Then, scaffold a project using this repo:

```sh
maizzle new https://github.com/cossssmin/freek.newsletter.git
```

Change working directory:

```sh
cd freek.newsletter
```

Start a local development server:

```sh
maizzle serve
```

To build the production-ready email template:

```sh
maizzle build production
```

You can either manually copy `build_production/template.blade.php` to your views directory, or configure Maizzle to output it there automatically when you build for production, in `config.production.js` ([docs](https://maizzle.com/docs/build-config/#destination)).

## Documentation

Maizzle documentation is available at https://maizzle.com
