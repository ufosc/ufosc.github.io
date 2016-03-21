# Web Development

## How to write

All of the following code can be written in any simple text editor, such as NotePad or TextEdit. Atom or Sublime Text are nice text editors with some built in support for some more advanced features. (Side note: This is a markdown file, and can be viewed in a markdown format by pressing `control + shift + m` in atom). To view the webpages, you can simply open them up in a web browser by either typing the file path into your browser or dragging the file from your file explore onto the browser. If you are using Atom or Sublime Text, you can also install plugins to view the webpage inside the editor itself. Consult Google for details.

## HTML

**HyperText Markup Language** - It is basically the content of a webpage and how it is organized. Not necessarily the organization you see.

- It's what bots, used by search engine, see to evaluate how nice a web page is

- Page readers, how the blind navigate the internet

- Uses tags to describe type of element
    - Some tags are just one line
    - Some are multiple lines

- Also has meta tags that describe the content of page

### Examples

#### Basic Version

```html
<!DOCTYPE html>
<html>
    <head>

        <meta charset="UTF-8" content="en">
        <title>Sample Page </title>
        <meta name="description" content="This is being used as a simple sample">

    </head>
    <body>
        <!-- How to comment -->
        <h1> Primary Title </h1>

        <h2> Page topic </h1>

        <h3> Part 1 </h3>
        <p> Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>

    </body>
</html>
```

#### Intermediate

GOTO: Intermediate.html

## CSS

**Cascading Style Sheets** - Styling for html elements. Makes the web pretty.

- Describes each tag, class, id or combination of the above

- In CSS3 (newest version), css can handle some animations and logic

- Some features not always enabled on browsers

- Some differences between how browsers default display elements

### Examples

#### Basic

```css
body {
    color: blue;
    margin: auto;
    text-align: center;
    width: 900px;
}

header {
    border-style: solid;
    border-width: 10px 2px 5px 0px;
    border-color: pink;
}

p {
    font-family: "Times New Roman", Times, serif;
}
```

#### Intermediate

GOTO: Intermediate.css

## Polymer

Is a **Web Component library**. Web Components are a set of reusable widgets or components for web applications.

- Custom Elements

- Shadow DOM

    - Elements with encapsulation

- HTML Imports

- HTML Templates

- Only works in some browsers

    - Webkit based Chrome, Opera, Safari

    - Special changes for Firefox to work (official support soon)

    - Backwards compatibility with Java polyfills

### Why

- Modern programing paradigms

- Increased readability

- Material Design looks cool

- Responsive Design, works on multiple screen sizes

### How to get started

In terminal after step 1

1. Download node.js

    - **Node.js** is a runtime environment for developing web applications.
    
    - Can be found here https://nodejs.org/en/ or via system package manager 

    - Also contains npm, a package manager for (mostly) javascript modules

2. `npm install -g bower`

    - **Bower** is a package manager that manages dependencies on a per project basis

3. `bower init`

    - You can just hit enter for the set up, only matters for a real project

4. `bower install --save Polymer/polymer#^1.2.0`

    - This will add a bower_compnents folder with a polymer folder at the root of project

5. `bower update`

    - Updates all packages for that project

- You can skip 1-5 if you just want to use the polymer-starter-kit, which has most of it included

#### Start a webpage

To run the webpage in a browser use the following python (must have python installed)

On Linux and OSX use:

`python -m SimpleHTTPServer 8080`

On Windows use:

`python -m http.server 8080`

Then type the following url in your preferred browser

`localhost:8080`

### Basic element

#### Google Map

1. Check out polymer-elements https://elements.polymer-project.org/

    - Find one you like

2. Copy and paste the bower command to install that component to your project

    - `bower install --save GoogleWebComponents/google-map`

3. Add the following line to the head of the html
    - `<script src="bower_components/webcomponentsjs/webcomponents.js"></script>`
        - Which allows for polymer functionality
    - `<link rel="import" href="bower_components/google-map/google-map.html">`

4. And include the google-map element
    - `<google-map></google-map>`

Diving into the google-map component, see that it includes polymer as well as google-map-marker. Contains defaults, template, values you can add, and different behaviors.

#### Custom Element

##### Basic

```html
<link rel="import" href="bower_compnents/polymer/polymer.html">

<dom-module id="contact-card">
<style>
    h1{
        color: blue;
    }
</style>

<template>
    <h1>Boba Fett</h1>
</template>
</dom-module>

<script>
    Polymer({
        is: "contact-card"
    });
</script>
```

##### Intermediate

GOTO: contact-card2.html

GOTO: material-contact.html

## References

http://www.w3schools.com/

https://www.polymer-project.org/1.0/docs/start/getting-the-code.html

https://codelabs.developers.google.com/codelabs/polymer-first-elements/index.html?index=..%2F..%2Findex#0

https://www.youtube.com/watch?v=CdV0VGYhKXk&list=PLLnpHn493BHGhoGAb2PRKzv4Zw3QoatK-
