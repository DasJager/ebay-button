# eBay Buy It Now Confirmation Script I was bored so I made this for my grandma :)

## Overview

This Tampermonkey script replaces the "Buy It Now" button on eBay with a custom button that requires user confirmation before proceeding with the purchase. The script dynamically fetches the logged-in user's name and personalizes the confirmation message. This added step helps prevent accidental purchases by ensuring the user explicitly confirms their intent to buy an item.

![Button](https://github.com/DasJager/ebay-button/blob/main/button.gif)

![Button Clicked](https://github.com/DasJager/ebay-button/blob/main/clickbutton.gif)

## Features

- **Custom "Buy It Now" Button**: Replaces the default "Buy It Now" button with a more prominent, custom-styled button.
- **Personalized Confirmation Modal**: Displays a confirmation modal asking the user by name if they are sure they want to proceed with the purchase.
- **Safe Navigation**: Only navigates to the purchase page if the user confirms their intent by clicking "Yes" in the modal.

## Installation

### Prerequisites

- **Browser**: This script is designed to run in any modern web browser that supports Tampermonkey.
- **Tampermonkey**: Ensure that you have the [Tampermonkey extension](https://www.tampermonkey.net/) installed in your browser.

### Steps

1. **Install Tampermonkey**: If you haven't already, install the Tampermonkey extension in your browser.
2. **Add the Script**:
   - Open the Tampermonkey dashboard by clicking on the Tampermonkey icon in your browser toolbar and selecting "Dashboard."
   - Click the "+" button to create a new script.
   - Copy the entire script from this repository and paste it into the Tampermonkey script editor.
   - Save the script.
3. **Visit eBay**: Navigate to any eBay item page that has a "Buy It Now" option. The original "Buy It Now" button will be replaced by the custom button.

## How It Works

- **Button Replacement**: The script identifies the "Buy It Now" button on the eBay page and replaces it with a custom button that says, "Are you sure you want to buy this?"
- **User Name Retrieval**: The script attempts to fetch the logged-in user's name from the eBay page. If it can't find the name, it defaults to "user."
- **Confirmation Modal**: When the custom button is clicked, a modal appears with a personalized message, "Are you sure you want to buy this, [User Name]?"
- **Conditional Navigation**: If the user clicks "Yes," the script redirects the browser to the purchase URL. If "No" is clicked, the modal simply closes, and no action is taken.

## Usage Notes

- **Personalization**: The script personalizes the confirmation modal using the username found on the eBay page. This feature enhances user experience by making the prompt more relevant.
- **Security**: The script only runs on eBay pages (`https://www.ebay.com/*`) and does not access any sensitive information other than the visible username on the page.

## Limitations

- **Username Detection**: The script depends on the current structure of eBay’s webpage to find the username. If eBay changes its layout, the script may need to be updated to continue working properly.

## License

This project is licensed under the MIT License. Feel free to modify and distribute the script according to the terms of this license.
