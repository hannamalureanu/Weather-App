# 🌤️ Weather App – Full Stack (Flask + React)

Aplicație web completă care furnizează date meteo actuale și prognoză pe 5 zile pentru orice oraș din lume. Include hartă interactivă, istoric al căutărilor (salvat în fișier CSV), grafice cu evoluția temperaturii și umidității, și suport pentru temă dark/light cu persistentă în localStorage.

---

## 🚀 Funcționalități principale

- **Vremea curentă** – temperatură, umiditate, presiune, descriere, viteză vânt, pictogramă.
- **Prognoză 5 zile** – o zi pe card, cu toate detaliile.
- **Grafic dual** – evoluția temperaturii și umidității în aceleași axe (cu scale separate).
- **Hartă interactivă** – localizarea orașului pe hartă OpenStreetMap (folosind Leaflet).
- **Istoric căutări** – fiecare căutare de vreme curentă se salvează automat într-un fișier CSV (`history.csv`).
  - Exportă istoricul ca fișier CSV direct din interfață.
  - Șterge tot istoricul cu un singur buton.
- **Temă dark / light** – comutator vizual, iar preferința utilizatorului este salvată în `localStorage` și restaurată la reîncărcare.
- **Persistența ultimului oraș** – după reîmprospătarea paginii, aplicația încarcă automat datele pentru ultimul oraș căutat.

---

## 🧰 Tehnologii utilizate

### Backend (Python)
- **Flask** – framework web pentru crearea API-urilor.
- **Flask-CORS** – permite cereri cross-origin de la frontend.
- **Requests** – consumul API-ului OpenWeatherMap.
- **python-dotenv** – gestionarea variabilelor de mediu (cheia API).
- **CSV** – salvare și citire a istoricului căutărilor.

### Frontend (React)
- **React** (functional components, hooks) – interfața utilizator.
- **Recharts** – graficul cu două axe (temperatură / umiditate).
- **React-Leaflet** + **Leaflet** – hartă interactivă și marker.
- **CSS3** – stilizare, tranziții, temă dark/light.

### API extern
- **OpenWeatherMap** – furnizează datele meteo curente și prognoza.

---

## 📂 Structura proiectului

Proiectul este organizat în două părți principale: backend (Python) și frontend (React).

- **backend/** – aici se află serverul Flask, fișierul cu cheia API, dependințele Python și istoricul salvat.
- **frontend/** – aici este interfața aplicației, componentele React, stilurile și configurațiile.
- **.gitignore** – ascunde fișierele care nu trebuie încărcate pe GitHub (de exemplu, mediul virtual, modulele Node, cheia secretă).
- **README.md** – acest fișier.

În backend vei găsi:
- `app.py` – codul principal al serverului
- `.env` – fișierul tău secret cu cheia API (nu se încarcă pe GitHub)
- `.env.example` – un exemplu pentru alți utilizatori
- `requirements.txt` – lista cu toate bibliotecile Python necesare
- `history.csv` – se creează automat după primele căutări

În frontend vei găsi:
- `src/App.js` – componenta principală
- `src/App.css` – stilurile pentru temă light/dark
- `src/MapComponent.jsx` – harta interactivă
- `src/ThemeContext.js` – gestionarea temei și persistenta în localStorage
- `public/` – fișiere statice
- `package.json` – dependințele React

---
