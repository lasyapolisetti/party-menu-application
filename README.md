# 🍽️ Party Menu Application

A modern, responsive food discovery web application built with **React 19**, **Vite**, and **React Router DOM 7**. The application provides a seamless browsing experience where users can securely sign in, explore a curated party menu, filter dishes based on preferences, view detailed recipe information, and save their favorite recipes for future access.

The project demonstrates modern React development practices, including authentication, protected routing, reusable components, state management using Context API, responsive design, and persistent client-side storage.

---

## 📸 Preview

Login page :
<img width="1892" height="896" alt="image" src="https://github.com/user-attachments/assets/611b1bbc-5279-42ca-b6e4-4a9b6b847648" />

Menu Page :
<img width="1895" height="353" alt="image" src="https://github.com/user-attachments/assets/bd24f852-3a41-4b0c-b1da-05dfc3882c42" />
<img width="1877" height="516" alt="image" src="https://github.com/user-attachments/assets/521f0e58-9df7-46e1-b075-2d5ad8e02c50" />

After Selecting an item :
<img width="875" height="546" alt="image" src="https://github.com/user-attachments/assets/d4072821-65b1-4988-b35c-098aaf6da183" />


---

# ✨ Features

## 🔐 User Authentication

- Secure user authentication using the provided Sign In API.
- Displays loading state while authenticating.
- Shows appropriate error messages for invalid credentials.
- Stores authentication token and user information in Local Storage.
- Automatically redirects authenticated users to the Menu page.
- Clears authentication data during logout.

---

## 🛡️ Protected Routing

- Implements route protection using a custom `ProtectedRoute` component.
- Prevents unauthorized users from accessing the main Menu page.
- Automatically redirects unauthenticated users to the Sign In page.
- Maintains authentication state across browser refreshes.

---

## 🍽️ Interactive Menu Browser

The main menu page provides an intuitive interface for discovering dishes.

Users can:

- Browse all available menu items
- View dish cards in a responsive grid layout
- See total number of matching dishes
- Navigate directly to detailed recipe pages

Each food card displays:

- Dish image
- Veg / Non-Veg badge
- Category
- Dish name
- Short description
- Serving information

---

## 🔍 Search Functionality

Users can quickly find dishes by entering keywords.

Features include:

- Case-insensitive search
- Partial text matching
- Instant filtering after clicking the Search button
- Proper empty-state handling when no dishes match

---

## 🏷️ Category Filtering

Filter menu items based on food categories.

Available filters include:

- All
- Starter
- Main Course
- Sides
- Dessert

The displayed menu updates dynamically based on the selected category.

---

## 🥗 Diet Filtering

Users can filter dishes based on dietary preferences.

Options include:

- All
- Vegetarian
- Non-Vegetarian

Filters work seamlessly alongside category selection and search functionality.

---

## 📖 Food Detail Page

Each dish has a dedicated detail page displaying complete information.

Information includes:

- Hero image
- Dish name
- Category
- Veg / Non-Veg badge
- Number of servings
- Complete description
- Ingredients list
- Save / Remove Recipe option
- Navigation back to the Menu page

---

## ❤️ Saved Recipes

Users can bookmark their favorite dishes for quick access.

Features include:

- Save recipes from the detail page
- Remove saved recipes anytime
- Live badge displaying total saved recipes
- Persistent storage using Local Storage
- Responsive saved recipes page
- Empty state when no recipes have been saved

---

## 💾 Persistent Local Storage

Application data persists even after refreshing the browser.

Stored data includes:

- Authentication Token
- User Information
- Saved Recipes

---

## 📱 Responsive Design

The application is fully responsive and optimized for different screen sizes.

Supports:

- Desktop
- Tablet
- Mobile

Responsive layouts are implemented using modern CSS Grid and Flexbox.

---

## ⚠️ Error Handling

The application gracefully handles various error scenarios, including:

- Invalid login credentials
- Authentication failures
- Missing menu items
- Empty search results
- Empty saved recipe list
- Unknown routes (404)

---

## 🚪 Logout

Users can securely log out of the application.

Logging out:

- Removes authentication token
- Clears user information
- Redirects back to the Sign In page

---

# 🛠️ Tech Stack

| Technology | Purpose |
|------------|----------|
| React 19 | Frontend Framework |
| Vite 6 | Build Tool |
| React Router DOM 7 | Client-side Routing |
| Context API | Global State Management |
| JavaScript (ES6+) | Application Logic |
| HTML5 | Structure |
| CSS3 | Styling |
| Local Storage | Client-side Persistence |

---

# 📂 Project Structure

```
party-menu-app/
│
├── public/
│
├── src/
│   ├── assets/
│   ├── components/
│   ├── context/
│   ├── data/
│   ├── hooks/
│   ├── pages/
│   ├── routes/
│   ├── styles/
│   ├── utils/
│   ├── App.jsx
│   └── main.jsx
│
├── package.json
├── vite.config.js
└── README.md
```

---

# 🚀 Getting Started

## Clone the Repository

```bash
git clone https://github.com/your-username/party-menu-application.git
```

## Navigate to the Project

```bash
cd party-menu-application
```

## Install Dependencies

```bash
npm install
```

## Start Development Server

```bash
npm run dev
```

## Build for Production

```bash
npm run build
```

---

# 🔑 Test Credentials

Use the following credentials to access the application.

```
Email:
admin@example.com

Password:
admin123
```

---

# 💾 Local Storage Keys

| Key | Description |
|------|-------------|
| party_menu_token | Stores authentication token |
| party_menu_user | Stores authenticated user information |
| party_menu_saved_recipes | Stores saved recipes |

---

# 🌍 Deployment

The application can be deployed using platforms such as:

- Vercel
- Netlify

---

# 🎯 Learning Outcomes

This project demonstrates practical implementation of:

- React Component Architecture
- Context API
- Protected Routes
- API Integration
- Local Storage Management
- Client-side Routing
- Reusable UI Components
- State Management
- Responsive Web Design
- Modern JavaScript (ES6+)
- CSS Grid & Flexbox
- Clean Project Organization

---

# 👨‍💻 Author

**Lasya Polisetty**

B.Tech Student | Frontend Developer

---

## 📄 License

This project was developed for educational and learning purposes as part of a frontend web development assignment.
