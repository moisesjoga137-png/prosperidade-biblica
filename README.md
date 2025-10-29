(https://github.com/user-attachments/files/23200681/prosperidade-biblica-pro.html)

<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="theme-color" content="#1e3a8a">
    <title>Prosperidade Bíblica Pro</title>
    
    <!-- Fontes Premium -->
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    
    <!-- Ícones (Lucide) -->
    <script src="https://unpkg.com/lucide@latest/dist/umd/lucide.js"></script>
    
    <!-- Chart.js -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    
    <!-- Animate.css -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"/>
    
    <!-- Manifest PWA -->
    <link rel="manifest" href="data:application/manifest+json,{
        'name': 'Prosperidade Bíblica Pro',
        'short_name': 'Prosperidade',
        'start_url': '.',
        'display': 'standalone',
        'background_color': '#f5f7fa',
        'theme_color': '#1e3a8a',
        'icons': [{'src': 'data:image/svg+xml,%3Csvg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22%3E%3Ctext y=%22.9em%22 font-size=%2290%%22%3E%EF%B8%8F%3C/text%3E%3C/svg%3E', 'sizes': '192x192', 'type': 'image/svg+xml'}]
    }">
    
    <style>
        :root {
            --primary: #1e3a8a;
            --primary-light: #3b82f6;
            --success: #10b981;
            --warning: #f59e0b;
            --danger: #ef4444;
            --light: #f8f9fa;
            --dark: #1f2937;
            --gray: #6b7280;
            --border: #e5e7eb;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, #f0f4ff 0%, #e0eaff 100%);
            color: var(--dark);
            line-height: 1.6;
            min-height: 100vh;
            padding: env(safe-area-inset-top) env(safe-area-inset-right) env(safe-area-inset-bottom) env(safe-area-inset-left);
        }
        
        .container {
            max-width: 100%;
            margin: 0 auto;
            background: white;
            border-radius: 0;
            box-shadow: 0 -5px 30px rgba(0,0,0,0.05);
            overflow: hidden;
            height: 100vh;
            display: flex;
            flex-direction: column;
        }
        
        /* Header */
        header {
            background: linear-gradient(135deg, var(--primary), var(--primary-light));
            color: white;
            text-align: center;
            padding: 20px 15px;
            position: relative;
            overflow: hidden;
        }
        header::before {
            content: '';
            position: absolute;
            top: 0; left: 0; right: 0; bottom: 0;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" opacity="0.05"><path fill="white" d="M50 10 L61.8 35.5 H88.2 L67.3 51.5 L79.1 77 L58.2 61 L37.3 77 L49.1 51.5 L28.2 35.5 H54.6 Z"/></svg>') center/cover;
            animation: float 20s infinite;
        }
        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-10px) rotate(5deg); }
        }
        header h1 {
            font-family: 'Playfair Display', serif;
            font-size: 1.9rem;
            margin-bottom: 5px;
            position: relative;
            z-index: 1;
        }
        header p {
            font-size: 0.95rem;
            opacity: 0.9;
            position: relative;
            z-index: 1;
        }
        
        /* Navegação */
        nav {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            background: white;
            border-top: 1px solid var(--border);
            display: flex;
            justify-content: space-around;
            padding: 8px 0;
            z-index: 1000;
            box-shadow: 0 -2px 10px rgba(0,0,0,0.05);
        }
        nav button {
            background: none;
            border: none;
            padding: 10px;
            font-size: 0.8rem;
            color: var(--gray);
            cursor: pointer;
            border-radius: 12px;
            transition: all 0.3s;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 4px;
            min-width: 60px;
        }
        nav button i {
            font-size: 1.4rem;
        }
        nav button.active {
            color: var(--primary);
            background: rgba(59, 130, 246, 0.1);
        }
        nav button span {
            font-weight: 600;
        }
        
        /* Main */
        main {
            flex: 1;
            overflow-y: auto;
            padding: 20px;
            padding-bottom: 80px;
        }
        .page {
            display: none;
            animation: fadeIn 0.5s ease-in-out;
        }
        .page.active {
            display: block;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* Cards */
        .card {
            background: white;
            border-radius: 16px;
            padding: 18px;
            margin: 15px 0;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            border: 1px solid var(--border);
            transition: transform 0.2s, box-shadow 0.2s;
        }
        .card:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
        }
        .card h3 {
            color: var(--primary);
            margin-bottom: 12px;
            font-size: 1.1rem;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        .card h3 i {
            color: var(--primary-light);
        }
        
        /* Forms */
        .form-group {
            margin-bottom: 16px;
        }
        label {
            display: block;
            margin-bottom: 6px;
            font-weight: 600;
            color: var(--dark);
            font-size: 0.9rem;
        }
        input, textarea, select {
            width: 100%;
            padding: 12px 14px;
            border: 1.5px solid var(--border);
            border-radius: 12px;
            font-size: 1rem;
            transition: all 0.3s;
            background: #fafafa;
        }
        input:focus, textarea:focus, select:focus {
            outline: none;
            border-color: var(--primary-light);
            background: white;
            box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.15);
        }
        .btn {
            background: var(--primary);
            color: white;
            border: none;
            padding: 14px;
            border-radius: 12px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            width: 100%;
            margin-top: 10px;
        }
        .btn:hover {
            background: var(--primary-light);
            transform: translateY(-1px);
        }
        .btn-success { background: var(--success); }
        .btn-success:hover { background: #059669; }
        .btn-danger { background: var(--danger); }
        .btn-danger:hover { background: #dc2626; }
        
        /* Transações */
        .transaction {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px;
            background: var(--light);
            border-radius: 12px;
            margin: 8px 0;
            font-size: 0.95rem;
            position: relative;
            overflow: hidden;
        }
        .transaction::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            bottom: 0;
            width: 5px;
            background: var(--success);
        }
        .transaction.saida::before {
            background: var(--danger);
        }
        .transaction .info {
            flex: 1;
        }
        .transaction .value {
            font-weight: 700;
            font-size: 1.1rem;
        }
        .transaction.entrada .value { color: var(--success); }
        .transaction.saida .value { color: var(--danger); }
        
        /* Gráfico */
        .chart-container {
            position: relative;
            height: 220px;
            margin: 20px 0;
        }
        
        /* Princípios */
        .principio {
            background: linear-gradient(135deg, #f8faff 0%, #f0f4ff 100%);
            border-radius: 16px;
            padding: 16px;
            margin: 15px 0;
            border-left: 5px solid var(--primary-light);
            position: relative;
        }
        .principio.completed {
            opacity: 0.7;
            border-left-color: var(--success);
        }
        .principio .action-btn {
            position: absolute;
            top: 12px;
            right: 12px;
            background: rgba(59, 130, 246, 0.1);
            color: var(--primary);
            border: none;
            width: 36px;
            height: 36px;
            border-radius: 50%;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .principio.completed .action-btn {
            background: var(--success);
            color: white;
        }
        
        /* Notas */
        .note {
            background: #fff9db;
            border-radius: 12px;
            padding: 14px;
            margin: 10px 0;
            position: relative;
            border: 1px solid #fde68a;
        }
        .note .date {
            font-size: 0.8rem;
            color: var(--gray);
            margin-bottom: 6px;
        }
        .note .tags {
            margin-top: 8px;
            display: flex;
            gap: 6px;
            flex-wrap: wrap;
        }
        .tag {
            background: var(--primary);
            color: white;
            font-size: 0.7rem;
            padding: 4px 8px;
            border-radius: 8px;
        }
        
        /* Dashboard */
        .dashboard {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 12px;
            margin: 15px 0;
        }
        .stat-card {
            background: linear-gradient(135deg, #dbeafe 0%, #bfdbfe 100%);
            padding: 16px;
            border-radius: 16px;
            text-align: center;
            font-weight: 600;
        }
        .stat-card.success { background: linear-gradient(135deg, #d1fae5 0%, #a7f3d0 100%); }
        .stat-card.warning { background: linear-gradient(135deg, #fef3c7 0%, #fde68a 100%); }
        .stat-card .value {
            font-size: 1.4rem;
            margin: 8px 0;
            color: var(--primary);
        }
        .stat-card .label {
            font-size: 0.8rem;
            color: var(--gray);
        }
        
        /* Barra de Progresso */
        .progress-container {
            margin-top: 15px;
            text-align: center;
        }
        .progress-bar {
            background: #e5e7eb;
            border-radius: 12px;
            height: 12px;
            overflow: hidden;
            margin-bottom: 8px;
        }
        .progress-fill {
            background: var(--success);
            height: 100%;
            width: 0%;
            transition: width 0.6s ease;
        }
        .progress-text {
            font-size: 0.85rem;
            color: var(--gray);
        }
        
        /* Toast */
        .toast {
            position: fixed;
            bottom: 80px;
            left: 50%;
            transform: translateX(-50%);
            background: var(--dark);
            color: white;
            padding: 12px 20px;
            border-radius: 12px;
            font-size: 0.9rem;
            z-index: 3000;
            opacity: 0;
            transition: all 0.4s;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        .toast.show {
            opacity: 1;
            bottom: 100px;
        }
        
        @media (min-width: 480px) {
            main { padding: 25px; }
            .card { padding: 22px; }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <header>
            <h1>Prosperidade Bíblica Pro</h1>
            <p>Mente Milionária + Sabedoria da Palavra</p>
        </header>

        <!-- Navegação -->
        <nav>
            <button onclick="showPage('dashboard')" class="active">
                <i data-lucide="home"></i>
                <span>Início</span>
            </button>
            <button onclick="showPage('orcamento')">
                <i data-lucide="dollar-sign"></i>
                <span>Orçamento</span>
            </button>
            <button onclick="showPage('principios')">
                <i data-lucide="book-open"></i>
                <span>Princípios</span>
            </button>
            <button onclick="showPage('anotacoes')">
                <i data-lucide="edit-3"></i>
                <span>Anotações</span>
            </button>
        </nav>

        <!-- Conteúdo -->
        <main>
            <!-- Dashboard -->
            <div id="dashboard" class="page active">
                <div class="card animate__animated animate__fadeIn">
                    <h3><i data-lucide="trending-up"></i> Resumo Financeiro</h3>
                    <div class="dashboard">
                        <div class="stat-card">
                            <div class="value" id="saldoAtual">R$ 0,00</div>
                            <div class="label">Saldo Atual</div>
                        </div>
                        <div class="stat-card success">
                            <div class="value" id="totalEntradas">R$ 0,00</div>
                            <div class="label">Entradas</div>
                        </div>
                        <div class="stat-card warning">
                            <div class="value" id="totalSaidas">R$ 0,00</div>
                            <div class="label">Saídas</div>
                        </div>
                        <div class="stat-card">
                            <div class="value" id="progressoMeta">0%</div>
                            <div class="label">Meta Mensal</div>
                        </div>
                    </div>
                </div>

                <div class="card">
                    <h3><i data-lucide="target"></i> Meta do Mês</h3>
                    <div class="form-group">
                        <label>Meta de Poupança</label>
                        <input type="number" id="metaPoupanca" placeholder="Ex: 1000" step="0.01">
                    </div>
                    <button type="button" class="btn btn-success" onclick="salvarMeta()">Salvar Meta</button>
                    
                    <!-- Barra de Progresso -->
                    <div class="progress-container">
                        <div class="progress-bar">
                            <div id="progressFill" class="progress-fill"></div>
                        </div>
                        <div id="progressText" class="progress-text">0% da meta</div>
                    </div>
                </div>

                <div class="card">
                    <canvas id="graficoMensal" class="chart-container"></canvas>
                </div>
            </div>

            <!-- Orçamento -->
            <div id="orcamento" class="page">
                <div class="card">
                    <h3><i data-lucide="plus-circle"></i> Nova Transação</h3>
                    <form id="formTransacao">
                        <div class="form-group">
                            <label>Tipo</label>
                            <select id="tipoTransacao">
                                <option value="entrada">Entrada (+)</option>
                                <option value="saida">Saída (-)</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label>Valor</label>
                            <input type="number" id="valorTransacao" placeholder="0,00" step="0.01" required>
                        </div>
                        <div class="form-group">
                            <label>Descrição</label>
                            <input type="text" id="descTransacao" placeholder="Ex: Salário, Supermercado" required>
                        </div>
                        <div class="form-group">
                            <label>Data</label>
                            <input type="date" id="dataTransacao" required>
                        </div>
                        <button type="submit" class="btn">Adicionar</button>
                    </form>
                </div>

                <div id="listaTransacoes"></div>
            </div>

            <!-- Princípios -->
            <div id="principios" class="page">
                <div class="card">
                    <h3><i data-lucide="lightbulb"></i> 17 Princípios da Riqueza</h3>
                    <p style="font-size:0.9rem; color:var(--gray);">Marque como concluído ao aplicar na prática.</p>
                </div>
                <div id="listaPrincipios"></div>
            </div>

            <!-- Anotações -->
            <div id="anotacoes" class="page">
                <div class="card">
                    <h3><i data-lucide="feather"></i> Nova Reflexão</h3>
                    <form id="formNota">
                        <div class="form-group">
                            <textarea id="textoNota" placeholder="O que Deus falou? Qual insight milionário?" rows="4" required></textarea>
                        </div>
                        <div class="form-group">
                            <label>Tags (opcional)</label>
                            <input type="text" id="tagsNota" placeholder="Ex: gratidão, dízimo, investimento">
                        </div>
                        <button type="submit" class="btn">Salvar Reflexão</button>
                    </form>
                </div>
                <div id="listaNotas"></div>
            </div>
        </main>
    </div>

    <!-- Toast -->
    <div class="toast" id="toast"></div>

    <script>
        // Inicialização
        lucide.createIcons();
        
        // Dados
        let transacoes = JSON.parse(localStorage.getItem('transacoes')) || [];
        let metaPoupanca = parseFloat(localStorage.getItem('metaPoupanca')) || 0;
        let principiosConcluidos = JSON.parse(localStorage.getItem('principiosConcluidos')) || [];
        let notas = JSON.parse(localStorage.getItem('notas')) || [];
        let grafico = null;

        // Navegação
        function showPage(pageId) {
            document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
            document.getElementById(pageId).classList.add('active');
            document.querySelectorAll('nav button').forEach(b => b.classList.remove('active'));
            event.target.closest('button').classList.add('active');
            
            if (pageId === 'dashboard') atualizarDashboard();
            if (pageId === 'orcamento') carregarTransacoes();
            if (pageId === 'principios') carregarPrincipios();
            if (pageId === 'anotacoes') carregarNotas();
        }

        // Toast
        function showToast(msg, type = 'success') {
            const toast = document.getElementById('toast');
            toast.textContent = msg;
            toast.className = 'toast show';
            toast.style.background = type === 'success' ? '#10b981' : '#ef4444';
            setTimeout(() => toast.className = 'toast', 3000);
        }

        // Dashboard
        function atualizarDashboard() {
            const entradas = transacoes.filter(t => t.tipo === 'entrada').reduce((s, t) => s + t.valor, 0);
            const saidas = transacoes.filter(t => t.tipo === 'saida').reduce((s, t) => s + t.valor, 0);
            const saldo = entradas - saidas;
            
            document.getElementById('saldoAtual').textContent = `R$ ${saldo.toFixed(2)}`;
            document.getElementById('totalEntradas').textContent = `R$ ${entradas.toFixed(2)}`;
            document.getElementById('totalSaidas').textContent = `R$ ${saidas.toFixed(2)}`;
            
            const progresso = metaPoupanca > 0 ? Math.min(100, (saldo / metaPoupanca * 100)) : 0;
            document.getElementById('progressoMeta').textContent = `${progresso.toFixed(0)}%`;
            document.getElementById('progressFill').style.width = `${progresso}%`;
            document.getElementById('progressText').textContent = `${progresso.toFixed(0)}% da meta`;
            
            document.getElementById('metaPoupanca').value = metaPoupanca || '';

            atualizarGrafico(entradas, saidas);
        }

        function salvarMeta() {
            const valor = parseFloat(document.getElementById('metaPoupanca').value);
            if (isNaN(valor) || valor < 0) {
                showToast('Digite uma meta válida!', 'error');
                return;
            }
            metaPoupanca = valor;
            localStorage.setItem('metaPoupanca', metaPoupanca);
            showToast('Meta salva com sucesso!');
            atualizarDashboard();
        }

        function atualizarGrafico(entradas, saidas) {
            const ctx = document.getElementById('graficoMensal').getContext('2d');
            if (grafico) grafico.destroy();
            
            grafico = new Chart(ctx, {
                type: 'doughnut',
                data: {
                    labels: ['Entradas', 'Saídas', 'Disponível'],
                    datasets: [{
                        data: [entradas, saidas, Math.max(0, entradas - saidas)],
                        backgroundColor: ['#10b981', '#ef4444', '#3b82f6'],
                        borderWidth: 0,
                        borderRadius: 8
                    }]
                },
                options: {
                    responsive: true,
                    plugins: {
                        legend: { position: 'bottom', labels: { padding: 20, font: { size: 12 } } }
                    },
                    cutout: '70%'
                }
            });
        }

        // Transações
        document.getElementById('formTransacao').addEventListener('submit', (e) => {
            e.preventDefault();
            const valor = parseFloat(document.getElementById('valorTransacao').value);
            if (isNaN(valor) || valor <= 0) {
                showToast('Digite um valor válido!', 'error');
                return;
            }
            const transacao = {
                tipo: document.getElementById('tipoTransacao').value,
                valor: valor,
                descricao: document.getElementById('descTransacao').value.trim(),
                data: document.getElementById('dataTransacao').value,
                id: Date.now()
            };
            if (!transacao.descricao) {
                showToast('Descrição é obrigatória!', 'error');
                return;
            }
            transacoes.push(transacao);
            localStorage.setItem('transacoes', JSON.stringify(transacoes));
            e.target.reset();
            document.getElementById('dataTransacao').valueAsDate = new Date();
            showToast('Transação adicionada!');
            if (document.getElementById('orcamento').classList.contains('active')) carregarTransacoes();
            atualizarDashboard();
        });

        function carregarTransacoes() {
            const lista = document.getElementById('listaTransacoes');
            lista.innerHTML = transacoes.sort((a,b) => new Date(b.data) - new Date(a.data)).map((t, i) => `
                <div class="transaction ${t.tipo}">
                    <div class="info">
                        <div><strong>${t.descricao}</strong></div>
                        <div style="font-size:0.8rem; color:var(--gray);">${new Date(t.data).toLocaleDateString('pt-BR')}</div>
                    </div>
                    <div class="value">${t.tipo === 'entrada' ? '+' : '-'} R$ ${t.valor.toFixed(2)}</div>
                    <button class="btn-danger" style="margin-left:8px; padding:6px 10px; font-size:0.8rem;" onclick="excluirTransacao(${i})">Excluir</button>
                </div>
            `).join('') || '<p style="text-align:center; color:var(--gray);">Nenhuma transação ainda.</p>';
        }

        function excluirTransacao(i) {
            if (confirm('Tem certeza que deseja excluir?')) {
                transacoes.splice(i, 1);
                localStorage.setItem('transacoes', JSON.stringify(transacoes));
                carregarTransacoes();
                atualizarDashboard();
                showToast('Transação excluída.');
            }
        }

        // Princípios
        const principios = [
            {id:1, titulo:"Eu crio minha vida", biblia:"Provérbios 23:7", acao:"Declare: 'Eu crio abundância com Deus'"},
            {id:2, titulo:"Jogo para ganhar", biblia:"Mateus 25:14-30", acao:"Invista com ousadia"},
            {id:3, titulo:"Admiro os ricos", biblia:"Provérbios 14:30", acao:"Celebre sucessos alheios"},
            {id:4, titulo:"Associo com positivos", biblia:"Provérbios 13:20", acao:"Busque mentores de fé"},
            {id:5, titulo:"Foco em oportunidades", biblia:"Filipenses 4:13", acao:"Veja portas abertas"},
            {id:6, titulo:"Como posso servir?", biblia:"Mateus 20:28", acao:"Dê valor primeiro"},
            {id:7, titulo:"Ricos fazem o bem", biblia:"1 Timóteo 6:17-19", acao:"Use riqueza para Deus"},
            {id:8, titulo:"Gerencio bem", biblia:"Lucas 16:11", acao:"Orçamento diário"},
            {id:9, titulo:"Net worth", biblia:"Provérbios 21:5", acao:"Multiplique ativos"},
            {id:10, titulo:"Auto-empregado", biblia:"Gênesis 2:15", acao:"Crie renda extra"},
            {id:11, titulo:"Visão de 5 anos", biblia:"Habacuque 2:3", acao:"Planeje longo prazo"},
            {id:12, titulo:"Mente aberta", biblia:"Provérbios 18:15", acao:"Estude com oração"},
            {id:13, titulo:"Confortável com ideias", biblia:"Tiago 1:5", acao:"Teste com fé"},
            {id:14, titulo:"Sonhos enormes", biblia:"Efésios 3:20", acao:"Sonhe com Deus"},
            {id:15, titulo:"Classe mundial", biblia:"Colossenses 3:23", acao:"Excelência total"},
            {id:16, titulo:"Autoeducação", biblia:"Provérbios 4:7", acao:"Leia Bíblia + livros"},
            {id:17, titulo:"Ação imediata", biblia:"Tiago 2:17", acao:"Aja hoje!"}
        ];

        function carregarPrincipios() {
            const lista = document.getElementById('listaPrincipios');
            lista.innerHTML = principios.map(p => `
                <div class="principio ${principiosConcluidos.includes(p.id) ? 'completed' : ''}">
                    <h4><strong>#${p.id}</strong> ${p.titulo}</h4>
                    <p><strong>Bíblia:</strong> ${p.biblia}</p>
                    <p><strong>Ação:</strong> ${p.acao}</p>
                    <button class="action-btn" onclick="togglePrincipio(${p.id})">
                        ${principiosConcluidos.includes(p.id) ? 'Completed' : 'Question'}
                    </button>
                </div>
            `).join('');
        }

        function togglePrincipio(id) {
            const index = principiosConcluidos.indexOf(id);
            if (index > -1) {
                principiosConcluidos.splice(index, 1);
            } else {
                principiosConcluidos.push(id);
            }
            localStorage.setItem('principiosConcluidos', JSON.stringify(principiosConcluidos));
            carregarPrincipios();
            showToast(principiosConcluidos.includes(id) ? 'Princípio aplicado!' : 'Marcado como pendente');
        }

        // Anotações
        document.getElementById('formNota').addEventListener('submit', (e) => {
            e.preventDefault();
            const texto = document.getElementById('textoNota').value.trim();
            if (!texto) {
                showToast('Escreva sua reflexão!', 'error');
                return;
            }
            const nota = {
                texto: texto,
                tags: document.getElementById('tagsNota').value.split(',').map(t => t.trim()).filter(t => t),
                data: new Date().toISOString(),
                id: Date.now()
            };
            notas.unshift(nota);
            localStorage.setItem('notas', JSON.stringify(notas));
            e.target.reset();
            showToast('Reflexão salva!');
            carregarNotas();
        });

        function carregarNotas() {
            const lista = document.getElementById('listaNotas');
            lista.innerHTML = notas.map(n => `
                <div class="note">
                    <div class="date">${new Date(n.data).toLocaleString('pt-BR')}</div>
                    <div>${n.texto.replace(/\n/g, '<br>')}</div>
                    ${n.tags.length ? `<div class="tags">${n.tags.map(t => `<span class="tag">#${t}</span>`).join('')}</div>` : ''}
                    <button class="btn-danger" style="margin-top:8px; padding:4px 8px; font-size:0.7rem;" onclick="excluirNota(${n.id})">Excluir</button>
                </div>
            `).join('') || '<p style="text-align:center; color:var(--gray);">Nenhuma reflexão ainda.</p>';
        }

        function excluirNota(id) {
            notas = notas.filter(n => n.id !== id);
            localStorage.setItem('notas', JSON.stringify(notas));
            carregarNotas();
            showToast('Reflexão excluída.');
        }

        // Inicialização
        document.getElementById('dataTransacao').valueAsDate = new Date();
        atualizarDashboard();
        carregarTransacoes();
        carregarPrincipios();
        carregarNotas();
    </script>
</body>
</html>
