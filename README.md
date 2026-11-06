# Questlog – Projektchecklista

## Projektbeskrivning
Questlog är en React-applikation där användaren kan hålla koll på sina spel. Det går att visa, skapa, redigera och ta bort spel samt filtrera dem efter status.

Applikationen använder Questlog API för att hantera data.

---

## 1. Projektuppsättning
- [ ] Skapa React-projekt med Vite och TypeScript.
- [ ] Installera React Router.
- [ ] Skapa projektets mappstruktur.
- [ ] Skapa TypeScript-typ för spel (`Game`).
- [ ] Skapa grundläggande layout och navigation.

## 2. Sidor och routing (G-krav)
- [ ] Skapa en sida som visar alla spel (`/games`).
- [ ] Skapa en detaljsida för ett specifikt spel (`/games/:id`).
- [ ] Skapa en sida för att lägga till nya spel (`/games/new`).
- [ ] Skapa en 404-sida för okända adresser.
- [ ] Implementera React Router.
- [ ] Skapa en gemensam layout med navigation mellan sidorna.

## 3. API och CRUD (G-krav)
- [ ] Anslut applikationen till Questlog API.
- [ ] Hämta och visa alla spel (GET).
- [ ] Hämta och visa ett specifikt spel (GET).
- [ ] Skapa nya spel (POST).
- [ ] Redigera befintliga spel (PATCH).
- [ ] Ta bort spel (DELETE).
- [ ] Skicka med rätt `handle` i API-anropen.
- [ ] Kontrollera `response.ok` vid API-anrop.
- [ ] Hantera fel från API:et.

## 4. Statusfilter (G-krav)
- [ ] Visa filter för alla spel.
- [ ] Skapa filter för Want to play.
- [ ] Skapa filter för Playing.
- [ ] Skapa filter för Completed.
- [ ] Skapa filter för Dropped.
- [ ] Se till att filtreringen visar rätt spel.

## 5. Komponenter (G-krav)
- [ ] Skapa återanvändbara komponenter.
- [ ] Skapa en Navbar-komponent.
- [ ] Skapa en GameCard-komponent.
- [ ] Skapa en GameList-komponent.
- [ ] Skapa en StatusFilter-komponent.
- [ ] Skapa en Loading-komponent.
- [ ] Skapa en ErrorMessage-komponent.
- [ ] Skicka data mellan komponenter med props.

## 6. Laddning och felhantering (G-krav)
- [ ] Visa ett laddningsmeddelande medan spel hämtas.
- [ ] Visa ett laddningsmeddelande på detaljsidan.
- [ ] Visa ett tydligt felmeddelande om API-anrop misslyckas.
- [ ] Hantera om ett spel inte hittas.
- [ ] Förhindra att formulär skickas med ogiltiga uppgifter.

## 7. Custom hooks (VG-krav)
- [ ] Skapa `useGames(status)` för att hämta spellistan.
- [ ] Skapa `useGame(id)` för att hämta ett specifikt spel.
- [ ] Skapa `useSaveGame()` för POST, PATCH och DELETE.
- [ ] Flytta all API- och fetch-logik till egna hooks.
- [ ] Se till att komponenterna använder hooks istället för att själva göra API-anrop.
- [ ] Samla hooks i mappen `src/hooks/`.

## 8. use




# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Oxc](https://oxc.rs)
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/)

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type-aware lint rules:

```js
export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...

      // Remove tseslint.configs.recommended and replace with this
      tseslint.configs.recommendedTypeChecked,
      // Alternatively, use this for stricter rules
      tseslint.configs.strictTypeChecked,
      // Optionally, add this for stylistic rules
      tseslint.configs.stylisticTypeChecked,

      // Other configs...
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])

```

You can also install [eslint-plugin-react-x](https://npmx.dev/package/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://npmx.dev/package/eslint-plugin-react-dom) for React-specific lint rules:

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...
      // Enable lint rules for React
      reactX.configs['recommended-typescript'],
      // Enable lint rules for React DOM
      reactDom.configs.recommended,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])

```
