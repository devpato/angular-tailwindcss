# Angular Tailwind

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 11.2.0.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Setup TailwindCSS in Angular

1. Install with `npm install -D tailwindcss`

2. Install TailwindCSS plugins(Optional):

  * `npm i @tailwindcss/typography`

  * `npm i @tailwindcss/forms`

3. Create a TailwindCSS configuration file in the workspace or project root. Name that configuration file `tailwind.config.js`

It should look like this:

```javascript
module.exports = {
    prefix: '',
    purge: {
      content: [
        './src/**/*.{html,ts}',
      ]
    },
    darkMode: 'class', // or 'media' or 'class'
    theme: {
      extend: {},
    },
    variants: {
      extend: {},
    },
    plugins: [require('@tailwindcss/forms'),require('@tailwindcss/typography')],
};
```

4. In your styles.scss file add the following TailwindCSS imports

```css
@import 'tailwindcss/base';
@import 'tailwindcss/components';
@import 'tailwindcss/utilities';
```

if you are using CSS not SCSS, your file should look like this:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

<h2>Making sure TailwindCSS in Angular is working</h2>


Go to any of you components and write the following:

```html
<button
  class="py-2 px-4 border border-transparent shadow-sm text-sm font-medium rounded-md text-white bg-red-400">Hello</button>
```


Now run `ng serve`, you should see the following button

![angular tailwindcss](https://dev-to-uploads.s3.amazonaws.com/i/tvvo9pqx7ua7yc2kjzhz.png)


<h2>To learn more about Angular and TailwindCSS</h2>
https://dev.to/angular/setup-tailwindcss-in-angular-the-easy-way-1i5l