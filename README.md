# KHG Auto Workshops Website

Updated website files for KHG Auto Workshops.

## Main files

- `index.html` — Home page with featured vehicles, automotive service slider and Google review slider.
- `vehicles.html` — Vehicle listing page with search and price filter.
- `vehicle-detail.html` — Dynamic vehicle detail page. Vehicle cards link here using the vehicle `id` from `vehicles-data.js`.
- `sell-your-car.html` — Sell/trade enquiry form.
- `finance.html` — Finance enquiry form.
- `contact.html` — Contact page and contact form.
- `styles.css` — Website styling and responsive layout.
- `main.js` — Menu, sliders, vehicle cards, filters and vehicle detail rendering.
- `vehicles-data.js` — Edit dummy stock, services and reviews here.
- `assets/logo.png` — Logo.

## Vehicle editing

Add or edit vehicles inside `vehicles-data.js`. There are now 30 dummy vehicle listings. Every vehicle must have a unique `id`. The vehicle cards automatically link to:

`vehicle-detail.html?id=vehicle-id-here`

### How to add multiple vehicle images

1. Put your vehicle photos inside:

`assets/vehicles/`

2. Use simple file names, for example:

`corolla-front.jpg`
`corolla-side.jpg`
`corolla-back.jpg`
`corolla-interior.jpg`

3. Open `vehicles-data.js` and find the car you want to update. Keep `image` as the main listing image, then add every photo inside `images` like this:

```js
image: "assets/vehicles/corolla-front.jpg",
images: [
  "assets/vehicles/corolla-front.jpg",
  "assets/vehicles/corolla-side.jpg",
  "assets/vehicles/corolla-back.jpg",
  "assets/vehicles/corolla-interior.jpg"
],
```

4. You can add any number of images. One car can have 4 images and another car can have 9 or more images. The vehicle detail page will automatically show the main photo with a thumbnail sidebar.

5. The first image in `images` should normally be the front/main car photo. The vehicle list page uses `image`, so keep that filled in as well.

6. Recommended image size: around 1200px wide, landscape/horizontal photos, JPG or PNG.

## Form sending

The Sell Your Car, Finance and Contact forms use FormSubmit AJAX to send enquiries directly to:

`info@khgautoworkshops.com.au`

The forms now submit without redirecting users to a FormSubmit page. Users stay on the same page and see a success or error message below the form.

## Google review slider

The review slider content is stored in `vehicles-data.js` under `reviews`. Replace or add reviews there whenever needed.
