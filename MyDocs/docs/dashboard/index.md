---
title: Dashboard
icon: material/view-dashboard
---

# <span class="h1">Population française</span>

<p class="intro">
    Application interactive d'analyse démographique française avec <strong>Streamlit</strong>
</p>

---

## <span class="h2">Introduction</span>

Ce projet a pour but d'analyser les vrais chiffres de la population (données publique `'data.gouv.fr'`) et d'étudier les différentes corrélation sur **la violence exercées sur les femmes en france**.

> Le but de ce projet est de trouver des patterns sur la condition de l'agresseur et de l'agressé pour mieux prévenir le danger.

[:fontawesome-brands-github:  Repo Github](https://github.com/Lamizana/Dashboard-population-France){ .md-button  }

---

## <span class="h2">Sections disponibles</span>

| Section | Description | Status |
|---------|-------------|--------|
| Décès | Analyse des décès par âge, sexe, période | ✅ Opérationnel |
| Naissance | Données de natalité | 🔜 À venir |
| Population | Vue d'ensemble démographique | 🔜 À venir |
| Violences | Statistiques sur les violences | 🔜 À venir |
| Féminicides | Données sur les féminicides | 🔜 À venir |

---

## Technologies utilisées


<div class="soft-skills-grid">

<div class="soft-skill-card">
    <span class="soft-skill-title">Streamlit</span><br><br>
    <span class="soft-skill-desc">Framework web interactif</span>
</div>

<div class="soft-skill-card">
    <span class="soft-skill-title">Plotly</span><br><br>
    <span class="soft-skill-desc"> Visualisations dynamiques</span>
</div>

<div class="soft-skill-card">
    <span class="soft-skill-title">Pandas</span><br><br>
    <span class="soft-skill-desc">Manipulation des données</span>
</div>

<div class="soft-skill-card">
    <span class="soft-skill-title">GeoPandas</span><br><br>
    <span class="soft-skill-desc">Cartographie</span>
</div>

<div class="soft-skill-card">
    <span class="soft-skill-title">INSEE</span><br><br>
    <span class="soft-skill-desc">Source des données démographiques</span>
</div>

</div>

---

## Dashboard

<style>
    .dashboard-container {
        position: relative;
        width: 100%;
        height: 85vh;  /* Hauteur adaptative */
        border: 1px solid #ddd;
        border-radius: 8px;
        overflow: hidden;
        box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    }
    .dashboard-container iframe {
        width: 100%;
        height: 100%;
        border: none;
    }
    .loading-message {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        color: #666;
        font-family: sans-serif;
    }
</style>

<div class="dashboard-container">
    <iframe 
        src="https://dashboard-population-france.streamlit.app/?embed=true"
        loading="lazy"
        title="Dashboard Population France">
    </iframe>
</div>

---

*Source : INSEE | data.gouv.fr*
