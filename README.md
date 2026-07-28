# 🌪️ TAZZ KITE — Vent & spots kite autour de Marseille

**Le vent décide. Tazz t'envoie.**

Page statique (GitHub Pages) qui aide à décider **quand partir et où aller** kiter autour de Marseille :

- 🗺️ **10 spots** : Le Jaï, Berre Plage, Carro, Sainte-Croix, Les Laurons, Plage Napoléon, Beauduc, La Ciotat, Six-Fours, L'Almanarre
- 📈 **Prévisions 7 jours** : Open-Meteo — modèle AROME Météo-France (haute résolution, J0→J+4) fusionné avec le meilleur modèle global (J+4→J+7)
- 📡 **Vent réel** :
  - balise **Pioupiou** La Capte (Almanarre) appelée en direct depuis le navigateur
  - **METAR** des aérodromes de Marignane, Istres, Le Castellet et Toulon-Hyères, rafraîchis toutes les 30 min par une GitHub Action (l'API aviationweather.gov n'autorise pas les appels navigateur)
- 🪁 **Reco d'ailes automatique** pour deux gabarits (75 kg / 50 kg par défaut, modifiable) avec un quiver partagé 5 / 9 / 12 m² — arbitrage inclus quand les deux veulent la même aile
- ✅ Chaque spot connaît ses **directions de vent idéales** : une case n'est « GO » que si la direction colle

## Fonctionnement

Tout est dans [`index.html`](index.html) (zéro dépendance, zéro clé API). Les réglages (prénoms, poids, quiver) sont stockés en localStorage.

`.github/workflows/metar.yml` tourne toutes les 30 min et commite `data/metar.json` s'il a changé.

> ⚠️ GitHub désactive les crons après 60 jours sans activité sur le repo — un petit commit de temps en temps les relance, ou re-activer dans l'onglet Actions.

## Sécurité

Le kite en side-off (Carro, le Jaï côté étang par Mistral) exige autonomie et moyens de sécu. Vérifiez les arrêtés municipaux et les corridors de navigation estivaux. Cette page est une aide à la décision, pas un bulletin officiel.

---

🤖 Généré avec [Claude Code](https://claude.com/claude-code) — esprit PragmaForma, mascotte Tazz 100 % originale.
