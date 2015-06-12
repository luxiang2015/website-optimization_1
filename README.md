## Website Performance Optimization portfolio project

####Part 1: Optimize critical rendering path for index.html


1. To inspect the site on your phone, you can run a local server

```bash
$> cd /path/to/your-project-folder
$> python -m SimpleHTTPServer 8080
```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.

``` bash
$> cd /path/to/your-project-folder
$> ngrok 8080
```

Copy the public URL ngrok gives you and try running it through PageSpeed Insights to check the score.



####Part 2: Optimize Frames per Second in pizza.html
Open the pizza.html in the chrome and check the FPS using the developer tool. Several changes have been made to the views/js/main.js including :
1. In function updatePosition(), the calculation was moved outside of the for loop.
2. In function changePizzaSize(), the calculation was carried out only once with one pizza.
3. In document.addEventListener，in the for loop, the maximum of i was reduced from 200 to 20.

Another change was made to the views/css/style.css/
In the 'mover' class, 'backface-visibility: hidden;' was added.


