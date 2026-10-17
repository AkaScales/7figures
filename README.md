# 7-Figures Printers

Static site, no build step. Almost everything you will want to change lives in **config.js**.

## Change the logo
1. Put your logo file in the `images/` folder (png, svg or jpg).
2. Open `config.js` and set `logo: "images/your-logo.png"`.
3. Change `brandName` there too.

## Change the videos
1. Put your new .mp4 in the `videos/` folder (vertical works best).
2. In `index.html`, search for `testimony-1.mp4` (it appears twice: hero and testimonials section) and change the `src` path. Change `poster-1.jpg` the same way.
3. To add a third video, copy one whole `<figure class="phone">...</figure>` block.
Tip: iPhone .mov must be converted to .mp4 (H.264).

## Change model pictures / car picture
In `config.js`: `gallery[].image` and `heroCarImage`. Put your pictures in `images/`. Leave "" to use the built-in artwork.

## Change the supercar pictures
In `config.js`, edit the `cars` list: put your own photos in `images/` and set `image: "images/my-car.jpg"`. Add or remove lines freely.

## Prices and checkout links
In `config.js`: `prices` and `links` (Stripe, Whop, Gumroad, Calendly).

## Deploy
1. Create a GitHub repo and push this folder:
   git init && git add . && git commit -m "Launch site"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/7-figures-printers.git
   git push -u origin main
2. vercel.com > Add New > Project > import the repo > Deploy.
Every later `git push` redeploys automatically.
