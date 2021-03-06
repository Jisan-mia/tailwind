## Tailwind CSS - is a css framework

### Prerequisites
  - Basic HTML
  - Basic CSS
  - Basic Computer Knowledge
  - Google Search
  - Git & Github

### Ways of Installing Tailwind CSS
1. Installing from cdn to our html file(couldn't be customized)
2. Install as PostCSS Plugin
3. Install Tailwind CLI using command line(easy way/best way)

### Steps to get started with tailwind css project
1. Node.js >= 12.3.0
2. `npm init -y` (initialize a node project)
3. `npm i -D tailwindcss` (installing tailwind css)
4. Extension: Tailwind CSS IntelliSense
5. `npx tailwindcss init` (create tailwind.config file for configuring tailwind projects)
6. Create `src` and `output` folder (write tailwind code in `src` folder and with the help of tailwind css compiler it will compile its code into vanilla/row css in `output` folder)
7. Create `src/[tailwind].css` file
8. Inside `src/[tailwind].css` file (@tailwind == tailwind directive)-> 
   ```css
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
   ```
9. create `.vscode/settings.json` file on the root. Inside ->
   ```json
    {
      "css.validate": false,
      "tailwindCSS.emmetCompletions": true
    }
   ```
10. Create a build script to compile tailwind css into row css ->
  - go to `package.json` file and inside `scripts` write the following ->
    ```json
    {
      "scripts": {
        "build": "tailwindcss -i ./src/tailwind.css -o ./output/tailwind.css -w"
      }
    }
    ```
  - `-i ./src/tailwind.css` (input file location) means input from this file
  - `-o ./output/tailwind.css` (output file location) means output compiled code in this file
  - `-w` (watch flag). when we'll update/modify `./src/tailwind.css` file, it'll automatically build.
11. After getting output into into `./output/tailwind.css` , we'll link up this file loc to the html folder.
    ```html
      <head>
        <link rel="stylesheet" href="./output/tailwind.css" />
      </head>
    ```
12. Now time to build -> `npm run build`