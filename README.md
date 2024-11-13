# 🌱 Plantsy App

Welcome to **Plantsy**! This application is designed for managing a plant store’s inventory, allowing users to add, update, search, view, and remove plants. It’s specifically built for administrators to maintain the plant catalog.

## Table of Contents

- [Project Overview](#project-overview)
- [Setup Instructions](#setup-instructions)
- [Features](#features)
  - [Core Features](#core-features)
  - [Advanced Features](#advanced-features)
- [Usage](#usage)
- [Endpoints](#endpoints)
- [Technologies Used](#technologies-used)
- [Deployment](#deployment)

## Project Overview

**Plantsy** is a React-based web app that interacts with a backend API to manage plant data. It allows users to:

- View a list of all plants.
- Add new plants to the inventory.
- Mark plants as sold out.
- Search plants by their name.
- Update plant prices.
- Remove plants from the inventory.

The app uses **React** for the frontend and a JSON server to manage backend operations.

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/briankipyegoon/react-hooks-cc-plantshop.git
cd react-hooks-cc-plantshop
```

### 2. Install Dependencies

Use this command to install all necessary dependencies:

```bash
npm install
```

### 3. Start the JSON Server

Launch the backend JSON server to manage API requests. It will run at `http://localhost:6001`.

```bash
npm run server
```

You can visit `http://localhost:6001/plants` to check that the backend is running correctly.

### 4. Start the React App

In a new terminal window, run the following to start the app:

```bash
npm start
```

The app will be available at `http://localhost:3000`.

### 5. Access the App

Go to `http://localhost:3000` in your browser to view the application.

## Features

### Core Features

1. **View All Plants**: The app displays all plants loaded from the backend when it starts.
2. **Add a New Plant**: Users can add a new plant to the catalog using a form. The new plant is instantly added to the list and saved to the backend.
3. **Mark as Sold Out**: Users can toggle the availability status of a plant between "In Stock" and "Out of Stock."
4. **Search for Plants**: The search bar allows users to filter plants by name, updating the displayed list in real-time.

### Advanced Features

1. **Update Plant Price**: Users can edit the price of a plant from the plant card, and the change will be saved to the backend.
2. **Delete a Plant**: Users can remove plants from the inventory, which will also delete them from the backend.

## Usage

### Add a Plant

To add a plant, fill out the "Plant Name", "Image URL", and "Price" fields in the form at the top, then click **Add Plant**. The plant will appear in the list.

### Search for Plants

Type part of a plant's name in the search bar to filter the list. The results will update dynamically as you type.

### Update Plant Price

To change a plant’s price, enter the new amount in the price field on the plant card and click **Update Price** to save the change. This update will be reflected in the backend.

### Mark a Plant as Sold Out

Each plant card has an **In Stock** button. Clicking this toggles the plant’s availability status between "In Stock" and "Out of Stock."

### Delete a Plant

Click the **Delete** button on a plant card to remove that plant from both the inventory list and the backend.

## Endpoints

The app connects to a local JSON server at `http://localhost:6001`. Below are the key API endpoints:

### GET `/plants`

Fetches the list of all plants.

#### Example Response:

```json
[
  {
    "id": 1,
    "name": "Aloe",
    "image": "./images/aloe.jpg",
    "price": 15.99
  },
  {
    "id": 2,
    "name": "ZZ Plant",
    "image": "./images/zz-plant.jpg",
    "price": 25.98
  }
]
```

### POST `/plants`

Adds a new plant to the inventory.

#### Request Headers:

```json
{
  "Content-Type": "application/json"
}
```

#### Request Body Example:

```json
{
  "name": "Snake Plant",
  "image": "./images/snake-plant.jpg",
  "price": 30.0
}
```

#### Example Response:

```json
{
  "id": 3,
  "name": "Snake Plant",
  "image": "./images/snake-plant.jpg",
  "price": 30.0
}
```

### PATCH `/plants/:id`

Updates the price of a specific plant.

#### Request Body Example:

```json
{
  "price": 35.0
}
```

### DELETE `/plants/:id`

Removes a plant from the inventory.

#### Example Response:

```json
{}
```

## Technologies Used

- **Frontend**: React, HTML, CSS, JavaScript.
- **Backend**: JSON Server (simulates a REST API).
- **Tools**: npm, Fetch API.

## Deployment

The app is live and can be accessed here:  
[Plantsy Live](https://spontaneous-sunshine-b01107.netlify.app/)

## License

This project is licensed under the MIT License.

---

This version maintains the original structure but uses different wording to convey the same ideas. Let me know if you need further revisions!
