# 🎉 Party Menu Application

A responsive React web app for browsing, filtering, and saving dishes from a curated party menu — built with React 19, React Router DOM 7, and Vite 6.

## Overview

Party Menu lets a signed-in user browse a catalogue of dishes, filter them by category and diet, search by name, view full dish details, and save favourite recipes for later — all persisted in the browser's local storage.

## Features

- **Authentication** against a live sign-in API, with token/user persistence and auto-redirect for already-authenticated users
- **Protected route** for the main Menu page (`/`) — all other routes are public
- **Category filters**: All, Starter, Main, Sides, Desert
- **Diet filters**: All, Veg, Non-Veg
- **Case-insensitive search** by dish name
- **Food Detail page** with full description, ingredients list, and a Save/Saved toggle
- **Saved Recipes page** with remove support and an instantly-updating header badge
- **404 page** with a context-aware link (Menu if signed in, Sign In otherwise)
- **Responsive design** (desktop / tablet / mobile) using Flexbox & CSS Grid, plain CSS only
- Loading states, error banners, and empty states throughout

## Installation

```bash
npm install
```

## Run instructions

```bash
npm run dev       # start the local dev server (Vite)
npm run build      # production build -> dist/
npm run preview    # preview the production build locally
```

## Folder structure

```
src/
  components/     Reusable UI building blocks (FoodCard, FilterBar, Navbar, ...)
  pages/          Route-level pages (SignIn, Menu, FoodDetail, SavedRecipes, NotFound)
  context/        AuthContext (React Context API)
  hooks/          useAuth, useSavedRecipes
  utils/          localStorage helpers + auth API client
  data/           Static menuData.js (filterMenuItems, getMenuItemById)
  styles/         index.css (design tokens + all component styles)
  App.jsx         Route definitions
  main.jsx        App entry point
```

## Authentication

- **Endpoint:** `POST https://serverless-api-teal.vercel.app/api/auth/signin`
- **Test credentials:** `admin@example.com` / `admin123`
- On success, the token and user object are saved to local storage (`party_menu_token`, `party_menu_user`) and the app redirects to `/`.
- On failure, the API's error message is shown in an error banner and the user stays on `/signin`.
- If a token already exists, visiting `/signin` redirects straight to the Menu page.

## Routes

| Route | Access | Description |
|---|---|---|
| `/signin` | Public | Sign in form |
| `/` | **Protected** | Menu page — requires a token |
| `/menu/:id` | Public | Dish detail page |
| `/saved-recipes` | Public | Saved recipes list |
| `*` | Public | 404 Not Found |

## Local storage keys

| Data | Key |
|---|---|
| Auth token | `party_menu_token` |
| User object | `party_menu_user` |
| Saved recipes | `party_menu_saved_recipes` |

## Menu data

Menu items are **static** (no API call) and live in `src/data/menuData.js`, following this schema per item: `id, name, category, isVeg, description, fullDescription, image, ingredients[], servings`.

> **Note:** The original assignment JSON (`rfcd.json`) is hosted behind an authenticated assessment URL that couldn't be fetched automatically while building this project. `menuData.js` ships with a hand-written dataset that follows the exact same schema and exports the same `filterMenuItems(params)` / `getMenuItemById(id)` functions — so you can swap in the real JSON array (assign it to the `menuItems` export) without touching any other file.

## Technologies

- React 19
- React Router DOM 7
- Vite 6
- Plain CSS (Flexbox + Grid, no UI framework)

## Deployment

This is a static Vite build, deployable to Vercel or Netlify:

```bash
npm run build
```

Deploy the generated `dist/` folder, or connect the repo directly to Vercel/Netlify and set the build command to `npm run build` with output directory `dist`.
