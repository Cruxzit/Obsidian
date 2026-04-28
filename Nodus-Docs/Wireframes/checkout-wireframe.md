Esta pagina serve para fazer o pagamento do [[produto-wireframe]] e redireciona para [[home-wireframe]] 

O wireframe de apresentação é este:

ChatGPT

![[Captura de ecrã 2025-12-29, às 23.53.03.png]]

```
<!DOCTYPE html>
<html lang="pt-PT">
<head>
    <meta charset="UTF-8">
    <title>Checkout – Wireframe</title>

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

        /* LAYOUT */
        .checkout-layout {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 24px;
        }

        /* COLUNA ESQUERDA */
        .steps {
            border: 2px solid #000;
            padding: 16px;
            display: flex;
            flex-direction: column;
            gap: 24px;
        }

        .step {
            border: 2px solid #000;
            padding: 12px;
        }

        .step-title {
            font-size: 14px;
            margin-bottom: 8px;
        }

        .step-content {
            border: 2px dashed #000;
            padding: 12px;
            font-size: 13px;
        }

        /* COLUNA DIREITA */
        .summary {
            border: 2px solid #000;
            padding: 16px;
            display: flex;
            flex-direction: column;
            gap: 16px;
            height: fit-content;
        }

        .summary-title {
            font-size: 14px;
            border-bottom: 2px solid #000;
            padding-bottom: 8px;
        }

        .cart-items {
            border: 2px dashed #000;
            padding: 12px;
            font-size: 13px;
        }

        .totals {
            border: 2px dashed #000;
            padding: 12px;
            font-size: 13px;
        }

        .confirm-button {
            border: 2px solid #000;
            padding: 14px;
            text-align: center;
            font-weight: bold;
            opacity: 0.5;
        }

        .note {
            font-size: 12px;
        }

        /* RESPONSIVO */
        @media (max-width: 900px) {
            .checkout-layout {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

<header>
    <h1>Checkout Simplificado</h1>
</header>

<main class="container">

    <section class="checkout-layout">

        <!-- PASSOS -->
        <div class="steps">

            <div class="step">
                <div class="step-title">
                    1. Identificação
                </div>
                <div class="step-content">
                    Login<br>
                    ou<br>
                    Email de convidado
                </div>
            </div>

            <div class="step">
                <div class="step-title">
                    2. Envio
                </div>
                <div class="step-content">
                    Formulário de morada<br>
                    (validação de campos)
                </div>
            </div>

            <div class="step">
                <div class="step-title">
                    3. Pagamento
                </div>
                <div class="step-content">
                    Dados de pagamento<br>
                    (simulação Stripe / PayPal)<br><br>
                    Estado:<br>
                    [ Loader / Processamento ]
                </div>
            </div>

        </div>

        <!-- RESUMO -->
        <aside class="summary">
            <div class="summary-title">
                Resumo da Encomenda
            </div>

            <div class="cart-items">
                Lista de produtos no carrinho<br>
                (quantidade + preço)
            </div>

            <div class="totals">
                Subtotal<br>
                Portes<br>
                <strong>Total a pagar</strong>
            </div>

            <div class="confirm-button">
                CONFIRMAR ENCOMENDA
            </div>

            <div class="note">
                Botão desativado até<br>
                todos os passos estarem válidos
            </div>
        </aside>

    </section>

</main>

</body>
</html>


```


ClaudAI

![[Pasted image 20251229134408.png]]
![[Captura de ecrã 2025-12-29, às 13.44.31.png]]

```
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Checkout - Wireframe</title>
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
            padding: 20px;
        }

        /* Header */
        .checkout-header {
            background: white;
            border: 3px solid #333;
            padding: 20px;
            margin-bottom: 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 18px;
            font-weight: bold;
            letter-spacing: 2px;
            border: 2px solid #333;
            padding: 10px 20px;
        }

        .secure-badge {
            border: 2px solid #333;
            padding: 10px 20px;
            font-size: 11px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
            background: repeating-linear-gradient(
                45deg,
                transparent,
                transparent 5px,
                #f0f0f0 5px,
                #f0f0f0 10px
            );
        }

        /* Progress Steps */
        .progress-steps {
            background: white;
            border: 2px solid #333;
            padding: 25px;
            margin-bottom: 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .step {
            flex: 1;
            text-align: center;
            position: relative;
        }

        .step-number {
            width: 40px;
            height: 40px;
            border: 3px solid #333;
            background: white;
            margin: 0 auto 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 16px;
        }

        .step.active .step-number {
            background: #333;
            color: white;
        }

        .step.completed .step-number {
            background: repeating-linear-gradient(
                45deg,
                #333,
                #333 5px,
                #555 5px,
                #555 10px
            );
            color: white;
        }

        .step-label {
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-weight: bold;
        }

        .step-connector {
            flex: 1;
            height: 3px;
            background: #333;
            margin: 0 10px;
            margin-top: -30px;
        }

        /* Main Grid */
        .checkout-grid {
            display: grid;
            grid-template-columns: 1.5fr 1fr;
            gap: 30px;
        }

        @media (max-width: 968px) {
            .checkout-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Form Section */
        .form-section {
            background: white;
            border: 2px solid #333;
            padding: 25px;
            margin-bottom: 20px;
        }

        .section-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 2px solid #333;
        }

        .section-title {
            font-size: 16px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .section-number {
            width: 30px;
            height: 30px;
            border: 2px solid #333;
            background: #333;
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-label {
            display: block;
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-weight: bold;
            margin-bottom: 8px;
        }

        .form-input {
            width: 100%;
            padding: 12px;
            border: 2px solid #333;
            background: white;
            font-family: 'Courier New', monospace;
            font-size: 12px;
        }

        .form-input:focus {
            outline: none;
            border-width: 3px;
        }

        .form-input.error {
            border-color: #d00;
            background: repeating-linear-gradient(
                45deg,
                transparent,
                transparent 10px,
                #ffe0e0 10px,
                #ffe0e0 11px
            );
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
        }

        .form-row-3 {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 15px;
        }

        .checkbox-group {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-top: 15px;
        }

        .checkbox {
            width: 20px;
            height: 20px;
            border: 2px solid #333;
            cursor: pointer;
        }

        .checkbox-label {
            font-size: 11px;
            cursor: pointer;
        }

        /* Auth Options */
        .auth-options {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            margin-bottom: 25px;
        }

        .auth-btn {
            padding: 15px;
            border: 2px solid #333;
            background: white;
            font-family: 'Courier New', monospace;
            font-size: 11px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
            cursor: pointer;
            transition: all 0.2s;
        }

        .auth-btn:hover,
        .auth-btn.active {
            background: #333;
            color: white;
        }

        .divider {
            text-align: center;
            margin: 25px 0;
            position: relative;
        }

        .divider::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 0;
            right: 0;
            height: 2px;
            background: #333;
        }

        .divider-text {
            background: white;
            padding: 0 15px;
            position: relative;
            font-size: 11px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Payment Methods */
        .payment-methods {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
            margin-bottom: 25px;
        }

        .payment-method {
            aspect-ratio: 2/1;
            border: 2px solid #333;
            background: white;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 10px;
            font-weight: bold;
            transition: all 0.2s;
        }

        .payment-method:hover,
        .payment-method.active {
            border-width: 3px;
            background: repeating-linear-gradient(
                45deg,
                #fff,
                #fff 10px,
                #f0f0f0 10px,
                #f0f0f0 20px
            );
        }

        /* Order Summary */
        .order-summary {
            background: white;
            border: 3px solid #333;
            padding: 25px;
            position: sticky;
            top: 20px;
        }

        .summary-header {
            font-size: 16px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 2px solid #333;
        }

        .cart-item {
            display: flex;
            gap: 15px;
            margin-bottom: 20px;
            padding-bottom: 20px;
            border-bottom: 1px solid #ddd;
        }

        .cart-item:last-child {
            border-bottom: 2px solid #333;
        }

        .item-image {
            width: 80px;
            height: 80px;
            border: 2px solid #333;
            background: repeating-linear-gradient(
                45deg,
                #fff,
                #fff 10px,
                #f9f9f9 10px,
                #f9f9f9 20px
            );
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 9px;
            font-weight: bold;
            color: #999;
        }

        .item-info {
            flex: 1;
        }

        .item-name {
            font-size: 12px;
            font-weight: bold;
            margin-bottom: 5px;
        }

        .item-specs {
            font-size: 10px;
            color: #666;
            margin-bottom: 8px;
        }

        .item-price {
            font-size: 12px;
            font-weight: bold;
        }

        .item-qty {
            font-size: 10px;
            color: #666;
        }

        /* Totals */
        .totals {
            margin-top: 20px;
        }

        .total-row {
            display: flex;
            justify-content: space-between;
            margin-bottom: 12px;
            font-size: 12px;
        }

        .total-row.final {
            margin-top: 15px;
            padding-top: 15px;
            border-top: 2px solid #333;
            font-size: 16px;
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
            margin-top: 20px;
            transition: all 0.2s;
        }

        .cta-button:hover:not(:disabled) {
            background: #555;
        }

        .cta-button:disabled {
            opacity: 0.5;
            cursor: not-allowed;
            background: repeating-linear-gradient(
                45deg,
                #666,
                #666 10px,
                #888 10px,
                #888 20px
            );
        }

        .security-note {
            margin-top: 15px;
            padding: 12px;
            border: 1px dashed #666;
            font-size: 10px;
            text-align: center;
            background: #f9f9f9;
        }

        /* Loading Overlay */
        .loading-overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(255, 255, 255, 0.95);
            z-index: 1000;
            align-items: center;
            justify-content: center;
        }

        .loading-overlay.active {
            display: flex;
        }

        .loading-content {
            text-align: center;
            border: 3px solid #333;
            padding: 40px;
            background: white;
        }

        .loader {
            width: 60px;
            height: 60px;
            border: 4px solid #333;
            margin: 0 auto 20px;
            background: repeating-linear-gradient(
                0deg,
                #333 0px,
                #333 10px,
                white 10px,
                white 20px
            );
            animation: loading 1s linear infinite;
        }

        @keyframes loading {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .loading-text {
            font-size: 14px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 10px;
        }

        .loading-subtext {
            font-size: 11px;
            color: #666;
        }

        /* Note Box */
        .note-box {
            margin: 30px 0;
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
    <div class="container">
        <!-- Header -->
        <div class="checkout-header">
            <div class="logo">[LOGO] TECHSTORE</div>
            <div class="secure-badge">🔒 CHECKOUT SEGURO SSL</div>
        </div>

        <!-- Progress Steps -->
        <div class="progress-steps">
            <div class="step completed">
                <div class="step-number">✓</div>
                <div class="step-label">Carrinho</div>
            </div>
            <div class="step-connector"></div>
            <div class="step active">
                <div class="step-number">1</div>
                <div class="step-label">Identificação</div>
            </div>
            <div class="step-connector"></div>
            <div class="step">
                <div class="step-number">2</div>
                <div class="step-label">Envio</div>
            </div>
            <div class="step-connector"></div>
            <div class="step">
                <div class="step-number">3</div>
                <div class="step-label">Pagamento</div>
            </div>
        </div>

        <!-- Main Grid -->
        <div class="checkout-grid">
            <!-- Left Column: Forms -->
            <div>
                <!-- Step 1: Identification -->
                <div class="form-section">
                    <div class="section-header">
                        <div class="section-title">1. Identificação</div>
                        <div class="section-number">1</div>
                    </div>

                    <div class="auth-options">
                        <button class="auth-btn">JÁ TENHO CONTA</button>
                        <button class="auth-btn active">CONTINUAR COMO CONVIDADO</button>
                    </div>

                    <div class="form-group">
                        <label class="form-label">Email *</label>
                        <input type="email" class="form-input" placeholder="seu@email.com" required>
                    </div>

                    <div class="checkbox-group">
                        <input type="checkbox" class="checkbox" id="newsletter">
                        <label class="checkbox-label" for="newsletter">Quero receber ofertas e novidades por email</label>
                    </div>
                </div>

                <!-- Step 2: Shipping -->
                <div class="form-section">
                    <div class="section-header">
                        <div class="section-title">2. Morada de Envio</div>
                        <div class="section-number">2</div>
                    </div>

                    <div class="form-row">
                        <div class="form-group">
                            <label class="form-label">Nome *</label>
                            <input type="text" class="form-input" placeholder="João" required>
                        </div>
                        <div class="form-group">
                            <label class="form-label">Apelido *</label>
                            <input type="text" class="form-input" placeholder="Silva" required>
                        </div>
                    </div>

                    <div class="form-group">
                        <label class="form-label">Morada *</label>
                        <input type="text" class="form-input" placeholder="Rua, número, andar" required>
                    </div>

                    <div class="form-row">
                        <div class="form-group">
                            <label class="form-label">Cidade *</label>
                            <input type="text" class="form-input" placeholder="Porto" required>
                        </div>
                        <div class="form-group">
                            <label class="form-label">Código Postal *</label>
                            <input type="text" class="form-input" placeholder="4000-000" required>
                        </div>
                    </div>

                    <div class="form-row">
                        <div class="form-group">
                            <label class="form-label">País *</label>
                            <input type="text" class="form-input" value="Portugal" readonly>
                        </div>
                        <div class="form-group">
                            <label class="form-label">Telefone *</label>
                            <input type="tel" class="form-input" placeholder="+351 XXX XXX XXX" required>
                        </div>
                    </div>

                    <div class="checkbox-group">
                        <input type="checkbox" class="checkbox" id="billing">
                        <label class="checkbox-label" for="billing">Morada de faturação é diferente</label>
                    </div>
                </div>

                <!-- Step 3: Payment -->
                <div class="form-section">
                    <div class="section-header">
                        <div class="section-title">3. Método de Pagamento</div>
                        <div class="section-number">3</div>
                    </div>

                    <div class="payment-methods">
                        <div class="payment-method active">
                            [VISA]<br/>CARTÃO
                        </div>
                        <div class="payment-method">
                            [PAYPAL]<br/>LOGO
                        </div>
                        <div class="payment-method">
                            [MB WAY]<br/>LOGO
                        </div>
                    </div>

                    <div class="form-group">
                        <label class="form-label">Número do Cartão *</label>
                        <input type="text" class="form-input" placeholder="XXXX XXXX XXXX XXXX" required>
                    </div>

                    <div class="form-row-3">
                        <div class="form-group">
                            <label class="form-label">Validade *</label>
                            <input type="text" class="form-input" placeholder="MM/AA" required>
                        </div>
                        <div class="form-group">
                            <label class="form-label">CVV *</label>
                            <input type="text" class="form-input" placeholder="XXX" required>
                        </div>
                    </div>

                    <div class="form-group">
                        <label class="form-label">Nome no Cartão *</label>
                        <input type="text" class="form-input" placeholder="JOÃO SILVA" required>
                    </div>
                </div>

                <!-- Technical Note -->
                <div class="note-box">
                    <div class="note-title">📋 NOTA TÉCNICA (Wireframe - Checkout)</div>
                    <p>
                        <strong>Redução de Atrito:</strong> Design one-page permite visão completa do processo. Resumo fixo (sticky) mantém contexto durante preenchimento.
                    </p>
                    <p>
                        <strong>Validação em Tempo Real:</strong> Campos são validados assincronamente. Feedback visual imediato (bordas vermelhas + padrão) reduz erros.
                    </p>
                    <p>
                        <strong>Processamento Assíncrono:</strong> Ao clicar "Confirmar", overlay de loading mascara operações críticas: (1) Validação stock, (2) Bloqueio pessimista de registos (SELECT FOR UPDATE), (3) Integração payment gateway, (4) Criação transacional da encomenda.
                    </p>
                    <p>
                        <strong>Estados do Botão:</strong> CTA desabilitado até validação completa de todos os campos obrigatórios, prevenindo submissões incompletas.
                    </p>
                </div>
            </div>

            <!-- Right Column: Order Summary -->
            <div>
                <div class="order-summary">
                    <div class="summary-header">Resumo da Encomenda</div>

                    <div class="cart-item">
                        <div class="item-image">[IMG]</div>
                        <div class="item-info">
                            <div class="item-name">Lenovo ThinkPad X1 Carbon</div>
                            <div class="item-specs">Intel i7 • 16GB • 512GB SSD</div>
                            <div class="item-price">€1.299,00</div>
                            <div class="item-qty">Quantidade: 1</div>
                        </div>
                    </div>

                    <div class="cart-item">
                        <div class="item-image">[IMG]</div>
                        <div class="item-info">
                            <div class="item-name">Dell UltraSharp 27" 4K</div>
                            <div class="item-specs">IPS • 60Hz • USB-C</div>
                            <div class="item-price">€549,00</div>
                            <div class="item-qty">Quantidade: 1</div>
                        </div>
                    </div>

                    <div class="totals">
                        <div class="total-row">
                            <span>Subtotal:</span>
                            <span>€1.848,00</span>
                        </div>
                        <div class="total-row">
                            <span>Portes de Envio:</span>
                            <span>€0,00</span>
                        </div>
                        <div class="total-row">
                            <span>IVA (23%):</span>
                            <span>€425,04</span>
                        </div>
                        <div class="total-row final">
                            <span>TOTAL A PAGAR:</span>
                            <span>€2.273,04</span>
                        </div>
                    </div>

                    <button class="cta-button" onclick="processOrder()" id="confirmBtn">
                        ▶ CONFIRMAR ENCOMENDA
                    </button>

                    <div class="security-note">
                        🔒 Pagamento processado de forma segura via SSL<br/>
                        Dados encriptados • Stripe/PayPal certificado
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Loading Overlay -->
    <div class="loading-overlay" id="loadingOverlay">
        <div class="loading-content">
            <div class="loader"></div>
            <div class="loading-text">PROCESSANDO ENCOMENDA</div>
            <div class="loading-subtext">
                Validando stock • Processando pagamento<br/>
                Por favor aguarde...
            </div>
        </div>
    </div>

    <script>
        // Simulate form validation
        const inputs = document.querySelectorAll('.form-input');
        const confirmBtn = document.getElementById('confirmBtn');
        
        function validateForm() {
            let allValid = true;
            inputs.forEach(input => {
                if (input.hasAttribute('required') && !input.value) {
                    allValid = false;
                }
            });
            confirmBtn.disabled = !allValid;
        }

        inputs.forEach(input => {
            input.addEventListener('input', validateForm);
        });

        // Initial state
        validateForm();

        // Process order simulation
        function processOrder() {
            const overlay = document.getElementById('loadingOverlay');
            overlay.classList.add('active');
            
            // Simulate async processing
            setTimeout(() => {
                overlay.classList.remove('active');
                alert('✓ ENCOMENDA CONFIRMADA!\n\nNúmero: #1843\nEstado: Pagamento confirmado\nEnvio: 24-48h\n\nReceberá um email de confirmação.');
            }, 3000);
        }
    </script>
</body>
</html>

```
