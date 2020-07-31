# CSS learning

---

# CSS syntax

```css
selector {
	property1:value;
	property2:value;
}
```

- Example

    ```css
    h1 {
    	color:blue;
    }
    ```

---

# CSS selectors

- Element

    ```css
    h1 {
    	color:blue;
    }
    div{
    	color:blue;
    }
    header{
    	color:blue;
    }
    footer{
    	color:blue;
    }
    span{
    	color:blue;
    }
    strong{
    	color:blue;
    }
    a{
    	color:blue;
    }
    btn{
    	color:blue;
    }
    ......
    ```

- Class

    ```html
    <h1 class="big-header">
    	Title
    </h1>

    <a herf="index.html">
    	Home
    </a>

    <div class="red-square">
    	Content
    </div>
    ```

    ```css
    .class-name {
    	proparty:value;
    }
    ```

    ---

    ```html
    <button class="btn btn-1">
    	button1
    </button>
    <button class="btn btn-2">
    	button2
    </button>
    <button class="btn btn-3">
    	button3
    </button>
    ```

    ```css
    .btn {
    	padding: 10px;
    	color: white;
    }

    .btn-1 {background-color: green;}
    .btn-2 {background-color: blue;}
    .btn-3 {background-color: purple;}
    ```

- ID

    ```html
    <h1 id="main-header">
    	Title
    </h1>
    ```

    ```css
    #id {
    	property:value;
    }
    ```

---

# CSS Selector Combinations

- **Specify multiple selectors**

    ```css
    .selector-1.selector-2 {
    	property: value;
    }
    ```

    ---

    - Example 1

        ```html
        <h1 class="large-heading">
            Title
        </h1>
        ```

        ```css
        h1.large-header {
            font-size: 200%;
        }
        ```

    - Example 2

        ```html
        <h2 id="big-blue" class="large blue">
            Title
        </h2>
        ```

        ```css
        #big-blue.large.blue{
            color: blue;
            font-size: 200%;
        }
        ```

- **Use multiple selectors to specify an ancestor of an element**

    ```css
    .ancestor .child {
    	property: value;
    }
    ```

    ---

    - Example 1

        ```html
        <div>
            <p>Selected</p>
            <p>Selected</p>
            <span>
                <p>Selected</p>
            </span>
        </div>
        ```

        ```css
        div p {
            color: red;
        }
        ```

    - Example 2

        ```html
        <header class="main-header">
            <h1 class="brown">
                Selected
            </h1>
        </header>
        ```

        ```css
        header.main-header h1.brown {
            color: brown;
        }
        ```

- **Share a set of style properties and values between multiple selector**

    ```css
    .big {
    	font-size: 200%;
    }
    .large {
    	font-size: 200%;
    }
    ```

    🔽

    ```css
    .big, .large {
    	font-size: 200%;
    }
    ```

- **Everything selector**

    ```css
    * {
    	font-family: Arial;
    }
    ```

---

# How to Load CSS

- **Inline**

    ```html
    <h1 style="color: blue;">
    	Blue Title
    </h1>
    ```

- **Style Element**

    ```html
    <head>
        <style>
            .blue {
                color:blue;
            }
        </style>
    </head>
    ```

- **External CSS**

    ```html
    <head>
    	<link rel="stylesheet" herf="style.css">
    </head>
    ```