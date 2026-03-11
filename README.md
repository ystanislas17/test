<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Infographie Profil - Yann STANISLAS</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        body { font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif; background-color: #f8fafc; color: #0f172a; }
        .chart-container { position: relative; width: 100%; max-width: 600px; margin-left: auto; margin-right: auto; height: 350px; max-height: 400px; }
        .glass-card { background: rgba(255, 255, 255, 0.95); backdrop-filter: blur(10px); box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1), 0 8px 10px -6px rgba(0, 0, 0, 0.1); border-radius: 1rem; border: 1px solid #e2e8f0; }
        @media (min-width: 768px) { .chart-container { height: 400px; } }
    </style>
</head>
<body class="antialiased">
    <!-- PALETTE: Vibrant Corporate (Deep Blue #1E3A8A, Teal #0D9488, Amber #F59E0B). CONFIRMATION: NEITHER Mermaid JS NOR SVG were used anywhere in the output. PLAN: Intro -> Big Numbers -> Radar (Skills) -> Doughnut (Bierville Scope) -> Bar (Experience Timeline). VISUALIZATIONS: Big Numbers (Inform) -> HTML; Radar (Compare) -> Chart.js; Doughnut (Composition) -> Chart.js; Bar (Compare) -> Chart.js. -->

    <nav class="sticky top-0 z-50 bg-white/90 backdrop-blur-md border-b border-gray-200 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16 items-center">
                <div class="flex-shrink-0 flex items-center font-bold text-xl text-blue-900">
                    YS
                </div>
                <div class="hidden md:flex space-x-8">
                    <a href="#vision" class="text-gray-700 hover:text-teal-600 font-medium">Vision ESS</a>
                    <a href="#expertise" class="text-gray-700 hover:text-teal-600 font-medium">Expertise</a>
                    <a href="#parcours" class="text-gray-700 hover:text-teal-600 font-medium">Parcours</a>
                </div>
            </div>
        </div>
    </nav>

    <header class="bg-gradient-to-r from-blue-900 to-teal-800 text-white py-20 px-4">
        <div class="max-w-4xl mx-auto text-center">
            <h1 class="text-4xl md:text-5xl font-extrabold mb-6 tracking-tight">Yann STANISLAS</h1>
            <h2 class="text-2xl md:text-3xl font-light text-teal-100 mb-8">Directeur de Structure – Expert en Gestion & Engagement Durable</h2>
            <p class="text-lg md:text-xl text-blue-100 max-w-2xl mx-auto">
                Allier la rigueur d'un gestionnaire financier et l'empathie d'un leader tourné vers l'humain pour pérenniser vos projets au sein de l'Économie Sociale et Solidaire.
            </p>
            <div class="mt-8 flex justify-center space-x-4">
                <span class="bg-white text-blue-900 px-4 py-2 rounded-full font-semibold shadow-lg">☎ 07.69.09.55.05</span>
                <span class="bg-white text-blue-900 px-4 py-2 rounded-full font-semibold shadow-lg">✉ y.stanislas17@gmail.com</span>
            </div>
        </div>
    </header>

    <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
        
        <section id="vision" class="mb-16">
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <div class="glass-card p-8 text-center transform transition duration-500 hover:scale-105">
                    <div class="text-5xl mb-4 text-teal-600">📈</div>
                    <h3 class="text-4xl font-extrabold text-blue-900 mb-2">7 Ans</h3>
                    <p class="text-gray-600 font-medium uppercase tracking-wide text-sm">Contrôle des flux & Audit</p>
                    <p class="text-gray-500 text-sm mt-2">Garantie de transparence et de redevabilité.</p>
                </div>
                <div class="glass-card p-8 text-center transform transition duration-500 hover:scale-105 border-t-4 border-teal-500">
                    <div class="text-5xl mb-4 text-amber-500">🏢</div>
                    <h3 class="text-4xl font-extrabold text-blue-900 mb-2">+3 Ans</h3>
                    <p class="text-gray-600 font-medium uppercase tracking-wide text-sm">Direction de Site (Bierville)</p>
                    <p class="text-gray-500 text-sm mt-2">Pilotage global d'un domaine d'envergure.</p>
                </div>
                <div class="glass-card p-8 text-center transform transition duration-500 hover:scale-105">
                    <div class="text-5xl mb-4 text-rose-500">🎓</div>
                    <h3 class="text-4xl font-extrabold text-blue-900 mb-2">1 Titre</h3>
                    <p class="text-gray-600 font-medium uppercase tracking-wide text-sm">Titre Pro RPMS en cours</p>
                    <p class="text-gray-500 text-sm mt-2">Certification des acquis en gestion de structure.</p>
                </div>
            </div>
        </section>

        <section id="expertise" class="mb-16">
            <div class="text-center mb-10">
                <h2 class="text-3xl font-bold text-blue-900">Piliers de Compétences</h2>
                <div class="h-1 w-20 bg-teal-500 mx-auto mt-4 rounded-full"></div>
                <p class="mt-4 text-gray-600 max-w-2xl mx-auto">Une synergie entre le pilotage financier, la gestion opérationnelle et l'animation des relations humaines, indispensables au secteur de l'ESS.</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
                <div class="glass-card p-6">
                    <div class="chart-container">
                        <canvas id="skillsRadarChart"></canvas>
                    </div>
                </div>
                <div class="space-y-6">
                    <div class="flex items-start">
                        <div class="flex-shrink-0 bg-blue-100 p-3 rounded-lg text-blue-800 text-xl font-bold">1</div>
                        <div class="ml-4">
                            <h4 class="text-xl font-bold text-gray-900">Pilotage Stratégique & Budgétaire</h4>
                            <p class="text-gray-600 mt-1">Équilibre des comptes d'exploitation et garantie du développement durable de la structure.</p>
                        </div>
                    </div>
                    <div class="flex items-start">
                        <div class="flex-shrink-0 bg-teal-100 p-3 rounded-lg text-teal-800 text-xl font-bold">2</div>
                        <div class="ml-4">
                            <h4 class="text-xl font-bold text-gray-900">Audit & Transparence</h4>
                            <p class="text-gray-600 mt-1">Contrôle rigoureux des flux financiers répondant aux obligations de redevabilité sociales.</p>
                        </div>
                    </div>
                    <div class="flex items-start">
                        <div class="flex-shrink-0 bg-amber-100 p-3 rounded-lg text-amber-800 text-xl font-bold">3</div>
                        <div class="ml-4">
                            <h4 class="text-xl font-bold text-gray-900">Dialogue & Gouvernance</h4>
                            <p class="text-gray-600 mt-1">Coordination des parties prenantes et pratique confirmée du dialogue social pour fédérer les équipes.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="parcours" class="mb-16">
            <div class="glass-card p-8 bg-blue-50">
                <div class="text-center mb-10">
                    <h2 class="text-3xl font-bold text-blue-900">Analyse de l'Expérience Opérationnelle</h2>
                    <div class="h-1 w-20 bg-teal-500 mx-auto mt-4 rounded-full"></div>
                    <p class="mt-4 text-gray-700 max-w-2xl mx-auto">Répartition des responsabilités et de l'envergure temporelle des missions structurantes de mon parcours professionnel.</p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                    <div class="bg-white rounded-xl shadow-sm p-6 border border-gray-100">
                        <h3 class="text-lg font-bold text-center text-gray-800 mb-4">Périmètre d'Action : Domaine de Bierville</h3>
                        <p class="text-sm text-gray-500 text-center mb-6">Gestion globale d'un site d'envergure nécessitant une polyvalence opérationnelle.</p>
                        <div class="chart-container">
                            <canvas id="biervilleDoughnutChart"></canvas>
                        </div>
                    </div>
                    
                    <div class="bg-white rounded-xl shadow-sm p-6 border border-gray-100">
                        <h3 class="text-lg font-bold text-center text-gray-800 mb-4">Répartition Temporelle (Années d'Expertise)</h3>
                        <p class="text-sm text-gray-500 text-center mb-6">Une base solide en finance complétée par une solide expérience en direction de structure.</p>
                        <div class="chart-container">
                            <canvas id="experienceBarChart"></canvas>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="mb-16">
            <div class="bg-gradient-to-br from-teal-800 to-blue-900 rounded-2xl shadow-xl overflow-hidden">
                <div class="p-10 md:p-16 text-center text-white">
                    <h2 class="text-3xl font-bold mb-6">Prêt à accompagner votre croissance</h2>
                    <p class="text-lg text-teal-100 max-w-3xl mx-auto mb-8">
                        "Intègre, dynamique et pragmatique, j’ai à cœur de porter vos projets avec la rigueur d'un gestionnaire et l'empathie d'un leader tourné vers l'humain."
                    </p>
                    <div class="inline-flex items-center justify-center p-4 bg-white/10 rounded-lg border border-white/20 backdrop-blur-sm">
                        <span class="text-3xl mr-4">🤝</span>
                        <div class="text-left">
                            <p class="font-bold text-xl">Rencontrons-nous</p>
                            <p class="text-teal-200 text-sm">Pour discuter de vive voix de votre rayonnement.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

    </main>

    <footer class="bg-gray-900 text-gray-400 py-8 text-center text-sm">
        <p>© 2026 Yann STANISLAS - Candidature Directeur de Structure ESS</p>
    </footer>

    <script>
        const chartTooltipConfig = {
            tooltip: {
                callbacks: {
                    title: function(tooltipItems) {
                        const item = tooltipItems[0];
                        let label = item.chart.data.labels[item.dataIndex];
                        if (Array.isArray(label)) {
                            return label.join(' ');
                        } else {
                            return label;
                        }
                    }
                }
            }
        };

        const ctxRadar = document.getElementById('skillsRadarChart').getContext('2d');
        new Chart(ctxRadar, {
            type: 'radar',
            data: {
                labels: [
                    ['Pilotage', 'Stratégique'], 
                    ['Audit &', 'Transparence'], 
                    ['Dialogue', 'Social'], 
                    ['Gestion', 'Immobilière'], 
                    ['Management', 'd\'Équipes']
                ],
                datasets: [{
                    label: 'Niveau d\'Expertise',
                    data: [95, 90, 85, 85, 95], // Augmentation de la valeur pour la gestion immobilière
                    backgroundColor: 'rgba(13, 148, 136, 0.25)',
                    borderColor: 'rgba(13, 148, 136, 1)',
                    pointBackgroundColor: 'rgba(30, 58, 138, 1)',
                    pointBorderColor: '#fff',
                    pointHoverBackgroundColor: '#fff',
                    pointHoverBorderColor: 'rgba(30, 58, 138, 1)',
                    borderWidth: 3
                }]
            },
            options: {
                maintainAspectRatio: false,
                scales: {
                    r: {
                        angleLines: { color: 'rgba(15, 23, 42, 0.2)' }, // Lignes de grille plus visibles
                        grid: { color: 'rgba(15, 23, 42, 0.15)' },
                        pointLabels: {
                            font: { size: 12, family: "'Segoe UI', sans-serif", weight: 'bold' },
                            color: '#1e3a8a'
                        },
                        ticks: { display: false, min: 0, max: 100 }
                    }
                },
                plugins: chartTooltipConfig
            }
        });

        const ctxDoughnut = document.getElementById('biervilleDoughnutChart').getContext('2d');
        new Chart(ctxDoughnut, {
            type: 'doughnut',
            data: {
                labels: [
                    'Hébergement', 
                    'Restauration', 
                    'Séminaires', 
                    ['Entretien du', 'Patrimoine']
                ],
                datasets: [{
                    data: [35, 30, 20, 15],
                    backgroundColor: [
                        '#1e3a8a',
                        '#0d9488',
                        '#f59e0b',
                        '#e11d48'
                    ],
                    borderWidth: 0,
                    hoverOffset: 4
                }]
            },
            options: {
                maintainAspectRatio: false,
                cutout: '65%',
                plugins: {
                    ...chartTooltipConfig,
                    legend: {
                        position: 'bottom',
                        labels: { padding: 20, font: { family: "'Segoe UI', sans-serif" } }
                    }
                }
            }
        });

        const ctxBar = document.getElementById('experienceBarChart').getContext('2d');
        new Chart(ctxBar, {
            type: 'bar',
            data: {
                labels: [
                    ['Contrôle des', 'flux financiers'], 
                    ['Direction de', 'Site (Bierville)']
                ],
                datasets: [{
                    label: 'Années d\'expérience',
                    data: [7, 3.5],
                    backgroundColor: [
                        'rgba(30, 58, 138, 0.8)',
                        'rgba(13, 148, 136, 0.8)'
                    ],
                    borderRadius: 6
                }]
            },
            options: {
                maintainAspectRatio: false,
                indexAxis: 'y',
                scales: {
                    x: {
                        beginAtZero: true,
                        grid: { color: 'rgba(0, 0, 0, 0.05)' },
                        title: { display: true, text: 'Années' }
                    },
                    y: {
                        grid: { display: false },
                        ticks: { font: { weight: 'bold' } }
                    }
                },
                plugins: {
                    ...chartTooltipConfig,
                    legend: { display: false }
                }
            }
        });
    </script>
</body>
</html># test
