Esta é a pagina home

O wireframe de apresentação é este:

ChatGPT

![[Captura de ecrã 2025-12-30, às 00.01.38.png]]

```
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Página Inicial - Wireframe</title>
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
            line-height: 1.6;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
        }

        /* Header */
        .header {
            background: white;
            border-bottom: 3px solid #333;
        }

        .top-bar {
            border-bottom: 2px solid #333;
            padding: 10px 20px;
            display: flex;
            justify-content: space-between;
            font-size: 10px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .main-header {
            padding: 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 30px;
        }

        .logo {
            border: 3px solid #333;
            padding: 15px 30px;
            font-size: 18px;
            font-weight: bold;
            letter-spacing: 2px;
        }

        .search-bar {
            flex: 1;
            display: flex;
            border: 2px solid #333;
        }

        .search-input {
            flex: 1;
            padding: 12px 15px;
            border: none;
            font-family: 'Courier New', monospace;
            font-size: 12px;
        }

        .search-btn {
            padding: 12px 25px;
            border: none;
            border-left: 2px solid #333;
            background: #333;
            color: white;
            font-family: 'Courier New', monospace;
            font-size: 11px;
            font-weight: bold;
            cursor: pointer;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .search-btn:hover {
            background: #555;
        }

        .header-actions {
            display: flex;
            gap: 20px;
            font-size: 11px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .header-action {
            cursor: pointer;
            padding: 10px 15px;
            border: 2px solid #333;
            background: white;
            transition: all 0.2s;
        }

        .header-action:hover {
            background: #333;
            color: white;
        }

        /* Navigation */
        .main-nav {
            background: #333;
            color: white;
            padding: 0 20px;
            display: flex;
            justify-content: center;
            gap: 0;
        }

        .nav-item {
            padding: 15px 25px;
            border-right: 1px solid #555;
            cursor: pointer;
            font-size: 11px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.2s;
        }

        .nav-item:hover {
            background: #555;
        }

        /* Hero Section */
        .hero {
            margin: 20px;
            border: 3px solid #333;
            background: white;
            height: 500px;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            background: repeating-linear-gradient(
                45deg,
                #fff,
                #fff 30px,
                #f0f0f0 30px,
                #f0f0f0 60px
            );
        }

        .hero-content {
            text-align: center;
            padding: 40px;
            border: 2px solid #333;
            background: white;
        }

        .hero-tag {
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 15px;
            font-weight: bold;
        }

        .hero-title {
            font-size: 36px;
            font-weight: bold;
            margin-bottom: 15px;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .hero-subtitle {
            font-size: 14px;
            margin-bottom: 25px;
            color: #666;
        }

        .hero-cta {
            padding: 15px 40px;
            border: 3px solid #333;
            background: #333;
            color: white;
            font-family: 'Courier New', monospace;
            font-size: 12px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 2px;
            cursor: pointer;
            transition: all 0.2s;
        }

        .hero-cta:hover {
            background: white;
            color: #333;
        }

        .hero-indicators {
            position: absolute;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            gap: 10px;
        }

        .indicator {
            width: 12px;
            height: 12px;
            border: 2px solid #333;
            background: white;
            cursor: pointer;
        }

        .indicator.active {
            background: #333;
        }

        /* Section Title */
        .section {
            margin: 40px 20px;
        }

        .section-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 3px solid #333;
        }

        .section-title {
            font-size: 20px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .section-link {
            font-size: 11px;
            text-decoration: none;
            color: #333;
            border-bottom: 2px solid #333;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Category Grid */
        .category-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 20px;
            margin-bottom: 40px;
        }

        @media (max-width: 968px) {
            .category-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        .category-card {
            border: 2px solid #333;
            background: white;
            aspect-ratio: 1;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.2s;
            position: relative;
        }

        .category-card:hover {
            border-width: 3px;
            transform: translateY(-3px);
        }

        .category-icon {
            width: 80px;
            height: 80px;
            border: 2px solid #333;
            background: repeating-linear-gradient(
                90deg,
                #fff,
                #fff 10px,
                #f0f0f0 10px,
                #f0f0f0 20px
            );
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 10px;
            font-weight: bold;
        }

        .category-name {
            font-size: 13px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .category-count {
            font-size: 10px;
            color: #666;
            margin-top: 5px;
        }

        /* Product Grid */
        .product-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 20px;
        }

        @media (max-width: 968px) {
            .product-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        .product-card {
            border: 2px solid #333;
            background: white;
            cursor: pointer;
            transition: all 0.2s;
        }

        .product-card:hover {
            border-width: 3px;
            transform: translateY(-3px);
        }

        .product-image {
            aspect-ratio: 1;
            border-bottom: 2px solid #333;
            display: flex;
            align-items: center;
            justify-content: center;
            background: repeating-linear-gradient(
                45deg,
                #fff,
                #fff 20px,
                #f9f9f9 20px,
                #f9f9f9 40px
            );
            font-size: 11px;
            font-weight: bold;
            color: #999;
            position: relative;
        }

        .product-badge {
            position: absolute;
            top: 10px;
            right: 10px;
            padding: 5px 10px;
            border: 2px solid #333;
            background: white;
            font-size: 9px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .product-info {
            padding: 15px;
        }

        .product-category {
            font-size: 9px;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: #666;
            margin-bottom: 8px;
        }

        .product-name {
            font-size: 12px;
            font-weight: bold;
            margin-bottom: 10px;
            line-height: 1.4;
        }

        .product-price {
            font-size: 16px;
            font-weight: bold;
            margin-bottom: 5px;
        }

        .product-old-price {
            font-size: 12px;
            color: #999;
            text-decoration: line-through;
        }

        .product-actions {
            display: flex;
            gap: 10px;
            margin-top: 12px;
        }

        .product-btn {
            flex: 1;
            padding: 10px;
            border: 2px solid #333;
            background: white;
            font-family: 'Courier New', monospace;
            font-size: 10px;
            font-weight: bold;
            text-transform: uppercase;
            cursor: pointer;
            transition: all 0.2s;
        }

        .product-btn.primary {
            background: #333;
            color: white;
        }

        .product-btn:hover {
            background: #555;
            color: white;
        }

        /* Features Banner */
        .features-banner {
            margin: 40px 20px;
            border: 2px solid #333;
            background: white;
            display: grid;
            grid-template-columns: repeat(4, 1fr);
        }

        @media (max-width: 968px) {
            .features-banner {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        .feature-item {
            padding: 30px 20px;
            text-align: center;
            border-right: 2px solid #333;
        }

        .feature-item:last-child {
            border-right: none;
        }

        .feature-icon {
            width: 50px;
            height: 50px;
            border: 2px solid #333;
            margin: 0 auto 15px;
            background: repeating-linear-gradient(
                45deg,
                transparent,
                transparent 5px,
                #f0f0f0 5px,
                #f0f0f0 10px
            );
        }

        .feature-title {
            font-size: 12px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 5px;
        }

        .feature-desc {
            font-size: 10px;
            color: #666;
        }

        /* Footer */
        .footer {
            margin-top: 60px;
            border-top: 3px solid #333;
            background: white;
            padding: 40px 20px 20px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 40px;
            margin-bottom: 30px;
        }

        @media (max-width: 968px) {
            .footer-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        .footer-column h3 {
            font-size: 12px;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 2px solid #333;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 8px;
            font-size: 11px;
        }

        .footer-links a {
            color: #333;
            text-decoration: none;
            border-bottom: 1px solid transparent;
            transition: border-color 0.2s;
        }

        .footer-links a:hover {
            border-bottom-color: #333;
        }

        .footer-bottom {
            padding-top: 20px;
            border-top: 2px solid #333;
            text-align: center;
            font-size: 10px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Note Box */
        .note-box {
            margin: 40px 20px;
            border: 2px dashed #666;
            padding: 20px;
            background: #fffef0;
            font-size: 11px;
            line-height: 1.6;
        }

        .note-title {
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <div class="header">
        <div class="top-bar">
            <div>📍 ENVIO GRÁTIS PARA PORTUGAL • ENCOMENDAS ACIMA DE €50</div>
            <div>[CONTACTO: +351 XXX XXX XXX]</div>
        </div>
        <div class="main-header">
            <div class="logo">[LOGO]<br/>TECHSTORE</div>
            <div class="search-bar">
                <input type="text" class="search-input" placeholder="Pesquisar produtos, marcas, categorias...">
                <button class="search-btn">🔍 PESQUISAR</button>
            </div>
            <div class="header-actions">
                <div class="header-action">👤 CONTA</div>
                <div class="header-action">🛒 CARRINHO (0)</div>
            </div>
        </div>
        <nav class="main-nav">
            <div class="nav-item">COMPUTADORES</div>
            <div class="nav-item">COMPONENTES</div>
            <div class="nav-item">PERIFÉRICOS</div>
            <div class="nav-item">GAMING</div>
            <div class="nav-item">REDE</div>
            <div class="nav-item">OFERTAS</div>
        </nav>
    </div>

    <div class="container">
        <!-- Hero Banner -->
        <div class="hero">
            <div class="hero-content">
                <div class="hero-tag">[NOVIDADE] PROMOÇÃO DE INVERNO</div>
                <h1 class="hero-title">ATÉ 30% OFF<br/>EM PORTÁTEIS</h1>
                <p class="hero-subtitle">Ofertas exclusivas em computadores de alta performance</p>
                <button class="hero-cta">VER OFERTAS ▶</button>
            </div>
            <div class="hero-indicators">
                <div class="indicator active"></div>
                <div class="indicator"></div>
                <div class="indicator"></div>
            </div>
        </div>

        <!-- Categories Section -->
        <div class="section">
            <div class="section-header">
                <h2 class="section-title">Categorias Populares</h2>
                <a href="#" class="section-link">VER TODAS →</a>
            </div>
            <div class="category-grid">
                <div class="category-card">
                    <div class="category-icon">[ICON]</div>
                    <div class="category-name">PORTÁTEIS</div>
                    <div class="category-count">248 produtos</div>
                </div>
                <div class="category-card">
                    <div class="category-icon">[ICON]</div>
                    <div class="category-name">DESKTOPS</div>
                    <div class="category-count">186 produtos</div>
                </div>
                <div class="category-card">
                    <div class="category-icon">[ICON]</div>
                    <div class="category-name">COMPONENTES</div>
                    <div class="category-count">512 produtos</div>
                </div>
                <div class="category-card">
                    <div class="category-icon">[ICON]</div>
                    <div class="category-name">MONITORES</div>
                    <div class="category-count">94 produtos</div>
                </div>
            </div>
        </div>

        <!-- Featured Products -->
        <div class="section">
            <div class="section-header">
                <h2 class="section-title">Produtos em Destaque</h2>
                <a href="#" class="section-link">VER TODOS →</a>
            </div>
            <div class="product-grid">
                <div class="product-card">
                    <div class="product-image">
                        [PRODUTO]<br/>300x300px
                        <div class="product-badge">-15%</div>
                    </div>
                    <div class="product-info">
                        <div class="product-category">PORTÁTEIS</div>
                        <div class="product-name">Lenovo ThinkPad X1 Carbon Gen 11</div>
                        <div class="product-price">€1.299,00</div>
                        <div class="product-old-price">€1.499,00</div>
                        <div class="product-actions">
                            <button class="product-btn primary">COMPRAR</button>
                            <button class="product-btn">♡</button>
                        </div>
                    </div>
                </div>

                <div class="product-card">
                    <div class="product-image">
                        [PRODUTO]<br/>300x300px
                        <div class="product-badge">NOVO</div>
                    </div>
                    <div class="product-info">
                        <div class="product-category">COMPONENTES</div>
                        <div class="product-name">NVIDIA RTX 4080 Super 16GB</div>
                        <div class="product-price">€1.099,00</div>
                        <div class="product-actions">
                            <button class="product-btn primary">COMPRAR</button>
                            <button class="product-btn">♡</button>
                        </div>
                    </div>
                </div>

                <div class="product-card">
                    <div class="product-image">
                        [PRODUTO]<br/>300x300px
                    </div>
                    <div class="product-info">
                        <div class="product-category">MONITORES</div>
                        <div class="product-name">Dell UltraSharp 27" 4K IPS</div>
                        <div class="product-price">€549,00</div>
                        <div class="product-actions">
                            <button class="product-btn primary">COMPRAR</button>
                            <button class="product-btn">♡</button>
                        </div>
                    </div>
                </div>

                <div class="product-card">
                    <div class="product-image">
                        [PRODUTO]<br/>300x300px
                        <div class="product-badge">TOP</div>
                    </div>
                    <div class="product-info">
                        <div class="product-category">DESKTOPS</div>
                        <div class="product-name">Apple Mac Mini M2 Pro</div>
                        <div class="product-price">€1.449,00</div>
                        <div class="product-actions">
                            <button class="product-btn primary">COMPRAR</button>
                            <button class="product-btn">♡</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Features Banner -->
        <div class="features-banner">
            <div class="feature-item">
                <div class="feature-icon"></div>
                <div class="feature-title">ENVIO RÁPIDO</div>
                <div class="feature-desc">24-48h em Portugal Continental</div>
            </div>
            <div class="feature-item">
                <div class="feature-icon"></div>
                <div class="feature-title">PAGAMENTO SEGURO</div>
                <div class="feature-desc">SSL & métodos certificados</div>
            </div>
            <div class="feature-item">
                <div class="feature-icon"></div>
                <div class="feature-title">GARANTIA 3 ANOS</div>
                <div class="feature-desc">Em produtos selecionados</div>
            </div>
            <div class="feature-item">
                <div class="feature-icon"></div>
                <div class="feature-title">SUPORTE 24/7</div>
                <div class="feature-desc">Assistência técnica dedicada</div>
            </div>
        </div>

        <!-- Technical Note -->
        <div class="note-box">
            <div class="note-title">📋 NOTA TÉCNICA (Wireframe - Página Inicial)</div>
            <p>
                <strong>Estrutura de Conversão:</strong> Layout otimizado para descoberta de produtos através de hierarquia clara: Hero Banner (promoções) → Categorias (navegação rápida) → Produtos Destacados (conversão direta).
            </p>
            <p>
                <strong>Hero Dinâmico:</strong> Banner rotativo configurável via CMS com CTAs para campanhas sazonais e lançamentos de produtos.
            </p>
            <p>
                <strong>Grid Responsivo:</strong> Sistema de grid adaptativo (4 colunas desktop → 2 colunas mobile) garante usabilidade em todos os dispositivos.
            </p>
            <p>
                <strong>Badges Contextuais:</strong> Indicadores visuais ("NOVO", "-15%", "TOP") destacam produtos relevantes e criam urgência de compra.
            </p>
            <p>
                <strong>Trust Elements:</strong> Barra de features (envio, garantia, suporte) reforça confiança e reduz fricção no processo de compra.
            </p>
        </div>
    </div>

    <!-- Footer -->
    <div class="footer">
        <div class="footer-grid">
            <div class="footer-column">
                <h3>Sobre</h3>
                <ul class="footer-links">
                    <li><a href="#">Quem Somos</a></li>
                    <li><a href="#">Carreiras</a></li>
                    <li><a href="#">Imprensa</a></li>
                    <li><a href="#">Blog</a></li>
                </ul>
            </div>
            <div class="footer-column">
                <h3>Apoio ao Cliente</h3>
                <ul class="footer-links">
                    <li><a href="#">Centro de Ajuda</a></li>
                    <li><a href="#">Envios & Devoluções</a></li>
                    <li><a href="#">Garantias</a></li>
                    <li><a href="#">Contactos</a></li>
                </ul>
            </div>
            <div class="footer-column">
                <h3>Informação Legal</h3>
                <ul class="footer-links">
                    <li><a href="#">Termos & Condições</a></li>
                    <li><a href="#">Política de Privacidade</a></li>
                    <li><a href="#">Cookies</a></li>
                    <li><a href="#">Livro de Reclamações</a></li>
                </ul>
            </div>
            <div class="footer-column">
                <h3>Newsletter</h3>
                <ul class="footer-links">
                    <li>[INPUT: EMAIL]</li>
                    <li>[BOTÃO: SUBSCREVER]</li>
                    <li style="margin-top: 15px;">[ÍCONES SOCIAIS]</li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            © 2025 TECHSTORE • TODOS OS DIREITOS RESERVADOS • WIREFRAME LOW-FI
        </div>
    </div>
</body>
</html>

```



ClaudAI

![[Pasted image 20251230000259.png]]
![[Pasted image 20251230000322.png]]
![[Pasted image 20251230000348.png]]

```
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Página Inicial - Wireframe</title>
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
            line-height: 1.6;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
        }

        /* Header */
        .header {
            background: white;
            border-bottom: 3px solid #333;
        }

        .top-bar {
            border-bottom: 2px solid #333;
            padding: 10px 20px;
            display: flex;
            justify-content: space-between;
            font-size: 10px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .main-header {
            padding: 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 30px;
        }

        .logo {
            border: 3px solid #333;
            padding: 15px 30px;
            font-size: 18px;
            font-weight: bold;
            letter-spacing: 2px;
        }

        .search-bar {
            flex: 1;
            display: flex;
            border: 2px solid #333;
        }

        .search-input {
            flex: 1;
            padding: 12px 15px;
            border: none;
            font-family: 'Courier New', monospace;
            font-size: 12px;
        }

        .search-btn {
            padding: 12px 25px;
            border: none;
            border-left: 2px solid #333;
            background: #333;
            color: white;
            font-family: 'Courier New', monospace;
            font-size: 11px;
            font-weight: bold;
            cursor: pointer;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .search-btn:hover {
            background: #555;
        }

        .header-actions {
            display: flex;
            gap: 20px;
            font-size: 11px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .header-action {
            cursor: pointer;
            padding: 10px 15px;
            border: 2px solid #333;
            background: white;
            transition: all 0.2s;
        }

        .header-action:hover {
            background: #333;
            color: white;
        }

        /* Navigation */
        .main-nav {
            background: #333;
            color: white;
            padding: 0 20px;
            display: flex;
            justify-content: center;
            gap: 0;
        }

        .nav-item {
            padding: 15px 25px;
            border-right: 1px solid #555;
            cursor: pointer;
            font-size: 11px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.2s;
        }

        .nav-item:hover {
            background: #555;
        }

        /* Hero Section */
        .hero {
            margin: 20px;
            border: 3px solid #333;
            background: white;
            height: 500px;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            background: repeating-linear-gradient(
                45deg,
                #fff,
                #fff 30px,
                #f0f0f0 30px,
                #f0f0f0 60px
            );
        }

        .hero-content {
            text-align: center;
            padding: 40px;
            border: 2px solid #333;
            background: white;
        }

        .hero-tag {
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 15px;
            font-weight: bold;
        }

        .hero-title {
            font-size: 36px;
            font-weight: bold;
            margin-bottom: 15px;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .hero-subtitle {
            font-size: 14px;
            margin-bottom: 25px;
            color: #666;
        }

        .hero-cta {
            padding: 15px 40px;
            border: 3px solid #333;
            background: #333;
            color: white;
            font-family: 'Courier New', monospace;
            font-size: 12px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 2px;
            cursor: pointer;
            transition: all 0.2s;
        }

        .hero-cta:hover {
            background: white;
            color: #333;
        }

        .hero-indicators {
            position: absolute;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            gap: 10px;
        }

        .indicator {
            width: 12px;
            height: 12px;
            border: 2px solid #333;
            background: white;
            cursor: pointer;
        }

        .indicator.active {
            background: #333;
        }

        /* Section Title */
        .section {
            margin: 40px 20px;
        }

        .section-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 3px solid #333;
        }

        .section-title {
            font-size: 20px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .section-link {
            font-size: 11px;
            text-decoration: none;
            color: #333;
            border-bottom: 2px solid #333;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Category Grid */
        .category-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 20px;
            margin-bottom: 40px;
        }

        @media (max-width: 968px) {
            .category-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        .category-card {
            border: 2px solid #333;
            background: white;
            aspect-ratio: 1;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.2s;
            position: relative;
        }

        .category-card:hover {
            border-width: 3px;
            transform: translateY(-3px);
        }

        .category-icon {
            width: 80px;
            height: 80px;
            border: 2px solid #333;
            background: repeating-linear-gradient(
                90deg,
                #fff,
                #fff 10px,
                #f0f0f0 10px,
                #f0f0f0 20px
            );
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 10px;
            font-weight: bold;
        }

        .category-name {
            font-size: 13px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .category-count {
            font-size: 10px;
            color: #666;
            margin-top: 5px;
        }

        /* Product Grid */
        .product-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 20px;
        }

        @media (max-width: 968px) {
            .product-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        .product-card {
            border: 2px solid #333;
            background: white;
            cursor: pointer;
            transition: all 0.2s;
        }

        .product-card:hover {
            border-width: 3px;
            transform: translateY(-3px);
        }

        .product-image {
            aspect-ratio: 1;
            border-bottom: 2px solid #333;
            display: flex;
            align-items: center;
            justify-content: center;
            background: repeating-linear-gradient(
                45deg,
                #fff,
                #fff 20px,
                #f9f9f9 20px,
                #f9f9f9 40px
            );
            font-size: 11px;
            font-weight: bold;
            color: #999;
            position: relative;
        }

        .product-badge {
            position: absolute;
            top: 10px;
            right: 10px;
            padding: 5px 10px;
            border: 2px solid #333;
            background: white;
            font-size: 9px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .product-info {
            padding: 15px;
        }

        .product-category {
            font-size: 9px;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: #666;
            margin-bottom: 8px;
        }

        .product-name {
            font-size: 12px;
            font-weight: bold;
            margin-bottom: 10px;
            line-height: 1.4;
        }

        .product-price {
            font-size: 16px;
            font-weight: bold;
            margin-bottom: 5px;
        }

        .product-old-price {
            font-size: 12px;
            color: #999;
            text-decoration: line-through;
        }

        .product-actions {
            display: flex;
            gap: 10px;
            margin-top: 12px;
        }

        .product-btn {
            flex: 1;
            padding: 10px;
            border: 2px solid #333;
            background: white;
            font-family: 'Courier New', monospace;
            font-size: 10px;
            font-weight: bold;
            text-transform: uppercase;
            cursor: pointer;
            transition: all 0.2s;
        }

        .product-btn.primary {
            background: #333;
            color: white;
        }

        .product-btn:hover {
            background: #555;
            color: white;
        }

        /* Features Banner */
        .features-banner {
            margin: 40px 20px;
            border: 2px solid #333;
            background: white;
            display: grid;
            grid-template-columns: repeat(4, 1fr);
        }

        @media (max-width: 968px) {
            .features-banner {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        .feature-item {
            padding: 30px 20px;
            text-align: center;
            border-right: 2px solid #333;
        }

        .feature-item:last-child {
            border-right: none;
        }

        .feature-icon {
            width: 50px;
            height: 50px;
            border: 2px solid #333;
            margin: 0 auto 15px;
            background: repeating-linear-gradient(
                45deg,
                transparent,
                transparent 5px,
                #f0f0f0 5px,
                #f0f0f0 10px
            );
        }

        .feature-title {
            font-size: 12px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 5px;
        }

        .feature-desc {
            font-size: 10px;
            color: #666;
        }

        /* Footer */
        .footer {
            margin-top: 60px;
            border-top: 3px solid #333;
            background: white;
            padding: 40px 20px 20px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 40px;
            margin-bottom: 30px;
        }

        @media (max-width: 968px) {
            .footer-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        .footer-column h3 {
            font-size: 12px;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 2px solid #333;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 8px;
            font-size: 11px;
        }

        .footer-links a {
            color: #333;
            text-decoration: none;
            border-bottom: 1px solid transparent;
            transition: border-color 0.2s;
        }

        .footer-links a:hover {
            border-bottom-color: #333;
        }

        .footer-bottom {
            padding-top: 20px;
            border-top: 2px solid #333;
            text-align: center;
            font-size: 10px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Note Box */
        .note-box {
            margin: 40px 20px;
            border: 2px dashed #666;
            padding: 20px;
            background: #fffef0;
            font-size: 11px;
            line-height: 1.6;
        }

        .note-title {
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <div class="header">
        <div class="top-bar">
            <div>📍 ENVIO GRÁTIS PARA PORTUGAL • ENCOMENDAS ACIMA DE €50</div>
            <div>[CONTACTO: +351 XXX XXX XXX]</div>
        </div>
        <div class="main-header">
            <div class="logo">[LOGO]<br/>TECHSTORE</div>
            <div class="search-bar">
                <input type="text" class="search-input" placeholder="Pesquisar produtos, marcas, categorias...">
                <button class="search-btn">🔍 PESQUISAR</button>
            </div>
            <div class="header-actions">
                <div class="header-action">👤 CONTA</div>
                <div class="header-action">🛒 CARRINHO (0)</div>
            </div>
        </div>
        <nav class="main-nav">
            <div class="nav-item">COMPUTADORES</div>
            <div class="nav-item">COMPONENTES</div>
            <div class="nav-item">PERIFÉRICOS</div>
            <div class="nav-item">GAMING</div>
            <div class="nav-item">REDE</div>
            <div class="nav-item">OFERTAS</div>
        </nav>
    </div>

    <div class="container">
        <!-- Hero Banner -->
        <div class="hero">
            <div class="hero-content">
                <div class="hero-tag">[NOVIDADE] PROMOÇÃO DE INVERNO</div>
                <h1 class="hero-title">ATÉ 30% OFF<br/>EM PORTÁTEIS</h1>
                <p class="hero-subtitle">Ofertas exclusivas em computadores de alta performance</p>
                <button class="hero-cta">VER OFERTAS ▶</button>
            </div>
            <div class="hero-indicators">
                <div class="indicator active"></div>
                <div class="indicator"></div>
                <div class="indicator"></div>
            </div>
        </div>

        <!-- Categories Section -->
        <div class="section">
            <div class="section-header">
                <h2 class="section-title">Categorias Populares</h2>
                <a href="#" class="section-link">VER TODAS →</a>
            </div>
            <div class="category-grid">
                <div class="category-card">
                    <div class="category-icon">[ICON]</div>
                    <div class="category-name">PORTÁTEIS</div>
                    <div class="category-count">248 produtos</div>
                </div>
                <div class="category-card">
                    <div class="category-icon">[ICON]</div>
                    <div class="category-name">DESKTOPS</div>
                    <div class="category-count">186 produtos</div>
                </div>
                <div class="category-card">
                    <div class="category-icon">[ICON]</div>
                    <div class="category-name">COMPONENTES</div>
                    <div class="category-count">512 produtos</div>
                </div>
                <div class="category-card">
                    <div class="category-icon">[ICON]</div>
                    <div class="category-name">MONITORES</div>
                    <div class="category-count">94 produtos</div>
                </div>
            </div>
        </div>

        <!-- Featured Products -->
        <div class="section">
            <div class="section-header">
                <h2 class="section-title">Produtos em Destaque</h2>
                <a href="#" class="section-link">VER TODOS →</a>
            </div>
            <div class="product-grid">
                <div class="product-card">
                    <div class="product-image">
                        [PRODUTO]<br/>300x300px
                        <div class="product-badge">-15%</div>
                    </div>
                    <div class="product-info">
                        <div class="product-category">PORTÁTEIS</div>
                        <div class="product-name">Lenovo ThinkPad X1 Carbon Gen 11</div>
                        <div class="product-price">€1.299,00</div>
                        <div class="product-old-price">€1.499,00</div>
                        <div class="product-actions">
                            <button class="product-btn primary">COMPRAR</button>
                            <button class="product-btn">♡</button>
                        </div>
                    </div>
                </div>

                <div class="product-card">
                    <div class="product-image">
                        [PRODUTO]<br/>300x300px
                        <div class="product-badge">NOVO</div>
                    </div>
                    <div class="product-info">
                        <div class="product-category">COMPONENTES</div>
                        <div class="product-name">NVIDIA RTX 4080 Super 16GB</div>
                        <div class="product-price">€1.099,00</div>
                        <div class="product-actions">
                            <button class="product-btn primary">COMPRAR</button>
                            <button class="product-btn">♡</button>
                        </div>
                    </div>
                </div>

                <div class="product-card">
                    <div class="product-image">
                        [PRODUTO]<br/>300x300px
                    </div>
                    <div class="product-info">
                        <div class="product-category">MONITORES</div>
                        <div class="product-name">Dell UltraSharp 27" 4K IPS</div>
                        <div class="product-price">€549,00</div>
                        <div class="product-actions">
                            <button class="product-btn primary">COMPRAR</button>
                            <button class="product-btn">♡</button>
                        </div>
                    </div>
                </div>

                <div class="product-card">
                    <div class="product-image">
                        [PRODUTO]<br/>300x300px
                        <div class="product-badge">TOP</div>
                    </div>
                    <div class="product-info">
                        <div class="product-category">DESKTOPS</div>
                        <div class="product-name">Apple Mac Mini M2 Pro</div>
                        <div class="product-price">€1.449,00</div>
                        <div class="product-actions">
                            <button class="product-btn primary">COMPRAR</button>
                            <button class="product-btn">♡</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Features Banner -->
        <div class="features-banner">
            <div class="feature-item">
                <div class="feature-icon"></div>
                <div class="feature-title">ENVIO RÁPIDO</div>
                <div class="feature-desc">24-48h em Portugal Continental</div>
            </div>
            <div class="feature-item">
                <div class="feature-icon"></div>
                <div class="feature-title">PAGAMENTO SEGURO</div>
                <div class="feature-desc">SSL & métodos certificados</div>
            </div>
            <div class="feature-item">
                <div class="feature-icon"></div>
                <div class="feature-title">GARANTIA 3 ANOS</div>
                <div class="feature-desc">Em produtos selecionados</div>
            </div>
            <div class="feature-item">
                <div class="feature-icon"></div>
                <div class="feature-title">SUPORTE 24/7</div>
                <div class="feature-desc">Assistência técnica dedicada</div>
            </div>
        </div>

        <!-- Technical Note -->
        <div class="note-box">
            <div class="note-title">📋 NOTA TÉCNICA (Wireframe - Página Inicial)</div>
            <p>
                <strong>Estrutura de Conversão:</strong> Layout otimizado para descoberta de produtos através de hierarquia clara: Hero Banner (promoções) → Categorias (navegação rápida) → Produtos Destacados (conversão direta).
            </p>
            <p>
                <strong>Hero Dinâmico:</strong> Banner rotativo configurável via CMS com CTAs para campanhas sazonais e lançamentos de produtos.
            </p>
            <p>
                <strong>Grid Responsivo:</strong> Sistema de grid adaptativo (4 colunas desktop → 2 colunas mobile) garante usabilidade em todos os dispositivos.
            </p>
            <p>
                <strong>Badges Contextuais:</strong> Indicadores visuais ("NOVO", "-15%", "TOP") destacam produtos relevantes e criam urgência de compra.
            </p>
            <p>
                <strong>Trust Elements:</strong> Barra de features (envio, garantia, suporte) reforça confiança e reduz fricção no processo de compra.
            </p>
        </div>
    </div>

    <!-- Footer -->
    <div class="footer">
        <div class="footer-grid">
            <div class="footer-column">
                <h3>Sobre</h3>
                <ul class="footer-links">
                    <li><a href="#">Quem Somos</a></li>
                    <li><a href="#">Carreiras</a></li>
                    <li><a href="#">Imprensa</a></li>
                    <li><a href="#">Blog</a></li>
                </ul>
            </div>
            <div class="footer-column">
                <h3>Apoio ao Cliente</h3>
                <ul class="footer-links">
                    <li><a href="#">Centro de Ajuda</a></li>
                    <li><a href="#">Envios & Devoluções</a></li>
                    <li><a href="#">Garantias</a></li>
                    <li><a href="#">Contactos</a></li>
                </ul>
            </div>
            <div class="footer-column">
                <h3>Informação Legal</h3>
                <ul class="footer-links">
                    <li><a href="#">Termos & Condições</a></li>
                    <li><a href="#">Política de Privacidade</a></li>
                    <li><a href="#">Cookies</a></li>
                    <li><a href="#">Livro de Reclamações</a></li>
                </ul>
            </div>
            <div class="footer-column">
                <h3>Newsletter</h3>
                <ul class="footer-links">
                    <li>[INPUT: EMAIL]</li>
                    <li>[BOTÃO: SUBSCREVER]</li>
                    <li style="margin-top: 15px;">[ÍCONES SOCIAIS]</li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            © 2025 TECHSTORE • TODOS OS DIREITOS RESERVADOS • WIREFRAME LOW-FI
        </div>
    </div>
</body>
</html>
```
