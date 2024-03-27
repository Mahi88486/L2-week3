# Pseudo Code
* Define global variables
* apiKey = 'WK8q9xsTpPb2kRCSX0siCczAHMR4R5vjCc8eN10fsKJ5a9DZFzo0Dedw';
* searchResultsContainer = document.getElementById('search-results');
* similarResultsContainer = document.getElementById('similar-results');
* wishlistContainer = document.getElementById('wishlist');
* wishlistItemsContainer = document.getElementById('wishlist-items');

* Function to fetch images from Pexels API based on search query
function fetchImages(searchQuery) {
    * Construct API URL with search query and API key
    apiUrl = `https://api.pexels.com/v1/search?query=${searchQuery}&per_page=10`;

    * Make API request using fetch or XMLHttpRequest with Authorization header
    * Handle API response and extract image data
    * Call displaySearchResults function with image data
}

* Function to display search results in searchResultsContainer
function displaySearchResults(imagesData) {
    * Clear previous search results
    searchResultsContainer.innerHTML = '';

    * Loop through imagesData and create image cards with add to wishlist button
    for each image in imagesData {
        createImageCard(image, searchResultsContainer);
    }
}

* Function to create image card with add to wishlist button
function createImageCard(image, container) {
    * Create image element with src from image data
    * Create name element with text from image data
    * Create add to wishlist button with onclick event to add item to wishlist
    * Create card container and append image, name, and button elements
    * Append card container to specified container (searchResultsContainer or similarResultsContainer)
}

* Function to add item to wishlist and update local storage
function addToWishlist(image) {
    * Check if item already exists in wishlist
    * If not, create image card with remove from wishlist button and append to wishlistItemsContainer
    * Update local storage with wishlist items
}

* Function to remove item from wishlist and update local storage
function removeFromWishlist(image) {
    * Remove item from wishlistItemsContainer
    * Update local storage with updated wishlist items
}

* Function to update local storage with wishlist items
function updateLocalStorage(wishlistItems) {
    * Convert wishlistItems array to JSON format and store in local storage
}

* Function to load wishlist items from local storage
function loadWishlistFromStorage() {
    * Retrieve wishlist items from local storage
    * If items exist, loop through them and create image cards in wishlistItemsContainer
}

* Function to initialize Splide.js sliders for similar results and wishlist sections
function initSliders() {
    * Initialize Splide slider for similar results section
    * Initialize Splide slider for wishlist section
    * Optionally, add event listeners for slider navigation
}

* Main code
document.addEventListener('DOMContentLoaded', () => {
    * Load wishlist items from local storage on page load
    loadWishlistFromStorage();

    * Initialize Splide.js sliders
    initSliders();

    * Example: Fetch images for initial search query and display search results
    fetchImages('nature');
});
