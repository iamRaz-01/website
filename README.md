# Ex.07 Restaurant Website
# Date: 19 /10/2024
# AIM:
To develop a static Restaurant website to display the food items and services provided by them.

# DESIGN STEPS:
## Step 1:
Requirement collection.

## Step 2:
Creating the layout using HTML and CSS.

## Step 3:
Updating the sample content.

## Step 4:
Choose the appropriate style and color scheme.

## Step 5:
Validate the layout in various browsers.

## Step 6:
Validate the HTML code.

## Step 7:
Publish the website in the given URL.

# PROGRAM:
## Index.html
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width">
    <title>Restaurant Website</title>
    <link rel="stylesheet" href="./html/styles.css">
</head>

<body>
    <section id="home" class="common">
        <nav>
            <h3 style="color: rgb(255, 185, 94);">Home</h3>
            <a href="./html/menu.html">

                <h3>Menu</h3>
            </a>
            <a href="./html/administration.html">
                <h3>Administration</h3>
            </a>
            <a href="./html/contact.html">
                <h3>Contact us</h3>
            </a>



        </nav>
        <div class="banner">
            <h1>Welcome To Razz's </h1>
            <h1>Kitchen</h1>
            <h4>"Where Every Bite Tells a Story!"</h4>
        </div>


    </section>

</body>

</html>
```
## Menu.html 
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Restaurant Website</title>
    <link rel="stylesheet" href="./styles.css">
</head>

<body>
    <section id="menu" class="common">
        <nav>
            <a href="../index.html">
                <h3>Home</h3>
            </a>
            <h3 style="color: rgb(255, 185, 94);">Menu</h3>
            <a href="./administration.html">
                <h3>Administration</h3>
            </a>
            <a href="./contact.html">
                <h3>Contact us</h3>
            </a>

        </nav>
        <h1>"A Feast of Flavors Awaits You!" </h1>
        <div id="menuContainer">


        </div>





    </section>
    <script>
        const menuItems = [
            {
                imageSrc: './pictures/pizzaHome.jpg',
                title: 'Pizza',
                price: 50,
            },
            {
                imageSrc: './pictures/burger.jpg',
                title: 'Burger',
                price: 40,
            },
            {
                imageSrc: './pictures/pasta.jpeg',
                title: 'Pasta',
                price: 60,
            },
            {
                imageSrc: './pictures/salad.jpg',
                title: 'Salad',
                price: 30,
            },
            {
                imageSrc: './pictures/susi.jpeg',
                title: 'Sushi',
                price: 80,
            },

            {
                imageSrc: './pictures/noodles.jpeg',
                title: 'Noodles',
                price: 45,
            },
            {
                imageSrc: './pictures/steak.jpg',
                title: 'Steak',
                price: 100,
            },

            {
                imageSrc: './pictures/donut.jpeg',
                title: 'Donut',
                price: 15,
            },
            {
                imageSrc: './pictures/frenchfries.jpeg',
                title: 'FrenchFries',
                price: 40,
            },
            {
                imageSrc: './pictures/wrap.jpeg',
                title: 'Wrap',
                price: 60,
            },
            {
                imageSrc: './pictures/frankie.jpeg',
                title: 'Frankie',
                price: 80,
            },
            {
                imageSrc: './pictures/briyani.jpeg',
                title: 'Briyani',
                price: 130,
            },
            {
                imageSrc: './pictures/friedC.jpeg',
                title: 'FriedChicken',
                price: 100,
            },

            {
                imageSrc: './pictures/tandoori.jpg',
                title: 'Tandoori',
                price: 450,
            },
            {
                imageSrc: './pictures/bbq.jpeg',
                title: 'BBQ',
                price: 100,
            },

            {
                imageSrc: './pictures/grill.jpeg',
                title: 'Grill',
                price: 15,
            },
        ];

        menuItems.forEach(createFoodItem);



        function createFoodItem(item) {
            // Create the main card div
            const menuCard = document.createElement('div');
            menuCard.classList.add('menuCard');

            // Create and set the image element
            const img = document.createElement('img');
            img.src = item.imageSrc;
            img.alt = item.title;

            // Create the content div
            const content = document.createElement('div');
            content.classList.add('content');

            // Create and set the title element
            const heading = document.createElement('h2');
            heading.textContent = `${item.title} @${item.price}`;

            // Append the heading to content div
            content.appendChild(heading);

            // Append the image and content div to the card
            menuCard.appendChild(img);
            menuCard.appendChild(content);

            // Append the card to the menu container
            document.getElementById('menuContainer').appendChild(menuCard);
        }

    </script>

</body>

</html>
```
## Administration.html
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Administration</title>
    <link rel="stylesheet" href="./styles.css">
</head>

<body>
    <section id="administration" class="common">
        <nav>
            <a href="../index.html">
                <h3>Home</h3>
            </a>
            <a href="./menu.html">
                <h3>Menu</h3>
            </a>
            <h3 style="color: rgb(255, 185, 94)">Administration</h3>
            <a href="./contact.html">
                <h3>Contact us</h3>
            </a>

        </nav>
        <h1>"Meet the Minds Behind the Magic!"</h1>
        <div id="menuContainer" style="overflow-y: unset;">



        </div>

        <script>



            function createPersonCard(person) {
                const peopleCard = document.createElement('div');
                peopleCard.classList.add('people');

                const img = document.createElement('img');
                img.src = person.imageSrc;
                img.alt = person.name;

                const nameHeading = document.createElement('h2');
                nameHeading.style.color = 'rgb(255, 185, 94)';
                nameHeading.textContent = person.name;

                const designationParagraph = document.createElement('p');
                designationParagraph.textContent = person.designation;

                peopleCard.appendChild(img);
                peopleCard.appendChild(nameHeading);
                peopleCard.appendChild(designationParagraph);

                document.getElementById('menuContainer').appendChild(peopleCard);
            }
            const people = [
                {
                    imageSrc: './pictures/ceo.png',
                    name: 'John Doe',
                    designation: 'CEO',
                },
                {
                    imageSrc: './pictures/operations.png',
                    name: 'Michael Brown',
                    designation: 'Operations',
                },
                {
                    imageSrc: './pictures/chef.png',
                    name: 'Jane Smith',
                    designation: 'Master Cheif',
                },
                {
                    imageSrc: './pictures/mChef.png',
                    name: 'Alice Johnson',
                    designation: 'Associate Chief',
                },

                {
                    imageSrc: './pictures/master.png',
                    name: 'Emily Davis',
                    designation: 'Waiter',
                },
                {
                    imageSrc: './pictures/waiter.png',
                    name: 'Robert Wilson',
                    designation: 'Waiter',
                },
            ];
            people.forEach(createPersonCard)
        </script>


</body>

</html>
```
## Contact.html
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contact Us</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <div class="container">
        <section id="administration" class="common">
            <nav>
                <a href="../index.html">
                    <h3>Home</h3>
                </a>
                <a href="./menu.html">
                    <h3>Menu</h3>
                </a>
                <a href="./administration.html">
                    <h3>Administration</h3>
                </a>
                <h3 style="color: rgb(255, 185, 94)">Contact us</h3>

            </nav>
            <h1>Contact Us</h1>
            <div id="contact">
                <h2>Razz's kitchen</h2>
                <h3>no:3/401,5th main road , kodungaiyur , chennai 600118</h3>
                <h4>8124311160</h4>
                <h4>abdulrasak.nasriudeen@gmail.com</h4>

            </div>
        </section>

    </div>
</body>

</html>
```
## Styles.css
```css
/* Font Family */
@import url('https://fonts.googleapis.com/css2?family=Playwrite+HU:wght@100..400&family=Sora:wght@100..800&display=swap');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Playwrite HU", cursive;

}

/* Body and font styling */
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    background-color: black ;
    
}

/* Header and Navigation Menu */
header {
    background-color: black;
    padding: 1rem;
    position: fixed;
}

header nav ul {
    list-style: none;
    display: flex;
    justify-content: center;
}

header nav ul li {
    margin: 0 20px;
}

header nav ul li a {
    color: white;
    text-decoration: none;
    font-weight: bold;
    font-size: 18px;
}
.common{
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    font-family: "Playwrite HU", cursive;
}

#home{
    width: 2100px;
    height: 1170px;
    background:url(./pictures/pizzaHome.jpg);
    background-size: cover; /* Ensures the image covers the entire container */
    background-position: center; /* Keeps the image centered */
    background-repeat: no-repeat;
    background-color: black;
    
}

.banner{
    width: 80%;
    height: 40%;
    color: #ecf0f1;
    font-size: 90px;
    display: flex;
    flex-direction: column;
    align-items: center;
}
.banner h4{
    position: absolute;
    top: 91%;
    font-size: 60px;
    color: rgb(255, 185, 94);
}
nav{
    width: 100%;
    display: flex;
    height: 10%;
    color: #ecf0f1;
    justify-content: flex-end;
    gap: 5%;
    align-items: center;
    font-size: 20px;
    
}
a{
    text-decoration: none;
    color: #ecf0f1;
}

/* Menu */
#menu{
    width: 2100px;
    height: 1170px;
    color: #ecf0f1;
}
#menu h1{
    font-size: 55px;
}

.menuCard{
    width: 300px;
    height: 400px;
    border-radius: 50px;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
    border: 4px solid #ecf0f1;
    
}
#menuContainer {
    display: grid;
    grid-template-columns: repeat(4, 1fr); /* Four equal-width columns */
    gap: 60px; /* Space between cards */
    padding: 20px;
    justify-content: center; /* Centers the grid horizontally */
    align-items: start; /* Aligns items to the top */
    overflow-y: scroll;
}
.menuCard img{
    width: 90%;
    height: 75%;
    border-radius: 30px;
}
.content{
    width: 90%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
}
.content h2{
    font-size: 25px;
    color: antiquewhite;

}
/* Administration */
#administration h1{
    font-size: 50px;
    margin-top: 30px;
    color: #ecf0f1;

}
.people{
    width: 300px;
    height: 400px;
    border-radius: 30px;
    border: 4px solid #ecf0f1;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
    color: #ecf0f1;
}
.people img{
    width: 90%;
    height: 60%;

}

/* Scroll Bar */
::-webkit-scrollbar {
    width: 10px; /* Width of the scrollbar */
}

::-webkit-scrollbar-track {
    background: #f1f1f1; /* Background color of the track */
    border-radius: 10px; /* Rounded corners for the track */
}

::-webkit-scrollbar-thumb {
    background: rgb(255, 185, 94); /* Color of the scrollbar handle */
    border-radius: 10px; /* Rounded corners for the handle */
    border: 2px solid black; /* Adds space around the handle */
}

::-webkit-scrollbar-thumb:hover {
    background: #555; /* Darker color on hover for the handle */
}
#contact{
    width: 1000px;
    height: 500px;
    margin-top: 100px;
    border-radius: 30px;
    color: #ecf0f1;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 20px;
}
```
# OUTPUT:
## Home page 
![image](https://github.com/user-attachments/assets/55cea701-12f0-4ca6-9b41-6b5f4116301e)
## Menu page 1
![image](https://github.com/user-attachments/assets/546c16c9-afa3-4a5d-aa85-b32965a7938a)
## Menu page 2
![image](https://github.com/user-attachments/assets/ef87c889-975f-41ad-b618-b734a15782bc)
## Administration page
![image](https://github.com/user-attachments/assets/352694f0-273e-4cfe-b31e-9ec0280749b4)
## Contact Pagw 
![image](https://github.com/user-attachments/assets/75bd1f14-fa90-4acf-8127-675d65cfdfc6)




# RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
