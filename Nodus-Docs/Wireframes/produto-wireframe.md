Esta é a pagina para o cliente ver o produto e tem ligação com o [[home-wireframe]] 

O wireframe de apresentação é este:

ChatGPT 

![[Pasted image 20251230000451.png]]

```
<!DOCTYPE html>
<html lang="pt-PT">
<head>
    <meta charset="UTF-8">
    <title>Produto – Wireframe</title>

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

        header {
            border-bottom: 2px solid #000;
            padding: 16px;
        }

        header h1 {
            margin: 0;
            font-size: 18px;
        }

        .container {
            padding: 20px;
        }

        /* LAYOUT PRINCIPAL */
        .product-layout {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 24px;
        }

        /* GALERIA */
        .gallery {
            border: 2px solid #000;
            padding: 12px;
            display: grid;
            grid-template-columns: 1fr 3fr;
            gap: 12px;
            height: 320px;
        }

        .thumbnails {
            border: 2px dashed #000;
            display: flex;
            flex-direction: column;
            gap: 8px;
            padding: 8px;
        }

        .thumbnail {
            border: 1px solid #000;
            height: 40px;
        }

        .main-image {
            border: 2px dashed #000;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 14px;
        }

        /* INFO PRODUTO */
        .product-info {
            border: 2px solid #000;
            padding: 16px;
            display: flex;
            flex-direction: column;
            gap: 16px;
        }

        .product-title {
            border-bottom: 2px solid #000;
            padding-bottom: 8px;
            font-size: 16px;
        }

        .price {
            font-size: 18px;
        }

        .stock {
            border: 2px dashed #000;
            padding: 8px;
            width: fit-content;
            font-size: 13px;
        }

        .cta {
            border: 2px solid #000;
            padding: 16px;
            text-align: center;
            font-weight: bold;
        }

        /* DETALHES */
        .details {
            margin-top: 24px;
            border: 2px solid #000;
            padding: 16px;
        }

        .tabs {
            display: flex;
            gap: 12px;
            margin-bottom: 16px;
        }

        .tab {
            border: 2px solid #000;
            padding: 8px 12px;
            font-size: 13px;
        }

        .content {
            border: 2px dashed #000;
            padding: 16px;
        }

        .spec-table {
            border: 1px solid #000;
            margin-top: 12px;
            font-size: 13px;
        }

        .spec-row {
            display: grid;
            grid-template-columns: 1fr 2fr;
            border-bottom: 1px solid #000;
            padding: 6px;
        }

        .spec-row:last-child {
            border-bottom: none;
        }

        /* RESPONSIVO */
        @media (max-width: 900px) {
            .product-layout {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

<header>
    <h1>Página de Produto (Cliente)</h1>
</header>

<main class="container">

    <!-- LAYOUT PRINCIPAL -->
    <section class="product-layout">

        <!-- GALERIA -->
        <div class="gallery">
            <div class="thumbnails">
                <div class="thumbnail"></div>
                <div class="thumbnail"></div>
                <div class="thumbnail"></div>
            </div>

            <div class="main-image">
                Imagem principal do produto
            </div>
        </div>

        <!-- INFO -->
        <div class="product-info">
            <div class="product-title">
                Nome do Produto
            </div>

            <div class="price">
                Preço: [ € XXX,XX ]
            </div>

            <div class="stock">
                Estado do stock (Em stock / Poucas unidades)
            </div>

            <div class="cta">
                ADICIONAR AO CARRINHO
            </div>
        </div>

    </section>

    <!-- DETALHES -->
    <section class="details">
        <div class="tabs">
            <div class="tab">Descrição</div>
            <div class="tab">Especificações Técnicas</div>
        </div>

        <div class="content">
            Conteúdo dinâmico da aba selecionada

            <div class="spec-table">
                <div class="spec-row">
                    <strong>CPU</strong>
                    <span>[ valor vindo do JSON ]</span>
                </div>
                <div class="spec-row">
                    <strong>RAM</strong>
                    <span>[ valor vindo do JSON ]</span>
                </div>
                <div class="spec-row">
                    <strong>Armazenamento</strong>
                    <span>[ valor vindo do JSON ]</span>
                </div>
            </div>
        </div>
    </section>

</main>

</body>
</html>

```


ClaudeAI

![[Pasted image 20251230000725.png]]
![[Captura de ecrã 2025-12-30, às 00.07.35.png]]

```
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Detalhe do Produto - Wireframe</title>
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
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Navigation */
        nav {
            border: 2px solid #333;
            padding: 15px 20px;
            background: white;
            margin-bottom: 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .breadcrumb {
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .breadcrumb a {
            color: #333;
            text-decoration: none;
            border-bottom: 1px solid #333;
        }

        .nav-actions {
            display: flex;
            gap: 15px;
            font-size: 11px;
            font-weight: bold;
        }

        /* Main Grid */
        .product-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin-bottom: 30px;
        }

        @media (max-width: 968px) {
            .product-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Gallery Section */
        .gallery-section {
            border: 2px solid #333;
            background: white;
            padding: 20px;
        }

        .main-image {
            width: 100%;
            aspect-ratio: 1;
            border: 2px solid #333;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 15px;
            background: repeating-linear-gradient(
                45deg,
                #fff,
                #fff 20px,
                #f0f0f0 20px,
                #f0f0f0 40px
            );
            position: relative;
        }

        .image-placeholder {
            font-size: 14px;
            text-transform: uppercase;
            letter-spacing: 2px;
            font-weight: bold;
        }

        .zoom-icon {
            position: absolute;
            top: 10px;
            right: 10px;
            border: 2px solid #333;
            background: white;
            padding: 8px 12px;
            font-size: 10px;
            font-weight: bold;
        }

        .thumbnail-list {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 10px;
        }

        .thumbnail {
            aspect-ratio: 1;
            border: 2px solid #333;
            background: white;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            font-size: 9px;
            transition: all 0.2s;
        }

        .thumbnail:hover,
        .thumbnail.active {
            background: #333;
            color: white;
        }

        /* Product Info Section */
        .info-section {
            border: 2px solid #333;
            background: white;
            padding: 25px;
        }

        .product-title {
            font-size: 22px;
            font-weight: bold;
            margin-bottom: 15px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .price-block {
            border: 3px solid #333;
            padding: 20px;
            margin-bottom: 15px;
            background: repeating-linear-gradient(
                0deg,
                transparent,
                transparent 10px,
                #f0f0f0 10px,
                #f0f0f0 11px
            );
        }

        .price-label {
            font-size: 10px;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 5px;
        }

        .price {
            font-size: 36px;
            font-weight: bold;
        }

        .old-price {
            font-size: 16px;
            text-decoration: line-through;
            color: #666;
            margin-left: 10px;
        }

        .stock-status {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 12px 15px;
            border: 2px solid #333;
            margin-bottom: 20px;
            font-size: 12px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .stock-status.in-stock {
            background: repeating-linear-gradient(
                90deg,
                #fff,
                #fff 5px,
                #e8e8e8 5px,
                #e8e8e8 10px
            );
        }

        .stock-status.low-stock {
            background: repeating-linear-gradient(
                45deg,
                #fff,
                #fff 5px,
                #ffd700 5px,
                #ffd700 6px
            );
        }

        .stock-indicator {
            width: 12px;
            height: 12px;
            border: 2px solid #333;
            background: white;
        }

        .stock-indicator.available {
            background: #333;
        }

        /* Quantity Selector */
        .quantity-section {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 20px;
        }

        .quantity-label {
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-weight: bold;
        }

        .quantity-controls {
            display: flex;
            border: 2px solid #333;
        }

        .qty-btn {
            width: 35px;
            height: 35px;
            border: none;
            background: white;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            font-family: 'Courier New', monospace;
        }

        .qty-btn:hover {
            background: #333;
            color: white;
        }

        .qty-input {
            width: 50px;
            text-align: center;
            border: none;
            border-left: 2px solid #333;
            border-right: 2px solid #333;
            font-family: 'Courier New', monospace;
            font-size: 14px;
            font-weight: bold;
        }

        /* CTA Button */
        .cta-button {
            width: 100%;
            padding: 18px;
            border: 3px solid #333;
            background: #333;
            color: white;
            font-family: 'Courier New', monospace;
            font-size: 14px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 2px;
            cursor: pointer;
            margin-bottom: 15px;
            transition: all 0.2s;
        }

        .cta-button:hover {
            background: white;
            color: #333;
        }

        .wishlist-button {
            width: 100%;
            padding: 12px;
            border: 2px solid #333;
            background: white;
            font-family: 'Courier New', monospace;
            font-size: 12px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
            cursor: pointer;
            transition: all 0.2s;
        }

        .wishlist-button:hover {
            background: #f0f0f0;
        }

        /* Tabs/Accordion */
        .details-section {
            border: 2px solid #333;
            background: white;
            margin-bottom: 20px;
        }

        .tab-buttons {
            display: flex;
            border-bottom: 2px solid #333;
        }

        .tab-btn {
            flex: 1;
            padding: 15px;
            border: none;
            border-right: 2px solid #333;
            background: white;
            font-family: 'Courier New', monospace;
            font-size: 12px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
            cursor: pointer;
            transition: all 0.2s;
        }

        .tab-btn:last-child {
            border-right: none;
        }

        .tab-btn:hover {
            background: #f0f0f0;
        }

        .tab-btn.active {
            background: #333;
            color: white;
        }

        .tab-content {
            padding: 25px;
            display: none;
        }

        .tab-content.active {
            display: block;
        }

        .tab-content p {
            font-size: 13px;
            line-height: 1.8;
            margin-bottom: 15px;
        }

        /* Specifications Table */
        .specs-table {
            width: 100%;
            border-collapse: collapse;
        }

        .specs-table tr {
            border-bottom: 1px solid #ddd;
        }

        .specs-table tr:last-child {
            border-bottom: none;
        }

        .specs-table td {
            padding: 12px 0;
            font-size: 12px;
        }

        .specs-table td:first-child {
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            width: 35%;
            font-size: 11px;
        }

        /* Meta Info */
        .meta-info {
            display: flex;
            gap: 20px;
            padding: 15px 25px;
            border-top: 2px solid #333;
            font-size: 11px;
        }

        .meta-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .icon-box {
            width: 16px;
            height: 16px;
            border: 2px solid #333;
            background: white;
        }

        /* Annotation */
        .note-box {
            border: 2px dashed #666;
            padding: 15px;
            margin-top: 20px;
            background: #fffef0;
            font-size: 11px;
            line-height: 1.6;
        }

        .note-title {
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 8px;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Navigation -->
        <nav>
            <div class="breadcrumb">
                <a href="#">INÍCIO</a> / <a href="#">COMPUTADORES</a> / <a href="#">PORTÁTEIS</a> / <span>LENOVO THINKPAD X1</span>
            </div>
            <div class="nav-actions">
                [CARRINHO: 0] | [CONTA]
            </div>
        </nav>

        <!-- Product Grid -->
        <div class="product-grid">
            <!-- Gallery Section -->
            <div class="gallery-section">
                <div class="main-image">
                    <span class="image-placeholder">[IMAGEM PRINCIPAL]<br/>600x600px</span>
                    <div class="zoom-icon">🔍 ZOOM</div>
                </div>
                <div class="thumbnail-list">
                    <div class="thumbnail active">[IMG 1]</div>
                    <div class="thumbnail">[IMG 2]</div>
                    <div class="thumbnail">[IMG 3]</div>
                    <div class="thumbnail">[IMG 4]</div>
                </div>
            </div>

            <!-- Product Info Section -->
            <div class="info-section">
                <h1 class="product-title">Lenovo ThinkPad X1 Carbon Gen 11</h1>
                
                <div class="price-block">
                    <div class="price-label">PREÇO</div>
                    <div>
                        <span class="price">€1.299,00</span>
                        <span class="old-price">€1.499,00</span>
                    </div>
                </div>

                <div class="stock-status in-stock">
                    <div class="stock-indicator available"></div>
                    <span>EM STOCK • ENVIO EM 24H</span>
                </div>

                <div class="quantity-section">
                    <span class="quantity-label">QUANTIDADE:</span>
                    <div class="quantity-controls">
                        <button class="qty-btn" onclick="decrementQty()">−</button>
                        <input type="text" class="qty-input" value="1" id="qtyInput" readonly>
                        <button class="qty-btn" onclick="incrementQty()">+</button>
                    </div>
                </div>

                <button class="cta-button">
                    ▶ ADICIONAR AO CARRINHO
                </button>

                <button class="wishlist-button">
                    ♡ ADICIONAR À WISHLIST
                </button>

                <div class="meta-info">
                    <div class="meta-item">
                        <div class="icon-box"></div>
                        <span>SKU: LNV-X1C11-001</span>
                    </div>
                    <div class="meta-item">
                        <div class="icon-box"></div>
                        <span>CATEGORIA: PORTÁTEIS</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- Details Section with Tabs -->
        <div class="details-section">
            <div class="tab-buttons">
                <button class="tab-btn active" onclick="switchTab(0)">DESCRIÇÃO</button>
                <button class="tab-btn" onclick="switchTab(1)">ESPECIFICAÇÕES TÉCNICAS</button>
                <button class="tab-btn" onclick="switchTab(2)">ENVIO & GARANTIA</button>
            </div>

            <!-- Tab 1: Description -->
            <div class="tab-content active" id="tab-0">
                <p>
                    <strong>[DESCRIÇÃO DO PRODUTO]</strong>
                </p>
                <p>
                    O Lenovo ThinkPad X1 Carbon Gen 11 representa o auge da engenharia de computadores portáteis empresariais. Com design ultraleve em fibra de carbono e certificação militar MIL-STD-810H, este portátil combina durabilidade excepcional com portabilidade máxima.
                </p>
                <p>
                    Equipado com processadores Intel Core de 13ª geração e até 32GB de RAM LPDDR5, o X1 Carbon oferece desempenho profissional para as tarefas mais exigentes. O ecrã de 14" com opções WUXGA ou 2.8K proporciona uma experiência visual cristalina.
                </p>
                <p>
                    [CARACTERÍSTICAS PRINCIPAIS]<br/>
                    • Peso: apenas 1.12kg<br/>
                    • Bateria: até 15h de autonomia<br/>
                    • Conectividade: Thunderbolt 4, Wi-Fi 6E<br/>
                    • Segurança: Leitor biométrico, TPM 2.0
                </p>
            </div>

            <!-- Tab 2: Specifications -->
            <div class="tab-content" id="tab-1">
                <p><strong>[ESPECIFICAÇÕES TÉCNICAS]</strong></p>
                <p style="font-size: 11px; color: #666; margin-bottom: 15px;">
                    ↓ Dados renderizados dinamicamente do campo JSON (products.specifications)
                </p>
                
                <table class="specs-table">
                    <tr>
                        <td>Processador</td>
                        <td>Intel Core i7-1365U (10 núcleos, até 5.2GHz)</td>
                    </tr>
                    <tr>
                        <td>Memória RAM</td>
                        <td>16GB LPDDR5-5200MHz (soldada)</td>
                    </tr>
                    <tr>
                        <td>Armazenamento</td>
                        <td>512GB PCIe NVMe Gen 4 SSD</td>
                    </tr>
                    <tr>
                        <td>Ecrã</td>
                        <td>14" WUXGA (1920x1200) IPS, 400 nits, anti-reflexo</td>
                    </tr>
                    <tr>
                        <td>Placa Gráfica</td>
                        <td>Intel Iris Xe Graphics integrada</td>
                    </tr>
                    <tr>
                        <td>Sistema Operativo</td>
                        <td>Windows 11 Pro (64-bit)</td>
                    </tr>
                    <tr>
                        <td>Bateria</td>
                        <td>57Wh, até 15 horas de autonomia</td>
                    </tr>
                    <tr>
                        <td>Conectividade</td>
                        <td>Wi-Fi 6E AX211, Bluetooth 5.1</td>
                    </tr>
                    <tr>
                        <td>Portas</td>
                        <td>2x Thunderbolt 4, 2x USB-A 3.2, HDMI 2.0, Jack 3.5mm</td>
                    </tr>
                    <tr>
                        <td>Dimensões</td>
                        <td>315.6 x 222.5 x 14.95mm</td>
                    </tr>
                    <tr>
                        <td>Peso</td>
                        <td>1.12kg</td>
                    </tr>
                    <tr>
                        <td>Garantia</td>
                        <td>3 anos (fabricante)</td>
                    </tr>
                </table>
            </div>

            <!-- Tab 3: Shipping -->
            <div class="tab-content" id="tab-2">
                <p><strong>[INFORMAÇÕES DE ENVIO & GARANTIA]</strong></p>
                <p>
                    <strong>ENVIO:</strong><br/>
                    • Envio expresso 24-48h para Portugal Continental<br/>
                    • Envio grátis em encomendas acima de €50<br/>
                    • Tracking disponível após processamento<br/>
                    • Regiões Autónomas: 3-5 dias úteis
                </p>
                <p>
                    <strong>GARANTIA:</strong><br/>
                    • 3 anos de garantia do fabricante<br/>
                    • 14 dias de devolução (produto não usado)<br/>
                    • Suporte técnico especializado<br/>
                    • Extensão de garantia disponível
                </p>
            </div>
        </div>

        <!-- Technical Note -->
        <div class="note-box">
            <div class="note-title">📋 NOTA TÉCNICA (Wireframe)</div>
            <p>
                <strong>Hierarquia da Informação:</strong> O layout prioriza conversão através de CTA proeminente e estado de stock visível (RF-013).
            </p>
            <p>
                <strong>Especificações Dinâmicas:</strong> A tabela de especificações é renderizada a partir do campo JSON (products.specifications), permitindo flexibilidade sem alterar o layout. Exemplo de estrutura JSON: {"cpu": "Intel i7-1365U", "ram": "16GB LPDDR5", "storage": "512GB NVMe"}
            </p>
            <p>
                <strong>Stock Proativo:</strong> O sistema verifica stock em tempo real e exibe estados visuais claros para evitar frustração no checkout.
            </p>
        </div>
    </div>

    <script>
        let quantity = 1;

        function incrementQty() {
            if (quantity < 99) {
                quantity++;
                document.getElementById('qtyInput').value = quantity;
            }
        }

        function decrementQty() {
            if (quantity > 1) {
                quantity--;
                document.getElementById('qtyInput').value = quantity;
            }
        }

        function switchTab(index) {
            // Hide all tabs
            const tabs = document.querySelectorAll('.tab-content');
            const buttons = document.querySelectorAll('.tab-btn');
            
            tabs.forEach(tab => tab.classList.remove('active'));
            buttons.forEach(btn => btn.classList.remove('active'));
            
            // Show selected tab
            document.getElementById('tab-' + index).classList.add('active');
            buttons[index].classList.add('active');
        }
    </script>
</body>
</html>

```
