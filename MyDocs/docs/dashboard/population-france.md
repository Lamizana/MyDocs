# <span class="h2">Population france</span>

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