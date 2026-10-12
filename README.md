# Atliekų kalendorius

Mažas internetinės programėlės prototipas, kuris perskaito naujausius buitinių, pakuočių ir stiklo atliekų grafikus iš oficialaus „Nemenčinės komunalininko“ grafikų puslapio ir leidžia ieškoti pagal gyvenvietę bei gatvę.

## Paleidimas

Reikia Python 3.11 arba naujesnio.

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
streamlit run app.py
```

Programa periodiškai iš naujo patikrina oficialų grafikų puslapį. Ji nesaugo naudotojo adreso serveryje; paieška atliekama įvedus tekstą.

## Kaip pasidalinti nuoroda

Paprasčiausias variantas — įkelti šio aplanko turinį į atskirą GitHub saugyklą ir prijungti ją prie [Streamlit Community Cloud](https://share.streamlit.io/). Kuriant programėlę nurodyk pagrindinį `app.py` failą. Po publikavimo gausi `streamlit.app` nuorodą, kurią galėsi nusiųsti kaimynui.

Šis prototipas neturi prisijungimų ar el. pašto prenumeratų. Prieš įkeliant kodą į GitHub, nekelk `.venv` aplanko ar jokių slaptažodžių ir API raktų. `.gitignore` jau paslepia virtualią aplinką ir vietinį „Streamlit“ paslapčių failą.

## El. pašto priminimai — vėlesnis etapas

Priminimams reikės duomenų bazės, kur būtų išsaugotas naudotojo el. paštas, pasirinktas grafiko įrašas ir sutikimas gauti pranešimus. Atskiras kasdienis procesas patikrintų artėjančius išvežimus ir per el. pašto siuntimo paslaugą išsiųstų priminimus. Programėlėje taip pat reikėtų atsisakymo nuorodos ir galimybės ištrinti prenumeratą.

## Dabartinės prototipo ribos

- PDF grafikuose gali būti kelių gyvenviečių, gatvių, numerių intervalų ir išimčių aprašymai vienoje eilutėje. Paieška parodo galimas grafiko grupes, o ne garantuotai patvirtina konkretų namo numerį.
- Pirmoji versija neremia priminimų ir kalendoriaus prenumeratos.
- Jei „Nemenkom“ pakeis puslapio ar lentelių struktūrą, parsavimo taisykles reikės atnaujinti.
