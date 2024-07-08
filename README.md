#Product list project

#Objective
The Objective of this #asessment is to work with ReST API's , understand asynchronous programming and build interactive web pages using Javascript.

## Instructions

### HTML Structure

- Create two sections/lists in your HTML page:
  - **Products**: To display the list of products.
  - **Save for Later**: To display the list of saved items.

### JavaScript Functions

Create the following functions in `public/js/script.js`:

1. `getProducts()`
   - Fetch products from `http://localhost:3000/products`.
   - Populate them in the DOM under `<ul id="products">`.
   - Return a promise with the JSON response from the API.

2. `getsaveforlater()`
   - Fetch saved items from `http://localhost:3000/saveforlater`.
   - Populate them in the DOM under `<ul id="saveforlaterList">`.
   - Return a promise with the JSON response from the API.

3. `addsaveforlater(id)`
   - Click event handler for the "Add to Save for Later" button corresponding to each product.
   - Take the `id` of a product as input, copy the respective product to the "Save for Later" section.
   - Post the product to `db.json` via `http://localhost:3000/saveforlater`.
   - Return a promise with the complete list of saved items loaded on the page.

4. `Deletesaveforlater(id)`
   - Function to delete a product from the save for later list by passing the `id`.

### Running the Project

1. Start the JSON server.
2. Open `index.html` in your browser:
   - The products and save for later lists should be populated on page load.
3. Interact with the page:
   - Click "Add to Save for Later" to move items to the save for later list.
   - Items should be added to `db.json` under the `saveforlater` collection.
   - Remove items from the save for later list by clicking the "Remove from Save for Later" button.
