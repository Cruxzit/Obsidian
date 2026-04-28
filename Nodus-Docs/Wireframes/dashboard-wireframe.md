Este dashboard é para o admin e tem ligação com o [[home-wireframe]] 


O wireframe de apresentação é este:
![[Captura de ecrã 2025-12-29, às 23.57.16.png]]
ChatGPT

```
<!DOCTYPE html>
<html lang="pt-PT">
<head>
    <meta charset="UTF-8">
    <title>Dashboard Financeiro – Wireframe</title>

    <style>
        * {
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        body {
            margin: 0;
            background: #ffffff;
            color: #000;
        }

        /* HEADER */
        header {
            border-bottom: 2px solid #000;
            padding: 16px;
        }

        header h1 {
            margin: 0;
            font-size: 18px;
        }

        /* CONTAINER */
        .container {
            padding: 20px;
            display: flex;
            flex-direction: column;
            gap: 24px;
        }

        /* KPI */
        .kpi-section {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 16px;
        }

        .kpi-box {
            border: 2px solid #000;
            padding: 12px;
            height: 80px;
        }

        .kpi-box strong {
            display: block;
            font-size: 12px;
            margin-bottom: 8px;
        }

        .kpi-box span {
            font-size: 14px;
        }

        /* Destaque apenas conceptual */
        .highlight {
            border-style: dashed;
        }

        /* GRÁFICO */
        .chart-section {
            border: 2px solid #000;
            padding: 12px;
            height: 260px;
        }

        .chart-placeholder {
            border: 2px dashed #000;
            height: 200px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 14px;
        }

        /* PARTE INFERIOR */
        .bottom-section {
            display: grid;
            grid-template-columns: 3fr 1fr;
            gap: 16px;
        }

        .table-box {
            border: 2px solid #000;
            padding: 12px;
        }

        .table-placeholder {
            border: 2px dashed #000;
            height: 140px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 13px;
        }

        .action-box {
            border: 2px solid #000;
            padding: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
        }

        /* RESPONSIVO (opcional mas aceitável) */
        @media (max-width: 900px) {
            .kpi-section {
                grid-template-columns: repeat(2, 1fr);
            }

            .bottom-section {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

<header>
    <h1>Dashboard Financeiro (Admin)</h1>
</header>

<main class="container">

    <!-- KPIs -->
    <section class="kpi-section">
        <div class="kpi-box">
            <strong>Vendas Brutas</strong>
            <span>[ € Total Faturado ]</span>
        </div>

        <div class="kpi-box">
            <strong>CMV</strong>
            <span>[ Soma cost_snapshot ]</span>
        </div>

        <div class="kpi-box">
            <strong>Despesas Operacionais</strong>
            <span>[ Soma expenses ]</span>
        </div>

        <div class="kpi-box highlight">
            <strong>Lucro Líquido Real</strong>
            <span>[ Vendas - CMV - Despesas ]</span>
        </div>
    </section>

    <!-- Gráfico -->
    <section class="chart-section">
        <strong>Receitas vs Custos Totais (Mensal)</strong>
        <div class="chart-placeholder">
            Área reservada para gráfico de barras / linhas
        </div>
    </section>

    <!-- Inferior -->
    <section class="bottom-section">
        <div class="table-box">
            <strong>Últimas Encomendas</strong>
            <div class="table-placeholder">
                Tabela de encomendas recentes
            </div>
        </div>

        <div class="action-box">
            Botão:<br>
            "Registar Nova Despesa"
        </div>
    </section>

</main>

</body>
</html>


```

ClaudeAI



```
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dashboard Financeiro - Wireframe</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Courier New', monospace;
            background: #f5f5f5;
            color: #333;
            padding: 20px;
            line-height: 1.6;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
        }

        /* Wireframe Box Style */
        .box {
            background: white;
            border: 2px solid #333;
            padding: 20px;
            margin-bottom: 20px;
        }

        .box-header {
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 2px solid #333;
            font-weight: bold;
        }

        header {
            border: 3px solid #333;
            padding: 20px;
            margin-bottom: 20px;
            background: white;
        }

        h1 {
            font-size: 24px;
            font-weight: bold;
            margin-bottom: 5px;
        }

        .subtitle {
            font-size: 12px;
            color: #666;
        }

        /* KPI Grid */
        .kpi-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 20px;
            margin-bottom: 20px;
        }

        @media (max-width: 968px) {
            .kpi-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        .kpi-box {
            border: 2px solid #333;
            padding: 20px;
            background: white;
            position: relative;
        }

        .kpi-box.highlight {
            border: 3px solid #333;
            background: repeating-linear-gradient(
                45deg,
                #fff,
                #fff 10px,
                #f0f0f0 10px,
                #f0f0f0 20px
            );
        }

        .kpi-label {
            font-size: 10px;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 10px;
            font-weight: bold;
        }

        .kpi-value {
            font-size: 28px;
            font-weight: bold;
            margin-bottom: 8px;
            font-family: 'Courier New', monospace;
        }

        .kpi-change {
            font-size: 11px;
            margin-top: 5px;
        }

        /* Main Grid */
        .main-grid {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 20px;
            margin-bottom: 20px;
        }

        @media (max-width: 968px) {
            .main-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Chart Placeholder */
        .chart-box {
            border: 2px solid #333;
            background: white;
            padding: 20px;
        }

        .chart-placeholder {
            border: 1px dashed #666;
            height: 300px;
            display: flex;
            align-items: flex-end;
            justify-content: space-around;
            padding: 20px;
            background: repeating-linear-gradient(
                0deg,
                transparent,
                transparent 39px,
                #ddd 39px,
                #ddd 40px
            );
            position: relative;
        }

        .chart-bar {
            width: 60px;
            background: white;
            border: 2px solid #333;
            position: relative;
            display: flex;
            flex-direction: column;
            justify-content: flex-end;
        }

        .bar-segment {
            width: 100%;
            border-top: 2px solid #333;
        }

        .bar-segment.revenue {
            background: repeating-linear-gradient(
                90deg,
                #fff,
                #fff 5px,
                #333 5px,
                #333 6px
            );
        }

        .bar-segment.cost {
            background: repeating-linear-gradient(
                45deg,
                #fff,
                #fff 5px,
                #666 5px,
                #666 6px
            );
        }

        .chart-label {
            text-align: center;
            font-size: 10px;
            font-weight: bold;
            margin-top: 5px;
        }

        .chart-legend {
            display: flex;
            gap: 20px;
            margin-top: 15px;
            font-size: 11px;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .legend-box {
            width: 20px;
            height: 20px;
            border: 2px solid #333;
        }

        /* Side Panel */
        .stats-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            margin-bottom: 20px;
        }

        .stat-box {
            border: 2px solid #333;
            padding: 15px;
            background: white;
        }

        .stat-label {
            font-size: 9px;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 5px;
        }

        .stat-value {
            font-size: 20px;
            font-weight: bold;
        }

        /* Button */
        .btn {
            width: 100%;
            padding: 15px;
            border: 3px solid #333;
            background: white;
            font-family: 'Courier New', monospace;
            font-size: 12px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
            cursor: pointer;
            transition: all 0.2s;
        }

        .btn:hover {
            background: #333;
            color: white;
        }

        /* Table */
        .table-box {
            border: 2px solid #333;
            background: white;
            padding: 20px;
        }

        table {
            width: 100%;
            border-collapse: collapse;
        }

        th {
            text-align: left;
            font-size: 10px;
            text-transform: uppercase;
            letter-spacing: 1px;
            padding: 10px;
            border-bottom: 2px solid #333;
            font-weight: bold;
        }

        td {
            padding: 10px;
            border-bottom: 1px solid #ddd;
            font-size: 12px;
        }

        tr:last-child td {
            border-bottom: none;
        }

        .status {
            display: inline-block;
            padding: 3px 8px;
            border: 1px solid #333;
            font-size: 10px;
            font-weight: bold;
        }

        .status.completed {
            background: repeating-linear-gradient(
                45deg,
                transparent,
                transparent 2px,
                #333 2px,
                #333 3px
            );
        }

        /* Annotations */
        .annotation {
            position: relative;
            display: inline-block;
        }

        .annotation::after {
            content: attr(data-note);
            position: absolute;
            bottom: 100%;
            left: 50%;
            transform: translateX(-50%);
            background: #333;
            color: white;
            padding: 5px 10px;
            font-size: 10px;
            white-space: nowrap;
            opacity: 0;
            pointer-events: none;
            transition: opacity 0.2s;
        }

        .annotation:hover::after {
            opacity: 1;
        }

        .filter-select {
            padding: 5px 10px;
            border: 2px solid #333;
            background: white;
            font-family: 'Courier New', monospace;
            font-size: 11px;
            font-weight: bold;
        }

        .section-title {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
        }

        .view-all {
            font-size: 11px;
            color: #333;
            text-decoration: none;
            border-bottom: 2px solid #333;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <header>
            <h1>DASHBOARD FINANCEIRO</h1>
            <p class="subtitle">Admin Panel • Visão ROI em Tempo Real</p>
        </header>

        <!-- KPI Cards -->
        <div class="kpi-grid">
            <div class="kpi-box">
                <div class="kpi-label">[1] Vendas Brutas</div>
                <div class="kpi-value">€45.820</div>
                <div class="kpi-change">▲ 12.5% vs anterior</div>
            </div>

            <div class="kpi-box">
                <div class="kpi-label">[2] CMV (Custo)</div>
                <div class="kpi-value">€18.450</div>
                <div class="kpi-change">▲ 8.2% vs anterior</div>
            </div>

            <div class="kpi-box">
                <div class="kpi-label">[3] Despesas Op.</div>
                <div class="kpi-value">€8.920</div>
                <div class="kpi-change">▼ 3.1% vs anterior</div>
            </div>

            <div class="kpi-box highlight">
                <div class="kpi-label">[4] LUCRO LÍQUIDO</div>
                <div class="kpi-value">€18.450</div>
                <div class="kpi-change">40.3% margem</div>
            </div>
        </div>

        <!-- Main Grid -->
        <div class="main-grid">
            <!-- Chart -->
            <div class="chart-box">
                <div class="section-title">
                    <div class="box-header">Receitas vs. Custos Totais</div>
                    <select class="filter-select">
                        <option>ÚLTIMOS 6 MESES</option>
                        <option>ÚLTIMOS 3 MESES</option>
                        <option>ÚLTIMO ANO</option>
                    </select>
                </div>
                
                <div class="chart-placeholder">
                    <div style="text-align: center;">
                        <div class="chart-bar">
                            <div class="bar-segment revenue" style="height: 180px;"></div>
                            <div class="bar-segment cost" style="height: 120px;"></div>
                        </div>
                        <div class="chart-label">JUL</div>
                    </div>
                    <div style="text-align: center;">
                        <div class="chart-bar">
                            <div class="bar-segment revenue" style="height: 195px;"></div>
                            <div class="bar-segment cost" style="height: 125px;"></div>
                        </div>
                        <div class="chart-label">AGO</div>
                    </div>
                    <div style="text-align: center;">
                        <div class="chart-bar">
                            <div class="bar-segment revenue" style="height: 185px;"></div>
                            <div class="bar-segment cost" style="height: 118px;"></div>
                        </div>
                        <div class="chart-label">SET</div>
                    </div>
                    <div style="text-align: center;">
                        <div class="chart-bar">
                            <div class="bar-segment revenue" style="height: 205px;"></div>
                            <div class="bar-segment cost" style="height: 135px;"></div>
                        </div>
                        <div class="chart-label">OUT</div>
                    </div>
                    <div style="text-align: center;">
                        <div class="chart-bar">
                            <div class="bar-segment revenue" style="height: 198px;"></div>
                            <div class="bar-segment cost" style="height: 130px;"></div>
                        </div>
                        <div class="chart-label">NOV</div>
                    </div>
                    <div style="text-align: center;">
                        <div class="chart-bar">
                            <div class="bar-segment revenue" style="height: 215px;"></div>
                            <div class="bar-segment cost" style="height: 140px;"></div>
                        </div>
                        <div class="chart-label">DEZ</div>
                    </div>
                </div>

                <div class="chart-legend">
                    <div class="legend-item">
                        <div class="legend-box" style="background: repeating-linear-gradient(90deg, #fff, #fff 5px, #333 5px, #333 6px);"></div>
                        <span>RECEITAS</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-box" style="background: repeating-linear-gradient(45deg, #fff, #fff 5px, #666 5px, #666 6px);"></div>
                        <span>CUSTOS</span>
                    </div>
                </div>
            </div>

            <!-- Side Panel -->
            <div>
                <div class="box">
                    <div class="box-header">Estatísticas Rápidas</div>
                    <div class="stats-grid">
                        <div class="stat-box">
                            <div class="stat-label">Encomendas</div>
                            <div class="stat-value">248</div>
                        </div>
                        <div class="stat-box">
                            <div class="stat-label">Ticket Médio</div>
                            <div class="stat-value">€184.76</div>
                        </div>
                    </div>
                </div>

                <div class="box">
                    <div class="box-header">Ação Rápida</div>
                    <button class="btn">+ Nova Despesa</button>
                </div>
            </div>
        </div>

        <!-- Orders Table -->
        <div class="table-box">
            <div class="section-title">
                <div class="box-header">Últimas Encomendas</div>
                <a href="#" class="view-all">VER TODAS →</a>
            </div>
            <table>
                <thead>
                    <tr>
                        <th>ID</th>
                        <th>CLIENTE</th>
                        <th>DATA</th>
                        <th>VALOR</th>
                        <th>CMV</th>
                        <th>MARGEM</th>
                        <th>ESTADO</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>#1842</td>
                        <td>João Silva</td>
                        <td>28/12/2025</td>
                        <td>€320.00</td>
                        <td>€145.00</td>
                        <td>€175.00</td>
                        <td><span class="status completed">COMPLETO</span></td>
                    </tr>
                    <tr>
                        <td>#1841</td>
                        <td>Maria Santos</td>
                        <td>27/12/2025</td>
                        <td>€189.90</td>
                        <td>€82.50</td>
                        <td>€107.40</td>
                        <td><span class="status completed">COMPLETO</span></td>
                    </tr>
                    <tr>
                        <td>#1840</td>
                        <td>Pedro Costa</td>
                        <td>27/12/2025</td>
                        <td>€450.00</td>
                        <td>€198.00</td>
                        <td>€252.00</td>
                        <td><span class="status">PENDENTE</span></td>
                    </tr>
                    <tr>
                        <td>#1839</td>
                        <td>Ana Ferreira</td>
                        <td>26/12/2025</td>
                        <td>€125.50</td>
                        <td>€58.30</td>
                        <td>€67.20</td>
                        <td><span class="status completed">COMPLETO</span></td>
                    </tr>
                    <tr>
                        <td>#1840</td>
                        <td>Rui Oliveira</td>
                        <td>26/12/2025</td>
                        <td>€278.00</td>
                        <td>€115.00</td>
                        <td>€163.00</td>
                        <td><span class="status completed">COMPLETO</span></td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
</body>
</html>

```
