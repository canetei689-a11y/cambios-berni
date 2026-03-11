
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cambios Berni - Casa de Cambios</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: #f0f0f0;
            padding-bottom: 80px;
        }

        /* HEADER */
        header {
            background: #2a2a2a;
            color: white;
            padding: 20px;
            text-align: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.3);
        }

        header h1 {
            font-size: 1.8em;
            font-weight: bold;
            letter-spacing: 1px;
        }

        header p {
            font-size: 0.9em;
            color: #ccc;
            margin-top: 5px;
        }

        .location {
            font-size: 0.8em;
            color: #999;
            margin-top: 8px;
        }

        /* MAIN CONTAINER */
        .container {
            max-width: 600px;
            margin: 20px auto;
            padding: 0 15px;
        }

        /* BOTÓN WHATSAPP PRINCIPAL */
        .whatsapp-btn {
            display: block;
            background: #25D366;
            color: white;
            padding: 16px;
            border-radius: 8px;
            text-align: center;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1em;
            margin-bottom: 20px;
            box-shadow: 0 4px 12px rgba(37, 211, 102, 0.3);
            transition: all 0.3s;
        }

        .whatsapp-btn:hover {
            background: #1fa853;
            box-shadow: 0 6px 16px rgba(37, 211, 102, 0.4);
        }

        /* TABLA DE MONEDAS */
        .rates-table {
            background: white;
            border-radius: 10px;
            padding: 20px;
            margin-bottom: 20px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }

        .rates-table h2 {
            font-size: 1.2em;
            color: #333;
            margin-bottom: 20px;
            text-align: center;
        }

        table {
            width: 100%;
            border-collapse: collapse;
        }

        table thead {
            border-bottom: 2px solid #333;
        }

        table th {
            padding: 12px;
            text-align: center;
            color: #333;
            font-weight: bold;
            font-size: 0.95em;
        }

        table td {
            padding: 15px 12px;
            text-align: center;
            color: #333;
            border-bottom: 1px solid #e0e0e0;
        }

        table tbody tr:hover {
            background: #f9f9f9;
        }

        .flag-img {
            width: 30px;
            height: 20px;
            margin-right: 8px;
            border-radius: 3px;
            vertical-align: middle;
        }

        .currency-name {
            text-align: left;
            display: flex;
            align-items: center;
            justify-content: flex-start;
        }

        .compra {
            color: #27ae60;
            font-weight: bold;
            font-size: 1.05em;
        }

        .venta {
            color: #e74c3c;
            font-weight: bold;
            font-size: 1.05em;
        }

        /* CONVERSOR */
        .converter-section {
            background: white;
            border-radius: 10px;
            padding: 20px;
            margin-bottom: 20px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }

        .converter-section h2 {
            font-size: 1.2em;
            color: #333;
            margin-bottom: 20px;
            text-align: center;
        }

        .converter-form {
            display: grid;
            gap: 15px;
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
            align-items: flex-end;
        }

        .form-group {
            display: flex;
            flex-direction: column;
        }

        .form-group label {
            font-size: 0.9em;
            color: #555;
            margin-bottom: 8px;
            font-weight: bold;
        }

        .form-group input,
        .form-group select {
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 6px;
            font-size: 1em;
            color: #333;
            transition: border-color 0.3s;
        }

        .form-group input:focus,
        .form-group select:focus {
            outline: none;
            border-color: #333;
            box-shadow: 0 0 5px rgba(0,0,0,0.1);
        }

        .result-box {
            background: #2a2a2a;
            color: white;
            padding: 20px;
            border-radius: 8px;
            text-align: center;
            margin: 15px 0;
        }

        .result-label {
            font-size: 0.95em;
            color: #ccc;
            margin-bottom: 8px;
        }

        .result-value {
            font-size: 2em;
            font-weight: bold;
            color: white;
        }

        .calculate-btn {
            width: 100%;
            padding: 14px;
            background: #f0f0f0;
            color: #333;
            border: none;
            border-radius: 6px;
            font-weight: bold;
            font-size: 1em;
            cursor: pointer;
            transition: all 0.3s;
        }

        .calculate-btn:hover {
            background: #e0e0e0;
            box-shadow: 0 4px 12px rgba(0,0,0,0.2);
        }

        /* SECCIÓN ADMIN */
        .admin-section {
            background: white;
            border-radius: 10px;
            padding: 20px;
            margin-bottom: 20px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }

        .admin-section h2 {
            font-size: 1.2em;
            color: #333;
            margin-bottom: 20px;
            text-align: center;
        }

        .admin-form {
            display: grid;
            gap: 15px;
        }

        .admin-form .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
        }

        .admin-btn {
            padding: 12px;
            background: #333;
            color: white;
            border: none;
            border-radius: 6px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
        }

        .admin-btn:hover {
            background: #555;
        }

        /* FOOTER NAVIGATION */
        .footer-nav {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            background: white;
            border-top: 2px solid #ddd;
            display: flex;
            justify-content: space-around;
            align-items: center;
            height: 70px;
            box-shadow: 0 -2px 10px rgba(0,0,0,0.1);
            z-index: 100;
        }

        .nav-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-decoration: none;
            color: #666;
            font-size: 0.75em;
            flex: 1;
            height: 100%;
            justify-content: center;
            transition: all 0.3s;
        }

        .nav-item:hover {
            color: #333;
            background: #f9f9f9;
        }

        .nav-item .icon {
            font-size: 1.8em;
            margin-bottom: 4px;
        }

        @media (max-width: 600px) {
            header h1 {
                font-size: 1.5em;
            }

            .container {
                padding: 0 10px;
            }

            table th, table td {
                padding: 10px 5px;
                font-size: 0.9em;
            }

            .result-value {
                font-size: 1.6em;
            }

            .footer-nav {
                height: 60px;
            }

            .nav-item .icon {
                font-size: 1.5em;
                margin-bottom: 2px;
            }

            .nav-item {
                font-size: 0.65em;
            }

            .flag-img {
                width: 25px;
                height: 17px;
            }
        }
    </style>
</head>
<body>
    <!-- HEADER -->
    <header>
        <h1>CAMBIOS BERNI</h1>
        <p>Compra y Venta de Monedas</p>
        <div class="location">📍 14 de Mayo casi Bertini, Luque - Paraguay</div>
    </header>

    <!-- MAIN CONTENT -->
    <div class="container">
        <!-- BOTÓN WHATSAPP PRINCIPAL -->
        <a href="https://wa.me/59898340843?text=Hola%20Berni%2C%20necesito%20cotizar" class="whatsapp-btn">
            💬 Cotizar por WhatsApp
        </a>

        <!-- TABLA DE TASAS -->
        <div class="rates-table">
            <h2>Monedas Disponibles</h2>
            <table>
                <thead>
                    <tr>
                        <th>Moneda</th>
                        <th>Compra</th>
                        <th>Venta</th>
                    </tr>
                </thead>
                <tbody id="ratesBody">
                    <!-- Se llena con JavaScript -->
                </tbody>
            </table>
        </div>

        <!-- CONVERSOR -->
        <div class="converter-section">
            <h2>Conversor de Monedas</h2>
            <div class="converter-form">
                <div class="form-row">
                    <div class="form-group">
                        <label for="from-currency">Tengo:</label>
                        <select id="from-currency">
                            <option value="usd">USD - Dólar</option>
                            <option value="eur">EUR - Euro</option>
                            <option value="ars">ARS - Peso Argentino</option>
                            <option value="clp">CLP - Peso Chileno</option>
                            <option value="uyu">UYU - Peso Uruguayo</option>
                            <option value="mxn">MXN - Peso Mexicano</option>
                            <option value="pen">PEN - Sol Peruano</option>
                            <option value="brl">BRL - Real Brasileño</option>
                            <option value="oro">ORO - Oro (gramo)</option>
                            <option value="plata">PLATA - Plata (gramo)</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="from-amount">Cantidad:</label>
                        <input type="number" id="from-amount" placeholder="100" step="0.01" value="100">
                    </div>
                </div>

                <div class="form-row">
                    <div class="form-group">
                        <label for="to-currency">Quiero:</label>
                        <select id="to-currency">
                            <option value="usd">USD - Dólar</option>
                            <option value="eur">EUR - Euro</option>
                            <option value="ars">ARS - Peso Argentino</option>
                            <option value="clp">CLP - Peso Chileno</option>
                            <option value="uyu">UYU - Peso Uruguayo</option>
                            <option value="mxn">MXN - Peso Mexicano</option>
                            <option value="pen">PEN - Sol Peruano</option>
                            <option value="brl">BRL - Real Brasileño</option>
                            <option value="oro">ORO - Oro (gramo)</option>
                            <option value="plata">PLATA - Plata (gramo)</option>
                        </select>
                    </div>
                </div>

                <div class="result-box">
                    <div class="result-label">Recibo:</div>
                    <div class="result-value" id="result">0 Gs.</div>
                </div>

                <button class="calculate-btn" onclick="convertirMoneda()">Calcular</button>
            </div>
        </div>

        <!-- SECCIÓN ADMIN -->
        <div class="admin-section">
            <h2>⚙️ Actualizar Precios</h2>
            <div class="admin-form">
                <div class="form-group">
                    <label for="admin-currency">Divisa:</label>
                    <select id="admin-currency">
                        <option value="usd">USD - Dólar</option>
                        <option value="eur">EUR - Euro</option>
                        <option value="ars">ARS - Peso Argentino</option>
                        <option value="clp">CLP - Peso Chileno</option>
                        <option value="uyu">UYU - Peso Uruguayo</option>
                        <option value="mxn">MXN - Peso Mexicano</option>
                        <option value="pen">PEN - Sol Peruano</option>
                        <option value="brl">BRL - Real Brasileño</option>
                        <option value="oro">ORO - Oro (gramo)</option>
                        <option value="plata">PLATA - Plata (gramo)</option>
                    </select>
                </div>

                <div class="form-row">
                    <div class="form-group">
                        <label for="admin-compra">Compra:</label>
                        <input type="text" id="admin-compra" placeholder="7250">
                    </div>
                    <div class="form-group">
                        <label for="admin-venta">Venta:</label>
                        <input type="text" id="admin-venta" placeholder="7350">
                    </div>
                </div>

                <button class="admin-btn" onclick="actualizarPrecio()">Actualizar Precio</button>
            </div>
        </div>
    </div>

    <!-- FOOTER NAVIGATION -->
    <div class="footer-nav">
        <a href="#inicio" class="nav-item">
            <div class="icon">🏠</div>
            <div>Inicio</div>
        </a>
        <a href="#servicios" class="nav-item">
            <div class="icon">💼</div>
            <div>Servicios</div>
        </a>
        <a href="https://wa.me/59898340843" class="nav-item">
            <div class="icon">📞</div>
            <div>Contacto</div>
        </a>
        <a href="#redes" class="nav-item">
            <div class="icon">📱</div>
            <div>Redes</div>
        </a>
    </div>

    <script>
        // DATOS DE DIVISAS CON BANDERAS
        const defaultRates = {
            usd: { 
                compra: 6350, 
                venta: 6520, 
                name: 'USD',
                flag: 'https://flagcdn.com/w40/us.png'
            },
            eur: { 
                compra: 7300, 
                venta: 7700, 
                name: 'EUR',
                flag: 'https://flagcdn.com/w40/eu.png'
            },
            brl: { 
                compra: 1200, 
                venta: 1270, 
                name: 'BRL',
                flag: 'https://flagcdn.com/w40/br.png'
            },
            ars: { 
                compra: 4.20, 
                venta: 4.70, 
                name: 'ARS',
                flag: 'https://flagcdn.com/w40/ar.png'
            },
            clp: { 
                compra: 6, 
                venta: 9, 
                name: 'CLP',
                flag: 'https://flagcdn.com/w40/cl.png'
            },
            uyu: { 
                compra: 100, 
                venta: 210, 
                name: 'UYU',
                flag: 'https://flagcdn.com/w40/uy.png'
            },
            mxn: { 
                compra: 300, 
                venta: 500, 
                name: 'MXN',
                flag: 'https://flagcdn.com/w40/mx.png'
            },
            pen: { 
                compra: 1800, 
                venta: 2150, 
                name: 'PEN',
                flag: 'https://flagcdn.com/w40/pe.png'
            },
            oro: { 
                compra: 500000, 
                venta: 800000, 
                name: 'ORO (g)',
                flag: '✨'
            },
            plata: { 
                compra: 3500, 
                venta: 36000, 
                name: 'PLATA (g)',
                flag: '💎'
            }
        };

        // CARGAR PRECIOS
        function cargarPrecios() {
            const stored = localStorage.getItem('cambiosBerniRates');
            return stored ? JSON.parse(stored) : defaultRates;
        }

        // GUARDAR PRECIOS
        function guardarPrecios(rates) {
            localStorage.setItem('cambiosBerniRates', JSON.stringify(rates));
        }

        // MOSTRAR TABLA DE TASAS
        function mostrarTasas() {
            const rates = cargarPrecios();
            const tbody = document.getElementById('ratesBody');
            tbody.innerHTML = '';

            Object.entries(rates).forEach(([key, value]) => {
                const row = document.createElement('tr');
                let flagHTML = '';
                
                if (value.flag.startsWith('http')) {
                    flagHTML = `<img src="${value.flag}" alt="${value.name}" class="flag-img">`;
                } else {
                    flagHTML = `<span style="font-size: 1.5em; margin-right: 8px;">${value.flag}</span>`;
                }

                row.innerHTML = `
                    <td class="currency-name">
                        ${flagHTML} ${value.name}
                    </td>
                    <td class="compra">${value.compra.toLocaleString('es-ES')}</td>
                    <td class="venta">${value.venta.toLocaleString('es-ES')}</td>
                `;
                tbody.appendChild(row);
            });
        }

        // CONVERTIR MONEDA
        function convertirMoneda() {
            const rates = cargarPrecios();
            const fromCurrency = document.getElementById('from-currency').value;
            const toCurrency = document.getElementById('to-currency').value;
            const amount = parseFloat(document.getElementById('from-amount').value) || 0;

            if (amount <= 0) {
                document.getElementById('result').textContent = '0 Gs.';
                return;
            }

            // Convertir a Guaraní primero, luego a la moneda destino
            const amountInGs = amount * rates[fromCurrency].venta;
            const result = amountInGs / rates[toCurrency].compra;

            document.getElementById('result').textContent = 
                result.toLocaleString('es-ES', { maximumFractionDigits: 2 }) + ' ' + rates[toCurrency].name;
        }

        // ACTUALIZAR PRECIO - FUNCIÓN CORREGIDA
        function actualizarPrecio() {
            const currency = document.getElementById('admin-currency').value;
            const compraText = document.getElementById('admin-compra').value;
            const ventaText = document.getElementById('admin-venta').value;

            // Validación básica
            if (!compraText || !ventaText) {
                alert('❌ Por favor completa los campos de Compra y Venta');
                return;
            }

            // Convertir texto a número (acepta coma o punto)
            const compra = parseFloat(compraText.replace(',', '.'));
            const venta = parseFloat(ventaText.replace(',', '.'));

            // Validación de números
            if (isNaN(compra) || isNaN(venta)) {
                alert('❌ Ingresa números válidos');
                return;
            }

            if (compra <= 0 || venta <= 0) {
                alert('❌ Los precios deben ser mayores a 0');
                return;
            }

            // Actualizar precios
            let rates = cargarPrecios();
            rates[currency].compra = compra;
            rates[currency].venta = venta;
            guardarPrecios(rates);

            alert('✅ Precio actualizado correctamente');
            document.getElementById('admin-compra').value = '';
            document.getElementById('admin-venta').value = '';
            mostrarTasas();
            convertirMoneda();
        }

        // AUTO-CALCULAR
        document.getElementById('from-amount').addEventListener('input', convertirMoneda);
        document.getElementById('from-currency').addEventListener('change', convertirMoneda);
        document.getElementById('to-currency').addEventListener('change', convertirMoneda);

        // INICIALIZAR
        window.addEventListener('DOMContentLoaded', () => {
            mostrarTasas();
            convertirMoneda();
        });
    </script>
</body>
</html>
