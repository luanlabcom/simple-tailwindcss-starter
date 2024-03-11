# STEP BY STEP GUIDE TO CREATE A SIMPLE TAILWIND STARTER DIRECTORY

## Prequisite:
- `npm -v`
- `node -v`

If node version is deprecated, switch to a new one that fit the current tailwind version.

- `nvm list`
- `nvm install [node version]` 
*for example: `nvm install v16.14.0`*
- `nvm use [node version]` 
*for example: `nvm use v16.14.0`*

> If you download this repo from Github, 
>
> you don't need to go through any of the steps below, 
>
> just run `npm install` and you have a project ready to use with tailwindcss

## Step 1: 
- `npm init -y`

## Step 2: 
- `mkdir ./src`
Follow this guide from the tailwind official docs: https://tailwindcss.com/docs/installation

> Pay Attention: Step 4 of the docs!
> Instead of running the CLI tool manually
> We will set up an NPM script.
> So please ignore this CLI tool: `npx tailwindcss -i ./src/input.css -o ./src/output.css --watch`
> Instead, go to the `package.json` file and create this NPM script:
>```javascript
> "scripts": {
>    "build": "tailwindcss -i ./src/input.css -o ./src/output.css",
>    "watch": "tailwindcss -i ./src/input.css -o ./src/output.css --watch"
>  },
> ```
> Run these scripts using `npm run build` and `npm run watch`

## Step 3:
Create an `index.html` file in `./src` and add a boilerplate in the HTML file

To cross-check: the result should look like this screenshot: https://drive.google.com/file/d/1erT6YU8eUu0UVDv102tED6agAXXEfVNC/view?usp=drive_link

```html
<!-- h1.text-3xl.font-bold.underline -->
<h1 class="text-3xl font-bold underline">
    This tailwind starter is broughted to you by LuanLab.com
</h1>
```

> **IMPORTANT**: 
> Every time you modify the `index.html` with TailwindCSS class.
> REMEMBER TO RUN THE SCRIPT: `npm run build`
> otherwise, there's no style changed showing up.
>
> Another alternative is you run `npm run watch` and every time you save the `index.html` file, tailwind will automatically compile those tailwind classes to CSS for you, and you can see the result immeditately without doing a thing.


Congratulations! Now you can start using TailwindCSS in your project.