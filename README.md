# NFT preview card component

Another simple HTML and CSS work, feel free to use it on your webpage or any other personal use

## Welcome 🤗
I wanna thank you firstly for checking on my humble work. If you find any issue, please feel free to correct me.

## equipements 🤓
Here is what I used to make the webpage:
| Editor | Languages | Frameworks |
| --- | ---| --- |
| [Vs code](https://code.visualstudio.com/)| Vanilla HTML and CSS | None|

I beleive you can use any text editor to make this, [Replit](https://replit.com/~) for example...

## Code 🧐
For the code, all you need to remember is that **HTML is used to structure** while **CSS is used to style**. And the way to display them can be different from each person.
Here is the HTML code I made for this one

```html
<body>
    <main>
        <img class="NFT" src="/images/image-equilibrium.jpg">
        <img class="eye" src="/images/icon-view.svg">
        <h2>Equilibrium #3429</h2>
        <p class="describtion">Our Equilibrium collection promotes balance and calm.</p>
        <div class="prices">

            <a class="price-1"><img class="ETH-sym" src="/images/icon-ethereum.svg">&nbsp;0.041 ETH</a>
            <div class="d">
                <a class="price-2"><img class="hour" src="/images/icon-clock.svg">&nbsp;3 days left</a>
            </div>
        </div>
        <hr>
        <div class="artist-info">
            <div>
                <img class="avatar" src="/images/image-avatar.png">
            </div>
            <div class="footer">
                <p class="artist">Creation of <a class="name">Jules Wyvern</a></p>
            </div>
        </div>
    </main>
    <div class="attribution">
        Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>. Coded by <a href="https://www.frontendmentor.io/profile/Hicham2012" target="_blank">Hicham ZAADLA</a>.
    </div>
</body>
```
### We added two pictures, one will be always visible while the other will only appear when we hover over it.
```html
        <img class="NFT" src="/images/image-equilibrium.jpg">
        <img class="eye" src="/images/icon-view.svg">
```
Let's look into the CSS to see why it will come in handy, and how we will display them 🧐
```css
@import url('https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,700&family=Outfit:wght@300;400;600&display=swap');
* {
    box-sizing: border-box;
}

:root {
    /************\
      Colors
  \************/
    /*** Screen-size ***/
    --desktop: 1440px;
    --mobile: 375px;
    /*** Primary ***/
    --Soft-blue: hsl(215, 51%, 70%);
    --Cyan: hsl(178, 100%, 50%);
    --Cyan-2: hsl(178, 100%, 50%, 0.5);
    /*** Neutral ***/
    /* main BG */
    --Very-dark-blue-1: hsl(217, 54%, 11%);
    /* card BG */
    --Very-dark-blue-2: hsl(216, 50%, 16%);
    /* shadow */
    --shadow: hsl(218, 80%, 8%);
    --shadow-2: hsl(216, 90%, 10%);
    /* line */
    --Very-dark-blue-3: hsl(214, 64%, 12%);
    --White: hsl(0, 0%, 100%);
    /************\
    Typography
  \************/
    --paragraphe: 18px;
}

html {
    font-size: 18px;
}

body {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background: red;
}


/*****  *****\
 Desktop view
\*****  *****/

@media only screen and (max-width: 1440px) {
    body {
        background: var(--Very-dark-blue-1);
    }
    main {
        margin-top: 1.5rem;
        border-radius: 1em;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        max-width: 18rem;
        background: var(--Very-dark-blue-2);
        box-shadow: 0em 1.3em 0em 0.9em var(--shadow), 0em 2em 0em 0.45em var(--shadow), 0em 2.8em 0em 0.1em var(--shadow), 0em 1.8em 0em 2.5em var(--shadow-2);
    }
    .eye {
        display: inline-flex;
        margin-top: -15.7rem;
        z-index: 1rem;
        cursor: pointer;
        opacity: 0;
        padding: 6.53rem 6.5rem;
        border-radius: 0.5em;
        transition: opacity 150ms;
    }
    .eye:hover {
        opacity: 1;
        background: var(--Cyan-2);
    }
    .NFT {
        display: flex;
        width: 87%;
        margin-top: 1.15rem;
        border-radius: 0.5em;
    }
    h2 {
        margin-right: 5.7rem;
        margin-top: 0.8em;
        font-family: 'Outfit', sans-serif;
        font-size: 1.2rem;
        color: var(--White);
        margin-bottom: 0rem;
        cursor: pointer;
        transition: color 120ms;
    }
    h2:hover {
        color: var(--Cyan);
    }
    .describtion {
        font-family: 'Outfit', sans-serif;
        color: var(--Soft-blue);
        font-weight: 300;
        font-size: 0.9rem;
        margin-right: 2rem;
        margin-left: 1.2rem;
        margin-top: 0.7rem;
        margin-bottom: 0rem;
        line-height: 1.5rem;
    }
    .prices {
        display: flex;
        font-family: 'Outfit';
        margin-left: -5rem;
        margin-right: -4rem;
        margin-top: 1.2rem;
        margin-bottom: 1rem;
    }
    .ETH-sym {
        display: flex;
    }
    .price-1 {
        display: flex;
        color: var(--Cyan);
        font-size: 0.9rem;
        font-weight: 400;
        margin-left: 1rem;
    }
    .hour {
        display: flex;
        margin-right: 0rem;
    }
    .price-2 {
        display: flex;
        color: var(--Soft-blue);
        margin-left: 5.8rem;
        font-size: 0.85rem;
    }
    hr {
        margin-top: 0rem;
        width: 85%;
        border: 1px solid var(--Very-dark-blue-3);
    }
    .artist-info {
        display: flex;
        margin-left: -2.5rem;
        color: var(--Soft-blue);
        margin-bottom: 1rem;
        margin-top: 0.2rem;
    }
    .avatar {
        width: 28%;
        border-radius: 50%;
        border: 0.2rem solid var(--White);
    }
    .footer {
        font-family: 'Outfit', sans-serif;
        font-size: 0.9rem;
        margin-top: -0.3rem;
        margin-left: -5.5em;
    }
    .name {
        color: var(--White);
        cursor: pointer;
        transition: color 120ms;
    }
    .name:hover {
        color: var(--Cyan);
    }
    .attribution {
        margin-top: 5.3rem;
        font-family: 'Outfit', sans-serif;
        font-weight: 300;
        color: var(--Cyan);
    }
    .attribution a {
        text-decoration: none;
        color: var(--White);
        font-size: 0.7rem;
    }
}


/***** *****\
 Mobile view
\***** *****/

@media only screen and (max-width: 375px) {
    main {
        max-width: 17.5rem;
    }
    .eye {
        display: inline-flex;
        margin-top: -15.4rem;
        padding: 6.38rem 6.33rem;
    }
    h2 {
        margin-right: 5.2rem;
    }
    .prices {
        margin-left: -2.9rem;
        margin-right: -2rem;
    }
    .price-2 {
        margin-left: 5.2rem;
    }
}


/*****               *****\
 Mobile view (Galaxy Fold)
\*****               *****/

@media only screen and (max-width: 280px) {
    main {
        max-width: 13rem;
    }
    h2 {
        margin-right: 3.2rem;
        margin-top: 0.8em;
        font-family: 'Outfit', sans-serif;
        font-size: 1rem;
        color: var(--White);
        margin-bottom: 0rem;
    }
    .describtion {
        margin-right: 1rem;
        margin-left: 0.7rem;
    }
    .prices {
        display: flex;
        font-family: 'Outfit';
        margin-left: -5rem;
        margin-right: -4rem;
        margin-top: 1.2rem;
        margin-bottom: 1rem;
    }
    .ETH-sym {
        display: flex;
    }
    .price-1 {
        display: flex;
        color: var(--Cyan);
        font-size: 0.9rem;
        font-weight: 400;
        margin-left: 1rem;
    }
    .hour {
        display: flex;
        margin-right: 0rem;
    }
    .price-2 {
        display: flex;
        color: var(--Soft-blue);
        margin-left: 1.8rem;
        font-size: 0.85rem;
    }
    .artist-info {
        display: flex;
        margin-left: 0.5rem;
        color: var(--Soft-blue);
        margin-bottom: 1rem;
        margin-top: 0.2rem;
    }
    .avatar {
        width: 24%;
        border-radius: 50%;
        border: 0.2rem solid var(--White);
    }
    .footer {
        font-family: 'Outfit', sans-serif;
        font-size: 0.8rem;
        margin-top: -0.5rem;
        margin-left: -5.5em;
    }
    .attribution {
        margin-top: 5.3rem;
        font-family: 'Outfit', sans-serif;
        font-weight: 400;
        color: var(--Cyan);
        font-size: 0.55rem;
        word-spacing: 0.1rem;
    }
    .attribution a {
        text-decoration: none;
        color: var(--White);
        font-size: 0.5rem;
    }
    .eye {
        display: inline-flex;
        /* border: 2px solid black; */
        margin-top: -11.3rem;
        z-index: 1rem;
        cursor: pointer;
        opacity: 0;
        padding: 4.3rem;
        border-radius: 0.5em;
        transition: opacity 150ms;
    }
}
```
You can see that there is barely a 'px' unite, and also the :root that is used as palette, other than that the code is self explanotary

## Shoutout 🙏
I wanna thank [frontend Mentor](www.frontendmentor.io) for making funny challenges.
Big thanks to the feedbacks I received on my first challenge!!

  ### Again, please feel free to correct me if I made any issue 🙌