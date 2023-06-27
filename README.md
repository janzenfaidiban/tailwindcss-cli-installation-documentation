# Tailwind CLI Installation Process

## Install JSON Package

    ```
    npm init
    ```

## Install Tailwind CSS

Install tailwind css
    ```
    npm install -D tailwindcss
    ```

Creating tailwind.config.js
    ```
    npx tailwindcss init
    ```


## Configure your template paths

Add path to template files here ```tailwind.config.js```

Create folder ```dist``` and a file ```index.html``` inside, then setup 
    ```
    /** @type {import('tailwindcss').Config} */
    module.exports = {
    content: ["./dist/*.{html,js}"],
    theme: {
        extend: {},
    },
    plugins: [],
    }
    ```




## Add the Tailwind directives to your CSS

Create a folder ```src``` and ```input.css``` inside the folder

Run this commands to get ```style.css```

    ```
    npx tailwindcss -i ./src/input.css -o ./dist/style.css --watch
    ```

Link ```style.css``` with ```index.html```

    ```
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>

        <link rel="stylesheet" href="style.css">

    </head>
    <body>

        <h1 class="bg-slate-400">Hello SaCode</h1>
        
    </body>
    </html>
    ```

## Setup NPM Run Dev in package.json

    ```
    "scripts": {
        "test": "echo \"Error: no test specified\" && exit 1",
        "dev": "tailwindcss -i ./src/input.css -o ./dist/output.css --watch"
    },
    ```

now, we can online run this command ```npm run dev```

## Start the Tailwind CLI build process

now, we can online run this command ```npm run dev```


## Start using Tailwind in your HTML

Open ```index.html``` in your browser to see results