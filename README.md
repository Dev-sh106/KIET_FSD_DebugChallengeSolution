Here we have fix the bugs.
Bug 1: Boundary Price Filtering
Issue: Products at exact boundary prices (e.g., ₹500) were being excluded from filters.
Fix: Updated the matchPrice logic to use >= and <= operators, ensuring boundary prices are included in the filtered results.
Bug 2: Category Filter Inactivity
Issue: Clicking category buttons had no effect on the product grid.
Fix: Correctly implemented the matchCategory filter in useMemo to check if a product's category matches the selected state.
Bug 3: Faulty Delete Logic
Issue: The cart delete button removed all items except the one clicked.
Fix: Fixed the removeFromCart function to filter out only the item with the matching id.
Bug 4: Cart Badge Count
Issue: The header badge always showed 0 or nothing.
Fix: Implemented a proper reduce function to sum up the qty of all items in the cartItems array.
Bug 5: "Added" Button State
Issue: The "Add to Cart" button didn't reflect that a product was already in the cart.
Fix: Passed a boolean inCart prop to the ProductCard component by checking the product ID against the current cart items.
Bug 6: Incorrect Cart Total
Issue: The total always displayed ₹0.
Fix: Updated the total calculation to correctly multiply each item's price by its quantity using .reduce().
Bug 7: Quantity Boundary Issue
Issue: The minus (−) button allowed quantities to drop to 0 or below.
Fix: Added a disabled attribute to the decrease button that triggers when item.qty <= 1.
Bug 8: Inverted Sort Order
Issue: "Price: Low to High" sorted items in descending order and vice versa.
Fix: Corrected the comparison logic in the sortBy switch case within App.js to ensure proper ascending/descending order.
Bug 9: Rating Rounding Error
Issue: A 4.5 rating showed only 4 stars instead of rounding up.
Fix: Changed the star fill logic to use Math.round(rating) so that half-star ratings are displayed correctly.

























# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
