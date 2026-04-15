---
title: Dashboard
---

# <span class="h1">Dashboard - Population France</span>

<p class="intro">
    Application interactive d'analyse démographique française avec <strong>Streamlit</strong>
</p>

---

## <span class="h2">Introduction</span>

Ce projet a pour but d'analyser les vrais chiffres de la population (données publique 'data.gouv.fr') et d'étudier les différentes corrélation sur **la violence exercées sur les femmes en france**.

> Le but de ce projet est de trouver des patterns sur la condition de l'agresseur et de l'agressé pour mieux prévenir le danger.

[:fontawesome-brands-github:  Repo Github](https://github.com/Lamizana/Dashboard-population-France){ .md-button  }

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
