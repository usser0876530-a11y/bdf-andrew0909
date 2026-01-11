<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ANDREW - BOT 2 FICHE</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
        }

        .header {
            background: white;
            border-radius: 20px;
            padding: 30px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 30px;
        }

        .header-left {
            display: flex;
            align-items: center;
            gap: 20px;
        }

        .logo {
            width: 120px;
            height: auto;
        }

        .title {
            font-size: 32px;
            font-weight: 700;
            color: #2d3748;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .subtitle {
            font-size: 16px;
            color: #718096;
            margin-top: 5px;
        }

        .stats-container {
            display: flex;
            gap: 15px;
        }

        .stat-box {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 15px 25px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.3);
        }

        .stat-number {
            font-size: 28px;
            font-weight: 700;
        }

        .stat-label {
            font-size: 12px;
            opacity: 0.9;
            margin-top: 5px;
        }

        .controls {
            background: white;
            border-radius: 20px;
            padding: 30px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
            margin-bottom: 30px;
        }

        .upload-zone {
            border: 3px dashed #667eea;
            border-radius: 15px;
            padding: 40px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s;
            margin-bottom: 20px;
        }

        .upload-zone:hover {
            background: #f7fafc;
            border-color: #764ba2;
        }

        .upload-zone.dragover {
            background: #edf2f7;
            border-color: #764ba2;
        }

        .upload-icon {
            font-size: 48px;
            margin-bottom: 10px;
        }

        .search-bar {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .search-input {
            flex: 1;
            padding: 15px 20px;
            border: 2px solid #e2e8f0;
            border-radius: 12px;
            font-size: 16px;
            transition: all 0.3s;
        }

        .search-input:focus {
            outline: none;
            border-color: #667eea;
            box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1);
        }

        .btn {
            padding: 15px 30px;
            border: none;
            border-radius: 12px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
        }

        .btn-primary {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.3);
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 15px 40px rgba(102, 126, 234, 0.4);
        }

        .fiches-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(400px, 1fr));
            gap: 25px;
        }

        .fiche-card {
            background: white;
            border-radius: 20px;
            padding: 25px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.2);
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }

        .fiche-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
        }

        .fiche-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 2px solid #edf2f7;
        }

        .fiche-name {
            font-size: 22px;
            font-weight: 700;
            color: #2d3748;
        }

        .status-badge {
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
            text-transform: uppercase;
        }

        .status-valide {
            background: #c6f6d5;
            color: #22543d;
        }

        .status-invalide {
            background: #fed7d7;
            color: #742a2a;
        }

        .status-attente {
            background: #feebc8;
            color: #7c2d12;
        }

        .fiche-info {
            margin-bottom: 15px;
        }

        .info-label {
            font-size: 12px;
            color: #718096;
            font-weight: 600;
            text-transform: uppercase;
            margin-bottom: 5px;
        }

        .info-value {
            font-size: 15px;
            color: #2d3748;
            font-weight: 500;
        }

        .iban-container {
            background: #f7fafc;
            padding: 15px;
            border-radius: 10px;
            margin-top: 15px;
        }

        .iban-valid {
            background: #c6f6d5;
        }

        .iban-invalid {
            background: #fed7d7;
        }

        .bank-logo {
            width: 80px;
            height: auto;
            margin-top: 10px;
            border-radius: 5px;
        }

        .progress-bar {
            width: 100%;
            height: 8px;
            background: #e2e8f0;
            border-radius: 10px;
            overflow: hidden;
            margin-top: 15px;
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, #667eea 0%, #764ba2 100%);
            transition: width 0.3s;
        }

        .dossier-status {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-top: 15px;
            padding: 12px;
            background: #f7fafc;
            border-radius: 10px;
        }

        .status-icon {
            font-size: 24px;
        }

        .empty-state {
            text-align: center;
            padding: 60px 20px;
            color: #718096;
        }

        .empty-icon {
            font-size: 80px;
            margin-bottom: 20px;
            opacity: 0.5;
        }

        input[type="file"] {
            display: none;
        }

        .filter-buttons {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
        }

        .filter-btn {
            padding: 10px 20px;
            border: 2px solid #e2e8f0;
            background: white;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s;
            font-weight: 600;
        }

        .filter-btn.active {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border-color: transparent;
        }

        .action-buttons {
            display: flex;
            gap: 10px;
            margin-top: 15px;
        }

        .btn-small {
            padding: 8px 16px;
            font-size: 14px;
            border-radius: 8px;
        }

        .btn-success {
            background: #48bb78;
            color: white;
        }

        .btn-danger {
            background: #f56565;
            color: white;
        }

        .btn-info {
            background: #4299e1;
            color: white;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <div class="header-left">
                <img src="https://upload.wikimedia.org/wikipedia/commons/0/0e/Banque_de_France_2022_logo.svg" alt="Logo" class="logo">
                <div>
                    <div class="title">ANDREW GESTIONNAIRE</div>
                    <div class="subtitle">Système de gestion des dossiers clients</div>
                </div>
            </div>
            <div class="stats-container">
                <div class="stat-box">
                    <div class="stat-number" id="totalFiches">0</div>
                    <div class="stat-label">DOSSIERS</div>
                </div>
                <div class="stat-box">
                    <div class="stat-number" id="ibanValides">0</div>
                    <div class="stat-label">IBAN VALIDES</div>
                </div>
                <div class="stat-box">
                    <div class="stat-number" id="dossiersComplets">0</div>
                    <div class="stat-label">COMPLETS</div>
                </div>
            </div>
        </div>

        <div class="controls">
            <div class="upload-zone" id="uploadZone">
                <div class="upload-icon">📁</div>
                <h3>Glissez-déposez votre fichier CSV ici</h3>
                <p style="color: #718096; margin-top: 10px;">ou cliquez pour sélectionner un fichier</p>
                <input type="file" id="fileInput" accept=".txt,.csv">
            </div>

            <div class="filter-buttons">
                <button class="filter-btn active" onclick="filterFiches('all')">📊 Tous</button>
                <button class="filter-btn" onclick="filterFiches('valide')">✅ IBAN Valides</button>
                <button class="filter-btn" onclick="filterFiches('invalide')">❌ IBAN Invalides</button>
                <button class="filter-btn" onclick="filterFiches('complet')">🎯 Dossiers Complets</button>
                <button class="filter-btn" onclick="filterFiches('attente')">⏳ En Attente</button>
            </div>

            <div class="search-bar">
                <input type="text" class="search-input" id="searchInput" placeholder="🔍 Rechercher par nom, téléphone, ville...">
                <button class="btn btn-primary" onclick="searchFiches()">Rechercher</button>
            </div>
        </div>

        <div id="fichesContainer" class="fiches-grid"></div>
    </div>

    <script>
        let allFiches = [];
        let currentFilter = 'all';

        // Validation IBAN améliorée
        function validateIBAN(iban) {
            if (!iban || typeof iban !== 'string') return false;
            
            const cleanIban = iban.replace(/\s/g, '').toUpperCase();
            
            if (cleanIban.length < 15 || cleanIban.length > 34) return false;
            if (!/^[A-Z]{2}[0-9]{2}[A-Z0-9]+$/.test(cleanIban)) return false;
            
            const rearranged = cleanIban.slice(4) + cleanIban.slice(0, 4);
            let numericString = '';
            
            for (let char of rearranged) {
                if (char >= '0' && char <= '9') {
                    numericString += char;
                } else {
                    numericString += (char.charCodeAt(0) - 55).toString();
                }
            }
            
            // Calcul du modulo 97 par morceaux pour éviter les dépassements
            let remainder = 0;
            for (let i = 0; i < numericString.length; i++) {
                remainder = (remainder * 10 + parseInt(numericString[i])) % 97;
            }
            
            return remainder === 1;
        }

        // Déterminer l'état du dossier
        function getDossierStatus(fiche) {
            if (!fiche) return 'attente';
            
            const hasAllFields = fiche.nom && fiche.prenom && fiche.numero && 
                                fiche.date_naissance && fiche.adresse && fiche.email &&
                                fiche.code_postal && fiche.ville;
            const ibanValid = validateIBAN(fiche.iban);
            
            if (hasAllFields && ibanValid) return 'complet';
            if (!ibanValid && fiche.iban) return 'invalide';
            return 'attente';
        }

        // Obtenir le logo de la banque
        function getBankLogo(bic) {
            const banks = {
                'SOGEFRPP': 'https://upload.wikimedia.org/wikipedia/fr/thumb/2/24/Soci%C3%A9t%C3%A9_G%C3%A9n%C3%A9rale_2020.svg/200px-Soci%C3%A9t%C3%A9_G%C3%A9n%C3%A9rale_2020.svg.png',
                'BOUSFRPP': 'https://upload.wikimedia.org/wikipedia/commons/thumb/6/6d/Boursorama_Banque_logo.svg/200px-Boursorama_Banque_logo.svg.png',
                'CMCIFRPP': 'https://upload.wikimedia.org/wikipedia/fr/thumb/1/16/CIC_logo.svg/200px-CIC_logo.svg.png',
                'CCBPFRPP': 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSGuPRdibO03ifdufrx6KzwfiEXQpuC2l1jIw&s',
                'CMCIFR2A': 'https://upload.wikimedia.org/wikipedia/fr/thumb/1/16/CIC_logo.svg/200px-CIC_logo.svg.png',
                'CEPAFRPP': 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSGuPRdibO03ifdufrx6KzwfiEXQpuC2l1jIw&s',
                'CRLYFRPP': 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR8V_YLaIt50XR2k7BN0892YedNCwMlozbX_w&s',
                'AGRIFRPP': 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSeKEtmI44P9bIuYlRZQGLZNmjA-ZK2hTdOEQ&s'
            };
            
            const code = bic.substring(0, 8);
            return banks[code] || '';
        }

        // Créer une carte de fiche
        function createFicheCard(fiche) {
            if (!fiche) return '';
            
            const ibanValid = validateIBAN(fiche.iban);
            const status = getDossierStatus(fiche);
            const progress = calculateProgress(fiche);
            
            const statusInfo = {
                'complet': { label: '✅ Complet', class: 'status-valide', icon: '✅' },
                'invalide': { label: '❌ IBAN Invalide', class: 'status-invalide', icon: '❌' },
                'attente': { label: '⏳ En Attente', class: 'status-attente', icon: '⏳' }
            };
            
            const statusData = statusInfo[status];
            const bankLogo = getBankLogo(fiche.bic || '');
            
            return `
                <div class="fiche-card" data-status="${status}">
                    <div class="fiche-header">
                        <div class="fiche-name">${fiche.prenom || ''} ${fiche.nom || ''}</div>
                        <span class="status-badge ${statusData.class}">${statusData.label}</span>
                    </div>
                    
                    <div class="fiche-info">
                        <div class="info-label">📱 Téléphone</div>
                        <div class="info-value">${fiche.numero || 'Non renseigné'}</div>
                    </div>
                    
                    <div class="fiche-info">
                        <div class="info-label">🎂 Date de Naissance</div>
                        <div class="info-value">${fiche.date_naissance || 'Non renseignée'}</div>
                    </div>
                    
                    <div class="fiche-info">
                        <div class="info-label">📍 Adresse</div>
                        <div class="info-value">${fiche.adresse || 'Non renseignée'}<br>${fiche.code_postal || ''} ${fiche.ville || ''}</div>
                    </div>
                    
                    <div class="fiche-info">
                        <div class="info-label">📧 Email</div>
                        <div class="info-value">${fiche.email || 'Non renseigné'}</div>
                    </div>
                    
                    <div class="iban-container ${ibanValid ? 'iban-valid' : 'iban-invalid'}">
                        <div class="info-label">${ibanValid ? '✅' : '❌'} IBAN ${ibanValid ? 'VALIDE' : 'INVALIDE'}</div>
                        <div class="info-value" style="word-break: break-all;">${fiche.iban || 'Non renseigné'}</div>
                        <div class="info-label" style="margin-top: 10px">BIC: ${fiche.bic || 'Non renseigné'}</div>
                        ${bankLogo ? `<img src="${bankLogo}" class="bank-logo" alt="Logo Banque" onerror="this.style.display='none'">` : ''}
                    </div>
                    
                    <div class="dossier-status">
                        <div class="status-icon">${statusData.icon}</div>
                        <div>
                            <div style="font-weight: 600; color: #2d3748;">État du Dossier</div>
                            <div style="font-size: 14px; color: #718096;">${statusData.label}</div>
                        </div>
                    </div>
                    
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: ${progress}%"></div>
                    </div>
                    <div style="text-align: center; margin-top: 5px; font-size: 12px; color: #718096;">
                        Complétude: ${progress}%
                    </div>
                    
                    <div class="action-buttons">
                        <button class="btn btn-small btn-success" onclick="validateDossier('${fiche.numero}')">✅ Valider</button>
                        <button class="btn btn-small btn-info" onclick="editDossier('${fiche.numero}')">✏️ Modifier</button>
                        <button class="btn btn-small btn-danger" onclick="deleteDossier('${fiche.numero}')">🗑️ Supprimer</button>
                    </div>
                </div>
            `;
        }

        // Calculer le pourcentage de complétude
        function calculateProgress(fiche) {
            const fields = ['nom', 'prenom', 'numero', 'date_naissance', 'adresse', 'code_postal', 'ville', 'email', 'iban', 'bic'];
            let filled = 0;
            fields.forEach(field => {
                if (fiche[field] && fiche[field].trim() !== '') filled++;
            });
            
            const ibanValid = validateIBAN(fiche.iban);
            if (ibanValid) filled += 1;
            
            return Math.round((filled / (fields.length + 1)) * 100);
        }

        // Afficher les fiches
        function displayFiches(fiches) {
            const container = document.getElementById('fichesContainer');
            
            if (fiches.length === 0) {
                container.innerHTML = `
                    <div class="empty-state">
                        <div class="empty-icon">📭</div>
                        <h2>Aucun dossier trouvé</h2>
                        <p>Importez un fichier CSV pour commencer</p>
                    </div>
                `;
                return;
            }
            
            container.innerHTML = fiches.map(fiche => createFicheCard(fiche)).join('');
            updateStats();
        }

        // Mettre à jour les statistiques
        function updateStats() {
            document.getElementById('totalFiches').textContent = allFiches.length;
            
            const ibanValides = allFiches.filter(f => validateIBAN(f.iban)).length;
            document.getElementById('ibanValides').textContent = ibanValides;
            
            const complets = allFiches.filter(f => getDossierStatus(f) === 'complet').length;
            document.getElementById('dossiersComplets').textContent = complets;
        }

        // Filtrer les fiches
        function filterFiches(filter) {
            currentFilter = filter;
            
            // Réinitialiser la recherche
            document.getElementById('searchInput').value = '';
            
            document.querySelectorAll('.filter-btn').forEach(btn => {
                btn.classList.remove('active');
            });
            
            // Trouver le bon bouton à activer
            const buttons = document.querySelectorAll('.filter-btn');
            buttons.forEach(btn => {
                const btnText = btn.textContent.toLowerCase();
                if ((filter === 'all' && btnText.includes('tous')) ||
                    (filter === 'valide' && btnText.includes('valides')) ||
                    (filter === 'invalide' && btnText.includes('invalides')) ||
                    (filter === 'complet' && btnText.includes('complets')) ||
                    (filter === 'attente' && btnText.includes('attente'))) {
                    btn.classList.add('active');
                }
            });
            
            let filtered = allFiches;
            
            if (filter === 'valide') {
                filtered = allFiches.filter(f => validateIBAN(f.iban));
            } else if (filter === 'invalide') {
                filtered = allFiches.filter(f => !validateIBAN(f.iban));
            } else if (filter === 'complet') {
                filtered = allFiches.filter(f => getDossierStatus(f) === 'complet');
            } else if (filter === 'attente') {
                filtered = allFiches.filter(f => getDossierStatus(f) === 'attente');
            }
            
            displayFiches(filtered);
        }

        // Rechercher
        function searchFiches() {
            const query = document.getElementById('searchInput').value.toLowerCase().trim();
            
            // Réinitialiser le filtre à "Tous"
            currentFilter = 'all';
            document.querySelectorAll('.filter-btn').forEach(btn => {
                btn.classList.remove('active');
            });
            document.querySelectorAll('.filter-btn')[0].classList.add('active');
            
            if (!query) {
                displayFiches(allFiches);
                return;
            }
            
            const results = allFiches.filter(f => {
                return (f.nom && f.nom.toLowerCase().includes(query)) ||
                       (f.prenom && f.prenom.toLowerCase().includes(query)) ||
                       (f.numero && f.numero.includes(query)) ||
                       (f.ville && f.ville.toLowerCase().includes(query)) ||
                       (f.email && f.email.toLowerCase().includes(query)) ||
                       (f.adresse && f.adresse.toLowerCase().includes(query)) ||
                       (f.iban && f.iban.toLowerCase().includes(query));
            });
            
            displayFiches(results);
            
            // Message si aucun résultat
            if (results.length === 0 && query) {
                const container = document.getElementById('fichesContainer');
                container.innerHTML = `
                    <div class="empty-state">
                        <div class="empty-icon">🔍</div>
                        <h2>Aucun résultat trouvé</h2>
                        <p>Essayez avec un autre terme de recherche</p>
                        <button class="btn btn-primary" style="margin-top: 20px;" onclick="clearSearch()">Effacer la recherche</button>
                    </div>
                `;
            }
        }
        
        // Effacer la recherche
        function clearSearch() {
            document.getElementById('searchInput').value = '';
            currentFilter = 'all';
            document.querySelectorAll('.filter-btn').forEach(btn => {
                btn.classList.remove('active');
            });
            document.querySelectorAll('.filter-btn')[0].classList.add('active');
            displayFiches(allFiches);
        }

        // Actions
        function validateDossier(numero) {
            alert(`✅ Dossier validé pour le numéro: ${numero}`);
        }

        function editDossier(numero) {
            alert(`✏️ Modification du dossier: ${numero}`);
        }

        function deleteDossier(numero) {
            if (confirm(`Voulez-vous vraiment supprimer ce dossier?`)) {
                allFiches = allFiches.filter(f => f.numero !== numero);
                displayFiches(allFiches);
            }
        }

        // Gestion du fichier
        const uploadZone = document.getElementById('uploadZone');
        const fileInput = document.getElementById('fileInput');

        uploadZone.addEventListener('click', () => fileInput.click());

        uploadZone.addEventListener('dragover', (e) => {
            e.preventDefault();
            uploadZone.classList.add('dragover');
        });

        uploadZone.addEventListener('dragleave', () => {
            uploadZone.classList.remove('dragover');
        });

        uploadZone.addEventListener('drop', (e) => {
            e.preventDefault();
            uploadZone.classList.remove('dragover');
            const file = e.dataTransfer.files[0];
            if (file) processFile(file);
        });

        fileInput.addEventListener('change', (e) => {
            const file = e.target.files[0];
            if (file) processFile(file);
        });

        function processFile(file) {
            const reader = new FileReader();
            reader.onload = (e) => {
                const content = e.target.result;
                const lines = content.trim().split('\n');
                
                if (lines.length < 2) {
                    alert('❌ Le fichier est vide ou invalide');
                    return;
                }
                
                const headers = lines[0].split(',').map(h => h.trim());
                
                allFiches = [];
                
                for (let i = 1; i < lines.length; i++) {
                    const line = lines[i].trim();
                    if (line === '') continue;
                    
                    const values = [];
                    let currentValue = '';
                    let inQuotes = false;
                    
                    // Parser CSV avec gestion des virgules dans les guillemets
                    for (let char of line) {
                        if (char === '"') {
                            inQuotes = !inQuotes;
                        } else if (char === ',' && !inQuotes) {
                            values.push(currentValue.trim());
                            currentValue = '';
                        } else {
                            currentValue += char;
                        }
                    }
                    values.push(currentValue.trim());
                    
                    const fiche = {};
                    headers.forEach((header, index) => {
                        fiche[header] = values[index] ? values[index].replace(/^"|"$/g, '') : '';
                    });
                    
                    allFiches.push(fiche);
                }
                
                if (allFiches.length === 0) {
                    alert('❌ Aucune donnée trouvée dans le fichier');
                    return;
                }
                
                displayFiches(allFiches);
                alert(`✅ ${allFiches.length} dossier(s) importé(s) avec succès !`);
            };
            
            reader.onerror = () => {
                alert('❌ Erreur lors de la lecture du fichier');
            };
            
            reader.readAsText(file, 'UTF-8');
        }

        // Recherche en temps réel avec debounce
        let searchTimeout;
        document.getElementById('searchInput').addEventListener('input', function() {
            clearTimeout(searchTimeout);
            searchTimeout = setTimeout(() => {
                searchFiches();
            }, 300); // Attendre 300ms après la dernière frappe
        });

        // Afficher l'état vide au démarrage
        displayFiches([]);
    </script>
</body>
</html>
