            box-shadow: 0 8px 24px rgba(0, 0, 0, 0.4), 0 0 20px var(--glow-color);
        }

        [data-theme="dark"][data-performance="modern"] body::before {
            background: radial-gradient(circle at 20% 80%, rgba(59, 130, 246, 0.3) 0%, transparent 50%),
                        radial-gradient(circle at 80% 20%, rgba(16, 185, 129, 0.2) 0%, transparent 50%),
                        radial-gradient(circle at 50% 50%, rgba(139, 92, 246, 0.1) 0%, transparent 70%);
            opacity: 0.4;
        }

        /* Performance Mode - Minimal effects */
        [data-performance="performance"] {
            --animation-duration: 0.05s;
        }

        [data-performance="performance"] * {
            transition-duration: 0.05s !important;
            animation-duration: 0.05s !important;
        }

        [data-performance="performance"] .modern-card {
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
            backdrop-filter: none;
        }

        [data-performance="performance"] .modern-card:hover {
            transform: none;
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
        }

        [data-performance="performance"] .modern-button {
            box-shadow: none;
            background: var(--primary-color);
        }

        [data-performance="performance"] .modern-button:hover {
            transform: none;
            box-shadow: none;
            background: var(--secondary-color);
        }

        [data-performance="performance"] body::before {
            display: none;
        }

        [data-performance="performance"] .bottom-nav {
            backdrop-filter: none;
            background: var(--card-bg);
            border-top: 2px solid var(--border-color);
        }

        [data-performance="performance"] .calendar-day:hover {
            transform: none;
        }

        [data-performance="performance"] .task-indicator:hover {
            transform: none;
        }

        [data-performance="performance"] .bottom-nav-item:hover {
            background: var(--border-color);
        }

        /* Modern Mode - Enhanced visuals */
        [data-performance="modern"] {
            --animation-duration: 0.4s;
        }

        [data-performance="modern"] .modern-card {
            backdrop-filter: blur(15px);
            background: rgba(255, 255, 255, 0.85);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        [data-theme="dark"][data-performance="modern"] .modern-card {
            background: rgba(30, 41, 59, 0.85);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        [data-performance="modern"] .modern-card:hover {
            transform: translateY(-4px) scale(1.02);
            box-shadow: 0 16px 48px rgba(0, 0, 0, 0.15);
        }

        [data-performance="modern"] .modern-button {
            box-shadow: 0 8px 25px var(--shadow-color);
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            position: relative;
            overflow: hidden;
        }

        [data-performance="modern"] .modern-button::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            transition: left 0.6s;
        }

        [data-performance="modern"] .modern-button:hover::before {
            left: 100%;
        }

        [data-performance="modern"] .modern-button:hover {
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 16px 40px var(--shadow-color);
        }

        [data-performance="modern"] .bottom-nav {
            backdrop-filter: blur(25px);
            background: rgba(255, 255, 255, 0.8);
            border-top: 1px solid rgba(255, 255, 255, 0.3);
        }

        [data-theme="dark"][data-performance="modern"] .bottom-nav {
            background: rgba(15, 23, 42, 0.8);
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        [data-performance="modern"] .bottom-nav-item {
            border-radius: 16px;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        [data-performance="modern"] .bottom-nav-item:hover {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            transform: translateY(-2px) scale(1.05);
            box-shadow: 0 8px 20px var(--shadow-color);
        }

        [data-performance="modern"] .calendar-day {
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        [data-performance="modern"] .calendar-day:hover {
            transform: scale(1.05) translateY(-2px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
            z-index: 10;
        }

        [data-performance="modern"] .task-indicator {
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        [data-performance="modern"] .task-indicator:hover {
            transform: translateY(-3px) scale(1.1);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
            z-index: 20;
        }

        [data-performance="modern"] body::before {
            background: radial-gradient(circle at 20% 80%, var(--glow-color) 0%, transparent 50%),
                        radial-gradient(circle at 80% 20%, var(--secondary-color) 0%, transparent 50%);
            opacity: 0.3;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }

        /* Color Palettes */
        [data-theme="palette1"] {
            --bg-color: #F0F8FF;
            --primary-color: #1E90FF;
            --secondary-color: #98FB98;
            --accent-color: #87CEEB;
            --text-color: #2F4F4F;
            --card-bg: #FFFFFF;
            --border-color: #B0E0E6;
            --shadow-color: rgba(30, 144, 255, 0.2);
            --glow-color: rgba(30, 144, 255, 0.4);
        }

        [data-theme="palette2"] {
            --bg-color: #E6F0FA;
            --primary-color: #3CB371;
            --secondary-color: #20B2AA;
            --accent-color: #98FB98;
            --text-color: #006400;
            --card-bg: #FFFFFF;
            --border-color: #90EE90;
            --shadow-color: rgba(60, 179, 113, 0.3);
            --glow-color: rgba(60, 179, 113, 0.5);
        }

        [data-theme="palette3"] {
            --bg-color: #E6E6FA;
            --primary-color: #6A5ACD;
            --secondary-color: #BA55D3;
            --accent-color: #DDA0DD;
            --text-color: #4B0082;
            --card-bg: #FFFFFF;
            --border-color: #D8BFD8;
            --shadow-color: rgba(106, 90, 205, 0.3);
            --glow-color: rgba(106, 90, 205, 0.5);
        }

        [data-theme="palette4"] {
            --bg-color: #FFFACD;
            --primary-color: #FFD700;
            --secondary-color: #FFA500;
            --accent-color: #FFFF99;
            --text-color: #8B4513;
            --card-bg: #FFFFFF;
            --border-color: #F0E68C;
            --shadow-color: rgba(255, 215, 0, 0.3);
            --glow-color: rgba(255, 215, 0, 0.5);
        }

        [data-theme="palette5"] {
            --bg-color: #F5F5F5;
            --primary-color: #FF4500;
            --secondary-color: #2E8B57;
            --accent-color: #FFA07A;
            --text-color: #2F2F2F;
            --card-bg: #FFFFFF;
            --border-color: #D3D3D3;
            --shadow-color: rgba(255, 69, 0, 0.3);
            --glow-color: rgba(255, 69, 0, 0.5);
        }

        /* Font Size Classes */
        .font-size-small {
            --font-size-multiplier: 0.875;
        }

        .font-size-normal {
            --font-size-multiplier: 1;
        }

        .font-size-large {
            --font-size-multiplier: 1.125;
        }

        .font-size-xl {
            --font-size-multiplier: 1.25;
        }

        body {
            font-family: 'Roboto', sans-serif;
            background: linear-gradient(135deg, var(--bg-color) 0%, var(--accent-color) 100%);
            color: var(--text-color);
            transition: all 0.3s ease;
            padding-bottom: 90px;
            position: relative;
            overflow-x: hidden;
            min-height: 100vh;
            font-size: calc(14px * var(--font-size-multiplier));
        }

        /* Optimized animations - reduced for performance */
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 20% 80%, var(--glow-color) 0%, transparent 50%);
            pointer-events: none;
            z-index: -1;
            opacity: 0.2;
        }

        .modern-card {
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            box-shadow: 0 2px 8px var(--shadow-color);
            transition: transform 0.2s ease, box-shadow 0.2s ease;
            position: relative;
            overflow: hidden;
        }

        .modern-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 12px var(--shadow-color);
        }

        .modern-button {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            border: none;
            border-radius: 8px;
            padding: 10px 20px;
            font-weight: 600;
            font-size: calc(14px * var(--font-size-multiplier));
            transition: all 0.2s ease;
            cursor: pointer;
            position: relative;
            overflow: hidden;
            box-shadow: 0 2px 4px var(--shadow-color);
        }

        .modern-button:hover {
            transform: translateY(-1px);
            box-shadow: 0 4px 8px var(--shadow-color);
        }

        .modern-button:active {
            transform: translateY(0);
        }

        .modern-input {
            background: var(--card-bg);
            border: 2px solid var(--border-color);
            border-radius: 12px;
            padding: 14px 16px;
            font-size: calc(14px * var(--font-size-multiplier));
            transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
            width: 100%;
            color: var(--text-color);
            position: relative;
            box-shadow: 
                0 2px 4px rgba(0, 0, 0, 0.05),
                0 1px 2px rgba(0, 0, 0, 0.1);
            font-weight: 500;
        }

        .modern-input:focus {
            outline: none;
            border-color: var(--primary-color);
            box-shadow: 
                0 0 0 3px rgba(59, 130, 246, 0.1),
                0 4px 12px rgba(0, 0, 0, 0.1);
            transform: translateY(-1px);
        }

        .modern-input:hover {
            border-color: var(--primary-color);
            box-shadow: 
                0 4px 8px rgba(0, 0, 0, 0.08),
                0 2px 4px rgba(0, 0, 0, 0.12);
        }

        /* ===== SELECTORES ULTRA MODERNOS PERSONALIZADOS ===== */
        
        /* Ocultar selectores nativos */
        select.modern-input, input[type="date"].modern-input {
            display: none;
        }

        /* Contenedor personalizado para selectores */
        .custom-selector {
            position: relative;
            background: var(--card-bg);
            border-radius: 12px;
            border: 2px solid var(--border-color);
            padding: 12px 16px;
            font-weight: 600;
            font-size: calc(14px * var(--font-size-multiplier));
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
            color: var(--text-color);
            min-height: 48px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .custom-selector .selector-display {
            flex: 1;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .custom-selector .selector-icon {
            font-size: calc(20px * var(--font-size-multiplier));
            transition: all 0.3s ease;
        }

        .custom-selector .selector-text {
            font-weight: 700;
            color: var(--text-color);
        }

        .custom-selector .selector-arrow {
            width: 24px;
            height: 24px;
            background: var(--primary-color);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
        }

        .custom-selector .selector-arrow::after {
            content: '▼';
            color: white;
            font-size: 12px;
            font-weight: bold;
            transition: all 0.3s ease;
        }

        /* Dropdown personalizado */
        .custom-dropdown {
            position: absolute;
            top: 100%;
            left: 0;
            right: 0;
            background: var(--card-bg);
            border: 2px solid var(--primary-color);
            border-radius: 12px;
            margin-top: 4px;
            z-index: 9999;
            opacity: 0;
            visibility: hidden;
            transform: translateY(-10px);
            transition: all 0.3s ease;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
            max-height: 300px;
            overflow-y: auto;
        }

        .custom-dropdown.active {
            opacity: 1;
            visibility: visible;
            transform: translateY(0) scale(1);
        }

        .custom-dropdown-item {
            padding: 16px 24px;
            cursor: pointer;
            transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
            border-bottom: 1px solid rgba(0, 0, 0, 0.05);
            display: flex;
            align-items: center;
            gap: 12px;
            font-weight: 600;
            color: var(--text-color);
        }

        .custom-dropdown-item:first-child {
            border-radius: 17px 17px 0 0;
        }

        .custom-dropdown-item:last-child {
            border-radius: 0 0 17px 17px;
            border-bottom: none;
        }

        .custom-dropdown-item:only-child {
            border-radius: 17px;
        }

        .custom-dropdown-item:hover {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            transform: translateX(8px) scale(1.02);
            box-shadow: 0 8px 25px var(--shadow-color);
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
        }

        .custom-dropdown-item.selected {
            background: linear-gradient(135deg, var(--accent-color) 0%, var(--primary-color) 100%);
            color: white;
            font-weight: 800;
            box-shadow: 0 8px 25px var(--glow-color);
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.4);
        }

        .custom-dropdown-item .item-icon {
            font-size: calc(18px * var(--font-size-multiplier));
            min-width: 24px;
        }

        /* Efectos Hover Simplificados */
        .custom-selector:hover {
            border-color: var(--primary-color);
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.12);
            transform: translateY(-1px);
        }

        .custom-selector:hover .selector-arrow {
            transform: rotate(180deg);
        }

        /* Estado activo (dropdown abierto) */
        .custom-selector.active {
            border-color: var(--primary-color);
            box-shadow: 0 0 0 3px var(--shadow-color);
            z-index: 9998;
            position: relative;
        }

        .custom-selector.active .selector-arrow {
            transform: rotate(180deg);
        }

        /* Calendario personalizado */
        .custom-calendar {
            position: absolute;
            top: 100%;
            left: 0;
            right: 0;
            background: var(--card-bg);
            border: 2px solid var(--primary-color);
            border-radius: 12px;
            margin-top: 4px;
            z-index: 9999;
            opacity: 0;
            visibility: hidden;
            transform: translateY(-10px);
            transition: all 0.3s ease;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
            padding: 16px;
            min-width: 320px;
            width: 320px;
            max-height: 400px;
            overflow: visible;
        }

        .custom-calendar.active {
            opacity: 1;
            visibility: visible;
            transform: translateY(0) scale(1);
        }

        .calendar-header-custom {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding: 0 8px;
        }

        .calendar-nav-custom {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            border: none;
            color: white;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            box-shadow: 0 8px 20px var(--shadow-color);
            font-size: 18px;
            font-weight: bold;
        }

        .calendar-nav-custom:hover {
            transform: scale(1.15) translateY(-2px);
            box-shadow: 0 12px 30px var(--glow-color);
            background: linear-gradient(135deg, var(--accent-color) 0%, var(--primary-color) 100%);
        }

        .calendar-month-custom {
            font-size: calc(18px * var(--font-size-multiplier));
            font-weight: 800;
            color: var(--primary-color);
            text-align: center;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }

        .calendar-grid-custom {
            display: grid;
            grid-template-columns: repeat(7, 1fr);
            gap: 1px;
            background: var(--border-color);
            border-radius: 8px;
            padding: 1px;
            overflow: hidden;
            margin-bottom: 12px;
        }

        .calendar-day-header-custom {
            text-align: center;
            font-weight: 700;
            color: var(--primary-color);
            padding: 8px 4px;
            font-size: calc(12px * var(--font-size-multiplier));
            text-transform: uppercase;
            letter-spacing: 1px;
            background: var(--card-bg);
            border-bottom: 1px solid var(--border-color);
        }

        .calendar-days-container-custom {
            display: grid;
            grid-template-columns: repeat(7, 1fr);
            grid-column: 1 / -1;
            gap: 1px;
        }

        .calendar-day-custom {
            aspect-ratio: 1;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            font-weight: 600;
            font-size: calc(14px * var(--font-size-multiplier));
            transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
            position: relative;
            background: var(--card-bg);
            border: 1px solid transparent;
            min-height: 32px;
        }

        .calendar-day-custom:hover {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            transform: scale(1.1) translateY(-2px);
            box-shadow: 0 8px 20px var(--shadow-color);
            border-color: var(--accent-color);
            text-shadow: 0 1px 2px rgba(0, 0, 0, 0.3);
        }

        .calendar-day-custom.selected {
            background: linear-gradient(135deg, var(--accent-color) 0%, var(--primary-color) 100%);
            color: white;
            transform: scale(1.05);
            box-shadow: 0 12px 30px var(--glow-color);
            border-color: white;
            font-weight: 800;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.4);
        }

        .calendar-day-custom.today {
            background: linear-gradient(135deg, var(--warning-color) 0%, #FFA500 100%);
            color: white;
            font-weight: 800;
            box-shadow: 0 8px 20px rgba(255, 215, 0, 0.4);
            animation: todayPulse 2s ease-in-out infinite;
        }

        .calendar-day-custom.other-month {
            opacity: 0.3;
            color: #999;
        }

        @keyframes todayPulse {
            0%, 100% { 
                box-shadow: 0 8px 20px rgba(255, 215, 0, 0.4);
            }
            50% { 
                box-shadow: 0 12px 30px rgba(255, 215, 0, 0.6);
                transform: scale(1.05);
            }
        }

        /* ===== ESTILOS PARA MODO OSCURO ===== */
        
        [data-theme="dark"] .custom-selector {
            background: var(--card-bg);
            border-color: var(--border-color);
            color: var(--text-color);
            box-shadow: 
                0 8px 25px rgba(0, 0, 0, 0.6),
                0 4px 12px rgba(0, 0, 0, 0.4),
                inset 0 2px 4px rgba(255, 255, 255, 0.08),
                inset 0 -2px 4px rgba(0, 0, 0, 0.3);
        }

        [data-theme="dark"] .custom-selector:hover {
            border-color: var(--primary-color);
            box-shadow: 
                0 15px 40px rgba(0, 0, 0, 0.8),
                0 8px 20px rgba(0, 0, 0, 0.6),
                0 0 0 6px var(--shadow-color),
                inset 0 3px 6px rgba(255, 255, 255, 0.15),
                inset 0 -3px 6px rgba(0, 0, 0, 0.4);
            color: white;
        }

        [data-theme="dark"] .custom-selector.active {
            border-color: var(--accent-color);
            box-shadow: 
                0 20px 50px rgba(0, 0, 0, 0.9),
                0 12px 30px rgba(0, 0, 0, 0.7),
                0 0 0 8px var(--glow-color),
                0 0 0 12px rgba(255, 255, 255, 0.05),
                inset 0 4px 8px rgba(255, 255, 255, 0.2),
                inset 0 -4px 8px rgba(0, 0, 0, 0.5);
            color: white;
        }

        [data-theme="dark"] .custom-dropdown {
            background: var(--card-bg);
            border-color: var(--primary-color);
            box-shadow: 
                0 25px 80px rgba(0, 0, 0, 0.8),
                0 12px 40px rgba(0, 0, 0, 0.6),
                0 0 0 12px var(--shadow-color);
        }

        [data-theme="dark"] .custom-dropdown-item {
            color: var(--text-color);
            border-bottom-color: rgba(255, 255, 255, 0.1);
        }

        [data-theme="dark"] .calendar-day-header-custom {
            color: var(--primary-color);
            background: var(--card-bg);
        }

        [data-theme="dark"] .calendar-month-custom {
            color: var(--primary-color);
        }

        [data-theme="dark"] .calendar-day-custom {
            color: var(--text-color);
            background: var(--card-bg);
        }

        [data-theme="dark"] .calendar-day-custom.other-month {
            color: #666;
        }

        [data-theme="dark"] .custom-dropdown-item:hover {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            box-shadow: 0 8px 20px var(--shadow-color);
        }

        [data-theme="dark"] .custom-dropdown-item.selected {
            background: linear-gradient(135deg, var(--accent-color) 0%, var(--primary-color) 100%);
            color: white;
            box-shadow: 0 8px 25px var(--glow-color);
        }

        [data-theme="dark"] .custom-calendar {
            background: var(--card-bg);
            border-color: var(--primary-color);
            box-shadow: 
                0 25px 80px rgba(0, 0, 0, 0.8),
                0 12px 40px rgba(0, 0, 0, 0.6),
                0 0 0 12px var(--shadow-color);
        }

        /* ===== MODO RENDIMIENTO - Efectos Reducidos ===== */
        
        [data-performance="performance"] .custom-selector {
            transition: all 0.2s ease;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
            background-image: none;
        }

        [data-performance="performance"] .custom-selector:hover {
            transform: none;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
        }

        [data-performance="performance"] .custom-selector.active {
            transform: none;
            box-shadow: 0 0 0 3px var(--shadow-color);
            animation: none;
        }

        [data-performance="performance"] .custom-dropdown {
            backdrop-filter: none;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
        }

        [data-performance="performance"] .custom-calendar {
            backdrop-filter: none;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
        }



        /* Modern Textarea */
        [data-performance="modern"] textarea.modern-input {
            resize: vertical;
            min-height: 80px;
        }

        [data-performance="modern"] textarea.modern-input:focus {
            min-height: 100px;
        }

        /* Logo Styles - Notebook and Pencil */
        .app-logo {
            width: 40px;
            height: 40px;
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            padding: 2px;
        }

        .logo-container {
            position: relative;
            width: 36px;
            height: 36px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        /* Notebook Base */
        .logo-notebook {
            width: 24px;
            height: 30px;
            background: linear-gradient(135deg, #FFFFFF 0%, #F8F9FA 100%);
            border: 2px solid var(--primary-color);
            border-radius: 3px;
            position: relative;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
            z-index: 1;
        }

        /* Notebook Spiral */
        .logo-notebook::before {
            content: '';
            position: absolute;
            left: -3px;
            top: 2px;
            bottom: 2px;
            width: 6px;
            background: repeating-linear-gradient(
                to bottom,
                var(--secondary-color) 0px,
                var(--secondary-color) 2px,
                transparent 2px,
                transparent 4px
            );
            border-radius: 3px;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        /* Notebook Lines */
        .logo-notebook::after {
            content: '';
            position: absolute;
            top: 6px;
            left: 3px;
            right: 3px;
            bottom: 6px;
            background: repeating-linear-gradient(
                to bottom,
                transparent 0px,
                transparent 3px,
                var(--border-color) 3px,
                var(--border-color) 4px
            );
            opacity: 0.6;
        }

        /* Pencil */
        .logo-pencil {
            width: 4px;
            height: 22px;
            background: linear-gradient(to bottom, 
                #FFD700 0%, 
                #FFA500 12%, 
                var(--primary-color) 12%, 
                var(--secondary-color) 35%, 
                var(--primary-color) 35%, 
                var(--primary-color) 70%, 
                #8B4513 70%, 
                #D2691E 85%,
                #654321 100%);
            border-radius: 2px 2px 0 0;
            position: absolute;
            right: -2px;
            top: 2px;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            transform: rotate(15deg);
            box-shadow: 0 2px 6px rgba(0, 0, 0, 0.2);
            z-index: 2;
        }

        /* Pencil Tip */
        .logo-pencil::before {
            content: '';
            position: absolute;
            top: -3px;
            left: -1px;
            width: 6px;
            height: 6px;
            background: linear-gradient(135deg, #FFD700 0%, #FFA500 50%, var(--accent-color) 100%);
            border-radius: 50%;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.3);
        }

        /* Pencil Point */
        .logo-pencil::after {
            content: '';
            position: absolute;
            bottom: -4px;
            left: 1px;
            width: 0;
            height: 0;
            border-left: 1px solid transparent;
            border-right: 1px solid transparent;
            border-top: 4px solid #2C2C2C;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            filter: drop-shadow(0 1px 2px rgba(0, 0, 0, 0.4));
        }

        /* Hover Effects */
        .app-logo:hover .logo-notebook {
            transform: scale(1.05) rotate(-2deg);
            box-shadow: 0 4px 16px rgba(0, 0, 0, 0.25);
            border-color: var(--secondary-color);
        }

        .app-logo:hover .logo-notebook::before {
            background: repeating-linear-gradient(
                to bottom,
                var(--accent-color) 0px,
                var(--accent-color) 2px,
                transparent 2px,
                transparent 4px
            );
        }

        .app-logo:hover .logo-pencil {
            transform: rotate(25deg) scale(1.1);
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
        }

        .app-logo:hover .logo-pencil::before {
            background: linear-gradient(135deg, var(--secondary-color) 0%, var(--primary-color) 50%, var(--accent-color) 100%);
            box-shadow: 0 2px 8px var(--glow-color);
            transform: scale(1.2);
        }

        .app-logo:hover .logo-pencil::after {
            border-top-color: #1a1a1a;
            transform: scale(1.1);
        }

        /* Modern Logo Animations */
        [data-performance="modern"] .app-logo {
            animation: logoFloat 4s ease-in-out infinite;
        }

        [data-performance="modern"] .logo-notebook {
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }

        [data-performance="modern"] .logo-pencil {
            animation: pencilWrite 3s ease-in-out infinite;
        }

        [data-performance="modern"] .app-logo:hover .logo-notebook {
            transform: scale(1.1) rotate(-3deg);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.3);
        }

        [data-performance="modern"] .app-logo:hover .logo-pencil {
            transform: rotate(30deg) scale(1.15);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.4);
        }

        [data-performance="modern"] .app-logo:hover .logo-pencil::before {
            animation: logoGlow 2s ease-in-out infinite alternate;
        }

        @keyframes logoFloat {
            0%, 100% { 
                transform: translateY(0px) rotate(0deg); 
            }
            25% { 
                transform: translateY(-1px) rotate(1deg); 
            }
            50% { 
                transform: translateY(-2px) rotate(0deg); 
            }
            75% { 
                transform: translateY(-1px) rotate(-1deg); 
            }
        }

        @keyframes pencilWrite {
            0%, 100% { 
                transform: rotate(15deg) translateX(0px); 
            }
            25% { 
                transform: rotate(18deg) translateX(1px); 
            }
            50% { 
                transform: rotate(15deg) translateX(0px); 
            }
            75% { 
                transform: rotate(12deg) translateX(-1px); 
            }
        }

        @keyframes logoGlow {
            0%, 100% { 
                box-shadow: 0 2px 8px var(--glow-color); 
            }
            50% { 
                box-shadow: 0 4px 16px var(--glow-color); 
            }
        }

        /* Bottom Navigation - Optimized */
        .bottom-nav {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            background: var(--card-bg);
            border-top: 1px solid var(--border-color);
            padding: 8px 12px 12px;
            z-index: 50;
            box-shadow: 0 -2px 8px var(--shadow-color);
            backdrop-filter: blur(10px);
        }

        .nav-container {
            display: grid;
            grid-template-columns: repeat(7, 1fr);
            gap: 4px;
            max-width: 750px;
            margin: 0 auto;
            align-items: center;
        }

        .bottom-nav-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 8px 4px;
            color: #6B7280;
            transition: all 0.2s ease;
            border-radius: 12px;
            cursor: pointer;
            position: relative;
            text-align: center;
        }

        .bottom-nav-item:hover {
            color: var(--primary-color);
            background: rgba(59, 130, 246, 0.1);
        }

        .bottom-nav-item.active {
            color: var(--primary-color);
            background: rgba(59, 130, 246, 0.1);
        }

        .bottom-nav-item svg {
            margin-bottom: 2px;
        }

        .bottom-nav-item span {
            font-size: calc(10px * var(--font-size-multiplier));
            font-weight: 600;
        }

        /* Calendar Styles - Optimized */
        .calendar-container {
            background: var(--card-bg);
            border-radius: 12px;
            padding: 16px;
            box-shadow: 0 2px 8px var(--shadow-color);
            position: relative;
            overflow: hidden;
        }

        .calendar-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 16px;
        }

        .calendar-nav-btn {
            background: var(--primary-color);
            color: white;
            border: none;
            border-radius: 8px;
            width: 36px;
            height: 36px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.2s ease;
        }

        .calendar-nav-btn:hover {
            background: var(--secondary-color);
        }

        .calendar-grid {
            display: grid;
            grid-template-columns: repeat(7, 1fr);
            gap: 1px;
            background: var(--border-color);
            border-radius: 8px;
            padding: 1px;
            overflow: hidden;
            min-height: 280px;
        }

        .calendar-days-grid {
            display: grid;
            grid-template-columns: repeat(7, 1fr);
            gap: 1px;
            grid-column: 1 / -1;
        }

        .calendar-day-header {
            text-align: center;
            font-weight: 700;
            color: var(--primary-color);
            padding: 12px 4px;
            font-size: calc(12px * var(--font-size-multiplier));
            text-transform: uppercase;
            letter-spacing: 0.5px;
            background: var(--card-bg);
        }

        .calendar-days-container {
            display: contents;
        }

        .calendar-day {
            min-height: 36px;
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            justify-content: flex-start;
            padding: 4px 2px;
            cursor: pointer;
            transition: all 0.2s ease;
            font-size: calc(10px * var(--font-size-multiplier));
            font-weight: 500;
            position: relative;
            background: var(--card-bg);
            border: 1px solid transparent;
        }

        .calendar-day-number {
            font-size: calc(12px * var(--font-size-multiplier));
            font-weight: 600;
            margin-bottom: 2px;
            color: #6B7280;
            width: 16px;
            height: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            transition: all 0.2s ease;
        }

        .calendar-day-content {
            width: 100%;
            flex: 1;
            display: flex;
            flex-direction: column;
            gap: 2px;
        }

        .calendar-day:hover {
            background: #F9FAFB;
            border-color: #E5E7EB;
        }

        .calendar-day:hover .calendar-day-number {
            background: #F3F4F6;
            color: #374151;
        }

        .calendar-day.selected {
            background: #F0F9FF;
            border-color: #3B82F6;
        }

        .calendar-day.selected .calendar-day-number {
            background: #3B82F6;
            color: white;
        }

        .calendar-day.today {
            background: #FFFBEB;
            border-color: #F59E0B;
        }

        .calendar-day.today .calendar-day-number {
            background: #F59E0B;
            color: white;
            font-weight: 700;
        }

        .calendar-day.other-month {
            opacity: 0.4;
            background: #FAFAFA;
        }

        .calendar-day.other-month .calendar-day-number {
            color: #D1D5DB;
        }

        .task-indicator {
            width: 100%;
            height: 10px;
            border-radius: 4px;
            font-size: calc(8px * var(--font-size-multiplier));
            padding: 1px 2px;
            margin-bottom: 1px;
            display: flex;
            align-items: center;
            gap: 1px;
            font-weight: 600;
            color: white;
            text-overflow: ellipsis;
            overflow: hidden;
            white-space: nowrap;
            box-shadow: 0 1px 2px rgba(0, 0, 0, 0.1);
            transition: all 0.2s ease;
        }

        .task-indicator:hover {
            transform: translateY(-1px);
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.15);
        }

        .task-indicator.completed {
            background: var(--success-color);
        }

        .task-indicator.pending {
            background: var(--primary-color);
        }

        .task-indicator.overdue {
            background: var(--danger-color);
        }

        .task-indicator.high-priority {
            background: var(--danger-color);
        }

        .task-indicator.completed::after {
            content: '✓';
            margin-right: 1px;
            font-weight: bold;
            font-size: calc(10px * var(--font-size-multiplier));
        }

        .task-indicator.high-priority::after {
            content: '🔥';
            margin-right: 1px;
        }

        .more-tasks-indicator {
            font-size: calc(8px * var(--font-size-multiplier));
            color: var(--primary-color);
            font-weight: 600;
            text-align: center;
            padding: 1px;
            background: rgba(59, 130, 246, 0.1);
            border-radius: 2px;
            cursor: pointer;
            transition: all 0.2s ease;
        }

        .more-tasks-indicator:hover {
            background: var(--primary-color);
            color: white;
        }

        /* Calendar Tooltip - Simplified */
        .calendar-tooltip {
            position: absolute;
            background: var(--card-bg);
            border: 1px solid var(--primary-color);
            border-radius: 8px;
            padding: 12px;
            box-shadow: 0 4px 12px var(--shadow-color);
            z-index: 1000;
            opacity: 0;
            transform: translateY(10px);
            transition: all 0.2s ease;
            pointer-events: none;
            max-width: 240px;
            min-width: 160px;
        }

        .calendar-tooltip.show {
            opacity: 1;
            transform: translateY(0);
        }

        .calendar-tooltip::before {
            content: '';
            position: absolute;
            top: -6px;
            left: 50%;
            transform: translateX(-50%);
            width: 0;
            height: 0;
            border-left: 6px solid transparent;
            border-right: 6px solid transparent;
            border-bottom: 6px solid var(--primary-color);
        }

        .calendar-tooltip .tooltip-date {
            font-weight: 700;
            font-size: calc(12px * var(--font-size-multiplier));
            color: var(--primary-color);
            margin-bottom: 6px;
            display: flex;
            align-items: center;
            gap: 4px;
        }

        .calendar-tooltip .tooltip-date::before {
            content: '📅';
            font-size: calc(14px * var(--font-size-multiplier));
        }

        .calendar-tooltip .tooltip-task {
            display: flex;
            align-items: center;
            gap: 6px;
            margin-bottom: 4px;
            padding: 4px 6px;
            border-radius: 4px;
            background: rgba(59, 130, 246, 0.05);
            transition: all 0.2s ease;
        }

        .calendar-tooltip .tooltip-task:hover {
            background: rgba(59, 130, 246, 0.1);
        }

        .calendar-tooltip .tooltip-task:last-child {
            margin-bottom: 0;
        }

        .calendar-tooltip .tooltip-more {
            text-align: center;
            font-size: calc(10px * var(--font-size-multiplier));
            color: var(--primary-color);
            font-weight: 600;
            margin-top: 6px;
            padding: 2px 6px;
            background: rgba(59, 130, 246, 0.1);
            border-radius: 8px;
        }

        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0, 0, 0, 0.5);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 1000;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
            backdrop-filter: blur(5px);
        }

        .modal-overlay.active {
            opacity: 1;
            visibility: visible;
        }

        .modal-content {
            background: var(--card-bg);
            border-radius: 12px;
            padding: 24px;
            max-width: 500px;
            width: 90%;
            max-height: 90vh;
            overflow-y: auto;
            transform: scale(0.9);
            transition: all 0.3s ease;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            border: 1px solid var(--border-color);
        }

        .modal-overlay.active .modal-content {
            transform: scale(1);
        }

        /* Delete Confirmation Modal */
        .delete-modal {
            text-align: center;
            max-width: 400px;
        }

        .delete-modal .modal-icon {
            width: 64px;
            height: 64px;
            margin: 0 auto 16px;
            background: linear-gradient(135deg, #FEE2E2 0%, #FECACA 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
        }

        [data-theme="dark"] .delete-modal .modal-icon {
            background: linear-gradient(135deg, #7F1D1D 0%, #991B1B 100%);
        }

        .delete-modal h3 {
            font-size: 18px;
            font-weight: 600;
            margin-bottom: 8px;
            color: var(--text-color);
        }

        .delete-modal p {
            color: #6B7280;
            margin-bottom: 24px;
            font-size: 14px;
        }

        .delete-modal .button-group {
            display: flex;
            gap: 12px;
            justify-content: center;
        }

        .delete-modal .cancel-btn {
            background: var(--card-bg);
            border: 2px solid var(--border-color);
            color: var(--text-color);
            padding: 10px 20px;
            border-radius: 8px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            flex: 1;
        }

        .delete-modal .cancel-btn:hover {
            background: var(--border-color);
            transform: translateY(-1px);
        }

        .delete-modal .confirm-btn {
            background: linear-gradient(135deg, #EF4444 0%, #DC2626 100%);
            border: 2px solid #EF4444;
            color: white;
            padding: 10px 20px;
            border-radius: 8px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            flex: 1;
        }

        .delete-modal .confirm-btn:hover {
            background: linear-gradient(135deg, #DC2626 0%, #B91C1C 100%);
            transform: translateY(-1px);
            box-shadow: 0 4px 12px rgba(239, 68, 68, 0.3);
        }

        /* Modern Modal Effects */
        [data-performance="modern"] .modal-overlay {
            backdrop-filter: blur(15px);
        }

        [data-performance="modern"] .modal-content {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        [data-theme="dark"][data-performance="modern"] .modal-content {
            background: rgba(30, 41, 59, 0.95);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .priority-badge {
            padding: 2px 8px;
            border-radius: 12px;
            font-size: calc(10px * var(--font-size-multiplier));
            font-weight: 500;
        }

        .priority-high {
            background: #FEE2E2;
            color: #DC2626;
        }

        .priority-medium {
            background: #FEF3C7;
            color: #D97706;
        }

        .priority-low {
            background: #D1FAE5;
            color: #059669;
        }

        .tab-content {
            display: none;
        }

        .tab-content.active {
            display: block;
        }

        .chat-container {
            height: 350px;
            display: flex;
            flex-direction: column;
        }

        .chat-messages {
            flex: 1;
            overflow-y: auto;
            padding: 12px;
            border: 1px solid var(--border-color);
            border-radius: 8px;
            margin-bottom: 12px;
            background: var(--bg-color);
        }

        .chat-input-container {
            display: flex;
            gap: 8px;
        }

        .filter-container {
            display: flex;
            gap: 8px;
            margin-bottom: 16px;
            flex-wrap: wrap;
        }

        /* Theme Selector - Optimized */
        .theme-selector {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .theme-option {
            width: 48px;
            height: 48px;
            border-radius: 50%;
            cursor: pointer;
            border: 2px solid transparent;
            transition: all 0.2s ease;
            position: relative;
            overflow: hidden;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
        }

        .theme-option:hover {
            transform: scale(1.1);
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
        }

        .theme-option.active {
            border-color: var(--primary-color);
            box-shadow: 0 4px 12px var(--shadow-color);
            transform: scale(1.05);
        }

        .theme-1 { 
            background: linear-gradient(135deg, #F0F8FF 0%, #1E90FF 50%, #98FB98 100%);
        }
        .theme-2 { 
            background: linear-gradient(135deg, #E6F0FA 0%, #3CB371 50%, #20B2AA 100%);
        }
        .theme-3 { 
            background: linear-gradient(135deg, #E6E6FA 0%, #6A5ACD 50%, #BA55D3 100%);
        }
        .theme-4 { 
            background: linear-gradient(135deg, #FFFACD 0%, #FFD700 50%, #FFA500 100%);
        }
        .theme-5 { 
            background: linear-gradient(135deg, #F5F5F5 0%, #FF4500 50%, #2E8B57 100%);
        }

        /* Font Size Controls */
        .font-size-controls {
            display: flex;
            gap: 8px;
            align-items: center;
            justify-content: center;
            margin-bottom: 16px;
        }

        .font-size-btn {
            padding: 8px 12px;
            border: 1px solid var(--border-color);
            background: var(--card-bg);
            color: var(--text-color);
            border-radius: 6px;
            cursor: pointer;
            transition: all 0.2s ease;
            font-size: calc(12px * var(--font-size-multiplier));
        }

        .font-size-btn:hover {
            background: var(--primary-color);
            color: white;
            border-color: var(--primary-color);
        }

        .font-size-btn.active {
            background: var(--primary-color);
            color: white;
            border-color: var(--primary-color);
        }

        /* Performance Mode Controls */
        .performance-btn {
            border: 2px solid var(--border-color);
            background: var(--card-bg);
            color: var(--text-color);
            cursor: pointer;
        }

        .performance-btn:hover {
            border-color: var(--primary-color);
            background: rgba(59, 130, 246, 0.05);
        }

        .performance-btn.active {
            border-color: var(--primary-color);
            background: var(--primary-color);
            color: white;
        }

        /* Responsive optimizations */
        @media (max-width: 768px) {
            .modal-content {
                padding: 16px;
                margin: 12px;
            }
            
            .filter-container {
                flex-direction: column;
            }

            .bottom-nav-item span {
                font-size: calc(9px * var(--font-size-multiplier));
            }

            .calendar-grid {
                gap: 2px;
                min-height: 200px;
            }

            .calendar-day {
                min-height: 28px;
                font-size: calc(9px * var(--font-size-multiplier));
            }

            .task-indicator {
                height: 8px;
                font-size: calc(7px * var(--font-size-multiplier));
            }

            .theme-option {
                width: 40px;
                height: 40px;
            }
        }

        /* Performance optimizations */
        * {
            box-sizing: border-box;
        }

        .will-change-transform {
            will-change: transform;
        }

        .gpu-accelerated {
            transform: translateZ(0);
        }

        /* Reduce motion for low-end devices */
        @media (prefers-reduced-motion: reduce) {
            * {
                animation-duration: 0.01ms !important;
                animation-iteration-count: 1 !important;
                transition-duration: 0.01ms !important;
            }
        }
    </style>
</head>

<body data-theme="palette1" data-performance="modern" class="font-size-normal">
    <!-- Header with Logo -->
    <header class="modern-card rounded-none border-0 border-b p-4 mb-6">
        <div class="max-w-7xl mx-auto">
            <div class="flex items-center justify-between">
                <div class="flex items-center space-x-3">
                    <div class="app-logo">
                        <div class="logo-container">
                            <div class="logo-notebook"></div>
                            <div class="logo-pencil"></div>
                        </div>
                    </div>
                    <div>
                        <h1 class="text-2xl font-bold" style="color: var(--primary-color)">TaskMaster AI</h1>
                        <p class="text-gray-600 text-xs">Gestión Inteligente de Tareas</p>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <div class="max-w-7xl mx-auto px-3 sm:px-4 lg:px-6">
        
        <!-- Tareas Pendientes Tab -->
        <div id="pendientes-tab" class="tab-content active">
            <div class="modern-card p-4">
                <h2 class="text-xl font-semibold mb-4">Tareas Pendientes</h2>
                
                <div class="filter-container">
                    <!-- Selector de Prioridad Personalizado -->
                    <div class="custom-selector" onclick="toggleDropdown('filterPriority')">
                        <div class="selector-display">
                            <span class="selector-icon">🎯</span>
                            <span class="selector-text" id="filterPriorityText">Todas las prioridades</span>
                        </div>
                        <div class="selector-arrow"></div>
                        <div class="custom-dropdown" id="filterPriorityDropdown">
                            <div class="custom-dropdown-item selected" onclick="selectPriority('all', 'Todas las prioridades', '🎯')">
                                <span class="item-icon">🎯</span>
                                <span>Todas las prioridades</span>
                            </div>
                            <div class="custom-dropdown-item" onclick="selectPriority('high', 'Alta Prioridad', '🔴')">
                                <span class="item-icon">🔴</span>
                                <span>Alta Prioridad</span>
                            </div>
                            <div class="custom-dropdown-item" onclick="selectPriority('medium', 'Media Prioridad', '🟡')">
                                <span class="item-icon">🟡</span>
                                <span>Media Prioridad</span>
                            </div>
                            <div class="custom-dropdown-item" onclick="selectPriority('low', 'Baja Prioridad', '🟢')">
                                <span class="item-icon">🟢</span>
                                <span>Baja Prioridad</span>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Selector de Fecha Personalizado -->
                    <div class="custom-selector" onclick="toggleCalendar('filterDate')">
                        <div class="selector-display">
                            <span class="selector-icon">📅</span>
                            <span class="selector-text" id="filterDateText">Seleccionar fecha</span>
                        </div>
                        <div class="selector-arrow"></div>
                        <div class="custom-calendar" id="filterDateCalendar">
                            <div class="calendar-header-custom">
                                <button class="calendar-nav-custom" onclick="previousMonth('filter'); event.stopPropagation();">‹</button>
                                <div class="calendar-month-custom" id="filterCalendarMonth"></div>
                                <button class="calendar-nav-custom" onclick="nextMonth('filter'); event.stopPropagation();">›</button>
                            </div>
                            <div class="calendar-grid-custom">
                                <div class="calendar-day-header-custom">Dom</div>
                                <div class="calendar-day-header-custom">Lun</div>
                                <div class="calendar-day-header-custom">Mar</div>
                                <div class="calendar-day-header-custom">Mié</div>
                                <div class="calendar-day-header-custom">Jue</div>
                                <div class="calendar-day-header-custom">Vie</div>
                                <div class="calendar-day-header-custom">Sáb</div>
                                <div class="calendar-days-container-custom" id="filterCalendarDays"></div>
                            </div>
                            <div style="text-align: center; margin-top: 12px;">
                                <button class="modern-button" onclick="clearDateFilter(); event.stopPropagation();" style="padding: 8px 16px; font-size: 12px;">
                                    Limpiar Filtro
                                </button>
                            </div>
                        </div>
                    </div>
                    
                    <span class="text-sm text-gray-600 flex items-center">
                        Total: <span id="taskCount" class="font-semibold ml-1" style="color: var(--primary-color)">0</span>
                    </span>
                </div>
                
                <div id="taskList" class="space-y-3">
                    <!-- Tasks will be rendered here -->
                </div>
                
                <div id="emptyState" class="text-center py-12 text-gray-500">
                    <div class="text-4xl mb-3">✅</div>
                    <p class="text-lg mb-2">No hay tareas pendientes</p>
                    <p class="text-sm">¡Excelente trabajo! Todas tus tareas están completadas</p>
                </div>
            </div>
        </div>

        <!-- Chat IA Tab -->
        <div id="chat-tab" class="tab-content">
            <div class="modern-card p-4">
                <h2 class="text-xl font-semibold mb-4">Chat con IA</h2>
                
                <div class="chat-container">
                    <div id="chatMessages" class="chat-messages">
                        <div class="text-center py-6 text-gray-500">
                            <p>🤖 ¡Hola! Soy tu asistente IA. ¿En qué puedo ayudarte hoy?</p>
                        </div>
                    </div>
                    
                    <div class="chat-input-container">
                        <input 
                            type="text" 
                            id="chatInput" 
                            placeholder="Escribe tu mensaje aquí..."
                            class="modern-input flex-1"
                            onkeypress="handleChatKeyPress(event)"
                        >
                        <button onclick="sendChatMessage()" class="modern-button">
                            Enviar
                        </button>
                    </div>
                </div>
            </div>
        </div>

        <!-- Crear Tarea Tab -->
        <div id="crear-tab" class="tab-content">
            <div class="modern-card p-4">
                <h2 class="text-xl font-semibold mb-4">Crear Nueva Tarea</h2>
                
                <form id="createTaskForm" class="space-y-4">
                    <div>
                        <label for="newTaskTitle" class="block text-sm font-medium mb-2">Título de la tarea</label>
                        <input 
                            type="text" 
                            id="newTaskTitle" 
                            placeholder="Ingresa el título de tu tarea"
                            class="modern-input"
                            required
                        >
                    </div>
                    
                    <div>
                        <label class="block text-sm font-medium mb-2">Fecha de vencimiento</label>
                        <!-- Selector de Fecha Personalizado -->
                        <div class="custom-selector" onclick="toggleCalendar('newTaskDate')">
                            <div class="selector-display">
                                <span class="selector-icon">📅</span>
                                <span class="selector-text" id="newTaskDateText">Seleccionar fecha</span>
                            </div>
                            <div class="selector-arrow"></div>
                            <div class="custom-calendar" id="newTaskDateCalendar">
                                <div class="calendar-header-custom">
                                    <button class="calendar-nav-custom" onclick="previousMonth('newTask'); event.stopPropagation();">‹</button>
                                    <div class="calendar-month-custom" id="newTaskCalendarMonth"></div>
                                    <button class="calendar-nav-custom" onclick="nextMonth('newTask'); event.stopPropagation();">›</button>
                                </div>
                                <div class="calendar-grid-custom">
                                    <div class="calendar-day-header-custom">Dom</div>
                                    <div class="calendar-day-header-custom">Lun</div>
                                    <div class="calendar-day-header-custom">Mar</div>
                                    <div class="calendar-day-header-custom">Mié</div>
                                    <div class="calendar-day-header-custom">Jue</div>
                                    <div class="calendar-day-header-custom">Vie</div>
                                    <div class="calendar-day-header-custom">Sáb</div>
                                    <div class="calendar-days-container-custom" id="newTaskCalendarDays"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div>
                        <label class="block text-sm font-medium mb-2">Prioridad</label>
                        <!-- Selector de Prioridad Personalizado -->
                        <div class="custom-selector" onclick="toggleDropdown('newTaskPriority')">
                            <div class="selector-display">
                                <span class="selector-icon">🎯</span>
                                <span class="selector-text" id="newTaskPriorityText">Seleccionar prioridad</span>
                            </div>
                            <div class="selector-arrow"></div>
                            <div class="custom-dropdown" id="newTaskPriorityDropdown">
                                <div class="custom-dropdown-item" onclick="selectNewTaskPriority('high', 'Alta Prioridad', '🔴')">
                                    <span class="item-icon">🔴</span>
                                    <span>Alta Prioridad</span>
                                </div>
                                <div class="custom-dropdown-item" onclick="selectNewTaskPriority('medium', 'Media Prioridad', '🟡')">
                                    <span class="item-icon">🟡</span>
                                    <span>Media Prioridad</span>
                                </div>
                                <div class="custom-dropdown-item" onclick="selectNewTaskPriority('low', 'Baja Prioridad', '🟢')">
                                    <span class="item-icon">🟢</span>
                                    <span>Baja Prioridad</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div>
                        <label class="block text-sm font-medium mb-2">Materia</label>
                        <!-- Selector de Materia Personalizado -->
                        <div class="custom-selector" onclick="toggleDropdown('newTaskSubject')">
                            <div class="selector-display">
                                <span class="selector-icon">📚</span>
                                <span class="selector-text" id="newTaskSubjectText">Seleccionar materia</span>
                            </div>
                            <div class="selector-arrow"></div>
                            <div class="custom-dropdown" id="newTaskSubjectDropdown">
                                <div class="custom-dropdown-item" onclick="selectNewTaskSubject('Matemáticas', 'Matemáticas', '📐')">
                                    <span class="item-icon">📐</span>
                                    <span>Matemáticas</span>
                                </div>
                                <div class="custom-dropdown-item" onclick="selectNewTaskSubject('Lengua y Literatura', 'Lengua y Literatura', '📚')">
                                    <span class="item-icon">📚</span>
                                    <span>Lengua y Literatura</span>
                                </div>
                                <div class="custom-dropdown-item" onclick="selectNewTaskSubject('Inglés', 'Inglés', '🌍')">
                                    <span class="item-icon">🌍</span>
                                    <span>Inglés</span>
                                </div>
                                <div class="custom-dropdown-item" onclick="selectNewTaskSubject('Ciencias Sociales', 'Ciencias Sociales', '🏛️')">
                                    <span class="item-icon">🏛️</span>
                                    <span>Ciencias Sociales</span>
                                </div>
                                <div class="custom-dropdown-item" onclick="selectNewTaskSubject('Ciencias Naturales', 'Ciencias Naturales', '🌿')">
                                    <span class="item-icon">🌿</span>
                                    <span>Ciencias Naturales</span>
                                </div>
                                <div class="custom-dropdown-item" onclick="selectNewTaskSubject('Química', 'Química', '🧪')">
                                    <span class="item-icon">🧪</span>
                                    <span>Química</span>
                                </div>
                                <div class="custom-dropdown-item" onclick="selectNewTaskSubject('Física', 'Física', '⚛️')">
                                    <span class="item-icon">⚛️</span>
                                    <span>Física</span>
                                </div>
                                <div class="custom-dropdown-item" onclick="selectNewTaskSubject('Otro', 'Otro', '📝')">
                                    <span class="item-icon">📝</span>
                                    <span>Otro</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div>
                        <label for="newTaskDescription" class="block text-sm font-medium mb-2">Descripción (opcional)</label>
                        <textarea 
                            id="newTaskDescription" 
                            placeholder="Agrega detalles adicionales sobre tu tarea"
                            rows="3"
                            class="modern-input resize-none"
                        ></textarea>
                    </div>
                    
                    <div class="flex gap-3">
                        <button type="button" onclick="clearCreateForm()" class="modern-button bg-gray-500 hover:bg-gray-600 flex-1">
                            Limpiar
                        </button>
                        <button type="submit" class="modern-button flex-1">
                            Crear Tarea
                        </button>
                    </div>
                </form>
            </div>
        </div>

        <!-- Calendario Tab -->
        <div id="calendario-tab" class="tab-content">
            <div class="modern-card p-4">
                <h2 class="text-xl font-semibold mb-4">Calendario Interactivo</h2>
                
                <div class="calendar-container">
                    <div class="calendar-header">
                        <button onclick="previousCalendarMonth()" class="calendar-nav-btn">
                            <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z"/>
                            </svg>
                        </button>
                        
                        <h3 id="calendarCurrentMonth" class="font-semibold text-lg" style="color: var(--primary-color)"></h3>
                        
                        <button onclick="nextCalendarMonth()" class="calendar-nav-btn">
                            <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"/>
                            </svg>
                        </button>
                    </div>
                    
                    <div class="calendar-grid">
                        <div class="calendar-day-header">Dom</div>
                        <div class="calendar-day-header">Lun</div>
                        <div class="calendar-day-header">Mar</div>
                        <div class="calendar-day-header">Mié</div>
                        <div class="calendar-day-header">Jue</div>
                        <div class="calendar-day-header">Vie</div>
                        <div class="calendar-day-header">Sáb</div>
                        <div class="calendar-days-grid" id="mainCalendarDays"></div>
                    </div>
                </div>
                
                <div id="selectedDateTasks" class="mt-4">
                    <!-- Tasks for selected date will appear here -->
                </div>
            </div>
        </div>

        <!-- Progreso Tab -->
        <div id="progreso-tab" class="tab-content">
            <div class="space-y-4">
                <div class="modern-card p-4">
                    <h2 class="text-xl font-semibold mb-4">📈 Progreso General</h2>
                    
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mb-6">
                        <div class="text-center">
                            <div class="w-20 h-20 mx-auto mb-3 relative">
                                <svg class="w-20 h-20 transform -rotate-90" viewBox="0 0 100 100">
                                    <circle cx="50" cy="50" r="40" stroke="var(--border-color)" stroke-width="6" fill="none"/>
                                    <circle id="progressCircle" cx="50" cy="50" r="40" stroke="var(--success-color)" stroke-width="6" fill="none" 
                                            stroke-dasharray="251.2" stroke-dashoffset="251.2" stroke-linecap="round"/>
                                </svg>
                                <div class="absolute inset-0 flex items-center justify-center">
                                    <span id="circleProgressText" class="text-lg font-bold" style="color: var(--primary-color)">0%</span>
                                </div>
                            </div>
                            <h3 class="font-semibold">Completado</h3>
                            <p class="text-gray-600 text-sm">Tareas finalizadas</p>
                        </div>
                        
                        <div class="text-center">
                            <div class="text-3xl font-bold mb-2" style="color: var(--primary-color)" id="totalTasksCount">0</div>
                            <h3 class="font-semibold">Total Tareas</h3>
                            <p class="text-gray-600 text-sm">Creadas hasta ahora</p>
                        </div>
                        
                        <div class="text-center">
                            <div class="text-3xl font-bold mb-2" style="color: var(--warning-color)" id="streakCount">0</div>
                            <h3 class="font-semibold">Racha Actual</h3>
                            <p class="text-gray-600 text-sm">Días consecutivos</p>
                        </div>
                    </div>
                    
                    <div class="grid grid-cols-2 md:grid-cols-4 gap-3 mb-4">
                        <div class="modern-card p-3 text-center">
                            <div class="text-xl font-bold" style="color: var(--success-color)" id="completedCountProgress">0</div>
                            <div class="text-xs text-gray-600">Completadas</div>
                        </div>
                        <div class="modern-card p-3 text-center">
                            <div class="text-xl font-bold" style="color: var(--warning-color)" id="pendingCountProgress">0</div>
                            <div class="text-xs text-gray-600">Pendientes</div>
                        </div>
                        <div class="modern-card p-3 text-center">
                            <div class="text-xl font-bold" style="color: var(--danger-color)" id="highPriorityCountProgress">0</div>
                            <div class="text-xs text-gray-600">Alta Prioridad</div>
                        </div>
                        <div class="modern-card p-3 text-center">
                            <div class="text-xl font-bold" style="color: var(--overdue-color)" id="overdueCountProgress">0</div>
                            <div class="text-xs text-gray-600">Vencidas</div>
                        </div>
                    </div>
                    
                    <div class="space-y-3">
                        <div>
                            <div class="flex justify-between items-center mb-1">
                                <span class="text-sm font-medium">Progreso Semanal</span>
                                <span class="text-sm" style="color: var(--primary-color)" id="weeklyProgressText">0%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-2">
                                <div id="weeklyProgressBar" class="h-2 rounded-full transition-all duration-300" style="background: var(--primary-color); width: 0%"></div>
                            </div>
                        </div>
                        
                        <div>
                            <div class="flex justify-between items-center mb-1">
                                <span class="text-sm font-medium">Productividad</span>
                                <span class="text-sm" style="color: var(--success-color)" id="productivityText">0%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-2">
                                <div id="productivityBar" class="h-2 rounded-full transition-all duration-300" style="background: var(--success-color); width: 0%"></div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="modern-card p-4">
                    <h3 class="text-lg font-semibold mb-3">🏆 Logros Recientes</h3>
                    <div id="achievementsList" class="space-y-2">
                        <!-- Achievements will be populated here -->
                    </div>
                </div>
            </div>
        </div>

        <!-- Estadísticas Tab -->
        <div id="estadisticas-tab" class="tab-content">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-4">
                <div class="modern-card p-4">
                    <h3 class="text-lg font-semibold mb-3">📊 Progreso Semanal</h3>
                    <canvas id="weeklyChart" width="400" height="200"></canvas>
                </div>
                
                <div class="modern-card p-4">
                    <h3 class="text-lg font-semibold mb-3">🎯 Por Prioridad</h3>
                    <canvas id="priorityChart" width="400" height="200"></canvas>
                </div>
                
                <div class="modern-card p-4 lg:col-span-2">
                    <h3 class="text-lg font-semibold mb-3">📈 Estadísticas Generales</h3>
                    <div class="grid grid-cols-2 md:grid-cols-4 gap-3">
                        <div class="text-center">
                            <div class="text-xl font-bold text-green-600" id="completedCount">0</div>
                            <div class="text-xs text-gray-600">Completadas</div>
                        </div>
                        <div class="text-center">
                            <div class="text-xl font-bold text-yellow-600" id="pendingCount">0</div>
                            <div class="text-xs text-gray-600">Pendientes</div>
                        </div>
                        <div class="text-center">
                            <div class="text-xl font-bold text-red-600" id="highPriorityCount">0</div>
                            <div class="text-xs text-gray-600">Alta Prioridad</div>
                        </div>
                        <div class="text-center">
                            <div class="text-xl font-bold" style="color: var(--primary-color)" id="progressPercentage">0%</div>
                            <div class="text-xs text-gray-600">Progreso</div>
                        </div>
                    </div>
                    
                    <div class="mt-4">
                        <div class="w-full bg-gray-200 rounded-full h-2">
                            <div id="progressBar" class="h-2 rounded-full transition-all duration-300" style="background: var(--primary-color); width: 0%"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Ajustes Tab -->
        <div id="ajustes-tab" class="tab-content">
            <div class="modern-card p-4 max-w-2xl mx-auto">
                <h2 class="text-xl font-semibold mb-4">Configuración</h2>
                
                <div class="space-y-6">
                    <div>
                        <h3 class="text-lg font-medium mb-3">📱 Tamaño de Fuente</h3>
                        <div class="font-size-controls">
                            <button class="font-size-btn" onclick="changeFontSize('small')">Pequeña</button>
                            <button class="font-size-btn active" onclick="changeFontSize('normal')">Normal</button>
                            <button class="font-size-btn" onclick="changeFontSize('large')">Grande</button>
                            <button class="font-size-btn" onclick="changeFontSize('xl')">Muy Grande</button>
                        </div>
                        <p class="text-sm text-gray-600 text-center">Ajusta el tamaño del texto según tu preferencia</p>
                    </div>
                    
                    <div>
                        <h3 class="text-lg font-medium mb-3">🎨 Paletas de Colores</h3>
                        <div class="theme-selector mb-3">
                            <div class="theme-option theme-1 active" onclick="changeTheme('palette1')" title="Azul Océano"></div>
                            <div class="theme-option theme-2" onclick="changeTheme('palette2')" title="Verde Natura"></div>
                            <div class="theme-option theme-3" onclick="changeTheme('palette3')" title="Púrpura Elegante"></div>
                            <div class="theme-option theme-4" onclick="changeTheme('palette4')" title="Dorado Solar"></div>
                            <div class="theme-option theme-5" onclick="changeTheme('palette5')" title="Tierra Cálida"></div>
                        </div>
                        <p class="text-sm text-gray-600 text-center">Selecciona tu paleta de colores favorita</p>
                    </div>
                    
                    <div>
                        <h3 class="text-lg font-medium mb-3">🌙 Modo Oscuro</h3>
                        <div class="flex gap-3 mb-3">
                            <button class="performance-btn flex-1 p-3 border rounded-lg text-center transition-all active" onclick="toggleDarkMode(false)" data-dark="light">
                                <div class="text-lg mb-1">☀️</div>
                                <div class="font-semibold text-sm">Modo Claro</div>
                                <div class="text-xs text-gray-600">Interfaz brillante y clara</div>
                            </button>
                            <button class="performance-btn flex-1 p-3 border rounded-lg text-center transition-all" onclick="toggleDarkMode(true)" data-dark="dark">
                                <div class="text-lg mb-1">🌙</div>
                                <div class="font-semibold text-sm">Modo Oscuro</div>
                                <div class="text-xs text-gray-600">Interfaz oscura y moderna</div>
                            </button>
                        </div>
                        <p class="text-sm text-gray-600 text-center">Cambia entre modo claro y oscuro</p>
                    </div>
                    
                    <div>
                        <h3 class="text-lg font-medium mb-3">⚡ Modo de Rendimiento</h3>
                        <div class="space-y-3 mb-4">
                            <div class="flex gap-3">
                                <button class="performance-btn flex-1 p-3 border rounded-lg text-center transition-all" onclick="changePerformanceMode('performance')" data-mode="performance">
                                    <div class="text-lg mb-1">🚀</div>
                                    <div class="font-semibold text-sm">Rendimiento</div>
                                    <div class="text-xs text-gray-600">Menos recursos, más velocidad</div>
                                </button>
                                <button class="performance-btn flex-1 p-3 border rounded-lg text-center transition-all active" onclick="changePerformanceMode('modern')" data-mode="modern">
                                    <div class="text-lg mb-1">✨</div>
                                    <div class="font-semibold text-sm">Moderno</div>
                                    <div class="text-xs text-gray-600">Efectos visuales mejorados</div>
                                </button>
                            </div>
                        </div>
                        <p class="text-sm text-gray-600 text-center mb-4">El modo rendimiento es ideal para dispositivos más lentos</p>
                    </div>
                    
                    <div>
                        <h3 class="text-lg font-medium mb-3">🔧 Preferencias</h3>
                        <div class="space-y-3">
                            <label class="flex items-center justify-between">
                                <span>Animaciones suaves</span>
                                <input type="checkbox" checked class="w-4 h-4 rounded" style="accent-color: var(--primary-color)">
                            </label>
                            <label class="flex items-center justify-between">
                                <span>Notificaciones</span>
                                <input type="checkbox" checked class="w-4 h-4 rounded" style="accent-color: var(--primary-color)">
                            </label>
                            <label class="flex items-center justify-between">
                                <span>Recordatorios automáticos</span>
                                <input type="checkbox" class="w-4 h-4 rounded" style="accent-color: var(--primary-color)">
                            </label>
                        </div>
                    </div>
                    
                    <div class="pt-3 border-t border-gray-200">
                        <button onclick="resetApp()" class="modern-button bg-red-500 hover:bg-red-600 w-full">
                            🔄 Restablecer Aplicación
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Bottom Navigation Bar -->
    <nav class="bottom-nav">
        <div class="nav-container">
            <button onclick="switchTab('pendientes')" class="bottom-nav-item active" data-tab="pendientes">
                <svg class="w-4 h-4 mb-1" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"/>
                </svg>
                <span class="text-xs font-medium">Pendientes</span>
            </button>
            
            <button onclick="switchTab('chat')" class="bottom-nav-item" data-tab="chat">
                <svg class="w-4 h-4 mb-1" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"/>
                </svg>
                <span class="text-xs font-medium">Chat IA</span>
            </button>
            
            <button onclick="switchTab('progreso')" class="bottom-nav-item" data-tab="progreso">
                <svg class="w-4 h-4 mb-1" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M13 7h8m0 0v8m0-8l-8 8-4-4-6 6"/>
                </svg>
                <span class="text-xs font-medium">Progreso</span>
            </button>
            
            <button onclick="switchTab('crear')" class="bottom-nav-item" data-tab="crear">
                <svg class="w-4 h-4 mb-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4v16m8-8H4"/>
                </svg>
                <span class="text-xs font-medium">Crear</span>
            </button>
            
            <button onclick="switchTab('calendario')" class="bottom-nav-item" data-tab="calendario">
                <svg class="w-4 h-4 mb-1" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M8 7V3a1 1 0 012 0v4h4V3a1 1 0 012 0v4h2a3 3 0 013 3v8a3 3 0 01-3 3H6a3 3 0 01-3-3v-8a3 3 0 013-3h2zM6 9a1 1 0 00-1 1v8a1 1 0 001 1h12a1 1 0 001-1v-8a1 1 0 00-1-1H6z"/>
                </svg>
                <span class="text-xs font-medium">Calendario</span>
            </button>
            
            <button onclick="switchTab('estadisticas')" class="bottom-nav-item" data-tab="estadisticas">
                <svg class="w-4 h-4 mb-1" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z"/>
                </svg>
                <span class="text-xs font-medium">Estadísticas</span>
            </button>
            
            <button onclick="switchTab('ajustes')" class="bottom-nav-item" data-tab="ajustes">
                <svg class="w-4 h-4 mb-1" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"/>
                    <path d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"/>
                </svg>
                <span class="text-xs font-medium">Ajustes</span>
            </button>
        </div>
    </nav>

    <!-- Calendar Tooltip -->
    <div id="calendarTooltip" class="calendar-tooltip"></div>

    <!-- Delete Confirmation Modal -->
    <div id="deleteModal" class="modal-overlay">
        <div class="modal-content delete-modal">
            <div class="modal-icon">🗑️</div>
            <h3>¿Eliminar tarea?</h3>
            <p id="deleteTaskTitle">¿Estás seguro de que deseas eliminar esta tarea? Esta acción no se puede deshacer.</p>
            <div class="button-group">
                <button class="cancel-btn" onclick="closeDeleteModal()">Cancelar</button>
                <button class="confirm-btn" onclick="confirmDeleteTask()">Eliminar</button>
            </div>
        </div>
    </div>

    <!-- Reset App Confirmation Modal -->
    <div id="resetModal" class="modal-overlay">
        <div class="modal-content delete-modal">
            <div class="modal-icon">🔄</div>
            <h3>¿Restablecer aplicación?</h3>
            <p>¿Estás seguro de que quieres restablecer toda la aplicación? Esto eliminará todas tus tareas, chat y configuraciones. Esta acción no se puede deshacer.</p>
            <div class="button-group">
                <button class="cancel-btn" onclick="closeResetModal()">Cancelar</button>
                <button class="confirm-btn" onclick="confirmResetApp()">Confirmar</button>
            </div>
        </div>
    </div>

    <script>
        // Global variables
        let tasks = JSON.parse(localStorage.getItem('taskmaster_tasks')) || [];
        let taskIdCounter = parseInt(localStorage.getItem('taskmaster_counter')) || 1;
        let chatMessages = JSON.parse(localStorage.getItem('taskmaster_chat')) || [];
        let currentDate = new Date();
        let calendarDate = new Date();
        let selectedDate = new Date();

        // Performance optimization: Debounce function
        function debounce(func, wait) {
            let timeout;
            return function executedFunction(...args) {
                const later = () => {
                    clearTimeout(timeout);
                    func.apply(this, args);
                };
                clearTimeout(timeout);
                timeout = setTimeout(later, wait);
            };
        }

        // Initialize app
        document.addEventListener('DOMContentLoaded', function() {
            // Initialize calendar dates
            filterCalendarDate = new Date();
            newTaskCalendarDate = new Date();
            
            // Load saved preferences
            loadSavedPreferences();
            
            // Initialize UI
            renderTasks();
            updateStatistics();
            updateProgressTab();
            renderChatMessages();
            drawCharts();
            renderMainCalendar();
            setDefaultDate();
            
            // Add form listener
            document.getElementById('createTaskForm').addEventListener('submit', function(e) {
                e.preventDefault();
                createNewTask();
            });

            // Optimize for low-end devices
            if (navigator.hardwareConcurrency && navigator.hardwareConcurrency <= 2) {
                document.body.classList.add('low-end-device');
                // Reduce animations and effects for low-end devices
                document.documentElement.style.setProperty('--animation-duration', '0.1s');
            }
        });

        // Load saved preferences - Updated
        function loadSavedPreferences() {
            const savedPalette = localStorage.getItem('taskmaster_color_palette') || 'palette1';
            const savedDarkMode = localStorage.getItem('taskmaster_dark_mode') === 'true';
            const savedFontSize = localStorage.getItem('taskmaster_font_size') || 'normal';
            const savedPerformance = localStorage.getItem('taskmaster_performance') || 'modern';
            
            // Load theme/palette
            if (savedDarkMode) {
                toggleDarkMode(true);
            } else {
                changeTheme(savedPalette);
            }
            
            // Always update theme selector to show current palette
            changeTheme(savedPalette);
            
            changeFontSize(savedFontSize);
            changePerformanceMode(savedPerformance);
        }

        // Font size management
        function changeFontSize(size) {
            // Remove all font size classes
            document.body.classList.remove('font-size-small', 'font-size-normal', 'font-size-large', 'font-size-xl');
            
            // Add new font size class
            document.body.classList.add(`font-size-${size}`);
            
            // Update active button
            document.querySelectorAll('.font-size-btn').forEach(btn => {
                btn.classList.remove('active');
            });
            
            // Find the button that was clicked
            const clickedBtn = Array.from(document.querySelectorAll('.font-size-btn')).find(btn => 
                btn.textContent.toLowerCase().includes(size === 'xl' ? 'muy grande' : size === 'large' ? 'grande' : size === 'small' ? 'pequeña' : 'normal')
            );
            if (clickedBtn) {
                clickedBtn.classList.add('active');
            }
            
            // Save preference
            localStorage.setItem('taskmaster_font_size', size);
        }

        // Navigation functions
        function switchTab(tabName) {
            // Remove active class from all tabs and nav items
            document.querySelectorAll('.tab-content').forEach(tab => {
                tab.classList.remove('active');
            });
            
            document.querySelectorAll('.bottom-nav-item').forEach(item => {
                item.classList.remove('active');
            });
            
            // Add active class to selected tab and nav item
            const targetTab = document.getElementById(`${tabName}-tab`);
            if (targetTab) {
                targetTab.classList.add('active');
            }
            
            const navItem = document.querySelector(`[data-tab="${tabName}"]`);
            if (navItem) {
                navItem.classList.add('active');
            }

            // Update charts if switching to statistics
            if (tabName === 'estadisticas') {
                setTimeout(drawCharts, 100);
            }
        }

        // Calendar rendering - FIXED for proper 7-column layout
        function renderMainCalendar() {
            const monthNames = [
                'Enero', 'Febrero', 'Marzo', 'Abril', 'Mayo', 'Junio',
                'Julio', 'Agosto', 'Septiembre', 'Octubre', 'Noviembre', 'Diciembre'
            ];
            
            document.getElementById('calendarCurrentMonth').textContent = 
                `${monthNames[calendarDate.getMonth()]} ${calendarDate.getFullYear()}`;
            
            const year = calendarDate.getFullYear();
            const month = calendarDate.getMonth();
            
            // Obtener el primer día del mes y calcular desde qué domingo empezar
            const firstDayOfMonth = new Date(year, month, 1);
            const lastDayOfMonth = new Date(year, month + 1, 0);
            
            // Calcular el primer domingo a mostrar
            const startDate = new Date(firstDayOfMonth);
            startDate.setDate(firstDayOfMonth.getDate() - firstDayOfMonth.getDay());
            
            const calendarDays = document.getElementById('mainCalendarDays');
            calendarDays.innerHTML = '';
            
            // Crear exactamente 42 días (6 semanas × 7 días) para mantener la estructura
            for (let i = 0; i < 42; i++) {
                const currentDate = new Date(startDate);
                currentDate.setDate(startDate.getDate() + i);
                
                const dayElement = document.createElement('div');
                dayElement.className = 'calendar-day';
                
                const dayNumber = document.createElement('div');
                dayNumber.className = 'calendar-day-number';
                dayNumber.textContent = currentDate.getDate();
                
                const dayContent = document.createElement('div');
                dayContent.className = 'calendar-day-content';
                
                dayElement.appendChild(dayNumber);
                dayElement.appendChild(dayContent);
                
                // Marcar días de otros meses
                if (currentDate.getMonth() !== month) {
                    dayElement.classList.add('other-month');
                }
                
                // Marcar día actual
                if (isToday(currentDate)) {
                    dayElement.classList.add('today');
                }
                
                // Marcar día seleccionado
                if (isSameDay(currentDate, selectedDate)) {
                    dayElement.classList.add('selected');
                }
                
                // Agregar indicadores de tareas
                const tasksForDate = getTasksForDate(currentDate);
                renderTaskIndicators(dayContent, tasksForDate);
                
                // Agregar event listeners
                dayElement.addEventListener('mouseenter', (e) => showCalendarTooltip(e, currentDate));
                dayElement.addEventListener('mouseleave', hideCalendarTooltip);
                dayElement.addEventListener('click', () => selectCalendarDate(currentDate));
                
                calendarDays.appendChild(dayElement);
            }
        }

        function renderTaskIndicators(container, tasks) {
            const maxVisible = 2; // Reduced for mobile optimization
            const visibleTasks = tasks.slice(0, maxVisible);
            
            visibleTasks.forEach(task => {
                const indicator = document.createElement('div');
                indicator.className = 'task-indicator';
                
                if (task.completed) {
                    indicator.classList.add('completed');
                } else if (isOverdue(task.date)) {
                    indicator.classList.add('overdue');
                } else if (task.priority === 'high') {
                    indicator.classList.add('high-priority');
                } else {
                    indicator.classList.add('pending');
                }
                
                indicator.textContent = task.title;
                container.appendChild(indicator);
            });
            
            if (tasks.length > maxVisible) {
                const moreIndicator = document.createElement('div');
                moreIndicator.className = 'more-tasks-indicator';
                moreIndicator.textContent = `+${tasks.length - maxVisible}`;
                container.appendChild(moreIndicator);
            }
        }

        // Calendar navigation
        function previousCalendarMonth() {
            calendarDate.setMonth(calendarDate.getMonth() - 1);
            renderMainCalendar();
        }

        function nextCalendarMonth() {
            calendarDate.setMonth(calendarDate.getMonth() + 1);
            renderMainCalendar();
        }

        function selectCalendarDate(date) {
            selectedDate = new Date(date);
            renderMainCalendar();
            showTasksForDate(date);
        }

        function showTasksForDate(date) {
            const tasksForDate = getTasksForDate(date);
            const container = document.getElementById('selectedDateTasks');
            
            if (tasksForDate.length === 0) {
                container.innerHTML = `
                    <div class="modern-card p-4 text-center">
                        <div class="text-3xl mb-3">📅</div>
                        <h3 class="text-lg font-semibold mb-2">No hay tareas para ${formatDate(date)}</h3>
                        <p class="text-gray-600">¡Perfecto! Este día está libre.</p>
                    </div>
                `;
                return;
            }
            
            container.innerHTML = `
                <div class="modern-card p-4">
                    <h3 class="text-lg font-semibold mb-3">Tareas para ${formatDate(date)}</h3>
                    <div class="space-y-2">
                        ${tasksForDate.map(task => `
                            <div class="flex items-center justify-between p-2 bg-gray-50 rounded-lg">
                                <div class="flex items-center gap-2">
                                    <input type="checkbox" ${task.completed ? 'checked' : ''} 
                                           onchange="toggleTask(${task.id})" 
                                           class="w-4 h-4 rounded">
                                    <div>
                                        <div class="font-medium ${task.completed ? 'line-through text-gray-500' : ''}">${task.title}</div>
                                        <div class="text-xs text-gray-600">${task.subject}</div>
                                    </div>
                                </div>
                                <div class="flex items-center gap-2">
                                    <span class="priority-badge priority-${task.priority}">
                                        ${task.priority === 'high' ? '🔴' : task.priority === 'medium' ? '🟡' : '🟢'}
                                    </span>
                                    <button onclick="deleteTask(${task.id})" class="text-red-500 hover:text-red-700">
                                        <svg class="w-3 h-3" fill="currentColor" viewBox="0 0 20 20">
                                            <path d="M9 2a1 1 0 000 2h2a1 1 0 100-2H9z"/>
                                            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zM8.707 7.293a1 1 0 00-1.414 1.414L8.586 10l-1.293 1.293a1 1 0 101.414 1.414L10 11.414l1.293 1.293a1 1 0 001.414-1.414L11.414 10l1.293-1.293a1 1 0 00-1.414-1.414L10 8.586 8.707 7.293z" clip-rule="evenodd"/>
                                        </svg>
                                    </button>
                                </div>
                            </div>
                        `).join('')}
                    </div>
                </div>
            `;
        }

        // Calendar tooltip - Fixed
        function showCalendarTooltip(event, date) {
            const tasksForDate = getTasksForDate(date);
            if (tasksForDate.length === 0) return;
            
            const tooltip = document.getElementById('calendarTooltip');
            const maxTasks = 3;
            const visibleTasks = tasksForDate.slice(0, maxTasks);
            
            tooltip.innerHTML = `
                <div class="tooltip-date">${formatDate(date)}</div>
                ${visibleTasks.map(task => `
                    <div class="tooltip-task">
                        <span class="priority-badge priority-${task.priority}">
                            ${task.priority === 'high' ? '🔴' : task.priority === 'medium' ? '🟡' : '🟢'}
                        </span>
                        <span class="${task.completed ? 'line-through text-gray-500' : ''}">${task.title}</span>
                    </div>
                `).join('')}
                ${tasksForDate.length > maxTasks ? `<div class="tooltip-more">+${tasksForDate.length - maxTasks} tareas más</div>` : ''}
            `;
            
            // Posicionar tooltip
            setTimeout(() => {
                const rect = event.target.getBoundingClientRect();
                const tooltipRect = tooltip.getBoundingClientRect();
                
                let left = rect.left + rect.width / 2 - tooltipRect.width / 2;
                let top = rect.top - tooltipRect.height - 10;
                
                // Ajustar si se sale de la pantalla
                if (left < 10) left = 10;
                if (left + tooltipRect.width > window.innerWidth - 10) {
                    left = window.innerWidth - tooltipRect.width - 10;
                }
                if (top < 10) top = rect.bottom + 10;
                
                tooltip.style.left = left + 'px';
                tooltip.style.top = top + 'px';
                tooltip.classList.add('show');
            }, 10);
        }

        function hideCalendarTooltip() {
            const tooltip = document.getElementById('calendarTooltip');
            tooltip.classList.remove('show');
        }

        // Task management - Optimized
        function createNewTask() {
            const title = document.getElementById('newTaskTitle').value.trim();
            const date = selectedNewTaskDate;
            const priority = selectedNewTaskPriority;
            const subject = selectedNewTaskSubject;
            const description = document.getElementById('newTaskDescription').value.trim();
            
            if (!title || !date || !priority || !subject) {
                alert('Por favor completa todos los campos obligatorios');
                return;
            }
            
            const newTask = {
                id: taskIdCounter++,
                title,
                date,
                priority,
                subject,
                description,
                completed: false,
                createdAt: new Date().toISOString()
            };
            
            tasks.push(newTask);
            saveTasks();
            
            // Clear form
            clearCreateForm();
            
            // Update UI efficiently
            requestAnimationFrame(() => {
                renderTasks();
                updateStatistics();
                updateProgressTab();
                renderMainCalendar();
                updateCharts();
            });
            
            // Show success message
            alert('¡Tarea creada exitosamente!');
            
            // Switch to pending tasks tab
            switchTab('pendientes');
        }

        function clearCreateForm() {
            document.getElementById('newTaskTitle').value = '';
            document.getElementById('newTaskDescription').value = '';
            
            // Limpiar selectores personalizados
            selectedNewTaskDate = '';
            selectedNewTaskPriority = '';
            selectedNewTaskSubject = '';
            
            // Resetear textos de selectores
            document.getElementById('newTaskDateText').textContent = 'Seleccionar fecha';
            document.getElementById('newTaskPriorityText').textContent = 'Seleccionar prioridad';
            document.getElementById('newTaskSubjectText').textContent = 'Seleccionar materia';
            
            // Resetear iconos
            document.querySelector('#newTaskDateCalendar').parentElement.querySelector('.selector-icon').textContent = '📅';
            document.querySelector('#newTaskPriorityDropdown').parentElement.querySelector('.selector-icon').textContent = '🎯';
            document.querySelector('#newTaskSubjectDropdown').parentElement.querySelector('.selector-icon').textContent = '📚';
            
            // Limpiar selecciones visuales
            document.querySelectorAll('#newTaskPriorityDropdown .custom-dropdown-item').forEach(item => {
                item.classList.remove('selected');
            });
            document.querySelectorAll('#newTaskSubjectDropdown .custom-dropdown-item').forEach(item => {
                item.classList.remove('selected');
            });
        }

        // Optimized task rendering
        function renderTasks() {
            // Si hay filtros activos, usar la función de filtros
            if (selectedFilterPriority !== 'all' || selectedFilterDate !== '') {
                filterTasks();
                return;
            }
            
            const taskList = document.getElementById('taskList');
            const emptyState = document.getElementById('emptyState');
            const pendingTasks = tasks.filter(task => !task.completed);
            
            if (pendingTasks.length === 0) {
                taskList.style.display = 'none';
                emptyState.style.display = 'block';
                document.getElementById('taskCount').textContent = '0';
                return;
            }
            
            taskList.style.display = 'block';
            emptyState.style.display = 'none';
            document.getElementById('taskCount').textContent = pendingTasks.length;
            
            taskList.innerHTML = '';
            
            pendingTasks.forEach(task => {
                const taskElement = document.createElement('div');
                taskElement.className = `modern-card p-3 ${isOverdue(task.date) ? 'border-red-300' : ''}`;
                taskElement.innerHTML = `
                    <div class="flex items-center justify-between">
                        <div class="flex items-center gap-3">
                            <input type="checkbox" onchange="toggleTask(${task.id})" 
                                   class="w-4 h-4 rounded" style="accent-color: var(--primary-color)">
                            <div>
                                <h3 class="font-semibold text-base">${task.title}</h3>
                                <div class="flex items-center gap-2 mt-1">
                                    <span class="text-sm text-gray-600">${task.subject}</span>
                                    <span class="text-sm text-gray-500">•</span>
                                    <span class="text-sm ${isOverdue(task.date) ? 'text-red-600 font-semibold' : 'text-gray-600'}">
                                        ${formatDate(task.date)}
                                    </span>
                                    ${isOverdue(task.date) ? '<span class="text-red-600 text-sm font-semibold">⚠️ Vencida</span>' : ''}
                                </div>
                                ${task.description ? `<p class="text-sm text-gray-600 mt-1">${task.description}</p>` : ''}
                            </div>
                        </div>
                        <div class="flex items-center gap-2">
                            <span class="priority-badge priority-${task.priority}">
                                ${task.priority === 'high' ? '🔴 Alta' : task.priority === 'medium' ? '🟡 Media' : '🟢 Baja'}
                            </span>
                            <button onclick="deleteTask(${task.id})" 
                                    class="text-red-500 hover:text-red-700 p-1 rounded-lg hover:bg-red-50 transition-colors">
                                <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                                    <path fill-rule="evenodd" d="M9 2a1 1 0 00-.894.553L7.382 4H4a1 1 0 000 2v10a2 2 0 002 2h8a2 2 0 002-2V6a1 1 0 100-2h-3.382l-.724-1.447A1 1 0 0011 2H9zM7 8a1 1 0 012 0v6a1 1 0 11-2 0V8zm5-1a1 1 0 00-1 1v6a1 1 0 102 0V8a1 1 0 00-1-1z" clip-rule="evenodd"/>
                                </svg>
                            </button>
                        </div>
                    </div>
                `;
                taskList.appendChild(taskElement);
            });
        }

        function toggleTask(taskId) {
            const task = tasks.find(t => t.id === taskId);
            if (task) {
                task.completed = !task.completed;
                task.completedAt = task.completed ? new Date().toISOString() : null;
                saveTasks();
                
                // Update UI efficiently
                requestAnimationFrame(() => {
                    renderTasks();
                    updateStatistics();
                    updateProgressTab();
                    renderMainCalendar();
                    updateCharts();
                });
            }
        }

        // Delete task with modern modal
        let taskToDelete = null;

        function deleteTask(taskId) {
            const task = tasks.find(t => t.id === taskId);
            if (!task) return;
            
            taskToDelete = taskId;
            document.getElementById('deleteTaskTitle').textContent = 
                `¿Estás seguro de que deseas eliminar "${task.title}"? Esta acción no se puede deshacer.`;
            
            const modal = document.getElementById('deleteModal');
            modal.classList.add('active');
        }

        function closeDeleteModal() {
            const modal = document.getElementById('deleteModal');
            modal.classList.remove('active');
            taskToDelete = null;
        }

        function confirmDeleteTask() {
            if (taskToDelete) {
                tasks = tasks.filter(t => t.id !== taskToDelete);
                saveTasks();
                
                // Update UI efficiently
                requestAnimationFrame(() => {
                    renderTasks();
                    updateStatistics();
                    updateProgressTab();
                    renderMainCalendar();
                    updateCharts();
                });
                
                closeDeleteModal();
            }
        }

        // ===== FUNCIONES PARA SELECTORES PERSONALIZADOS =====
        
        // Variables globales para selectores
        let selectedFilterPriority = 'all';
        let selectedFilterDate = '';
        let selectedNewTaskPriority = '';
        let selectedNewTaskSubject = '';
        let selectedNewTaskDate = '';
        let filterCalendarDate = new Date();
        let newTaskCalendarDate = new Date();

        // Función para alternar dropdown
        function toggleDropdown(selectorId) {
            const selector = document.querySelector(`[onclick="toggleDropdown('${selectorId}')"]`);
            const dropdown = document.getElementById(selectorId + 'Dropdown');
            
            // Cerrar otros dropdowns
            document.querySelectorAll('.custom-dropdown').forEach(dd => {
                if (dd !== dropdown) {
                    dd.classList.remove('active');
                    dd.parentElement.classList.remove('active');
                }
            });
            
            // Alternar el dropdown actual
            dropdown.classList.toggle('active');
            selector.classList.toggle('active');
            
            // Cerrar al hacer clic fuera
            if (dropdown.classList.contains('active')) {
                setTimeout(() => {
                    document.addEventListener('click', function closeDropdown(e) {
                        if (!selector.contains(e.target) && !dropdown.contains(e.target)) {
                            dropdown.classList.remove('active');
                            selector.classList.remove('active');
                            document.removeEventListener('click', closeDropdown);
                        }
                    });
                }, 100);
            }
        }

        // Función para alternar calendario
        function toggleCalendar(selectorId) {
            const selector = document.querySelector(`[onclick="toggleCalendar('${selectorId}')"]`);
            const calendar = document.getElementById(selectorId + 'Calendar');
            
            // Cerrar otros calendarios y dropdowns
            document.querySelectorAll('.custom-dropdown, .custom-calendar').forEach(element => {
                if (element !== calendar) {
                    element.classList.remove('active');
                    element.parentElement.classList.remove('active');
                }
            });
            
            // Alternar el calendario actual
            calendar.classList.toggle('active');
            selector.classList.toggle('active');
            
            // Renderizar calendario si se abre
            if (calendar.classList.contains('active')) {
                if (selectorId === 'filterDate') {
                    renderFilterCalendar();
                } else if (selectorId === 'newTaskDate') {
                    renderNewTaskCalendar();
                }
                
                // Cerrar al hacer clic fuera
                setTimeout(() => {
                    document.addEventListener('click', function closeCalendar(e) {
                        if (!selector.contains(e.target) && !calendar.contains(e.target)) {
                            calendar.classList.remove('active');
                            selector.classList.remove('active');
                            document.removeEventListener('click', closeCalendar);
                        }
                    });
                }, 100);
            }
        }

        // Seleccionar prioridad en filtros
        function selectPriority(value, text, icon) {
            selectedFilterPriority = value;
            document.getElementById('filterPriorityText').textContent = text;
            document.querySelector('#filterPriorityDropdown').parentElement.querySelector('.selector-icon').textContent = icon;
            
            // Actualizar selección visual
            document.querySelectorAll('#filterPriorityDropdown .custom-dropdown-item').forEach(item => {
                item.classList.remove('selected');
            });
            event.target.closest('.custom-dropdown-item').classList.add('selected');
            
            // Cerrar todos los menús automáticamente
            setTimeout(() => {
                closeAllMenus();
            }, 150);
            
            // Aplicar filtro
            filterTasks();
        }

        // Seleccionar prioridad para nueva tarea
        function selectNewTaskPriority(value, text, icon) {
            selectedNewTaskPriority = value;
            document.getElementById('newTaskPriorityText').textContent = text;
            document.querySelector('#newTaskPriorityDropdown').parentElement.querySelector('.selector-icon').textContent = icon;
            
            // Actualizar selección visual
            document.querySelectorAll('#newTaskPriorityDropdown .custom-dropdown-item').forEach(item => {
                item.classList.remove('selected');
            });
            event.target.closest('.custom-dropdown-item').classList.add('selected');
            
            // Cerrar todos los menús automáticamente
            setTimeout(() => {
                closeAllMenus();
            }, 150);
        }

        // Seleccionar materia para nueva tarea
        function selectNewTaskSubject(value, text, icon) {
            selectedNewTaskSubject = value;
            document.getElementById('newTaskSubjectText').textContent = text;
            document.querySelector('#newTaskSubjectDropdown').parentElement.querySelector('.selector-icon').textContent = icon;
            
            // Actualizar selección visual
            document.querySelectorAll('#newTaskSubjectDropdown .custom-dropdown-item').forEach(item => {
                item.classList.remove('selected');
            });
            event.target.closest('.custom-dropdown-item').classList.add('selected');
            
            // Cerrar todos los menús automáticamente
            setTimeout(() => {
                closeAllMenus();
            }, 150);
        }

        // Renderizar calendario de filtros - ARREGLADO para 7 columnas correctas
        function renderFilterCalendar() {
            const monthNames = ['Enero', 'Febrero', 'Marzo', 'Abril', 'Mayo', 'Junio',
                'Julio', 'Agosto', 'Septiembre', 'Octubre', 'Noviembre', 'Diciembre'];
            
            document.getElementById('filterCalendarMonth').textContent = 
                `${monthNames[filterCalendarDate.getMonth()]} ${filterCalendarDate.getFullYear()}`;
            
            const year = filterCalendarDate.getFullYear();
            const month = filterCalendarDate.getMonth();
            
            // Obtener el primer día del mes y calcular desde qué domingo empezar
            const firstDayOfMonth = new Date(year, month, 1);
            
            // Calcular el primer domingo a mostrar (inicio de la semana)
            const startDate = new Date(firstDayOfMonth);
            startDate.setDate(firstDayOfMonth.getDate() - firstDayOfMonth.getDay());
            
            const calendarDays = document.getElementById('filterCalendarDays');
            calendarDays.innerHTML = '';
            
            // Crear exactamente 42 días (6 semanas × 7 días) para mantener la estructura perfecta
            for (let i = 0; i < 42; i++) {
                const currentDate = new Date(startDate);
                currentDate.setDate(startDate.getDate() + i);
                
                const dayElement = document.createElement('div');
                dayElement.className = 'calendar-day-custom';
                dayElement.textContent = currentDate.getDate();
                
                // Marcar días de otros meses
                if (currentDate.getMonth() !== month) {
                    dayElement.classList.add('other-month');
                }
                
                // Marcar día actual
                if (isToday(currentDate)) {
                    dayElement.classList.add('today');
                }
                
                // Marcar día seleccionado
                if (selectedFilterDate === formatDateForInput(currentDate)) {
                    dayElement.classList.add('selected');
                }
                
                dayElement.addEventListener('click', () => selectFilterDate(currentDate));
                calendarDays.appendChild(dayElement);
            }
        }

        // Renderizar calendario de nueva tarea - ARREGLADO para 7 columnas correctas
        function renderNewTaskCalendar() {
            const monthNames = ['Enero', 'Febrero', 'Marzo', 'Abril', 'Mayo', 'Junio',
                'Julio', 'Agosto', 'Septiembre', 'Octubre', 'Noviembre', 'Diciembre'];
            
            document.getElementById('newTaskCalendarMonth').textContent = 
                `${monthNames[newTaskCalendarDate.getMonth()]} ${newTaskCalendarDate.getFullYear()}`;
            
            const year = newTaskCalendarDate.getFullYear();
            const month = newTaskCalendarDate.getMonth();
            
            // Obtener el primer día del mes y calcular desde qué domingo empezar
            const firstDayOfMonth = new Date(year, month, 1);
            
            // Calcular el primer domingo a mostrar (inicio de la semana)
            const startDate = new Date(firstDayOfMonth);
            startDate.setDate(firstDayOfMonth.getDate() - firstDayOfMonth.getDay());
            
            const calendarDays = document.getElementById('newTaskCalendarDays');
            calendarDays.innerHTML = '';
            
            // Crear exactamente 42 días (6 semanas × 7 días) para mantener la estructura perfecta
            for (let i = 0; i < 42; i++) {
                const currentDate = new Date(startDate);
                currentDate.setDate(startDate.getDate() + i);
                
                const dayElement = document.createElement('div');
                dayElement.className = 'calendar-day-custom';
                dayElement.textContent = currentDate.getDate();
                
                // Marcar días de otros meses
                if (currentDate.getMonth() !== month) {
                    dayElement.classList.add('other-month');
                }
                
                // Marcar día actual
                if (isToday(currentDate)) {
                    dayElement.classList.add('today');
                }
                
                // Marcar día seleccionado
                if (selectedNewTaskDate === formatDateForInput(currentDate)) {
                    dayElement.classList.add('selected');
                }
                
                dayElement.addEventListener('click', () => selectNewTaskDate(currentDate));
                calendarDays.appendChild(dayElement);
            }
        }

        // Función para cerrar todos los menús
        function closeAllMenus() {
            // Cerrar todos los dropdowns
            document.querySelectorAll('.custom-dropdown').forEach(dropdown => {
                dropdown.classList.remove('active');
            });
            
            // Cerrar todos los calendarios
            document.querySelectorAll('.custom-calendar').forEach(calendar => {
                calendar.classList.remove('active');
            });
            
            // Cerrar todos los selectores
            document.querySelectorAll('.custom-selector').forEach(selector => {
                selector.classList.remove('active');
            });
        }

        // Seleccionar fecha de filtro
        function selectFilterDate(date) {
            selectedFilterDate = formatDateForInput(date);
            document.getElementById('filterDateText').textContent = formatDate(date);
            
            // Cerrar todos los menús automáticamente
            setTimeout(() => {
                closeAllMenus();
            }, 150);
            
            // Aplicar filtro
            filterTasks();
        }

        // Seleccionar fecha de nueva tarea
        function selectNewTaskDate(date) {
            selectedNewTaskDate = formatDateForInput(date);
            document.getElementById('newTaskDateText').textContent = formatDate(date);
            
            // Cerrar todos los menús automáticamente
            setTimeout(() => {
                closeAllMenus();
            }, 150);
        }

        // Limpiar filtro de fecha
        function clearDateFilter() {
            selectedFilterDate = '';
            document.getElementById('filterDateText').textContent = 'Seleccionar fecha';
            
            // Cerrar calendario
            document.getElementById('filterDateCalendar').classList.remove('active');
            document.querySelector(`[onclick="toggleCalendar('filterDate')"]`).classList.remove('active');
            
            // Aplicar filtro
            filterTasks();
        }

        // Navegación de calendario
        function previousMonth(type) {
            if (type === 'filter') {
                filterCalendarDate.setMonth(filterCalendarDate.getMonth() - 1);
                renderFilterCalendar();
            } else if (type === 'newTask') {
                newTaskCalendarDate.setMonth(newTaskCalendarDate.getMonth() - 1);
                renderNewTaskCalendar();
            }
        }

        function nextMonth(type) {
            if (type === 'filter') {
                filterCalendarDate.setMonth(filterCalendarDate.getMonth() + 1);
                renderFilterCalendar();
            } else if (type === 'newTask') {
                newTaskCalendarDate.setMonth(newTaskCalendarDate.getMonth() + 1);
                renderNewTaskCalendar();
            }
        }

        // Optimized filter function
        function filterTasks() {
            const priorityFilter = selectedFilterPriority;
            const dateFilter = selectedFilterDate;
            
            let filteredTasks = tasks.filter(task => !task.completed);
            
            if (priorityFilter !== 'all') {
                filteredTasks = filteredTasks.filter(task => task.priority === priorityFilter);
            }
            
            if (dateFilter) {
                filteredTasks = filteredTasks.filter(task => task.date === dateFilter);
            }
            
            const taskList = document.getElementById('taskList');
            const emptyState = document.getElementById('emptyState');
            
            if (filteredTasks.length === 0) {
                taskList.style.display = 'none';
                emptyState.style.display = 'block';
                document.getElementById('taskCount').textContent = '0';
                return;
            }
            
            taskList.style.display = 'block';
            emptyState.style.display = 'none';
            document.getElementById('taskCount').textContent = filteredTasks.length;
            
            taskList.innerHTML = '';
            
            filteredTasks.forEach(task => {
                const taskElement = document.createElement('div');
                taskElement.className = `modern-card p-3 ${isOverdue(task.date) ? 'border-red-300' : ''}`;
                taskElement.innerHTML = `
                    <div class="flex items-center justify-between">
                        <div class="flex items-center gap-3">
                            <input type="checkbox" onchange="toggleTask(${task.id})" 
                                   class="w-4 h-4 rounded" style="accent-color: var(--primary-color)">
                            <div>
                                <h3 class="font-semibold text-base">${task.title}</h3>
                                <div class="flex items-center gap-2 mt-1">
                                    <span class="text-sm text-gray-600">${task.subject}</span>
                                    <span class="text-sm text-gray-500">•</span>
                                    <span class="text-sm ${isOverdue(task.date) ? 'text-red-600 font-semibold' : 'text-gray-600'}">
                                        ${formatDate(task.date)}
                                    </span>
                                    ${isOverdue(task.date) ? '<span class="text-red-600 text-sm font-semibold">⚠️ Vencida</span>' : ''}
                                </div>
                                ${task.description ? `<p class="text-sm text-gray-600 mt-1">${task.description}</p>` : ''}
                            </div>
                        </div>
                        <div class="flex items-center gap-2">
                            <span class="priority-badge priority-${task.priority}">
                                ${task.priority === 'high' ? '🔴 Alta' : task.priority === 'medium' ? '🟡 Media' : '🟢 Baja'}
                            </span>
                            <button onclick="deleteTask(${task.id})" 
                                    class="text-red-500 hover:text-red-700 p-1 rounded-lg hover:bg-red-50 transition-colors">
                                <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                                    <path fill-rule="evenodd" d="M9 2a1 1 0 00-.894.553L7.382 4H4a1 1 0 000 2v10a2 2 0 002 2h8a2 2 0 002-2V6a1 1 0 100-2h-3.382l-.724-1.447A1 1 0 0011 2H9zM7 8a1 1 0 012 0v6a1 1 0 11-2 0V8zm5-1a1 1 0 00-1 1v6a1 1 0 102 0V8a1 1 0 00-1-1z" clip-rule="evenodd"/>
                                </svg>
                            </button>
                        </div>
                    </div>
                `;
                taskList.appendChild(taskElement);
            });
        }

        // Chat functionality
        function sendChatMessage() {
            const input = document.getElementById('chatInput');
            const message = input.value.trim();
            
            if (!message) return;
            
            // Add user message
            chatMessages.push({
                type: 'user',
                message: message,
                timestamp: new Date().toISOString()
            });
            
            // Generate AI response
            const aiResponse = generateAIResponse(message);
            chatMessages.push({
                type: 'ai',
                message: aiResponse,
                timestamp: new Date().toISOString()
            });
            
            saveChatMessages();
            renderChatMessages();
            input.value = '';
        }

        function handleChatKeyPress(event) {
            if (event.key === 'Enter') {
                sendChatMessage();
            }
        }

        function generateAIResponse(userMessage) {
            const message = userMessage.toLowerCase();
            
            // Historia y fechas importantes
            if (message.includes('segunda guerra mundial') || message.includes('2da guerra mundial') || message.includes('wwii')) {
                return "🌍 La Segunda Guerra Mundial comenzó el 1 de septiembre de 1939 con la invasión alemana a Polonia y terminó el 2 de septiembre de 1945 con la rendición de Japón. Duró aproximadamente 6 años.";
            }
            
            if (message.includes('primera guerra mundial') || message.includes('1ra guerra mundial') || message.includes('wwi')) {
                return "⚔️ La Primera Guerra Mundial se desarrolló del 28 de julio de 1914 al 11 de noviembre de 1918. Comenzó con el asesinato del archiduque Francisco Fernando y terminó con el Armisticio de Compiègne.";
            }
            
            if (message.includes('independencia') && (message.includes('méxico') || message.includes('mexico'))) {
                return "🇲🇽 La Independencia de México comenzó el 16 de septiembre de 1810 con el Grito de Dolores de Miguel Hidalgo y se consumó el 27 de septiembre de 1821 con la entrada del Ejército Trigarante a la Ciudad de México.";
            }
            
            if (message.includes('revolución francesa')) {
                return "🇫🇷 La Revolución Francesa comenzó en 1789 con la toma de la Bastilla el 14 de julio y se extendió hasta 1799. Marcó el fin del Antiguo Régimen y el inicio de la era moderna.";
            }
            
            if (message.includes('descubrimiento de américa') || message.includes('cristóbal colón')) {
                return "🌎 Cristóbal Colón llegó a América el 12 de octubre de 1492, desembarcando en la isla de Guanahani (actual Bahamas). Este evento cambió la historia mundial para siempre.";
            }
            
            // Ciencias y matemáticas
            if (message.includes('teorema de pitágoras') || message.includes('pitágoras')) {
                return "📐 El Teorema de Pitágoras establece que en un triángulo rectángulo, el cuadrado de la hipotenusa es igual a la suma de los cuadrados de los catetos: a² + b² = c².";
            }
            
            if (message.includes('tabla periódica') || message.includes('elementos químicos')) {
                return "🧪 La tabla periódica fue creada por Dmitri Mendeléyev en 1869. Organiza los 118 elementos químicos conocidos según su número atómico y propiedades químicas.";
            }
            
            if (message.includes('velocidad de la luz')) {
                return "💫 La velocidad de la luz en el vacío es de aproximadamente 299,792,458 metros por segundo (300,000 km/s). Es una constante fundamental de la física.";
            }
            
            if (message.includes('adn') || message.includes('ácido desoxirribonucleico')) {
                return "🧬 El ADN (Ácido Desoxirribonucleico) contiene la información genética de los seres vivos. Fue descubierto por Friedrich Miescher en 1869 y su estructura de doble hélice por Watson y Crick en 1953.";
            }
            
            // Geografía
            if (message.includes('capital') && message.includes('francia')) {
                return "🗼 La capital de Francia es París, conocida como la 'Ciudad de la Luz'. Tiene una población de aproximadamente 2.2 millones de habitantes en la ciudad y 12 millones en el área metropolitana.";
            }
            
            if (message.includes('monte everest') || message.includes('montaña más alta')) {
                return "🏔️ El Monte Everest es la montaña más alta del mundo con 8,848.86 metros sobre el nivel del mar. Se encuentra en la cordillera del Himalaya, entre Nepal y Tíbet.";
            }
            
            if (message.includes('océano más grande') || message.includes('océano pacífico')) {
                return "🌊 El Océano Pacífico es el más grande del mundo, cubriendo aproximadamente un tercio de la superficie terrestre (165.2 millones de km²). Es más grande que toda la superficie terrestre combinada.";
            }
            
            // Literatura y arte
            if (message.includes('shakespeare')) {
                return "🎭 William Shakespeare (1564-1616) fue un dramaturgo y poeta inglés, considerado el mejor escritor en lengua inglesa. Escribió obras como 'Romeo y Julieta', 'Hamlet' y 'Macbeth'.";
            }
            
            if (message.includes('mona lisa') || message.includes('gioconda')) {
                return "🎨 La Mona Lisa (La Gioconda) fue pintada por Leonardo da Vinci entre 1503-1519. Se encuentra en el Museo del Louvre en París y es considerada la pintura más famosa del mundo.";
            }
            
            // Respuestas específicas de productividad (mejoradas)
            if (message.includes('tarea') || message.includes('crear')) {
                const taskResponses = [
                    "💡 Para crear una tarea efectiva: título claro, fecha realista, prioridad adecuada y descripción detallada. ¿Te ayudo con alguna tarea específica?",
                    "✅ Una buena tarea debe ser específica, medible y con fecha límite. ¿Qué tarea necesitas organizar?",
                    "📝 Divide las tareas grandes en subtareas más pequeñas. Esto hace que sean menos abrumadoras y más fáciles de completar."
                ];
                return taskResponses[Math.floor(Math.random() * taskResponses.length)];
            }
            
            if (message.includes('prioridad') || message.includes('importante')) {
                const priorityResponses = [
                    "🎯 Usa el método ABC: A (muy importante), B (importante), C (menos importante). Las tareas A siempre van primero.",
                    "⚡ Matriz de Eisenhower: Urgente e Importante (hacer ya), Importante no Urgente (planificar), Urgente no Importante (delegar), Ni urgente ni importante (eliminar).",
                    "🔥 Regla 80/20: El 20% de tus tareas producen el 80% de los resultados. Identifica y enfócate en ese 20% crucial."
                ];
                return priorityResponses[Math.floor(Math.random() * priorityResponses.length)];
            }
            
            if (message.includes('tiempo') || message.includes('organizar')) {
                const timeResponses = [
                    "⏰ Técnica Pomodoro: 25 min trabajo + 5 min descanso. Después de 4 pomodoros, toma un descanso de 15-30 minutos.",
                    "📅 Time-blocking: Asigna bloques específicos de tiempo para cada actividad. Trata cada bloque como una cita importante contigo mismo.",
                    "⚡ Regla de 2 minutos: Si algo toma menos de 2 minutos, hazlo inmediatamente. Si toma más, programa un tiempo específico para hacerlo."
                ];
                return timeResponses[Math.floor(Math.random() * timeResponses.length)];
            }
            
            if (message.includes('estudio') || message.includes('estudiar')) {
                const studyResponses = [
                    "📚 Técnica Feynman: Explica el concepto como si se lo enseñaras a un niño de 5 años. Si no puedes, necesitas estudiarlo más.",
                    "🧠 Repaso espaciado: Revisa el material después de 1 día, 3 días, 1 semana, 2 semanas y 1 mes para mejor retención.",
                    "🎯 Estudio activo: Haz resúmenes, mapas mentales, flashcards y enseña a otros. La lectura pasiva es menos efectiva."
                ];
                return studyResponses[Math.floor(Math.random() * studyResponses.length)];
            }
            
            if (message.includes('motivación') || message.includes('motivar')) {
                const motivationResponses = [
                    "🚀 Visualiza tu éxito: Imagina cómo te sentirás cuando logres tus metas. La visualización activa las mismas áreas cerebrales que la acción real.",
                    "🏆 Celebra pequeños logros: Cada tarea completada merece reconocimiento. Esto libera dopamina y refuerza hábitos positivos.",
                    "💪 Recuerda tu 'por qué': Conecta cada tarea con tus objetivos a largo plazo. El propósito es el combustible de la motivación."
                ];
                return motivationResponses[Math.floor(Math.random() * motivationResponses.length)];
            }
            
            // Respuestas para preguntas generales
            if (message.includes('hola') || message.includes('ayuda')) {
                const greetingResponses = [
                    "👋 ¡Hola! Soy tu asistente inteligente. Puedo ayudarte con productividad, historia, ciencias, matemáticas, geografía y mucho más. ¿Qué te gustaría saber?",
                    "🤖 ¡Saludos! Estoy aquí para responder tus preguntas sobre cualquier tema: desde organización de tareas hasta datos históricos y científicos. ¿En qué puedo ayudarte?",
                    "✨ ¡Hola! Soy tu compañero de aprendizaje. Pregúntame sobre historia, ciencias, matemáticas, técnicas de estudio o cualquier cosa que necesites saber."
                ];
                return greetingResponses[Math.floor(Math.random() * greetingResponses.length)];
            }
            
            // Si no encuentra una respuesta específica, intenta dar una respuesta inteligente
            if (message.includes('cuándo') || message.includes('cuando') || message.includes('fecha')) {
                return "📅 Para preguntas sobre fechas históricas específicas, puedes preguntarme sobre eventos como guerras mundiales, independencias, descubrimientos, etc. ¿Hay algún evento histórico particular que te interese?";
            }
            
            if (message.includes('qué es') || message.includes('que es') || message.includes('define')) {
                return "🤔 Puedo explicarte conceptos de ciencias, matemáticas, historia, geografía y más. ¿Sobre qué tema específico te gustaría que te explique?";
            }
            
            if (message.includes('cómo') || message.includes('como')) {
                return "💡 Puedo ayudarte con técnicas de estudio, métodos de organización, estrategias de productividad y explicaciones de procesos. ¿Qué proceso o técnica te interesa aprender?";
            }
            
            // Respuestas generales variadas (como último recurso)
            const generalResponses = [
                "🤖 Interesante pregunta. Aunque no tengo información específica sobre eso, puedo ayudarte con historia, ciencias, matemáticas, técnicas de estudio y productividad. ¿Hay algo de estos temas que te interese?",
                "💭 No tengo datos específicos sobre esa consulta, pero puedo asistirte con fechas históricas, conceptos científicos, técnicas de organización y métodos de estudio. ¿Te gustaría explorar alguno de estos temas?",
                "🧠 Esa es una pregunta que requiere información más específica. Sin embargo, puedo ayudarte con eventos históricos, principios científicos, fórmulas matemáticas y estrategias de productividad. ¿Qué te gustaría aprender?",
                "📚 Aunque no tengo información detallada sobre eso, soy experto en historia mundial, ciencias básicas, matemáticas y técnicas de estudio. ¿Hay algún tema educativo en el que pueda ayudarte?"
            ];
            
            return generalResponses[Math.floor(Math.random() * generalResponses.length)];
        }

        function renderChatMessages() {
            const container = document.getElementById('chatMessages');
            
            if (chatMessages.length === 0) {
                container.innerHTML = `
                    <div class="text-center py-6 text-gray-500">
                        <p>🤖 ¡Hola! Soy tu asistente IA. ¿En qué puedo ayudarte hoy?</p>
                    </div>
                `;
                return;
            }
            
            container.innerHTML = chatMessages.map(msg => `
                <div class="mb-3 ${msg.type === 'user' ? 'text-right' : 'text-left'}">
                    <div class="inline-block max-w-xs lg:max-w-md px-3 py-2 rounded-lg ${
                        msg.type === 'user' 
                            ? 'bg-blue-500 text-white' 
                            : 'bg-gray-200 text-gray-800'
                    }">
                        <p class="text-sm">${msg.message}</p>
                        <p class="text-xs opacity-75 mt-1">${formatTime(msg.timestamp)}</p>
                    </div>
                </div>
            `).join('');
            
            container.scrollTop = container.scrollHeight;
        }

        // Statistics and progress - Optimized
        function updateStatistics() {
            const completedTasks = tasks.filter(task => task.completed).length;
            const pendingTasks = tasks.filter(task => !task.completed).length;
            const highPriorityTasks = tasks.filter(task => task.priority === 'high' && !task.completed).length;
            const totalTasks = tasks.length;
            const progressPercentage = totalTasks > 0 ? Math.round((completedTasks / totalTasks) * 100) : 0;
            
            // Update statistics tab
            const elements = {
                'completedCount': completedTasks,
                'pendingCount': pendingTasks,
                'highPriorityCount': highPriorityTasks,
                'progressPercentage': progressPercentage + '%'
            };
            
            // Batch DOM updates
            requestAnimationFrame(() => {
                Object.entries(elements).forEach(([id, value]) => {
                    const element = document.getElementById(id);
                    if (element) element.textContent = value;
                });
                
                // Update progress bar
                const progressBar = document.getElementById('progressBar');
                if (progressBar) {
                    progressBar.style.width = progressPercentage + '%';
                }
            });
        }

        function updateProgressTab() {
            const completedTasks = tasks.filter(task => task.completed).length;
            const pendingTasks = tasks.filter(task => !task.completed).length;
            const highPriorityTasks = tasks.filter(task => task.priority === 'high' && !task.completed).length;
            const overdueTasks = tasks.filter(task => !task.completed && isOverdue(task.date)).length;
            const totalTasks = tasks.length;
            const progressPercentage = totalTasks > 0 ? Math.round((completedTasks / totalTasks) * 100) : 0;
            
            // Batch DOM updates
            requestAnimationFrame(() => {
                const elements = {
                    'totalTasksCount': totalTasks,
                    'completedCountProgress': completedTasks,
                    'pendingCountProgress': pendingTasks,
                    'highPriorityCountProgress': highPriorityTasks,
                    'overdueCountProgress': overdueTasks,
                    'circleProgressText': progressPercentage + '%'
                };
                
                Object.entries(elements).forEach(([id, value]) => {
                    const element = document.getElementById(id);
                    if (element) element.textContent = value;
                });
                
                // Update circular progress
                const circle = document.getElementById('progressCircle');
                if (circle) {
                    const circumference = 2 * Math.PI * 40;
                    const offset = circumference - (progressPercentage / 100) * circumference;
                    circle.style.strokeDashoffset = offset;
                }
                
                // Update weekly progress (real data)
                const weeklyProgress = calculateWeeklyProgress();
                document.getElementById('weeklyProgressText').textContent = weeklyProgress + '%';
                document.getElementById('weeklyProgressBar').style.width = weeklyProgress + '%';
                
                // Update productivity (real data)
                const productivity = calculateProductivity();
                document.getElementById('productivityText').textContent = productivity + '%';
                document.getElementById('productivityBar').style.width = productivity + '%';
                
                // Update streak (real data based on completed tasks)
                const streak = calculateCurrentStreak();
                document.getElementById('streakCount').textContent = streak;
            });
            
            // Update achievements
            updateAchievements();
        }

        function updateAchievements() {
            const achievements = [];
            const completedTasks = tasks.filter(task => task.completed).length;
            
            if (completedTasks >= 1) {
                achievements.push("🎉 Primera tarea completada");
            }
            if (completedTasks >= 5) {
                achievements.push("⭐ 5 tareas completadas");
            }
            if (completedTasks >= 10) {
                achievements.push("🏆 10 tareas completadas");
            }
            if (tasks.length >= 5) {
                achievements.push("📝 Organizador activo");
            }
            
            const achievementsList = document.getElementById('achievementsList');
            if (achievements.length === 0) {
                achievementsList.innerHTML = '<p class="text-gray-500 text-center">Completa tareas para desbloquear logros</p>';
            } else {
                achievementsList.innerHTML = achievements.map(achievement => `
                    <div class="flex items-center gap-2 p-2 bg-yellow-50 rounded-lg border border-yellow-200">
                        <span class="text-base">${achievement.split(' ')[0]}</span>
                        <span class="font-medium text-sm">${achievement.substring(achievement.indexOf(' ') + 1)}</span>
                    </div>
                `).join('');
            }
        }

        // Charts - Real-time data HD Quality
        function drawCharts() {
            // Usar setTimeout para asegurar que los elementos estén disponibles
            setTimeout(() => {
                drawWeeklyChart();
                drawPriorityChart();
            }, 100);
        }

        // Función para actualizar gráficos cuando cambian los datos - FUNCIONAL EN TIEMPO REAL
        function updateCharts() {
            // Actualizar inmediatamente cuando hay cambios en los datos
            requestAnimationFrame(() => {
                if (document.getElementById('weeklyChart')) {
                    drawWeeklyChart();
                }
                if (document.getElementById('priorityChart')) {
                    drawPriorityChart();
                }
            });
        }

        // Función roundRect para compatibilidad con navegadores antiguos
        if (!CanvasRenderingContext2D.prototype.roundRect) {
            CanvasRenderingContext2D.prototype.roundRect = function(x, y, width, height, radius) {
                if (width < 2 * radius) radius = width / 2;
                if (height < 2 * radius) radius = height / 2;
                this.beginPath();
                this.moveTo(x + radius, y);
                this.arcTo(x + width, y, x + width, y + height, radius);
                this.arcTo(x + width, y + height, x, y + height, radius);
                this.arcTo(x, y + height, x, y, radius);
                this.arcTo(x, y, x + width, y, radius);
                this.closePath();
                return this;
            };
        }

        function drawWeeklyChart() {
            const canvas = document.getElementById('weeklyChart');
            if (!canvas) return;
            
            // Set high DPI for crisp graphics
            const ctx = canvas.getContext('2d');
            const dpr = window.devicePixelRatio || 1;
            const rect = canvas.getBoundingClientRect();
            
            // Set actual size in memory (scaled up for high DPI)
            canvas.width = rect.width * dpr;
            canvas.height = rect.height * dpr;
            
            // Scale the canvas back down using CSS
            canvas.style.width = rect.width + 'px';
            canvas.style.height = rect.height + 'px';
            
            // Scale the drawing context so everything draws at the correct size
            ctx.scale(dpr, dpr);
            
            const width = rect.width;
            const height = rect.height;
            
            // Clear canvas
            ctx.clearRect(0, 0, width, height);
            
            // Enable anti-aliasing for smooth graphics
            ctx.imageSmoothingEnabled = true;
            ctx.imageSmoothingQuality = 'high';
            
            // Get real weekly data
            const days = ['Dom', 'Lun', 'Mar', 'Mié', 'Jue', 'Vie', 'Sáb'];
            const data = getRealWeeklyData();
            const maxValue = Math.max(...data, 1);
            
            // Enhanced gradient bars
            const barWidth = width / days.length * 0.7;
            const barSpacing = width / days.length * 0.3;
            
            const primaryColor = getComputedStyle(document.documentElement).getPropertyValue('--primary-color') || '#3B82F6';
            const secondaryColor = getComputedStyle(document.documentElement).getPropertyValue('--secondary-color') || '#10B981';
            
            data.forEach((value, index) => {
                const barHeight = maxValue > 0 ? (value / maxValue) * (height - 80) : 0;
                const x = index * (barWidth + barSpacing) + barSpacing / 2;
                const y = height - barHeight - 40;
                
                if (barHeight > 0) {
                    // Create gradient for bars
                    const gradient = ctx.createLinearGradient(x, y, x, y + barHeight);
                    gradient.addColorStop(0, primaryColor);
                    gradient.addColorStop(1, secondaryColor);
                    
                    // Draw shadow
                    ctx.shadowColor = 'rgba(0, 0, 0, 0.2)';
                    ctx.shadowBlur = 8;
                    ctx.shadowOffsetY = 4;
                    
                    // Draw rounded rectangle bar
                    ctx.fillStyle = gradient;
                    ctx.beginPath();
                    ctx.roundRect(x, y, barWidth, barHeight, 8);
                    ctx.fill();
                    
                    // Reset shadow
                    ctx.shadowColor = 'transparent';
                    ctx.shadowBlur = 0;
                    ctx.shadowOffsetY = 0;
                }
                
                // Draw enhanced labels
                ctx.fillStyle = '#374151';
                ctx.font = 'bold 14px system-ui, -apple-system, sans-serif';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                
                // Day labels
                ctx.fillText(days[index], x + barWidth / 2, height - 20);
                
                // Value labels with background
                if (value > 0) {
                    const valueText = value.toString();
                    const textMetrics = ctx.measureText(valueText);
                    const textWidth = textMetrics.width + 12;
                    const textHeight = 20;
                    const textX = x + barWidth / 2;
                    const textY = y - 15;
                    
                    // Background for value
                    ctx.fillStyle = 'rgba(255, 255, 255, 0.9)';
                    ctx.beginPath();
                    ctx.roundRect(textX - textWidth/2, textY - textHeight/2, textWidth, textHeight, 10);
                    ctx.fill();
                    
                    // Value text
                    ctx.fillStyle = primaryColor;
                    ctx.font = 'bold 12px system-ui, -apple-system, sans-serif';
                    ctx.fillText(valueText, textX, textY);
                }
            });
        }

        // Get real weekly completion data
        function getRealWeeklyData() {
            const now = new Date();
            const startOfWeek = new Date(now);
            startOfWeek.setDate(now.getDate() - now.getDay()); // Start from Sunday
            startOfWeek.setHours(0, 0, 0, 0);
            
            const weekData = [0, 0, 0, 0, 0, 0, 0]; // Sunday to Saturday
            
            tasks.filter(task => task.completed && task.completedAt).forEach(task => {
                const completedDate = new Date(task.completedAt);
                const daysDiff = Math.floor((completedDate - startOfWeek) / (1000 * 60 * 60 * 24));
                
                if (daysDiff >= 0 && daysDiff < 7) {
                    weekData[daysDiff]++;
                }
            });
            
            return weekData;
        }

        function drawPriorityChart() {
            const canvas = document.getElementById('priorityChart');
            if (!canvas) return;
            
            // Set high DPI for crisp graphics
            const ctx = canvas.getContext('2d');
            const dpr = window.devicePixelRatio || 1;
            const rect = canvas.getBoundingClientRect();
            
            // Set actual size in memory (scaled up for high DPI)
            canvas.width = rect.width * dpr;
            canvas.height = rect.height * dpr;
            
            // Scale the canvas back down using CSS
            canvas.style.width = rect.width + 'px';
            canvas.style.height = rect.height + 'px';
            
            // Scale the drawing context so everything draws at the correct size
            ctx.scale(dpr, dpr);
            
            const width = rect.width;
            const height = rect.height;
            const centerX = width / 2;
            const centerY = height / 2;
            const radius = Math.min(centerX, centerY) - 30;
            
            // Clear canvas
            ctx.clearRect(0, 0, width, height);
            
            // Enable anti-aliasing for smooth graphics
            ctx.imageSmoothingEnabled = true;
            ctx.imageSmoothingQuality = 'high';
            
            // Count tasks by priority
            const highPriority = tasks.filter(task => task.priority === 'high').length;
            const mediumPriority = tasks.filter(task => task.priority === 'medium').length;
            const lowPriority = tasks.filter(task => task.priority === 'low').length;
            const total = highPriority + mediumPriority + lowPriority;
            
            if (total === 0) {
                ctx.fillStyle = '#6B7280';
                ctx.font = 'bold 18px system-ui, -apple-system, sans-serif';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText('No hay datos', centerX, centerY);
                return;
            }
            
            // Enhanced pie chart with gradients and shadows
            const colors = [
                ['#EF4444', '#DC2626'], // High priority gradient
                ['#F59E0B', '#D97706'], // Medium priority gradient  
                ['#10B981', '#059669']  // Low priority gradient
            ];
            const values = [highPriority, mediumPriority, lowPriority];
            const labels = ['Alta', 'Media', 'Baja'];
            const icons = ['🔴', '🟡', '🟢'];
            
            let currentAngle = -Math.PI / 2;
            
            // Draw shadow for entire pie
            ctx.shadowColor = 'rgba(0, 0, 0, 0.2)';
            ctx.shadowBlur = 15;
            ctx.shadowOffsetX = 0;
            ctx.shadowOffsetY = 8;
            
            values.forEach((value, index) => {
                if (value > 0) {
                    const sliceAngle = (value / total) * 2 * Math.PI;
                    
                    // Create gradient for slice
                    const gradient = ctx.createRadialGradient(centerX, centerY, 0, centerX, centerY, radius);
                    gradient.addColorStop(0, colors[index][0]);
                    gradient.addColorStop(1, colors[index][1]);
                    
                    // Draw slice
                    ctx.beginPath();
                    ctx.moveTo(centerX, centerY);
                    ctx.arc(centerX, centerY, radius, currentAngle, currentAngle + sliceAngle);
                    ctx.closePath();
                    ctx.fillStyle = gradient;
                    ctx.fill();
                    
                    // Add stroke for definition
                    ctx.strokeStyle = 'rgba(255, 255, 255, 0.8)';
                    ctx.lineWidth = 3;
                    ctx.stroke();
                    
                    currentAngle += sliceAngle;
                }
            });
            
            // Reset shadow for labels
            ctx.shadowColor = 'transparent';
            ctx.shadowBlur = 0;
            ctx.shadowOffsetX = 0;
            ctx.shadowOffsetY = 0;
            
            // Draw labels with enhanced styling
            currentAngle = -Math.PI / 2;
            values.forEach((value, index) => {
                if (value > 0) {
                    const sliceAngle = (value / total) * 2 * Math.PI;
                    const labelAngle = currentAngle + sliceAngle / 2;
                    const labelRadius = radius * 0.65;
                    const labelX = centerX + Math.cos(labelAngle) * labelRadius;
                    const labelY = centerY + Math.sin(labelAngle) * labelRadius;
                    
                    // Draw label background
                    const labelText = labels[index];
                    const valueText = value.toString();
                    
                    ctx.font = 'bold 14px system-ui, -apple-system, sans-serif';
                    const textMetrics = ctx.measureText(labelText);
                    const bgWidth = Math.max(textMetrics.width, 40) + 16;
                    const bgHeight = 40;
                    
                    // Background circle
                    ctx.fillStyle = 'rgba(255, 255, 255, 0.95)';
                    ctx.beginPath();
                    ctx.arc(labelX, labelY, bgWidth/2, 0, 2 * Math.PI);
                    ctx.fill();
                    
                    // Border
                    ctx.strokeStyle = colors[index][0];
                    ctx.lineWidth = 2;
                    ctx.stroke();
                    
                    // Icon
                    ctx.font = '16px system-ui, -apple-system, sans-serif';
                    ctx.fillStyle = colors[index][0];
                    ctx.textAlign = 'center';
                    ctx.textBaseline = 'middle';
                    ctx.fillText(icons[index], labelX, labelY - 8);
                    
                    // Label text
                    ctx.font = 'bold 11px system-ui, -apple-system, sans-serif';
                    ctx.fillStyle = '#374151';
                    ctx.fillText(labelText, labelX, labelY + 4);
                    
                    // Value
                    ctx.font = 'bold 10px system-ui, -apple-system, sans-serif';
                    ctx.fillStyle = colors[index][0];
                    ctx.fillText(valueText, labelX, labelY + 14);
                    
                    currentAngle += sliceAngle;
                }
            });
            
            // Draw center circle for modern look
            ctx.fillStyle = 'rgba(255, 255, 255, 0.9)';
            ctx.beginPath();
            ctx.arc(centerX, centerY, radius * 0.3, 0, 2 * Math.PI);
            ctx.fill();
            
            ctx.strokeStyle = 'rgba(0, 0, 0, 0.1)';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // Center text
            ctx.fillStyle = '#374151';
            ctx.font = 'bold 12px system-ui, -apple-system, sans-serif';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            ctx.fillText('Total', centerX, centerY - 6);
            ctx.font = 'bold 16px system-ui, -apple-system, sans-serif';
            ctx.fillText(total.toString(), centerX, centerY + 8);
        }

        // Performance mode management
        function changePerformanceMode(mode) {
            document.body.setAttribute('data-performance', mode);
            
            // Update active performance button
            document.querySelectorAll('.performance-btn').forEach(btn => {
                btn.classList.remove('active');
            });
            
            const activeBtn = document.querySelector(`[data-mode="${mode}"]`);
            if (activeBtn) {
                activeBtn.classList.add('active');
            }
            
            // Save performance preference
            localStorage.setItem('taskmaster_performance', mode);
            
            // Show notification
            const modeText = mode === 'performance' ? 'Rendimiento' : 'Moderno';
            console.log(`Modo ${modeText} activado`);
        }

        // Theme management - Updated for dark mode palettes
        function changeTheme(themeName) {
            const currentTheme = document.body.getAttribute('data-theme');
            const isDark = currentTheme === 'dark';
            
            if (isDark) {
                // In dark mode, apply palette as data attribute
                document.body.setAttribute('data-palette', themeName);
            } else {
                // In light mode, change theme normally
                document.body.setAttribute('data-theme', themeName);
            }
            
            // Update active theme option
            document.querySelectorAll('.theme-option').forEach(option => {
                option.classList.remove('active');
            });
            
            // Map theme names to CSS classes
            const themeMap = {
                'palette1': 'theme-1',
                'palette2': 'theme-2',
                'palette3': 'theme-3',
                'palette4': 'theme-4',
                'palette5': 'theme-5'
            };
            
            const activeOption = document.querySelector(`.theme-option.${themeMap[themeName]}`);
            if (activeOption) {
                activeOption.classList.add('active');
            }
            
            // Save theme preference
            localStorage.setItem('taskmaster_color_palette', themeName);
        }

        // Dark mode toggle - Updated for palette support
        function toggleDarkMode(isDark) {
            if (isDark) {
                document.body.setAttribute('data-theme', 'dark');
                // Apply saved palette in dark mode
                const savedPalette = localStorage.getItem('taskmaster_color_palette') || 'palette1';
                document.body.setAttribute('data-palette', savedPalette);
            } else {
                // Restore saved color palette
                const savedPalette = localStorage.getItem('taskmaster_color_palette') || 'palette1';
                document.body.setAttribute('data-theme', savedPalette);
                document.body.removeAttribute('data-palette');
            }
            
            // Update active dark mode button
            document.querySelectorAll('[data-dark]').forEach(btn => {
                btn.classList.remove('active');
            });
            
            const activeBtn = document.querySelector(`[data-dark="${isDark ? 'dark' : 'light'}"]`);
            if (activeBtn) {
                activeBtn.classList.add('active');
            }
            
            // Save dark mode preference
            localStorage.setItem('taskmaster_dark_mode', isDark);
        }

        // Calculate weekly progress based on completed tasks this week
        function calculateWeeklyProgress() {
            const now = new Date();
            const startOfWeek = new Date(now);
            startOfWeek.setDate(now.getDate() - now.getDay());
            startOfWeek.setHours(0, 0, 0, 0);
            
            const endOfWeek = new Date(startOfWeek);
            endOfWeek.setDate(startOfWeek.getDate() + 6);
            endOfWeek.setHours(23, 59, 59, 999);
            
            const weeklyTasks = tasks.filter(task => {
                const taskDate = new Date(task.date);
                return taskDate >= startOfWeek && taskDate <= endOfWeek;
            });
            
            if (weeklyTasks.length === 0) return 0;
            
            const completedWeeklyTasks = weeklyTasks.filter(task => task.completed).length;
            return Math.round((completedWeeklyTasks / weeklyTasks.length) * 100);
        }

        // Calculate productivity based on tasks completed on time
        function calculateProductivity() {
            const completedTasks = tasks.filter(task => task.completed);
            if (completedTasks.length === 0) return 0;
            
            const onTimeTasks = completedTasks.filter(task => {
                if (!task.completedAt) return false;
                const completedDate = new Date(task.completedAt);
                const dueDate = new Date(task.date);
                dueDate.setHours(23, 59, 59, 999);
                return completedDate <= dueDate;
            });
            
            return Math.round((onTimeTasks.length / completedTasks.length) * 100);
        }

        // Calculate real streak based on completed tasks
        function calculateCurrentStreak() {
            const completedTasks = tasks.filter(task => task.completed && task.completedAt);
            if (completedTasks.length === 0) return 0;
            
            // Group completed tasks by date
            const tasksByDate = {};
            completedTasks.forEach(task => {
                const date = new Date(task.completedAt).toDateString();
                if (!tasksByDate[date]) {
                    tasksByDate[date] = [];
                }
                tasksByDate[date].push(task);
            });
            
            // Get sorted dates
            const dates = Object.keys(tasksByDate).sort((a, b) => new Date(b) - new Date(a));
            if (dates.length === 0) return 0;
            
            // Calculate consecutive days
            let streak = 0;
            const today = new Date().toDateString();
            const yesterday = new Date(Date.now() - 24 * 60 * 60 * 1000).toDateString();
            
            // Check if there are tasks completed today or yesterday to start counting
            if (dates.includes(today) || dates.includes(yesterday)) {
                let currentDate = new Date();
                
                for (let i = 0; i < dates.length; i++) {
                    const checkDate = currentDate.toDateString();
                    
                    if (dates.includes(checkDate)) {
                        streak++;
                        currentDate.setDate(currentDate.getDate() - 1);
                    } else {
                        break;
                    }
                }
            }
            
            return streak;
        }

        // Utility functions
        function isToday(date) {
            const today = new Date();
            return date.toDateString() === today.toDateString();
        }

        function isSameDay(date1, date2) {
            return date1.toDateString() === date2.toDateString();
        }

        function isOverdue(dateString) {
            const taskDate = new Date(dateString);
            const today = new Date();
            today.setHours(0, 0, 0, 0);
            return taskDate < today;
        }

        function formatDate(dateInput) {
            let date;
            if (typeof dateInput === 'string') {
                date = new Date(dateInput);
            } else {
                date = dateInput;
            }
            
            // Verificar si la fecha es válida
            if (isNaN(date.getTime())) {
                return 'Fecha inválida';
            }
            
            return date.toLocaleDateString('es-ES', {
                weekday: 'long',
                year: 'numeric',
                month: 'long',
                day: 'numeric'
            });
        }

        function formatDateForInput(date) {
            return date.toISOString().split('T')[0];
        }

        function formatTime(timestamp) {
            return new Date(timestamp).toLocaleTimeString('es-ES', {
                hour: '2-digit',
                minute: '2-digit'
            });
        }

        function getTasksForDate(date) {
            const dateString = formatDateForInput(date);
            return tasks.filter(task => task.date === dateString);
        }

        function setDefaultDate() {
            const today = new Date();
            // Establecer fecha por defecto para nueva tarea
            selectedNewTaskDate = formatDateForInput(today);
            document.getElementById('newTaskDateText').textContent = formatDate(today);
        }

        // Data persistence - Optimized
        function saveTasks() {
            try {
                localStorage.setItem('taskmaster_tasks', JSON.stringify(tasks));
                localStorage.setItem('taskmaster_counter', taskIdCounter.toString());
            } catch (e) {
                console.warn('Error saving tasks:', e);
            }
        }

        function saveChatMessages() {
            try {
                localStorage.setItem('taskmaster_chat', JSON.stringify(chatMessages));
            } catch (e) {
                console.warn('Error saving chat messages:', e);
            }
        }

        // Reset functionality with modern modal
        function resetApp() {
            const modal = document.getElementById('resetModal');
            modal.classList.add('active');
        }

        function closeResetModal() {
            const modal = document.getElementById('resetModal');
            modal.classList.remove('active');
        }

        function confirmResetApp() {
            // Limpiar todos los datos
            localStorage.clear();
            tasks = [];
            taskIdCounter = 1;
            chatMessages = [];
            
            // Resetear variables de selectores
            selectedFilterPriority = 'all';
            selectedFilterDate = '';
            selectedNewTaskPriority = '';
            selectedNewTaskSubject = '';
            selectedNewTaskDate = '';
            
            // Reset UI efficiently
            requestAnimationFrame(() => {
                renderTasks();
                updateStatistics();
                updateProgressTab();
                updateCharts();
                renderChatMessages();
                renderMainCalendar();
                setDefaultDate();
                
                // Resetear selectores visuales
                document.getElementById('filterPriorityText').textContent = 'Todas las prioridades';
                document.getElementById('filterDateText').textContent = 'Seleccionar fecha';
                document.getElementById('newTaskPriorityText').textContent = 'Seleccionar prioridad';
                document.getElementById('newTaskSubjectText').textContent = 'Seleccionar materia';
                
                // Resetear iconos
                document.querySelector('#filterPriorityDropdown').parentElement.querySelector('.selector-icon').textContent = '🎯';
                document.querySelector('#filterDateCalendar').parentElement.querySelector('.selector-icon').textContent = '📅';
                document.querySelector('#newTaskPriorityDropdown').parentElement.querySelector('.selector-icon').textContent = '🎯';
                document.querySelector('#newTaskSubjectDropdown').parentElement.querySelector('.selector-icon').textContent = '📚';
            });
            
            closeResetModal();
            
            // Mostrar mensaje de éxito
            setTimeout(() => {
                alert('✅ Aplicación restablecida exitosamente');
            }, 500);
        }
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9805f24d96a9dd20',t:'MTc1ODA4NDI0Ni4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
            --bg-color: #F5F5F5;
            --primary-color: #FF4500;
            --secondary-color: #2E8B57;
            --accent-color: #FFA07A;
            --text-color: #2F2F2F;
            --card-bg: #FFFFFF;
            --border-color: #D3D3D3;
            --shadow-color: rgba(255, 69, 0, 0.3);
            --glow-color: rgba(255, 69, 0, 0.5);
            --success-color: #2E8B57;
            --warning-color: #FFD700;
            --danger-color: #FF4500;
            --overdue-color: #DC143C;
        }

        body {
            font-family: 'Roboto', sans-serif;
            background: linear-gradient(135deg, var(--bg-color) 0%, var(--accent-color) 100%);
            color: var(--text-color);
            transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
            padding-bottom: 90px;
            position: relative;
            overflow-x: hidden;
            font-size: var(--base-font-size, 16px);
            min-height: 100vh;
            max-height: 100vh;
            overflow-y: auto;
        }

        /* Scroll container with border limit */
        .main-content {
            max-height: calc(100vh - 180px);
            overflow-y: auto;
            border: 3px solid var(--primary-color);
            border-radius: 20px;
            margin: 20px;
            padding: 20px;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            box-shadow: 0 8px 32px var(--shadow-color);
        }

        /* Custom scrollbar */
        .main-content::-webkit-scrollbar {
            width: 8px;
        }

        .main-content::-webkit-scrollbar-track {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
        }

        .main-content::-webkit-scrollbar-thumb {
            background: var(--primary-color);
            border-radius: 10px;
            opacity: 0.7;
        }

        .main-content::-webkit-scrollbar-thumb:hover {
            opacity: 1;
        }

        /* Dark Mode Variables */
        [data-dark-mode="true"] {
            --bg-color: #0F172A;
            --card-bg: #1E293B;
            --text-color: #F1F5F9;
            --border-color: #334155;
            --shadow-color: rgba(0, 0, 0, 0.5);
        }

        [data-dark-mode="true"][data-theme="palette1"] {
            --primary-color: #3B82F6;
            --secondary-color: #10B981;
            --accent-color: #1E293B;
            --glow-color: rgba(59, 130, 246, 0.4);
        }

        [data-dark-mode="true"][data-theme="palette2"] {
            --primary-color: #F59E0B;
            --secondary-color: #F97316;
            --accent-color: #1E293B;
            --glow-color: rgba(245, 158, 11, 0.4);
        }

        [data-dark-mode="true"][data-theme="palette3"] {
            --primary-color: #10B981;
            --secondary-color: #059669;
            --accent-color: #1E293B;
            --glow-color: rgba(16, 185, 129, 0.4);
        }

        [data-dark-mode="true"][data-theme="palette4"] {
            --primary-color: #8B5CF6;
            --secondary-color: #A855F7;
            --accent-color: #1E293B;
            --glow-color: rgba(139, 92, 246, 0.4);
        }

        [data-dark-mode="true"][data-theme="palette5"] {
            --primary-color: #EF4444;
            --secondary-color: #10B981;
            --accent-color: #1E293B;
            --glow-color: rgba(239, 68, 68, 0.4);
        }

        /* Font Size Classes */
        .font-size-small {
            --base-font-size: 14px;
        }

        .font-size-medium {
            --base-font-size: 16px;
        }

        .font-size-large {
            --base-font-size: 18px;
        }

        .font-size-xlarge {
            --base-font-size: 20px;
        }

        /* Scale all elements based on font size */
        .font-size-small .modern-card {
            padding: 16px;
        }

        .font-size-large .modern-card {
            padding: 28px;
        }

        .font-size-xlarge .modern-card {
            padding: 32px;
        }

        .font-size-small .modern-button {
            padding: 10px 20px;
            font-size: 12px;
        }

        .font-size-large .modern-button {
            padding: 16px 32px;
            font-size: 16px;
        }

        .font-size-xlarge .modern-button {
            padding: 18px 36px;
            font-size: 18px;
        }

        .font-size-small .bottom-nav-item span {
            font-size: 9px;
        }

        .font-size-large .bottom-nav-item span {
            font-size: 13px;
        }

        .font-size-xlarge .bottom-nav-item span {
            font-size: 14px;
        }

        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 20% 80%, var(--glow-color) 0%, transparent 50%),
                        radial-gradient(circle at 80% 20%, var(--glow-color) 0%, transparent 50%);
            pointer-events: none;
            z-index: -1;
            animation: backgroundPulse 8s ease-in-out infinite;
        }

        @keyframes backgroundPulse {
            0%, 100% { opacity: 0.3; }
            50% { opacity: 0.6; }
        }

        .modern-card {
            background: var(--card-bg);
            border: 2px solid var(--border-color);
            border-radius: 20px;
            box-shadow: 0 8px 32px var(--shadow-color), 
                        0 0 0 1px rgba(255, 255, 255, 0.1) inset;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
        }

        .modern-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: left 0.6s;
        }

        .modern-card:hover {
            transform: translateY(-8px) scale(1.02);
            box-shadow: 0 20px 60px var(--shadow-color), 
                        0 0 0 1px rgba(255, 255, 255, 0.2) inset,
                        0 0 30px var(--glow-color);
            border-color: var(--primary-color);
        }

        .modern-card:hover::before {
            left: 100%;
        }

        .modern-button {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            border: none;
            border-radius: 16px;
            padding: 14px 28px;
            font-weight: 600;
            font-size: 14px;
            transition: all 0.2s cubic-bezier(0.23, 1, 0.32, 1);
            cursor: pointer;
            position: relative;
            overflow: hidden;
            box-shadow: 0 4px 15px var(--shadow-color);
            will-change: transform, box-shadow;
            transform: translate3d(0, 0, 0);
            contain: layout style paint;
        }

        .modern-button::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            background: rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            transform: translate(-50%, -50%);
            transition: width 0.6s, height 0.6s;
        }

        .modern-button:hover {
            transform: translate3d(0, -3px, 0) scale(1.05);
            box-shadow: 0 12px 35px var(--shadow-color), 
                        0 0 20px var(--glow-color);
        }

        .modern-button:hover::before {
            width: 300px;
            height: 300px;
        }

        .modern-button:active {
            transform: translateY(-1px) scale(1.02);
        }

        @keyframes buttonBounce {
            0%, 100% { transform: translateY(-3px) scale(1.05); }
            50% { transform: translateY(-5px) scale(1.08); }
        }

        .modern-input {
            background: var(--card-bg);
            border: 2px solid var(--border-color);
            border-radius: 12px;
            padding: 14px 16px;
            font-size: 14px;
            transition: all 0.3s ease;
            width: 100%;
        }

        .modern-input:focus {
            outline: none;
            border-color: var(--primary-color);
            box-shadow: 0 0 0 3px rgba(74, 144, 226, 0.1);
        }

        /* Logo Styles */
        .app-logo {
            width: 40px;
            height: 40px;
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .logo-book {
            width: 28px;
            height: 20px;
            background: var(--primary-color);
            border-radius: 2px;
            position: relative;
            transform: perspective(20px) rotateX(5deg);
        }

        .logo-book::before {
            content: '';
            position: absolute;
            top: 2px;
            left: 2px;
            right: 2px;
            bottom: 2px;
            background: var(--card-bg);
            border-radius: 1px;
        }

        .logo-book::after {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 2px;
            height: 12px;
            background: var(--primary-color);
            transform: translate(-50%, -50%);
        }

        .logo-pencil {
            position: absolute;
            width: 20px;
            height: 2px;
            background: var(--secondary-color);
            border-radius: 1px;
            transform: rotate(45deg);
            top: 50%;
            left: 50%;
            margin-left: 8px;
            margin-top: -8px;
        }

        .logo-pencil::before {
            content: '';
            position: absolute;
            right: -3px;
            top: -1px;
            width: 0;
            height: 0;
            border-left: 3px solid var(--secondary-color);
            border-top: 2px solid transparent;
            border-bottom: 2px solid transparent;
        }

        /* Ultra-Smooth Bottom Navigation - 120+ FPS Optimized */
        .bottom-nav {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(135deg, #F0F8FF 0%, #E6F0FA 100%);
            border-top: 2px solid var(--border-color);
            padding: 10px 16px 14px;
            z-index: 50;
            box-shadow: 0 -12px 40px var(--shadow-color), 
                        0 0 0 1px rgba(255, 255, 255, 0.1) inset;
            backdrop-filter: blur(25px);
            will-change: transform;
            transform: translate3d(0, 0, 0);
            contain: layout style paint;
        }

        .bottom-nav::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, var(--primary-color), var(--secondary-color), var(--primary-color));
            animation: navGlow 3s ease-in-out infinite;
            will-change: opacity;
        }

        @keyframes navGlow {
            0%, 100% { 
                opacity: 0.6; 
                transform: scaleX(1) translateZ(0);
            }
            50% { 
                opacity: 1; 
                transform: scaleX(1.02) translateZ(0);
            }
        }

        .nav-container {
            display: grid;
            grid-template-columns: repeat(7, 1fr);
            gap: 8px;
            max-width: 750px;
            margin: 0 auto;
            align-items: center;
        }

        .bottom-nav-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 10px 6px;
            color: #6B7280;
            transition: all 0.15s cubic-bezier(0.23, 1, 0.32, 1);
            border-radius: 18px;
            cursor: pointer;
            position: relative;
            overflow: hidden;
            text-align: center;
            will-change: transform, box-shadow, color;
            transform: translate3d(0, 0, 0);
            user-select: none;
            contain: layout style paint;
        }

        .bottom-nav-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            opacity: 0;
            transition: all 0.25s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            border-radius: 18px;
            will-change: opacity, transform;
            transform: scale(0.9) translateZ(0);
        }

        .bottom-nav-item::after {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            background: rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            transform: translate(-50%, -50%) translateZ(0);
            transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            will-change: width, height;
        }

        .bottom-nav-item svg, .bottom-nav-item span {
            position: relative;
            z-index: 2;
            transition: all 0.25s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            will-change: transform;
            transform: translateZ(0);
        }

        .bottom-nav-item svg {
            margin-bottom: 2px;
        }

        .bottom-nav-item span {
            font-size: 11px;
            font-weight: 600;
        }

        .bottom-nav-item:hover {
            color: white;
            transform: translate3d(0, -5px, 0) scale(1.08);
            box-shadow: 0 12px 30px var(--shadow-color), 0 0 25px var(--glow-color);
        }

        .bottom-nav-item:hover::before {
            opacity: 1;
            transform: scale(1) translateZ(0);
        }

        .bottom-nav-item:hover::after {
            width: 100px;
            height: 100px;
        }

        .bottom-nav-item:hover svg {
            transform: scale(1.1) translateZ(0);
            animation: navIconBounce 0.6s cubic-bezier(0.68, -0.55, 0.265, 1.55);
        }

        .bottom-nav-item:active {
            transform: translateY(-3px) scale(1.05) translateZ(0);
            transition: transform 0.1s ease;
        }

        .bottom-nav-item.active {
            color: white;
            transform: translateY(-3px) scale(1.05) translateZ(0);
            animation: activeNavPulse 3s ease-in-out infinite;
        }

        .bottom-nav-item.active::before {
            opacity: 1;
            transform: scale(1) translateZ(0);
        }

        .bottom-nav-item.active svg {
            animation: activeNavIcon 2s ease-in-out infinite;
        }

        @keyframes activeNavPulse {
            0%, 100% { 
                box-shadow: 0 6px 20px var(--shadow-color), 0 0 20px var(--glow-color);
                transform: translateY(-3px) scale(1.05) translateZ(0);
            }
            50% { 
                box-shadow: 0 10px 30px var(--shadow-color), 0 0 30px var(--glow-color);
                transform: translateY(-4px) scale(1.08) translateZ(0);
            }
        }

        @keyframes navIconBounce {
            0% { transform: scale(1.1) translateZ(0); }
            30% { transform: scale(1.25) rotate(5deg) translateZ(0); }
            60% { transform: scale(1.15) rotate(-3deg) translateZ(0); }
            100% { transform: scale(1.1) translateZ(0); }
        }

        @keyframes activeNavIcon {
            0%, 100% { 
                transform: scale(1) translateZ(0); 
                filter: drop-shadow(0 0 5px rgba(255, 255, 255, 0.5));
            }
            50% { 
                transform: scale(1.05) translateZ(0); 
                filter: drop-shadow(0 0 8px rgba(255, 255, 255, 0.8));
            }
        }



        /* Google Calendar Style Enhanced - Ultra Smooth 60+ FPS */
        .calendar-container {
            background: var(--card-bg);
            border-radius: 16px;
            padding: 20px;
            box-shadow: 0 8px 32px var(--shadow-color), 
                        0 0 0 1px rgba(255, 255, 255, 0.1) inset;
            position: relative;
            overflow: hidden;
            transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            will-change: transform;
            transform: translateZ(0);
        }

        .calendar-container::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: conic-gradient(from 0deg, transparent, var(--glow-color), transparent);
            animation: calendarRotate 20s linear infinite;
            opacity: 0.03;
            will-change: transform;
            transform: translateZ(0);
        }

        @keyframes calendarRotate {
            0% { transform: rotate(0deg) translateZ(0); }
            100% { transform: rotate(360deg) translateZ(0); }
        }

        .calendar-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 24px;
            position: relative;
            z-index: 1;
        }

        .calendar-nav-btn {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            border: none;
            border-radius: 12px;
            width: 44px;
            height: 44px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.2s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            box-shadow: 0 4px 15px var(--shadow-color);
            position: relative;
            overflow: hidden;
            will-change: transform;
            transform: translateZ(0);
        }

        .calendar-nav-btn::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            background: rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            transform: translate(-50%, -50%) translateZ(0);
            transition: all 0.3s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            will-change: width, height;
        }

        .calendar-nav-btn:hover {
            transform: scale(1.08) translateZ(0);
            box-shadow: 0 8px 25px var(--shadow-color), 0 0 20px var(--glow-color);
        }

        .calendar-nav-btn:hover::before {
            width: 80px;
            height: 80px;
        }

        .calendar-nav-btn:active {
            transform: scale(1.02) translateZ(0);
            transition: transform 0.1s ease;
        }

        .calendar-grid {
            display: grid;
            grid-template-columns: repeat(7, 1fr);
            grid-template-rows: auto repeat(6, 1fr);
            gap: 1px;
            position: relative;
            z-index: 1;
            background: var(--border-color);
            border-radius: 12px;
            padding: 1px;
            overflow: hidden;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
            min-height: 280px;
        }

        .calendar-day-header {
            text-align: center;
            font-weight: 700;
            color: var(--primary-color);
            padding: 18px 8px;
            font-size: 14px;
            text-transform: uppercase;
            letter-spacing: 1px;
            background: linear-gradient(135deg, var(--card-bg) 0%, rgba(255, 255, 255, 0.9) 100%);
            border-bottom: 2px solid var(--border-color);
            position: relative;
            overflow: hidden;
            grid-row: 1;
        }

        .calendar-day-header::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.4), transparent);
            transition: left 0.6s ease;
        }

        .calendar-day-header:hover::before {
            left: 100%;
        }

        .calendar-days-container {
            display: contents;
        }

        .calendar-day {
            min-height: 45px;
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            justify-content: flex-start;
            padding: 6px 4px;
            cursor: pointer;
            transition: all 0.15s cubic-bezier(0.23, 1, 0.32, 1);
            font-size: 12px;
            font-weight: 500;
            position: relative;
            background: var(--card-bg);
            border: 1px solid transparent;
            will-change: transform, box-shadow, background-color;
            transform: translate3d(0, 0, 0);
            contain: layout style paint;
        }

        .calendar-day-number {
            font-size: 14px;
            font-weight: 600;
            margin-bottom: 4px;
            z-index: 2;
            position: relative;
            color: #6B7280;
            width: 20px;
            height: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            transition: all 0.2s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            will-change: transform, background-color;
            transform: translateZ(0);
        }

        .calendar-day-content {
            width: 100%;
            flex: 1;
            display: flex;
            flex-direction: column;
            gap: 4px;
            z-index: 2;
            position: relative;
        }

        .calendar-day:hover {
            background: #F9FAFB;
            border-color: #E5E7EB;
            transform: translate3d(0, -1px, 0);
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
        }

        .calendar-day:hover .calendar-day-number {
            background: #F3F4F6;
            color: #374151;
            transform: scale(1.05) translateZ(0);
        }

        .calendar-day.selected {
            background: #F0F9FF;
            border-color: #3B82F6;
            box-shadow: 0 2px 8px rgba(59, 130, 246, 0.15);
        }

        .calendar-day.selected .calendar-day-number {
            background: #3B82F6;
            color: white;
            transform: scale(1.05) translateZ(0);
        }

        .calendar-day.today {
            background: #FFFBEB;
            border-color: #F59E0B;
            position: relative;
        }

        .calendar-day.today .calendar-day-number {
            background: #F59E0B;
            color: white;
            font-weight: 700;
        }

        .calendar-day.other-month {
            opacity: 0.4;
            background: #FAFAFA;
        }

        .calendar-day.other-month .calendar-day-number {
            color: #D1D5DB;
        }

        .calendar-day.other-month:hover {
            opacity: 0.6;
            transform: translateY(-1px) translateZ(0);
        }

        /* Dark Mode Calendar Adjustments */
        [data-dark-mode="true"] .calendar-day {
            background: var(--card-bg);
            border-color: var(--border-color);
        }

        [data-dark-mode="true"] .calendar-day:hover {
            background: #334155;
            border-color: var(--primary-color);
        }

        [data-dark-mode="true"] .calendar-day.selected {
            background: rgba(59, 130, 246, 0.2);
            border-color: var(--primary-color);
        }

        [data-dark-mode="true"] .calendar-day.today {
            background: rgba(245, 158, 11, 0.2);
            border-color: #F59E0B;
        }

        [data-dark-mode="true"] .calendar-day.other-month {
            background: #0F172A;
            opacity: 0.5;
        }

        [data-dark-mode="true"] .calendar-day-number {
            color: var(--text-color);
        }

        [data-dark-mode="true"] .calendar-day:hover .calendar-day-number {
            background: rgba(59, 130, 246, 0.2);
            color: var(--text-color);
        }

        /* Ultra-smooth Calendar Transitions - 60+ FPS */
        .calendar-slide-left {
            animation: calendarSlideLeft 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }

        .calendar-slide-right {
            animation: calendarSlideRight 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }

        .calendar-fade-in {
            animation: calendarFadeIn 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }

        .calendar-fade-out {
            animation: calendarFadeOut 0.3s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }

        @keyframes calendarSlideLeft {
            0% { 
                opacity: 0; 
                transform: translateX(30px) scale(0.98) translateZ(0);
                filter: blur(2px);
            }
            100% { 
                opacity: 1; 
                transform: translateX(0) scale(1) translateZ(0);
                filter: blur(0px);
            }
        }

        @keyframes calendarSlideRight {
            0% { 
                opacity: 0; 
                transform: translateX(-30px) scale(0.98) translateZ(0);
                filter: blur(2px);
            }
            100% { 
                opacity: 1; 
                transform: translateX(0) scale(1) translateZ(0);
                filter: blur(0px);
            }
        }

        @keyframes calendarFadeIn {
            0% { 
                opacity: 0; 
                transform: translateY(20px) scale(0.96) translateZ(0);
                filter: blur(3px);
            }
            100% { 
                opacity: 1; 
                transform: translateY(0) scale(1) translateZ(0);
                filter: blur(0px);
            }
        }

        @keyframes calendarFadeOut {
            0% { 
                opacity: 1; 
                transform: translateY(0) scale(1) translateZ(0);
                filter: blur(0px);
            }
            100% { 
                opacity: 0; 
                transform: translateY(-20px) scale(0.96) translateZ(0);
                filter: blur(3px);
            }
        }

        .task-indicator {
            width: 100%;
            height: 12px;
            border-radius: 6px;
            font-size: 8px;
            padding: 1px 4px;
            margin-bottom: 1px;
            display: flex;
            align-items: center;
            gap: 2px;
            font-weight: 600;
            color: white;
            text-overflow: ellipsis;
            overflow: hidden;
            white-space: nowrap;
            animation: taskSlideIn 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.15);
            transition: all 0.2s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            will-change: transform;
            transform: translateZ(0);
            position: relative;
            overflow: hidden;
        }

        .task-indicator::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            transition: left 0.5s ease;
        }

        .task-indicator:hover {
            transform: translateY(-2px) scale(1.02) translateZ(0);
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.2);
        }

        .task-indicator:hover::before {
            left: 100%;
        }

        @keyframes taskSlideIn {
            0% { 
                opacity: 0; 
                transform: translateX(-15px) scale(0.9) translateZ(0);
                filter: blur(2px);
            }
            100% { 
                opacity: 1; 
                transform: translateX(0) scale(1) translateZ(0);
                filter: blur(0px);
            }
        }

        .task-indicator.completed {
            background: linear-gradient(135deg, #3CB371 0%, #2E8B57 100%);
            box-shadow: 0 3px 8px rgba(60, 179, 113, 0.3);
        }

        .task-indicator.completed:hover {
            box-shadow: 0 6px 15px rgba(60, 179, 113, 0.4);
        }

        .task-indicator.pending {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
        }

        .task-indicator.overdue {
            background: linear-gradient(135deg, #FF4500 0%, #DC143C 100%);
            animation: overdueFlash 2s ease-in-out infinite;
            box-shadow: 0 3px 8px rgba(255, 69, 0, 0.4);
        }

        .task-indicator.overdue:hover {
            box-shadow: 0 6px 15px rgba(255, 69, 0, 0.5);
        }

        .task-indicator.high-priority {
            background: linear-gradient(135deg, #FF4500 0%, #FF6347 100%);
            position: relative;
            box-shadow: 0 3px 8px rgba(255, 69, 0, 0.3);
        }

        .task-indicator.high-priority::after {
            content: '🔥';
            margin-right: 2px;
            animation: priorityBounce 1.5s ease-in-out infinite;
            filter: drop-shadow(0 0 3px rgba(255, 255, 255, 0.8));
        }

        @keyframes overdueFlash {
            0%, 100% { 
                opacity: 1; 
                box-shadow: 0 3px 8px rgba(255, 69, 0, 0.4);
            }
            50% { 
                opacity: 0.85; 
                box-shadow: 0 6px 15px rgba(255, 69, 0, 0.6);
            }
        }

        @keyframes priorityBounce {
            0%, 100% { transform: scale(1) translateZ(0); }
            50% { transform: scale(1.15) translateZ(0); }
        }

        .task-indicator.completed::after {
            content: '✓';
            margin-right: 2px;
            font-weight: bold;
            font-size: 12px;
            filter: drop-shadow(0 0 2px rgba(255, 255, 255, 0.8));
        }

        .more-tasks-indicator {
            font-size: 10px;
            color: var(--primary-color);
            font-weight: 600;
            text-align: center;
            padding: 2px;
            background: rgba(var(--primary-color), 0.1);
            border-radius: 4px;
            cursor: pointer;
            transition: all 0.2s ease;
        }

        .more-tasks-indicator:hover {
            background: var(--primary-color);
            color: white;
        }

        /* Enhanced Animated Tooltip Styles */
        .calendar-tooltip {
            position: absolute;
            background: linear-gradient(135deg, var(--card-bg) 0%, rgba(255, 255, 255, 0.95) 100%);
            border: 2px solid var(--primary-color);
            border-radius: 16px;
            padding: 16px;
            box-shadow: 0 12px 35px var(--shadow-color), 
                        0 0 0 1px rgba(255, 255, 255, 0.1) inset,
                        0 0 20px var(--glow-color);
            z-index: 1000;
            opacity: 0;
            transform: translateY(15px) scale(0.9) translateZ(0);
            transition: all 0.3s cubic-bezier(0.34, 1.56, 0.64, 1);
            pointer-events: none;
            max-width: 280px;
            min-width: 200px;
            will-change: transform, opacity;
            backdrop-filter: blur(10px);
            position: relative;
            overflow: hidden;
        }

        .calendar-tooltip::after {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.4), transparent);
            transition: left 0.6s ease;
        }

        .calendar-tooltip.show {
            opacity: 1;
            transform: translateY(0) scale(1) translateZ(0);
            animation: tooltipBounceIn 0.5s cubic-bezier(0.34, 1.56, 0.64, 1);
        }

        .calendar-tooltip.show::after {
            left: 100%;
        }

        @keyframes tooltipBounceIn {
            0% {
                opacity: 0;
                transform: translateY(20px) scale(0.8) rotateX(10deg) translateZ(0);
                filter: blur(3px);
            }
            60% {
                opacity: 0.8;
                transform: translateY(-5px) scale(1.05) rotateX(-2deg) translateZ(0);
                filter: blur(1px);
            }
            100% {
                opacity: 1;
                transform: translateY(0) scale(1) rotateX(0deg) translateZ(0);
                filter: blur(0px);
            }
        }

        .calendar-tooltip::before {
            content: '';
            position: absolute;
            top: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 0;
            height: 0;
            border-left: 10px solid transparent;
            border-right: 10px solid transparent;
            border-bottom: 10px solid var(--primary-color);
            filter: drop-shadow(0 -2px 4px rgba(0, 0, 0, 0.1));
        }

        .calendar-tooltip .tooltip-date {
            font-weight: 700;
            font-size: 14px;
            color: var(--primary-color);
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .calendar-tooltip .tooltip-date::before {
            content: '📅';
            font-size: 16px;
            animation: tooltipIconSpin 2s ease-in-out infinite;
        }

        @keyframes tooltipIconSpin {
            0%, 100% { transform: rotate(0deg) scale(1); }
            50% { transform: rotate(5deg) scale(1.1); }
        }

        .calendar-tooltip .tooltip-task {
            display: flex;
            align-items: center;
            gap: 8px;
            margin-bottom: 6px;
            padding: 6px 8px;
            border-radius: 8px;
            background: rgba(var(--primary-color), 0.05);
            transition: all 0.2s ease;
        }

        .calendar-tooltip .tooltip-task:hover {
            background: rgba(var(--primary-color), 0.1);
            transform: translateX(3px);
        }

        .calendar-tooltip .tooltip-task:last-child {
            margin-bottom: 0;
        }

        .calendar-tooltip .tooltip-more {
            text-align: center;
            font-size: 11px;
            color: var(--primary-color);
            font-weight: 600;
            margin-top: 8px;
            padding: 4px 8px;
            background: rgba(var(--primary-color), 0.1);
            border-radius: 12px;
            animation: tooltipPulse 2s ease-in-out infinite;
        }

        @keyframes tooltipPulse {
            0%, 100% { opacity: 0.7; transform: scale(1); }
            50% { opacity: 1; transform: scale(1.02); }
        }

        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0, 0, 0, 0.5);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 1000;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
        }

        .modal-overlay.active {
            opacity: 1;
            visibility: visible;
        }

        .modal-content {
            background: var(--card-bg);
            border-radius: 20px;
            padding: 32px;
            max-width: 500px;
            width: 90%;
            max-height: 90vh;
            overflow-y: auto;
            transform: scale(0.9) translateY(20px);
            transition: all 0.3s ease;
        }

        .modal-overlay.active .modal-content {
            transform: scale(1) translateY(0);
        }

        .priority-badge {
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 500;
        }

        .priority-high {
            background: #FEE2E2;
            color: #DC2626;
        }

        .priority-medium {
            background: #FEF3C7;
            color: #D97706;
        }

        .priority-low {
            background: #D1FAE5;
            color: #059669;
        }

        .tab-content {
            display: none;
        }

        .tab-content.active {
            display: block;
            animation: fadeIn 0.3s ease-out;
        }

        /* Enhanced Animations */
        .fade-in {
            animation: fadeInEnhanced 0.8s cubic-bezier(0.4, 0, 0.2, 1);
        }

        @keyframes fadeInEnhanced {
            0% { 
                opacity: 0; 
                transform: translateY(30px) scale(0.95);
                filter: blur(5px);
            }
            100% { 
                opacity: 1; 
                transform: translateY(0) scale(1);
                filter: blur(0px);
            }
        }

        .slide-up {
            animation: slideUpEnhanced 0.6s cubic-bezier(0.4, 0, 0.2, 1);
        }

        @keyframes slideUpEnhanced {
            0% { 
                opacity: 0; 
                transform: translateY(40px) rotateX(10deg);
            }
            100% { 
                opacity: 1; 
                transform: translateY(0) rotateX(0deg);
            }
        }

        .bounce-in {
            animation: bounceIn 0.8s cubic-bezier(0.68, -0.55, 0.265, 1.55);
        }

        @keyframes bounceIn {
            0% {
                opacity: 0;
                transform: scale(0.3) rotate(-10deg);
            }
            50% {
                opacity: 1;
                transform: scale(1.05) rotate(2deg);
            }
            70% {
                transform: scale(0.9) rotate(-1deg);
            }
            100% {
                opacity: 1;
                transform: scale(1) rotate(0deg);
            }
        }

        .float-animation {
            animation: floatAnimation 6s ease-in-out infinite;
        }

        @keyframes floatAnimation {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            33% { transform: translateY(-10px) rotate(1deg); }
            66% { transform: translateY(-5px) rotate(-1deg); }
        }

        /* Particle Effects */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .particle {
            position: absolute;
            width: 4px;
            height: 4px;
            background: var(--primary-color);
            border-radius: 50%;
            opacity: 0.6;
            animation: particleFloat 15s linear infinite;
        }

        @keyframes particleFloat {
            0% {
                transform: translateY(100vh) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 0.6;
            }
            90% {
                opacity: 0.6;
            }
            100% {
                transform: translateY(-100px) rotate(360deg);
                opacity: 0;
            }
        }

        /* Glow Effects */
        .glow-effect {
            position: relative;
        }

        .glow-effect::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: inherit;
            border-radius: inherit;
            filter: blur(20px);
            opacity: 0.3;
            z-index: -1;
            animation: glowPulse 3s ease-in-out infinite;
        }

        @keyframes glowPulse {
            0%, 100% { opacity: 0.3; transform: scale(1); }
            50% { opacity: 0.6; transform: scale(1.05); }
        }

        .theme-selector {
            display: flex;
            gap: 16px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .theme-option {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            cursor: pointer;
            border: 3px solid transparent;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }

        .theme-option::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: conic-gradient(from 0deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            animation: themeRotate 4s linear infinite;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        @keyframes themeRotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .theme-option:hover {
            transform: scale(1.15) rotate(5deg);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.3);
        }

        .theme-option:hover::before {
            opacity: 1;
        }

        .theme-option.active {
            border-color: var(--primary-color);
            box-shadow: 0 8px 25px var(--shadow-color), 0 0 20px var(--glow-color);
            transform: scale(1.1);
            animation: activeThemePulse 2s ease-in-out infinite;
        }

        @keyframes activeThemePulse {
            0%, 100% { 
                box-shadow: 0 8px 25px var(--shadow-color), 0 0 20px var(--glow-color);
            }
            50% { 
                box-shadow: 0 12px 35px var(--shadow-color), 0 0 30px var(--glow-color);
            }
        }

        .theme-1 { 
            background: linear-gradient(135deg, #F0F8FF 0%, #1E90FF 50%, #98FB98 100%);
        }
        .theme-2 { 
            background: linear-gradient(135deg, #FFFACD 0%, #FFD700 50%, #FFA500 100%);
        }
        .theme-3 { 
            background: linear-gradient(135deg, #E6F0FA 0%, #3CB371 50%, #20B2AA 100%);
        }
        .theme-4 { 
            background: linear-gradient(135deg, #E6E6FA 0%, #6A5ACD 50%, #BA55D3 100%);
        }
        .theme-5 { 
            background: linear-gradient(135deg, #F5F5F5 0%, #FF4500 50%, #2E8B57 100%);
        }

        /* Modern Font Size Selector */
        .font-size-selector {
            background: var(--card-bg);
            border: 2px solid var(--border-color);
            border-radius: 16px;
            padding: 8px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
        }

        /* Minimalist Task Creation Form */
        .minimalist-form {
            max-width: 600px;
            margin: 0 auto;
        }

        .form-field {
            margin-bottom: 24px;
            position: relative;
        }

        .form-field label {
            display: block;
            font-size: 14px;
            font-weight: 600;
            color: var(--text-color);
            margin-bottom: 8px;
            opacity: 0.8;
        }

        .minimalist-input {
            width: 100%;
            padding: 16px 20px;
            border: 2px solid var(--border-color);
            border-radius: 16px;
            background: var(--card-bg);
            font-size: 16px;
            color: var(--text-color);
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            outline: none;
        }

        .minimalist-input:focus {
            border-color: var(--primary-color);
            box-shadow: 0 0 0 4px rgba(var(--primary-color), 0.1);
            transform: translateY(-2px);
        }

        .minimalist-input::placeholder {
            color: #9CA3AF;
            opacity: 0.7;
        }

        /* Custom Dropdown Styles */
        .custom-dropdown {
            position: relative;
            width: 100%;
        }

        .dropdown-trigger {
            width: 100%;
            padding: 16px 20px;
            border: 2px solid var(--border-color);
            border-radius: 16px;
            background: var(--card-bg);
            font-size: 16px;
            color: var(--text-color);
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: all 0.15s cubic-bezier(0.23, 1, 0.32, 1);
            outline: none;
            will-change: transform, border-color, box-shadow;
            transform: translate3d(0, 0, 0);
            contain: layout style paint;
        }

        .dropdown-trigger:hover {
            border-color: var(--primary-color);
            transform: translate3d(0, -2px, 0);
            box-shadow: 0 4px 15px var(--shadow-color);
        }

        .dropdown-trigger.active {
            border-color: var(--primary-color);
            box-shadow: 0 0 0 4px rgba(var(--primary-color), 0.1);
        }

        .dropdown-arrow {
            width: 20px;
            height: 20px;
            transition: transform 0.3s ease;
            opacity: 0.6;
        }

        .dropdown-trigger.active .dropdown-arrow {
            transform: rotate(180deg);
        }

        .dropdown-menu {
            position: absolute;
            top: 100%;
            left: 0;
            right: 0;
            background: var(--card-bg);
            border: 2px solid var(--primary-color);
            border-radius: 16px;
            box-shadow: 0 12px 35px var(--shadow-color), 0 0 0 1px rgba(255, 255, 255, 0.1) inset;
            z-index: 1000;
            opacity: 0;
            visibility: hidden;
            transform: translate3d(0, -10px, 0) scale(0.95);
            transition: all 0.2s cubic-bezier(0.23, 1, 0.32, 1);
            max-height: 300px;
            overflow-y: auto;
            margin-top: 8px;
            will-change: transform, opacity;
            contain: layout style paint;
        }

        /* Special styling for calendar dropdown - no scroll, full display */
        #dateDropdown .dropdown-menu {
            max-height: none;
            overflow: visible;
            position: fixed;
            width: 400px;
            left: 50%;
            top: 50%;
            transform: translateX(-50%) translateY(-50%) scale(0.95);
            z-index: 2000;
        }

        #dateDropdown .dropdown-menu.show {
            transform: translateX(-50%) translateY(-50%) scale(1);
        }

        /* Calendar dropdown overlay */
        .calendar-dropdown-overlay {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0, 0, 0, 0.5);
            z-index: 1999;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
        }

        .calendar-dropdown-overlay.show {
            opacity: 1;
            visibility: visible;
        }

        /* Responsive calendar dropdown */
        @media (max-width: 768px) {
            #dateDropdown .dropdown-menu {
                width: 90vw;
                max-width: 350px;
            }
        }

        .dropdown-menu.show {
            opacity: 1;
            visibility: visible;
            transform: translate3d(0, 0, 0) scale(1);
        }

        .dropdown-item {
            padding: 16px 20px;
            cursor: pointer;
            transition: all 0.15s cubic-bezier(0.23, 1, 0.32, 1);
            border-bottom: 1px solid var(--border-color);
            display: flex;
            align-items: center;
            gap: 12px;
            will-change: transform, background-color, color;
            transform: translate3d(0, 0, 0);
            contain: layout style paint;
        }

        .dropdown-item:last-child {
            border-bottom: none;
        }

        .dropdown-item:hover {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            transform: translate3d(4px, 0, 0);
        }

        .dropdown-item:first-child {
            border-top-left-radius: 14px;
            border-top-right-radius: 14px;
        }

        .dropdown-item:last-child {
            border-bottom-left-radius: 14px;
            border-bottom-right-radius: 14px;
        }

        /* Priority Icons */
        .priority-icon {
            width: 20px;
            height: 20px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 12px;
            font-weight: bold;
        }

        .priority-high .priority-icon {
            background: #FEE2E2;
            color: #DC2626;
        }

        .priority-medium .priority-icon {
            background: #FEF3C7;
            color: #D97706;
        }

        .priority-low .priority-icon {
            background: #D1FAE5;
            color: #059669;
        }

        /* Subject Icons */
        .subject-icon {
            font-size: 18px;
            width: 24px;
            text-align: center;
        }

        /* Calendar Dropdown */
        .calendar-dropdown {
            padding: 20px;
        }

        .calendar-dropdown .calendar-container {
            border: none;
            box-shadow: none;
            padding: 0;
            background: transparent;
        }

        .calendar-dropdown .calendar-grid {
            background: transparent;
            border-radius: 12px;
            min-height: 240px;
        }

        .calendar-dropdown .calendar-day {
            min-height: 35px;
            font-size: 14px;
            border-radius: 8px;
            margin: 1px;
        }

        .calendar-dropdown .calendar-day:hover {
            background: var(--primary-color);
            color: white;
            transform: scale(1.05);
        }

        .calendar-dropdown .calendar-day.selected {
            background: var(--primary-color);
            color: white;
            font-weight: bold;
        }

        /* Form Actions */
        .form-actions {
            display: flex;
            gap: 16px;
            margin-top: 32px;
            justify-content: center;
        }

        .form-actions .modern-button {
            flex: 1;
            max-width: 200px;
            padding: 16px 32px;
            font-size: 16px;
            font-weight: 600;
        }

        .clear-button {
            background: transparent;
            border: 2px solid var(--border-color);
            color: var(--text-color);
            transition: all 0.3s ease;
        }

        .clear-button:hover {
            border-color: var(--primary-color);
            background: var(--primary-color);
            color: white;
            transform: translateY(-2px);
        }

        /* Responsive adjustments */
        @media (max-width: 768px) {
            .minimalist-form {
                padding: 0 16px;
            }
            
            .form-actions {
                flex-direction: column;
            }
            
            .form-actions .modern-button {
                max-width: none;
            }
        }

        .font-size-options {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 8px;
        }

        .font-size-option {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 16px 12px;
            border: 2px solid transparent;
            border-radius: 12px;
            background: transparent;
            cursor: pointer;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
        }

        .font-size-option::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            opacity: 0;
            transition: opacity 0.3s ease;
            border-radius: 10px;
        }

        .font-size-option .size-icon {
            font-size: 20px;
            font-weight: 600;
            margin-bottom: 8px;
            color: var(--text-color);
            transition: all 0.3s ease;
            position: relative;
            z-index: 2;
        }

        .font-size-option span {
            font-size: 12px;
            font-weight: 500;
            color: var(--text-color);
            transition: all 0.3s ease;
            position: relative;
            z-index: 2;
        }

        .font-size-option:hover {
            border-color: var(--primary-color);
            transform: translateY(-2px) scale(1.02);
            box-shadow: 0 8px 25px var(--shadow-color);
        }

        .font-size-option:hover::before {
            opacity: 0.1;
        }

        .font-size-option.active {
            border-color: var(--primary-color);
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            transform: translateY(-2px);
            box-shadow: 0 8px 25px var(--shadow-color), 0 0 20px var(--glow-color);
        }

        .font-size-option.active .size-icon,
        .font-size-option.active span {
            color: white;
        }

        .font-size-option[data-size="small"] .size-icon {
            font-size: 16px;
        }

        .font-size-option[data-size="medium"] .size-icon {
            font-size: 20px;
        }

        .font-size-option[data-size="large"] .size-icon {
            font-size: 24px;
        }

        .font-size-option[data-size="xlarge"] .size-icon {
            font-size: 28px;
        }

        .chat-container {
            height: 400px;
            display: flex;
            flex-direction: column;
        }

        .chat-messages {
            flex: 1;
            overflow-y: auto;
            padding: 16px;
            border: 1px solid var(--border-color);
            border-radius: 12px;
            margin-bottom: 16px;
            background: var(--bg-color);
        }

        .chat-input-container {
            display: flex;
            gap: 12px;
        }

        .filter-container {
            display: flex;
            gap: 12px;
            margin-bottom: 20px;
            flex-wrap: wrap;
        }

        @media (max-width: 768px) {
            .modal-content {
                padding: 24px;
                margin: 16px;
            }
            
            .filter-container {
                flex-direction: column;
            }

            .bottom-nav-item span {
                font-size: 10px;
            }

            .calendar-grid {
                gap: 4px;
            }

            .calendar-day {
                font-size: 12px;
            }
        }
    </style>
</head>

<body data-theme="palette1">
    <!-- Particle Effects -->
    <div class="particles" id="particles"></div>

    <!-- Header with Logo -->
    <header class="modern-card rounded-none border-0 border-b p-6 mb-8 glow-effect">
        <div class="max-w-7xl mx-auto">
            <div class="flex items-center justify-between">
                <div class="flex items-center space-x-4">
                    <!-- Logo Estilizado -->
                    <div class="app-logo float-animation">
                        <div class="logo-book"></div>
                        <div class="logo-pencil"></div>
                    </div>
                    <div>
                        <h1 class="text-4xl font-bold bounce-in" style="color: var(--primary-color)">TaskMaster AI</h1>
                        <p class="text-gray-600 text-sm fade-in">Gestión Inteligente de Tareas</p>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <div class="main-content max-w-7xl mx-auto">
        
        <!-- Tareas Pendientes Tab -->
        <div id="pendientes-tab" class="tab-content active">
            <div class="modern-card p-6 fade-in">
                <h2 class="text-2xl font-semibold mb-6">Tareas Pendientes</h2>
                
                <div class="filter-container">
                    <select id="filterPriority" onchange="filterTasks()" class="modern-input w-auto">
                        <option value="all">Todas las prioridades</option>
                        <option value="high">🔴 Alta</option>
                        <option value="medium">🟡 Media</option>
                        <option value="low">🟢 Baja</option>
                    </select>
                    
                    <input type="date" id="filterDate" onchange="filterTasks()" class="modern-input w-auto">
                    
                    <span class="text-sm text-gray-600 flex items-center">
                        Total: <span id="taskCount" class="font-semibold ml-1" style="color: var(--primary-color)">0</span>
                    </span>
                </div>
                
                <div id="taskList" class="space-y-4">
                    <!-- Tasks will be rendered here -->
                </div>
                
                <div id="emptyState" class="text-center py-16 text-gray-500">
                    <div class="text-6xl mb-4">✅</div>
                    <p class="text-xl mb-2">No hay tareas pendientes</p>
                    <p class="text-sm">¡Excelente trabajo! Todas tus tareas están completadas</p>
                </div>
            </div>
        </div>

        <!-- Chat IA Tab -->
        <div id="chat-tab" class="tab-content">
            <div class="modern-card p-6 fade-in">
                <h2 class="text-2xl font-semibold mb-6">Chat con IA</h2>
                
                <div class="chat-container">
                    <div id="chatMessages" class="chat-messages">
                        <div class="text-center py-8 text-gray-500">
                            <p>🤖 ¡Hola! Soy tu asistente IA. ¿En qué puedo ayudarte hoy?</p>
                        </div>
                    </div>
                    
                    <div class="chat-input-container">
                        <input 
                            type="text" 
                            id="chatInput" 
                            placeholder="Escribe tu mensaje aquí..."
                            class="modern-input flex-1"
                            onkeypress="handleChatKeyPress(event)"
                        >
                        <button onclick="sendChatMessage()" class="modern-button">
                            Enviar
                        </button>
                    </div>
                </div>
            </div>
        </div>

        <!-- Crear Tarea Tab -->
        <div id="crear-tab" class="tab-content">
            <div class="modern-card p-8 fade-in">
                <div class="text-center mb-8">
                    <h2 class="text-3xl font-bold mb-2" style="color: var(--primary-color)">✨ Nueva Tarea</h2>
                    <p class="text-gray-600">Crea tu tarea de forma simple y elegante</p>
                </div>
                
                <form id="createTaskForm" class="minimalist-form">
                    <!-- Título -->
                    <div class="form-field">
                        <label for="newTaskTitle">¿Qué necesitas hacer?</label>
                        <input 
                            type="text" 
                            id="newTaskTitle" 
                            placeholder="Escribe el título de tu tarea..."
                            class="minimalist-input"
                            required
                        >
                    </div>

                    <!-- Fecha -->
                    <div class="form-field">
                        <label>¿Para cuándo es?</label>
                        <div class="custom-dropdown" id="dateDropdown">
                            <button type="button" class="dropdown-trigger" onclick="toggleDropdown('dateDropdown')">
                                <span id="selectedDateText">Seleccionar fecha</span>
                                <svg class="dropdown-arrow" fill="currentColor" viewBox="0 0 20 20">
                                    <path d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"/>
                                </svg>
                            </button>
                            <div class="dropdown-menu">
                                <div class="calendar-dropdown">
                                    <div class="calendar-container">
                                        <div class="calendar-header">
                                            <button type="button" onclick="previousMonth()" class="calendar-nav-btn">
                                                <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                                                    <path d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z"/>
                                                </svg>
                                            </button>
                                            
                                            <h3 id="currentMonth" class="font-semibold text-sm" style="color: var(--primary-color)"></h3>
                                            
                                            <button type="button" onclick="nextMonth()" class="calendar-nav-btn">
                                                <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                                                    <path d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"/>
                                                </svg>
                                            </button>
                                        </div>
                                        
                                        <div class="calendar-grid">
                                            <div class="calendar-day-header">D</div>
                                            <div class="calendar-day-header">L</div>
                                            <div class="calendar-day-header">M</div>
                                            <div class="calendar-day-header">M</div>
                                            <div class="calendar-day-header">J</div>
                                            <div class="calendar-day-header">V</div>
                                            <div class="calendar-day-header">S</div>
                                            <div id="calendarDays" class="calendar-days-container"></div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <input type="hidden" id="newTaskDate" required>
                    </div>

                    <!-- Prioridad -->
                    <div class="form-field">
                        <label>¿Qué tan importante es?</label>
                        <div class="custom-dropdown" id="priorityDropdown">
                            <button type="button" class="dropdown-trigger" onclick="toggleDropdown('priorityDropdown')">
                                <span id="selectedPriorityText">Seleccionar prioridad</span>
                                <svg class="dropdown-arrow" fill="currentColor" viewBox="0 0 20 20">
                                    <path d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"/>
                                </svg>
                            </button>
                            <div class="dropdown-menu">
                                <div class="dropdown-item priority-high" onclick="selectPriority('high', '🔥 Alta prioridad')">
                                    <div class="priority-icon">🔥</div>
                                    <div>
                                        <div class="font-semibold">Alta prioridad</div>
                                        <div class="text-sm opacity-75">Urgente e importante</div>
                                    </div>
                                </div>
                                <div class="dropdown-item priority-medium" onclick="selectPriority('medium', '⚡ Prioridad media')">
                                    <div class="priority-icon">⚡</div>
                                    <div>
                                        <div class="font-semibold">Prioridad media</div>
                                        <div class="text-sm opacity-75">Importante pero no urgente</div>
                                    </div>
                                </div>
                                <div class="dropdown-item priority-low" onclick="selectPriority('low', '🌱 Baja prioridad')">
                                    <div class="priority-icon">🌱</div>
                                    <div>
                                        <div class="font-semibold">Baja prioridad</div>
                                        <div class="text-sm opacity-75">Cuando tengas tiempo</div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <input type="hidden" id="newTaskPriority" required>
                    </div>

                    <!-- Materia -->
                    <div class="form-field">
                        <label>¿De qué materia es?</label>
                        <div class="custom-dropdown" id="subjectDropdown">
                            <button type="button" class="dropdown-trigger" onclick="toggleDropdown('subjectDropdown')">
                                <span id="selectedSubjectText">Seleccionar materia</span>
                                <svg class="dropdown-arrow" fill="currentColor" viewBox="0 0 20 20">
                                    <path d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"/>
                                </svg>
                            </button>
                            <div class="dropdown-menu">
                                <div class="dropdown-item" onclick="selectSubject('Matemáticas')">
                                    <div class="subject-icon">📐</div>
                                    <span>Matemáticas</span>
                                </div>
                                <div class="dropdown-item" onclick="selectSubject('Lengua y Literatura')">
                                    <div class="subject-icon">📚</div>
                                    <span>Lengua y Literatura</span>
                                </div>
                                <div class="dropdown-item" onclick="selectSubject('Inglés')">
                                    <div class="subject-icon">🌍</div>
                                    <span>Inglés</span>
                                </div>
                                <div class="dropdown-item" onclick="selectSubject('Ciencias Sociales')">
                                    <div class="subject-icon">🏛️</div>
                                    <span>Ciencias Sociales</span>
                                </div>
                                <div class="dropdown-item" onclick="selectSubject('Ciencias Naturales')">
                                    <div class="subject-icon">🌿</div>
                                    <span>Ciencias Naturales</span>
                                </div>
                                <div class="dropdown-item" onclick="selectSubject('Química')">
                                    <div class="subject-icon">🧪</div>
                                    <span>Química</span>
                                </div>
                                <div class="dropdown-item" onclick="selectSubject('Física')">
                                    <div class="subject-icon">⚛️</div>
                                    <span>Física</span>
                                </div>
                                <div class="dropdown-item" onclick="selectSubject('Otro')">
                                    <div class="subject-icon">📝</div>
                                    <span>Otro</span>
                                </div>
                            </div>
                        </div>
                        <input type="hidden" id="newTaskSubject" required>
                    </div>

                    <!-- Descripción -->
                    <div class="form-field">
                        <label for="newTaskDescription">Detalles adicionales (opcional)</label>
                        <textarea 
                            id="newTaskDescription" 
                            placeholder="Agrega más información sobre tu tarea..."
                            rows="3"
                            class="minimalist-input resize-none"
                        ></textarea>
                    </div>
                    
                    <!-- Botones -->
                    <div class="form-actions">
                        <button type="button" onclick="clearCreateForm()" class="modern-button clear-button">
                            🗑️ Limpiar
                        </button>
                        <button type="submit" class="modern-button">
                            ✨ Crear Tarea
                        </button>
                    </div>
                </form>
            </div>
        </div>

        <!-- Calendario Tab -->
        <div id="calendario-tab" class="tab-content">
            <div class="modern-card p-6 fade-in">
                <h2 class="text-2xl font-semibold mb-6">Calendario Interactivo</h2>
                
                <div class="calendar-container">
                    <div class="calendar-header">
                        <button onclick="previousCalendarMonth()" class="calendar-nav-btn">
                            <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z"/>
                            </svg>
                        </button>
                        
                        <h3 id="calendarCurrentMonth" class="font-semibold text-xl" style="color: var(--primary-color)"></h3>
                        
                        <button onclick="nextCalendarMonth()" class="calendar-nav-btn">
                            <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"/>
                            </svg>
                        </button>
                    </div>
                    
                    <div class="calendar-grid">
                        <div class="calendar-day-header">Dom</div>
                        <div class="calendar-day-header">Lun</div>
                        <div class="calendar-day-header">Mar</div>
                        <div class="calendar-day-header">Mié</div>
                        <div class="calendar-day-header">Jue</div>
                        <div class="calendar-day-header">Vie</div>
                        <div class="calendar-day-header">Sáb</div>
                        <div id="mainCalendarDays" class="calendar-days-container"></div>
                    </div>
                </div>
                
                <div id="selectedDateTasks" class="mt-6">
                    <!-- Tasks for selected date will appear here -->
                </div>
            </div>
        </div>

        <!-- Progreso Tab -->
        <div id="progreso-tab" class="tab-content">
            <div class="space-y-6 fade-in">
                <div class="modern-card p-6">
                    <h2 class="text-2xl font-semibold mb-6">📈 Progreso General</h2>
                    
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-8">
                        <div class="text-center">
                            <div class="w-24 h-24 mx-auto mb-4 relative">
                                <svg class="w-24 h-24 transform -rotate-90" viewBox="0 0 100 100">
                                    <circle cx="50" cy="50" r="40" stroke="var(--border-color)" stroke-width="8" fill="none"/>
                                    <circle id="progressCircle" cx="50" cy="50" r="40" stroke="var(--success-color)" stroke-width="8" fill="none" 
                                            stroke-dasharray="251.2" stroke-dashoffset="251.2" stroke-linecap="round"/>
                                </svg>
                                <div class="absolute inset-0 flex items-center justify-center">
                                    <span id="circleProgressText" class="text-xl font-bold" style="color: var(--primary-color)">0%</span>
                                </div>
                            </div>
                            <h3 class="font-semibold text-lg">Completado</h3>
                            <p class="text-gray-600 text-sm">Tareas finalizadas</p>
                        </div>
                        
                        <div class="text-center">
                            <div class="text-4xl font-bold mb-2" style="color: var(--primary-color)" id="totalTasksCount">0</div>
                            <h3 class="font-semibold text-lg">Total Tareas</h3>
                            <p class="text-gray-600 text-sm">Creadas hasta ahora</p>
                        </div>
                        
                        <div class="text-center">
                            <div class="text-4xl font-bold mb-2" style="color: var(--warning-color)" id="streakCount">0</div>
                            <h3 class="font-semibold text-lg">Racha Actual</h3>
                            <p class="text-gray-600 text-sm">Días consecutivos</p>
                        </div>
                    </div>
                    
                    <div class="grid grid-cols-2 md:grid-cols-4 gap-4 mb-6">
                        <div class="modern-card p-4 text-center">
                            <div class="text-2xl font-bold" style="color: var(--success-color)" id="completedCountProgress">0</div>
                            <div class="text-sm text-gray-600">Completadas</div>
                        </div>
                        <div class="modern-card p-4 text-center">
                            <div class="text-2xl font-bold" style="color: var(--warning-color)" id="pendingCountProgress">0</div>
                            <div class="text-sm text-gray-600">Pendientes</div>
                        </div>
                        <div class="modern-card p-4 text-center">
                            <div class="text-2xl font-bold" style="color: var(--danger-color)" id="highPriorityCountProgress">0</div>
                            <div class="text-sm text-gray-600">Alta Prioridad</div>
                        </div>
                        <div class="modern-card p-4 text-center">
                            <div class="text-2xl font-bold" style="color: var(--overdue-color)" id="overdueCountProgress">0</div>
                            <div class="text-sm text-gray-600">Vencidas</div>
                        </div>
                    </div>
                    
                    <div class="space-y-4">
                        <div>
                            <div class="flex justify-between items-center mb-2">
                                <span class="text-sm font-medium">Progreso Semanal</span>
                                <span class="text-sm" style="color: var(--primary-color)" id="weeklyProgressText">0%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-3">
                                <div id="weeklyProgressBar" class="h-3 rounded-full transition-all duration-500" style="background: var(--primary-color); width: 0%"></div>
                            </div>
                        </div>
                        
                        <div>
                            <div class="flex justify-between items-center mb-2">
                                <span class="text-sm font-medium">Productividad</span>
                                <span class="text-sm" style="color: var(--success-color)" id="productivityText">0%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-3">
                                <div id="productivityBar" class="h-3 rounded-full transition-all duration-500" style="background: var(--success-color); width: 0%"></div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="modern-card p-6">
                    <h3 class="text-lg font-semibold mb-4">🏆 Logros Recientes</h3>
                    <div id="achievementsList" class="space-y-3">
                        <!-- Achievements will be populated here -->
                    </div>
                </div>
            </div>
        </div>

        <!-- Estadísticas Tab -->
        <div id="estadisticas-tab" class="tab-content">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-6 fade-in">
                <div class="modern-card p-6">
                    <h3 class="text-lg font-semibold mb-4">📊 Progreso Semanal</h3>
                    <canvas id="weeklyChart" width="400" height="200"></canvas>
                </div>
                
                <div class="modern-card p-6">
                    <h3 class="text-lg font-semibold mb-4">🎯 Por Prioridad</h3>
                    <canvas id="priorityChart" width="400" height="200"></canvas>
                </div>
                
                <div class="modern-card p-6 lg:col-span-2">
                    <h3 class="text-lg font-semibold mb-4">📈 Estadísticas Generales</h3>
                    <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
                        <div class="text-center">
                            <div class="text-2xl font-bold text-green-600" id="completedCount">0</div>
                            <div class="text-sm text-gray-600">Completadas</div>
                        </div>
                        <div class="text-center">
                            <div class="text-2xl font-bold text-yellow-600" id="pendingCount">0</div>
                            <div class="text-sm text-gray-600">Pendientes</div>
                        </div>
                        <div class="text-center">
                            <div class="text-2xl font-bold text-red-600" id="highPriorityCount">0</div>
                            <div class="text-sm text-gray-600">Alta Prioridad</div>
                        </div>
                        <div class="text-center">
                            <div class="text-2xl font-bold" style="color: var(--primary-color)" id="progressPercentage">0%</div>
                            <div class="text-sm text-gray-600">Progreso</div>
                        </div>
                    </div>
                    
                    <div class="mt-6">
                        <div class="w-full bg-gray-200 rounded-full h-3">
                            <div id="progressBar" class="h-3 rounded-full transition-all duration-500" style="background: var(--primary-color); width: 0%"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Ajustes Tab -->
        <div id="ajustes-tab" class="tab-content">
            <div class="modern-card p-6 fade-in max-w-2xl mx-auto">
                <h2 class="text-2xl font-semibold mb-6">Configuración</h2>
                
                <div class="space-y-8">
                    <div>
                        <h3 class="text-lg font-medium mb-4">🎨 Paletas de Color</h3>
                        <div class="theme-selector">
                            <div class="theme-option theme-1 active" onclick="changeTheme('palette1')" title="Azul Océano"></div>
                            <div class="theme-option theme-2" onclick="changeTheme('palette2')" title="Coral Sunset"></div>
                            <div class="theme-option theme-3" onclick="changeTheme('palette3')" title="Verde Natura"></div>
                            <div class="theme-option theme-4" onclick="changeTheme('palette4')" title="Azul Profesional"></div>
                            <div class="theme-option theme-5" onclick="changeTheme('palette5')" title="Tierra Cálida"></div>
                        </div>
                        <p class="text-sm text-gray-600 mt-2">Selecciona tu paleta de colores favorita</p>
                    </div>
                    
                    <div>
                        <h3 class="text-lg font-medium mb-4">📏 Tamaño de Fuente</h3>
                        <div class="space-y-4 mb-6">
                            <div class="font-size-selector">
                                <div class="font-size-options">
                                    <button type="button" class="font-size-option" data-size="small" onclick="changeFontSize('small')">
                                        <div class="size-icon">Aa</div>
                                        <span>Pequeño</span>
                                    </button>
                                    <button type="button" class="font-size-option active" data-size="medium" onclick="changeFontSize('medium')">
                                        <div class="size-icon">Aa</div>
                                        <span>Mediano</span>
                                    </button>
                                    <button type="button" class="font-size-option" data-size="large" onclick="changeFontSize('large')">
                                        <div class="size-icon">Aa</div>
                                        <span>Grande</span>
                                    </button>
                                    <button type="button" class="font-size-option" data-size="xlarge" onclick="changeFontSize('xlarge')">
                                        <div class="size-icon">Aa</div>
                                        <span>Extra Grande</span>
                                    </button>
                                </div>
                            </div>
                            <p class="text-sm text-gray-600">Ajusta el tamaño de toda la interfaz</p>
                        </div>
                    </div>
                    
                    <div>
                        <h3 class="text-lg font-medium mb-4">🌙 Modo Oscuro</h3>
                        <div class="mb-6">
                            <label class="flex items-center justify-between">
                                <span>Activar modo oscuro</span>
                                <button 
                                    id="darkModeToggle" 
                                    onclick="toggleDarkMode()" 
                                    class="relative inline-flex h-6 w-11 items-center rounded-full transition-colors focus:outline-none focus:ring-2 focus:ring-offset-2"
                                    style="background-color: var(--border-color); focus:ring-color: var(--primary-color);"
                                >
                                    <span id="darkModeSlider" class="inline-block h-4 w-4 transform rounded-full bg-white transition-transform translate-x-1"></span>
                                </button>
                            </label>
                            <p class="text-sm text-gray-600 mt-2">Cambia entre tema claro y oscuro</p>
                        </div>
                    </div>
                    
                    <div>
                        <h3 class="text-lg font-medium mb-4">🔧 Preferencias</h3>
                        <div class="space-y-4">
                            <label class="flex items-center justify-between">
                                <span>Animaciones suaves</span>
                                <input type="checkbox" checked class="w-5 h-5 rounded" style="accent-color: var(--primary-color)">
                            </label>
                            <label class="flex items-center justify-between">
                                <span>Notificaciones</span>
                                <input type="checkbox" checked class="w-5 h-5 rounded" style="accent-color: var(--primary-color)">
                            </label>
                            <label class="flex items-center justify-between">
                                <span>Recordatorios automáticos</span>
                                <input type="checkbox" class="w-5 h-5 rounded" style="accent-color: var(--primary-color)">
                            </label>
                        </div>
                    </div>
                    
                    <div class="pt-4 border-t border-gray-200">
                        <button onclick="resetApp()" class="modern-button bg-red-500 hover:bg-red-600">
                            🔄 Restablecer Aplicación
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Bottom Navigation Bar -->
    <nav class="bottom-nav">
        <div class="nav-container">
            <button onclick="switchTab('pendientes')" class="bottom-nav-item active" data-tab="pendientes">
                <svg class="w-5 h-5 mb-1" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"/>
                </svg>
                <span class="text-xs font-medium">Pendientes</span>
            </button>
            
            <button onclick="switchTab('chat')" class="bottom-nav-item" data-tab="chat">
                <svg class="w-5 h-5 mb-1" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"/>
                </svg>
                <span class="text-xs font-medium">Chat IA</span>
            </button>
            
            <button onclick="switchTab('progreso')" class="bottom-nav-item" data-tab="progreso">
                <svg class="w-5 h-5 mb-1" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M13 7h8m0 0v8m0-8l-8 8-4-4-6 6"/>
                </svg>
                <span class="text-xs font-medium">Progreso</span>
            </button>
            
            <button onclick="switchTab('crear')" class="bottom-nav-item" data-tab="crear">
                <svg class="w-5 h-5 mb-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4v16m8-8H4"/>
                </svg>
                <span class="text-xs font-medium">Crear</span>
            </button>
            
            <button onclick="switchTab('calendario')" class="bottom-nav-item" data-tab="calendario">
                <svg class="w-5 h-5 mb-1" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M8 7V3a1 1 0 012 0v4h4V3a1 1 0 012 0v4h2a3 3 0 013 3v8a3 3 0 01-3 3H6a3 3 0 01-3-3v-8a3 3 0 013-3h2zM6 9a1 1 0 00-1 1v8a1 1 0 001 1h12a1 1 0 001-1v-8a1 1 0 00-1-1H6z"/>
                </svg>
                <span class="text-xs font-medium">Calendario</span>
            </button>
            
            <button onclick="switchTab('estadisticas')" class="bottom-nav-item" data-tab="estadisticas">
                <svg class="w-5 h-5 mb-1" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z"/>
                </svg>
                <span class="text-xs font-medium">Estadísticas</span>
            </button>
            
            <button onclick="switchTab('ajustes')" class="bottom-nav-item" data-tab="ajustes">
                <svg class="w-5 h-5 mb-1" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"/>
                    <path d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"/>
                </svg>
                <span class="text-xs font-medium">Ajustes</span>
            </button>
        </div>
    </nav>

    <script>
        // Global variables
        let tasks = JSON.parse(localStorage.getItem('taskmaster_tasks')) || [];
        let taskIdCounter = parseInt(localStorage.getItem('taskmaster_counter')) || 1;
        let chatMessages = JSON.parse(localStorage.getItem('taskmaster_chat')) || [];
        let currentDate = new Date();
        let calendarDate = new Date();
        let selectedDate = new Date();

        // Performance optimizations and preloading
        function preloadElements() {
            // Preload critical CSS animations
            const preloadDiv = document.createElement('div');
            preloadDiv.style.position = 'absolute';
            preloadDiv.style.left = '-9999px';
            preloadDiv.style.opacity = '0';
            preloadDiv.innerHTML = `
                <div class="calendar-fade-in"></div>
                <div class="calendar-slide-left"></div>
                <div class="calendar-slide-right"></div>
                <div class="task-indicator completed"></div>
                <div class="task-indicator overdue"></div>
                <div class="calendar-tooltip show"></div>
            `;
            document.body.appendChild(preloadDiv);
            
            // Remove preload elements after a short delay
            setTimeout(() => {
                document.body.removeChild(preloadDiv);
            }, 100);
        }

        // Ultra-optimized tab switching with 120+ FPS performance
        function switchTab(tabName) {
            // Use double requestAnimationFrame for ultra-smooth transitions
            requestAnimationFrame(() => {
                requestAnimationFrame(() => {
                    // Batch DOM operations for better performance
                    const tabs = document.querySelectorAll('.tab-content');
                    const navItems = document.querySelectorAll('.bottom-nav-item');
                    
                    // Remove active classes in a single loop
                    tabs.forEach(tab => tab.classList.remove('active'));
                    navItems.forEach(item => item.classList.remove('active'));
                    
                    // Add active classes
                    const targetTab = document.getElementById(`${tabName}-tab`);
                    const navItem = document.querySelector(`[data-tab="${tabName}"]`);
                    
                    if (targetTab) targetTab.classList.add('active');
                    if (navItem) navItem.classList.add('active');

                    // Defer heavy operations
                    if (tabName === 'estadisticas') {
                        setTimeout(drawCharts, 50);
                    }
                });
            });
        }

        // Initialize app with performance optimizations
        document.addEventListener('DOMContentLoaded', function() {
            // Preload elements for smooth animations
            preloadElements();
            
            // Initialize core functionality
            renderTasks();
            updateStatistics();
            updateProgressTab();
            renderChatMessages();
            drawCharts();
            renderCalendar();
            renderMainCalendar();
            setDefaultDate();
            createParticles();
            
            // Optimized form submission with passive listeners
            document.getElementById('createTaskForm').addEventListener('submit', function(e) {
                e.preventDefault();
                createNewTask();
            }, { passive: false });

            // Add performance monitoring
            if ('performance' in window) {
                window.addEventListener('load', () => {
                    const perfData = performance.getEntriesByType('navigation')[0];
                    console.log(`TaskMaster AI loaded in ${Math.round(perfData.loadEventEnd - perfData.fetchStart)}ms`);
                });
            }
        });

        // Create floating particles
        function createParticles() {
            const particlesContainer = document.getElementById('particles');
            const particleCount = 20;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.animationDelay = Math.random() * 15 + 's';
                particle.style.animationDuration = (Math.random() * 10 + 10) + 's';
                particlesContainer.appendChild(particle);
            }
        }

        // Navigation functions
        function switchTab(tabName) {
            // Remove active class from all tabs and nav items
            document.querySelectorAll('.tab-content').forEach(tab => {
                tab.classList.remove('active');
            });
            
            document.querySelectorAll('.bottom-nav-item').forEach(item => {
                item.classList.remove('active');
            });
            
            // Add active class to selected tab and nav item
            const targetTab = document.getElementById(`${tabName}-tab`);
            if (targetTab) {
                targetTab.classList.add('active');
            }
            
            const navItem = document.querySelector(`[data-tab="${tabName}"]`);
            if (navItem) {
                navItem.classList.add('active');
            }

            // Update charts if switching to statistics
            if (tabName === 'estadisticas') {
                setTimeout(drawCharts, 100);
            }
        }

        // Ultra-smooth Calendar Rendering with 60+ FPS animations
        let calendarAnimationDirection = 'fade';
        let isCalendarAnimating = false;

        function renderCalendar(direction = 'fade') {
            if (isCalendarAnimating) return;
            isCalendarAnimating = true;
            
            const monthNames = [
                'Enero', 'Febrero', 'Marzo', 'Abril', 'Mayo', 'Junio',
                'Julio', 'Agosto', 'Septiembre', 'Octubre', 'Noviembre', 'Diciembre'
            ];
            
            document.getElementById('currentMonth').textContent = 
                `${monthNames[currentDate.getMonth()]} ${currentDate.getFullYear()}`;
            
            const firstDay = new Date(currentDate.getFullYear(), currentDate.getMonth(), 1);
            const startDate = new Date(firstDay);
            startDate.setDate(startDate.getDate() - firstDay.getDay());
            
            const calendarDays = document.getElementById('calendarDays');
            
            // Use requestAnimationFrame for smooth 60+ FPS animations
            requestAnimationFrame(() => {
                // Add appropriate exit animation
                const exitClass = direction === 'next' ? 'calendar-slide-right' : 
                                direction === 'prev' ? 'calendar-slide-left' : 'calendar-fade-out';
                calendarDays.classList.add(exitClass);
                
                setTimeout(() => {
                    calendarDays.innerHTML = '';
                    
                    // Pre-create all elements for better performance
                    const fragment = document.createDocumentFragment();
                    
                    // Calendar days with optimized rendering
                    for (let i = 0; i < 42; i++) {
                        const date = new Date(startDate);
                        date.setDate(startDate.getDate() + i);
                        
                        const dayElement = document.createElement('div');
                        dayElement.className = 'calendar-day';
                        
                        const dayNumber = document.createElement('div');
                        dayNumber.className = 'calendar-day-number';
                        dayNumber.textContent = date.getDate();
                        
                        const dayContent = document.createElement('div');
                        dayContent.className = 'calendar-day-content';
                        
                        dayElement.appendChild(dayNumber);
                        dayElement.appendChild(dayContent);
                        
                        if (date.getMonth() !== currentDate.getMonth()) {
                            dayElement.classList.add('other-month');
                        }
                        
                        if (isToday(date)) {
                            dayElement.classList.add('today');
                        }
                        
                        if (isSameDay(date, selectedDate)) {
                            dayElement.classList.add('selected');
                        }
                        
                        // Add task indicators with optimized rendering
                        const tasksForDate = getTasksForDate(date);
                        renderTaskIndicators(dayContent, tasksForDate);
                        
                        // Optimized event listeners
                        dayElement.addEventListener('mouseenter', (e) => showCalendarTooltip(e, date), { passive: true });
                        dayElement.addEventListener('mouseleave', hideCalendarTooltip, { passive: true });
                        dayElement.addEventListener('click', () => selectDate(date), { passive: true });
                        
                        fragment.appendChild(dayElement);
                    }
                    
                    // Batch DOM update
                    calendarDays.appendChild(fragment);
                    
                    // Remove exit animation and add entrance animation
                    requestAnimationFrame(() => {
                        calendarDays.classList.remove(exitClass);
                        const enterClass = direction === 'next' ? 'calendar-slide-left' : 
                                         direction === 'prev' ? 'calendar-slide-right' : 'calendar-fade-in';
                        calendarDays.classList.add(enterClass);
                        
                        setTimeout(() => {
                            calendarDays.classList.remove(enterClass);
                            isCalendarAnimating = false;
                        }, 400);
                    });
                }, 300);
            });
        }

        // Ultra-smooth Main Calendar Rendering with 60+ FPS animations
        let isMainCalendarAnimating = false;

        function renderMainCalendar(direction = 'fade') {
            if (isMainCalendarAnimating) return;
            isMainCalendarAnimating = true;
            
            const monthNames = [
                'Enero', 'Febrero', 'Marzo', 'Abril', 'Mayo', 'Junio',
                'Julio', 'Agosto', 'Septiembre', 'Octubre', 'Noviembre', 'Diciembre'
            ];
            
            document.getElementById('calendarCurrentMonth').textContent = 
                `${monthNames[calendarDate.getMonth()]} ${calendarDate.getFullYear()}`;
            
            const firstDay = new Date(calendarDate.getFullYear(), calendarDate.getMonth(), 1);
            const startDate = new Date(firstDay);
            startDate.setDate(startDate.getDate() - firstDay.getDay());
            
            const calendarDays = document.getElementById('mainCalendarDays');
            
            // Use requestAnimationFrame for smooth 60+ FPS animations
            requestAnimationFrame(() => {
                // Add appropriate exit animation
                const exitClass = direction === 'next' ? 'calendar-slide-right' : 
                                direction === 'prev' ? 'calendar-slide-left' : 'calendar-fade-out';
                calendarDays.classList.add(exitClass);
                
                setTimeout(() => {
                    calendarDays.innerHTML = '';
                    
                    // Pre-create all elements for better performance
                    const fragment = document.createDocumentFragment();
                    
                    // Calendar days with optimized rendering
                    for (let i = 0; i < 42; i++) {
                        const date = new Date(startDate);
                        date.setDate(startDate.getDate() + i);
                        
                        const dayElement = document.createElement('div');
                        dayElement.className = 'calendar-day';
                        
                        const dayNumber = document.createElement('div');
                        dayNumber.className = 'calendar-day-number';
                        dayNumber.textContent = date.getDate();
                        
                        const dayContent = document.createElement('div');
                        dayContent.className = 'calendar-day-content';
                        
                        dayElement.appendChild(dayNumber);
                        dayElement.appendChild(dayContent);
                        
                        if (date.getMonth() !== calendarDate.getMonth()) {
                            dayElement.classList.add('other-month');
                        }
                        
                        if (isToday(date)) {
                            dayElement.classList.add('today');
                        }
                        
                        // Add task indicators with optimized rendering
                        const tasksForDate = getTasksForDate(date);
                        renderTaskIndicators(dayContent, tasksForDate);
                        
                        // Optimized event listeners
                        dayElement.addEventListener('mouseenter', (e) => showCalendarTooltip(e, date), { passive: true });
                        dayElement.addEventListener('mouseleave', hideCalendarTooltip, { passive: true });
                        dayElement.addEventListener('click', () => showTasksForDate(date), { passive: true });
                        
                        fragment.appendChild(dayElement);
                    }
                    
                    // Batch DOM update
                    calendarDays.appendChild(fragment);
                    
                    // Remove exit animation and add entrance animation
                    requestAnimationFrame(() => {
                        calendarDays.classList.remove(exitClass);
                        const enterClass = direction === 'next' ? 'calendar-slide-left' : 
                                         direction === 'prev' ? 'calendar-slide-right' : 'calendar-fade-in';
                        calendarDays.classList.add(enterClass);
                        
                        setTimeout(() => {
                            calendarDays.classList.remove(enterClass);
                            isMainCalendarAnimating = false;
                        }, 400);
                    });
                }, 300);
            });
        }

        function getTasksForDate(date) {
            return tasks.filter(task => {
                const taskDate = new Date(task.date);
                return isSameDay(taskDate, date);
            });
        }

        function renderTaskIndicators(container, tasksForDate) {
            container.innerHTML = '';
            
            if (tasksForDate.length === 0) return;
            
            const maxVisible = 3;
            const visibleTasks = tasksForDate.slice(0, maxVisible);
            
            visibleTasks.forEach(task => {
                const indicator = document.createElement('div');
                indicator.className = 'task-indicator';
                
                // Determine task status and styling
                const today = new Date();
                const taskDate = new Date(task.date);
                
                if (task.completed) {
                    indicator.classList.add('completed');
                } else if (taskDate < today && !isSameDay(taskDate, today)) {
                    indicator.classList.add('overdue');
                } else if (task.priority === 'high') {
                    indicator.classList.add('high-priority');
                } else {
                    indicator.classList.add('pending');
                }
                
                indicator.textContent = task.title;
                container.appendChild(indicator);
            });
            
            // Show "more tasks" indicator if needed
            if (tasksForDate.length > maxVisible) {
                const moreIndicator = document.createElement('div');
                moreIndicator.className = 'more-tasks-indicator';
                moreIndicator.textContent = `+${tasksForDate.length - maxVisible} más`;
                container.appendChild(moreIndicator);
            }
        }

        function previousMonth() {
            if (isCalendarAnimating) return;
            currentDate.setMonth(currentDate.getMonth() - 1);
            renderCalendar('prev');
        }

        function nextMonth() {
            if (isCalendarAnimating) return;
            currentDate.setMonth(currentDate.getMonth() + 1);
            renderCalendar('next');
        }

        function previousCalendarMonth() {
            if (isMainCalendarAnimating) return;
            calendarDate.setMonth(calendarDate.getMonth() - 1);
            renderMainCalendar('prev');
        }

        function nextCalendarMonth() {
            if (isMainCalendarAnimating) return;
            calendarDate.setMonth(calendarDate.getMonth() + 1);
            renderMainCalendar('next');
        }

        function selectDate(date) {
            selectedDate = new Date(date);
            renderCalendar();
            document.getElementById('newTaskDate').value = formatDateForInput(date);
        }

        function showTasksForDate(date) {
            const tasksForDate = tasks.filter(task => {
                const taskDate = new Date(task.date);
                return isSameDay(taskDate, date);
            });

            const container = document.getElementById('selectedDateTasks');
            const dateStr = date.toLocaleDateString('es-ES', { 
                weekday: 'long', 
                year: 'numeric', 
                month: 'long', 
                day: 'numeric' 
            });

            if (tasksForDate.length === 0) {
                container.innerHTML = `
                    <div class="modern-card p-6 text-center">
                        <h3 class="text-lg font-semibold mb-2">📅 ${dateStr}</h3>
                        <p class="text-gray-600">No hay tareas programadas para este día</p>
                    </div>
                `;
            } else {
                container.innerHTML = `
                    <div class="modern-card p-6">
                        <h3 class="text-lg font-semibold mb-4">📅 ${dateStr}</h3>
                        <div class="space-y-3">
                            ${tasksForDate.map(task => `
                                <div class="flex items-center justify-between p-3 bg-gray-50 rounded-lg">
                                    <div class="flex items-center space-x-3">
                                        <input 
                                            type="checkbox" 
                                            ${task.completed ? 'checked' : ''} 
                                            onchange="toggleTask(${task.id})"
                                            class="w-4 h-4 rounded"
                                            style="accent-color: var(--primary-color)"
                                        >
                                        <div>
                                            <div class="font-medium ${task.completed ? 'line-through text-gray-500' : ''}">${task.title}</div>
                                            <div class="text-sm text-gray-600">📚 ${task.subject}</div>
                                        </div>
                                    </div>
                                    <span class="priority-badge ${getPriorityClass(task.priority)}">
                                        ${getPriorityText(task.priority)}
                                    </span>
                                </div>
                            `).join('')}
                        </div>
                    </div>
                `;
            }
        }

        function hasTasksOnDate(date) {
            return tasks.some(task => {
                const taskDate = new Date(task.date);
                return isSameDay(taskDate, date);
            });
        }

        function hasHighPriorityTasks(date) {
            return tasks.some(task => {
                const taskDate = new Date(task.date);
                return isSameDay(taskDate, date) && task.priority === 'high' && !task.completed;
            });
        }

        function showCalendarTooltip(event, date) {
            const tasksForDate = tasks.filter(task => {
                const taskDate = new Date(task.date);
                return isSameDay(taskDate, date);
            });

            if (tasksForDate.length === 0) return;

            // Remove existing tooltip
            hideCalendarTooltip();

            const tooltip = document.createElement('div');
            tooltip.className = 'calendar-tooltip';
            tooltip.id = 'calendar-tooltip';
            
            const dateStr = date.toLocaleDateString('es-ES', { 
                weekday: 'short', 
                month: 'short', 
                day: 'numeric' 
            });

            tooltip.innerHTML = `
                <div class="tooltip-date">${dateStr}</div>
                <div class="space-y-2">
                    ${tasksForDate.slice(0, 3).map(task => `
                        <div class="tooltip-task">
                            <span class="priority-badge ${getPriorityClass(task.priority)}">${getPriorityText(task.priority)}</span>
                            <span class="text-xs font-medium ${task.completed ? 'line-through text-gray-500' : ''}">${task.title}</span>
                        </div>
                    `).join('')}
                    ${tasksForDate.length > 3 ? `<div class="tooltip-more">+${tasksForDate.length - 3} tareas más...</div>` : ''}
                </div>
            `;

            document.body.appendChild(tooltip);

            // Position tooltip with improved positioning
            const rect = event.target.getBoundingClientRect();
            const tooltipRect = tooltip.getBoundingClientRect();
            
            let left = rect.left + (rect.width / 2) - (tooltipRect.width / 2);
            let top = rect.top - tooltipRect.height - 15;

            // Adjust horizontal position if tooltip goes off screen
            if (left < 10) {
                left = 10;
            } else if (left + tooltipRect.width > window.innerWidth - 10) {
                left = window.innerWidth - tooltipRect.width - 10;
            }

            // Adjust vertical position if tooltip goes off screen
            if (top < 10) {
                top = rect.bottom + 15;
                // Flip arrow direction
                tooltip.style.setProperty('--arrow-direction', 'up');
            }

            tooltip.style.left = left + 'px';
            tooltip.style.top = top + 'px';

            // Trigger show animation with slight delay for smooth effect
            requestAnimationFrame(() => {
                tooltip.classList.add('show');
            });
        }

        function hideCalendarTooltip() {
            const tooltip = document.getElementById('calendar-tooltip');
            if (tooltip) {
                tooltip.remove();
            }
        }

        function isToday(date) {
            const today = new Date();
            return isSameDay(date, today);
        }

        function isSameDay(date1, date2) {
            return date1.getDate() === date2.getDate() &&
                   date1.getMonth() === date2.getMonth() &&
                   date1.getFullYear() === date2.getFullYear();
        }

        function formatDateForInput(date) {
            return date.toISOString().split('T')[0];
        }

        // Task functions
        function setDefaultDate() {
            const today = new Date();
            selectedDate = today;
            document.getElementById('newTaskDate').value = formatDateForInput(today);
            renderCalendar();
        }

        function createNewTask() {
            const title = document.getElementById('newTaskTitle').value.trim();
            const description = document.getElementById('newTaskDescription').value.trim();
            const subject = document.getElementById('newTaskSubject').value.trim();
            const priority = document.getElementById('newTaskPriority').value;
            const date = document.getElementById('newTaskDate').value;

            if (!title || !priority || !date || !subject) {
                showNotification('Por favor completa todos los campos obligatorios', 'error');
                return;
            }

            const task = {
                id: taskIdCounter++,
                title,
                description,
                subject,
                priority,
                date,
                completed: false,
                createdAt: new Date().toISOString()
            };

            tasks.push(task);
            saveTasks();
            renderTasks();
            updateStatistics();
            updateProgressTab();
            renderCalendar();
            renderMainCalendar();
            clearCreateForm();
            showNotification('✅ Tarea creada exitosamente', 'success');
        }

        function clearCreateForm() {
            document.getElementById('createTaskForm').reset();
            setDefaultDate();
        }

        function renderTasks() {
            const container = document.getElementById('taskList');
            const emptyState = document.getElementById('emptyState');
            
            const activeTasks = getFilteredTasks();
            
            // Use requestAnimationFrame for smooth rendering
            requestAnimationFrame(() => {
                if (activeTasks.length === 0) {
                    container.innerHTML = '';
                    emptyState.style.display = 'block';
                    return;
                }
                
                emptyState.style.display = 'none';
                
                // Create document fragment for better performance
                const fragment = document.createDocumentFragment();
                
                activeTasks.forEach(task => {
                    const taskElement = document.createElement('div');
                    taskElement.className = 'modern-card p-4 slide-up';
                    taskElement.innerHTML = `
                        <div class="flex items-start justify-between">
                            <div class="flex items-start space-x-3 flex-1">
                                <input 
                                    type="checkbox" 
                                    ${task.completed ? 'checked' : ''} 
                                    onchange="toggleTask(${task.id})"
                                    class="mt-1 w-5 h-5 rounded"
                                    style="accent-color: var(--primary-color)"
                                >
                                <div class="flex-1">
                                    <h3 class="font-semibold text-lg mb-1">${task.title}</h3>
                                    ${task.description ? `<p class="text-gray-600 text-sm mb-2">${task.description}</p>` : ''}
                                    <div class="flex items-center space-x-4 text-sm text-gray-500">
                                        <span>📚 ${task.subject}</span>
                                        <span>📅 ${formatDate(task.date)}</span>
                                        <span class="priority-badge ${getPriorityClass(task.priority)}">
                                            ${getPriorityText(task.priority)}
                                        </span>
                                    </div>
                                </div>
                            </div>
                            <button 
                                onclick="deleteTask(${task.id})" 
                                class="text-red-500 hover:text-red-700 transition-colors p-2"
                                title="Eliminar tarea"
                            >
                                🗑️
                            </button>
                        </div>
                    `;
                    fragment.appendChild(taskElement);
                });
                
                // Single DOM update
                container.innerHTML = '';
                container.appendChild(fragment);
            });
        }

        function getFilteredTasks() {
            const priorityFilter = document.getElementById('filterPriority').value;
            const dateFilter = document.getElementById('filterDate').value;
            
            let filtered = tasks.filter(task => !task.completed);
            
            if (priorityFilter !== 'all') {
                filtered = filtered.filter(task => task.priority === priorityFilter);
            }
            
            if (dateFilter) {
                filtered = filtered.filter(task => task.date === dateFilter);
            }
            
            return filtered.sort((a, b) => new Date(a.date) - new Date(b.date));
        }

        function filterTasks() {
            renderTasks();
            updateStatistics();
        }

        function toggleTask(id) {
            const task = tasks.find(t => t.id === id);
            if (task) {
                task.completed = !task.completed;
                
                if (task.completed) {
                    task.completedAt = new Date().toISOString();
                    showNotification('✅ ¡Tarea completada!', 'success');
                } else {
                    delete task.completedAt;
                    showNotification('🔄 Tarea marcada como pendiente', 'info');
                }
                
                saveTasks();
                renderTasks();
                updateStatistics();
                updateProgressTab();
                drawCharts();
                renderCalendar();
                renderMainCalendar();
            }
        }

        function deleteTask(id) {
            if (confirm('¿Estás seguro de que quieres eliminar esta tarea?')) {
                tasks = tasks.filter(t => t.id !== id);
                saveTasks();
                renderTasks();
                updateStatistics();
                drawCharts();
                renderCalendar();
                renderMainCalendar();
                showNotification('🗑️ Tarea eliminada', 'success');
            }
        }

        // Chat functions
        function handleChatKeyPress(event) {
            if (event.key === 'Enter') {
                sendChatMessage();
            }
        }

        function sendChatMessage() {
            const input = document.getElementById('chatInput');
            const message = input.value.trim();
            
            if (!message) return;
            
            addChatMessage(message, 'user');
            input.value = '';
            
            // Simulate AI response
            setTimeout(() => {
                const aiResponse = generateAIResponse(message);
                addChatMessage(aiResponse, 'ai');
            }, 1000);
        }

        function addChatMessage(content, type) {
            const message = {
                content,
                type,
                timestamp: new Date().toISOString()
            };
            
            chatMessages.push(message);
            
            if (chatMessages.length > 50) {
                chatMessages = chatMessages.slice(-50);
            }
            
            localStorage.setItem('taskmaster_chat', JSON.stringify(chatMessages));
            renderChatMessages();
        }

        function renderChatMessages() {
            const container = document.getElementById('chatMessages');
            
            if (chatMessages.length === 0) {
                container.innerHTML = `
                    <div class="text-center py-8 text-gray-500">
                        <p>🤖 ¡Hola! Soy tu asistente IA. ¿En qué puedo ayudarte hoy?</p>
                    </div>
                `;
                return;
            }
            
            container.innerHTML = chatMessages.map(message => `
                <div class="flex ${message.type === 'user' ? 'justify-end' : 'justify-start'} mb-3">
                    <div class="max-w-xs px-4 py-3 rounded-lg ${
                        message.type === 'user' 
                            ? 'text-white' 
                            : 'bg-gray-100 text-gray-800'
                    }" ${message.type === 'user' ? 'style="background: var(--primary-color)"' : ''}>
                        <p class="text-sm">${message.content}</p>
                        <span class="text-xs opacity-70">${formatTime(message.timestamp)}</span>
                    </div>
                </div>
            `).join('');
            
            container.scrollTop = container.scrollHeight;
        }

        function generateAIResponse(message) {
            const lowerMessage = message.toLowerCase();
            
            if (lowerMessage.includes('tarea') || lowerMessage.includes('crear')) {
                return '¡Perfecto! Puedes crear una nueva tarea usando la sección "Crear" en la barra inferior. Allí encontrarás un calendario interactivo para seleccionar la fecha.';
            } else if (lowerMessage.includes('calendario')) {
                return 'El calendario te permite ver todas tus tareas organizadas por fecha. Puedes navegar entre meses y hacer clic en cualquier día para ver las tareas programadas.';
            } else if (lowerMessage.includes('estadística') || lowerMessage.includes('progreso')) {
                return 'En la sección "Estadísticas" puedes ver tu progreso semanal, distribución por prioridades y métricas generales de productividad.';
            } else if (lowerMessage.includes('ayuda') || lowerMessage.includes('cómo')) {
                return 'Estoy aquí para ayudarte. Puedes crear tareas, ver tu calendario, revisar estadísticas y personalizar la aplicación con diferentes temas de color. ¿Qué necesitas hacer?';
            } else {
                return 'Entiendo tu consulta. ¿Te gustaría que te ayude con alguna funcionalidad específica? Puedo ayudarte a organizar tus tareas de manera más eficiente.';
            }
        }

        // Statistics and Charts
        function updateStatistics() {
            const completed = tasks.filter(t => t.completed).length;
            const pending = tasks.filter(t => !t.completed).length;
            const highPriority = tasks.filter(t => t.priority === 'high' && !t.completed).length;
            const total = tasks.length;
            const progressPercent = total > 0 ? Math.round((completed / total) * 100) : 0;

            document.getElementById('taskCount').textContent = total;
            document.getElementById('completedCount').textContent = completed;
            document.getElementById('pendingCount').textContent = pending;
            document.getElementById('highPriorityCount').textContent = highPriority;
            document.getElementById('progressPercentage').textContent = `${progressPercent}%`;
            document.getElementById('progressBar').style.width = `${progressPercent}%`;
        }

        function updateProgressTab() {
            const completed = tasks.filter(t => t.completed).length;
            const pending = tasks.filter(t => !t.completed).length;
            const highPriority = tasks.filter(t => t.priority === 'high' && !t.completed).length;
            const total = tasks.length;
            const progressPercent = total > 0 ? Math.round((completed / total) * 100) : 0;
            
            // Get overdue tasks
            const today = new Date();
            const overdue = tasks.filter(t => {
                const taskDate = new Date(t.date);
                return !t.completed && taskDate < today && !isSameDay(taskDate, today);
            }).length;

            // Update progress circle
            const circle = document.getElementById('progressCircle');
            const circumference = 2 * Math.PI * 40; // radius = 40
            const offset = circumference - (progressPercent / 100) * circumference;
            circle.style.strokeDashoffset = offset;

            // Update all counters
            document.getElementById('circleProgressText').textContent = `${progressPercent}%`;
            document.getElementById('totalTasksCount').textContent = total;
            document.getElementById('completedCountProgress').textContent = completed;
            document.getElementById('pendingCountProgress').textContent = pending;
            document.getElementById('highPriorityCountProgress').textContent = highPriority;
            document.getElementById('overdueCountProgress').textContent = overdue;

            // Calculate weekly progress
            const weeklyCompleted = getWeeklyCompletedTasks();
            const weeklyTotal = getWeeklyTotalTasks();
            const weeklyProgress = weeklyTotal > 0 ? Math.round((weeklyCompleted / weeklyTotal) * 100) : 0;
            
            document.getElementById('weeklyProgressText').textContent = `${weeklyProgress}%`;
            document.getElementById('weeklyProgressBar').style.width = `${weeklyProgress}%`;

            // Calculate productivity (completed vs created this week)
            const productivity = Math.min(100, weeklyCompleted * 10); // Simple productivity metric
            document.getElementById('productivityText').textContent = `${productivity}%`;
            document.getElementById('productivityBar').style.width = `${productivity}%`;

            // Update streak
            const streak = calculateStreak();
            document.getElementById('streakCount').textContent = streak;

            // Update achievements
            updateAchievements();
        }

        function getWeeklyCompletedTasks() {
            const oneWeekAgo = new Date();
            oneWeekAgo.setDate(oneWeekAgo.getDate() - 7);
            
            return tasks.filter(task => {
                if (!task.completed || !task.completedAt) return false;
                const completedDate = new Date(task.completedAt);
                return completedDate >= oneWeekAgo;
            }).length;
        }

        function getWeeklyTotalTasks() {
            const oneWeekAgo = new Date();
            oneWeekAgo.setDate(oneWeekAgo.getDate() - 7);
            
            return tasks.filter(task => {
                const taskDate = new Date(task.date);
                return taskDate >= oneWeekAgo;
            }).length;
        }

        function calculateStreak() {
            const today = new Date();
            let streak = 0;
            let currentDate = new Date(today);
            
            while (true) {
                const hasCompletedTask = tasks.some(task => {
                    if (!task.completed || !task.completedAt) return false;
                    const completedDate = new Date(task.completedAt);
                    return isSameDay(completedDate, currentDate);
                });
                
                if (hasCompletedTask) {
                    streak++;
                    currentDate.setDate(currentDate.getDate() - 1);
                } else {
                    break;
                }
            }
            
            return streak;
        }

        function updateAchievements() {
            const achievements = [];
            const completed = tasks.filter(t => t.completed).length;
            const total = tasks.length;
            const streak = calculateStreak();
            
            if (completed >= 1) {
                achievements.push({
                    icon: '🎯',
                    title: 'Primera Tarea',
                    description: 'Completaste tu primera tarea'
                });
            }
            
            if (completed >= 5) {
                achievements.push({
                    icon: '🏃‍♂️',
                    title: 'En Marcha',
                    description: 'Completaste 5 tareas'
                });
            }
            
            if (completed >= 10) {
                achievements.push({
                    icon: '💪',
                    title: 'Productivo',
                    description: 'Completaste 10 tareas'
                });
            }
            
            if (streak >= 3) {
                achievements.push({
                    icon: '🔥',
                    title: 'Racha Activa',
                    description: `${streak} días consecutivos`
                });
            }
            
            if (total > 0 && (completed / total) >= 0.8) {
                achievements.push({
                    icon: '⭐',
                    title: 'Eficiente',
                    description: '80% de tareas completadas'
                });
            }

            const container = document.getElementById('achievementsList');
            if (achievements.length === 0) {
                container.innerHTML = '<p class="text-gray-500 text-center">Completa tareas para desbloquear logros</p>';
            } else {
                container.innerHTML = achievements.map(achievement => `
                    <div class="modern-card p-4 flex items-center space-x-3">
                        <div class="text-2xl">${achievement.icon}</div>
                        <div>
                            <div class="font-semibold">${achievement.title}</div>
                            <div class="text-sm text-gray-600">${achievement.description}</div>
                        </div>
                    </div>
                `).join('');
            }
        }

        function drawCharts() {
            drawWeeklyChart();
            drawPriorityChart();
        }

        function drawWeeklyChart() {
            const canvas = document.getElementById('weeklyChart');
            if (!canvas) return;
            
            const ctx = canvas.getContext('2d');
            const width = canvas.width;
            const height = canvas.height;
            
            // Clear canvas
            ctx.clearRect(0, 0, width, height);
            
            // Get weekly data
            const weeklyData = getWeeklyData();
            const maxValue = Math.max(...weeklyData, 1);
            
            // Draw bars
            const barWidth = width / 7 - 10;
            const days = ['Dom', 'Lun', 'Mar', 'Mié', 'Jue', 'Vie', 'Sáb'];
            
            weeklyData.forEach((value, index) => {
                const barHeight = (value / maxValue) * (height - 60);
                const x = index * (barWidth + 10) + 5;
                const y = height - barHeight - 30;
                
                // Draw bar
                ctx.fillStyle = getComputedStyle(document.documentElement).getPropertyValue('--primary-color');
                ctx.fillRect(x, y, barWidth, barHeight);
                
                // Draw day label
                ctx.fillStyle = '#333333';
                ctx.font = '12px Roboto';
                ctx.textAlign = 'center';
                ctx.fillText(days[index], x + barWidth/2, height - 10);
                
                // Draw value
                if (value > 0) {
                    ctx.fillText(value.toString(), x + barWidth/2, y - 5);
                }
            });
        }

        function drawPriorityChart() {
            const canvas = document.getElementById('priorityChart');
            if (!canvas) return;
            
            const ctx = canvas.getContext('2d');
            const width = canvas.width;
            const height = canvas.height;
            
            // Clear canvas
            ctx.clearRect(0, 0, width, height);
            
            // Get priority data
            const priorityData = {
                high: tasks.filter(t => t.priority === 'high').length,
                medium: tasks.filter(t => t.priority === 'medium').length,
                low: tasks.filter(t => t.priority === 'low').length
            };
            
            const total = priorityData.high + priorityData.medium + priorityData.low;
            if (total === 0) {
                ctx.fillStyle = '#999';
                ctx.font = '16px Roboto';
                ctx.textAlign = 'center';
                ctx.fillText('No hay datos', width/2, height/2);
                return;
            }
            
            // Draw pie chart
            const centerX = width / 2;
            const centerY = height / 2;
            const radius = Math.min(width, height) / 3;
            
            let currentAngle = 0;
            const colors = ['#DC2626', '#D97706', '#059669'];
            const labels = ['Alta', 'Media', 'Baja'];
            const values = [priorityData.high, priorityData.medium, priorityData.low];
            
            values.forEach((value, index) => {
                if (value > 0) {
                    const sliceAngle = (value / total) * 2 * Math.PI;
                    
                    // Draw slice
                    ctx.beginPath();
                    ctx.moveTo(centerX, centerY);
                    ctx.arc(centerX, centerY, radius, currentAngle, currentAngle + sliceAngle);
                    ctx.closePath();
                    ctx.fillStyle = colors[index];
                    ctx.fill();
                    
                    // Draw label
                    const labelAngle = currentAngle + sliceAngle / 2;
                    const labelX = centerX + Math.cos(labelAngle) * (radius + 20);
                    const labelY = centerY + Math.sin(labelAngle) * (radius + 20);
                    
                    ctx.fillStyle = '#333333';
                    ctx.font = '12px Roboto';
                    ctx.textAlign = 'center';
                    ctx.fillText(`${labels[index]}: ${value}`, labelX, labelY);
                    
                    currentAngle += sliceAngle;
                }
            });
        }

        function getWeeklyData() {
            const today = new Date();
            const weekData = [0, 0, 0, 0, 0, 0, 0]; // Sunday to Saturday
            
            tasks.filter(t => t.completed).forEach(task => {
                if (task.completedAt) {
                    const completedDate = new Date(task.completedAt);
                    const daysDiff = Math.floor((today - completedDate) / (1000 * 60 * 60 * 24));
                    
                    if (daysDiff < 7) {
                        const dayOfWeek = completedDate.getDay();
                        weekData[dayOfWeek]++;
                    }
                }
            });
            
            return weekData;
        }

        // Theme functions
        function changeTheme(theme) {
            document.body.setAttribute('data-theme', theme);
            
            // Update active theme indicator
            document.querySelectorAll('.theme-option').forEach(option => {
                option.classList.remove('active');
            });
            
            const themeMap = {
                'palette1': 'theme-1',
                'palette2': 'theme-2',
                'palette3': 'theme-3',
                'palette4': 'theme-4',
                'palette5': 'theme-5'
            };
            
            document.querySelector(`.${themeMap[theme]}`).classList.add('active');
            localStorage.setItem('taskmaster_theme', theme);
            
            // Redraw charts with new colors
            setTimeout(drawCharts, 100);
        }

        // Reset app
        function resetApp() {
            if (confirm('¿Estás seguro de que quieres restablecer toda la aplicación?')) {
                localStorage.clear();
                location.reload();
            }
        }

        // Utility functions
        function saveTasks() {
            localStorage.setItem('taskmaster_tasks', JSON.stringify(tasks));
            localStorage.setItem('taskmaster_counter', taskIdCounter.toString());
        }

        function getPriorityClass(priority) {
            return `priority-${priority}`;
        }

        function getPriorityText(priority) {
            const texts = {
                'high': 'Alta',
                'medium': 'Media',
                'low': 'Baja'
            };
            return texts[priority] || 'Sin prioridad';
        }

        function formatDate(dateString) {
            const date = new Date(dateString);
            return date.toLocaleDateString('es-ES', { 
                year: 'numeric', 
                month: 'short', 
                day: 'numeric' 
            });
        }

        function formatTime(timestamp) {
            const date = new Date(timestamp);
            return date.toLocaleTimeString('es-ES', { 
                hour: '2-digit', 
                minute: '2-digit' 
            });
        }

        function showNotification(message, type = 'info') {
            const notification = document.createElement('div');
            notification.className = `fixed top-4 right-4 z-50 px-6 py-3 rounded-lg text-white text-sm font-medium slide-up ${
                type === 'success' ? 'bg-green-500' :
                type === 'warning' ? 'bg-yellow-500' :
                type === 'error' ? 'bg-red-500' :
                'bg-blue-500'
            }`;
            notification.textContent = message;
            
            document.body.appendChild(notification);
            
            setTimeout(() => {
                notification.remove();
            }, 3000);
        }

        // Font size functions
        function changeFontSize(size) {
            // Remove all font size classes
            document.body.classList.remove('font-size-small', 'font-size-medium', 'font-size-large', 'font-size-xlarge');
            
            // Add the selected font size class
            document.body.classList.add(`font-size-${size}`);
            
            // Update active button
            document.querySelectorAll('.font-size-option').forEach(option => {
                option.classList.remove('active');
            });
            document.querySelector(`[data-size="${size}"]`).classList.add('active');
            
            // Save preference
            localStorage.setItem('taskmaster_font_size', size);
            
            // Show notification
            const sizeNames = {
                'small': 'Pequeño',
                'medium': 'Mediano', 
                'large': 'Grande',
                'xlarge': 'Extra Grande'
            };
            
            showNotification(`📏 Tamaño cambiado a ${sizeNames[size]}`, 'success');
            
            // Redraw charts with new size
            setTimeout(() => {
                drawCharts();
                renderCalendar();
                renderMainCalendar();
            }, 100);
        }

        // Dark mode functions
        function toggleDarkMode() {
            const isDarkMode = document.body.getAttribute('data-dark-mode') === 'true';
            const newMode = !isDarkMode;
            
            document.body.setAttribute('data-dark-mode', newMode.toString());
            
            // Update toggle button
            const toggle = document.getElementById('darkModeToggle');
            const slider = document.getElementById('darkModeSlider');
            
            if (newMode) {
                toggle.style.backgroundColor = 'var(--primary-color)';
                slider.style.transform = 'translateX(1.25rem)';
                slider.style.backgroundColor = 'white';
                showNotification('🌙 Modo oscuro activado', 'success');
            } else {
                toggle.style.backgroundColor = 'var(--border-color)';
                slider.style.transform = 'translateX(0.25rem)';
                slider.style.backgroundColor = 'white';
                showNotification('☀️ Modo claro activado', 'success');
            }
            
            // Save preference
            localStorage.setItem('taskmaster_dark_mode', newMode.toString());
            
            // Redraw charts and calendars with new colors
            setTimeout(() => {
                drawCharts();
                renderCalendar();
                renderMainCalendar();
            }, 100);
        }

        function initializeDarkMode() {
            const savedDarkMode = localStorage.getItem('taskmaster_dark_mode') === 'true';
            document.body.setAttribute('data-dark-mode', savedDarkMode.toString());
            
            // Update toggle button state
            const toggle = document.getElementById('darkModeToggle');
            const slider = document.getElementById('darkModeSlider');
            
            if (toggle && slider) {
                if (savedDarkMode) {
                    toggle.style.backgroundColor = 'var(--primary-color)';
                    slider.style.transform = 'translateX(1.25rem)';
                } else {
                    toggle.style.backgroundColor = 'var(--border-color)';
                    slider.style.transform = 'translateX(0.25rem)';
                }
            }
        }

        // Dropdown functionality
        function toggleDropdown(dropdownId) {
            const dropdown = document.getElementById(dropdownId);
            const trigger = dropdown.querySelector('.dropdown-trigger');
            const menu = dropdown.querySelector('.dropdown-menu');
            
            // Close all other dropdowns
            document.querySelectorAll('.custom-dropdown').forEach(dd => {
                if (dd.id !== dropdownId) {
                    dd.querySelector('.dropdown-trigger').classList.remove('active');
                    dd.querySelector('.dropdown-menu').classList.remove('show');
                }
            });
            
            // Remove existing overlay
            const existingOverlay = document.querySelector('.calendar-dropdown-overlay');
            if (existingOverlay) {
                existingOverlay.remove();
            }
            
            // Toggle current dropdown
            const isActive = trigger.classList.contains('active');
            
            if (isActive) {
                trigger.classList.remove('active');
                menu.classList.remove('show');
            } else {
                trigger.classList.add('active');
                menu.classList.add('show');
                
                // Add overlay for calendar dropdown
                if (dropdownId === 'dateDropdown') {
                    const overlay = document.createElement('div');
                    overlay.className = 'calendar-dropdown-overlay';
                    overlay.onclick = () => toggleDropdown(dropdownId);
                    document.body.appendChild(overlay);
                    
                    setTimeout(() => {
                        overlay.classList.add('show');
                    }, 10);
                }
            }
        }

        function selectPriority(value, text) {
            document.getElementById('newTaskPriority').value = value;
            document.getElementById('selectedPriorityText').textContent = text;
            
            // Close dropdown
            const dropdown = document.getElementById('priorityDropdown');
            dropdown.querySelector('.dropdown-trigger').classList.remove('active');
            dropdown.querySelector('.dropdown-menu').classList.remove('show');
            
            showNotification(`Prioridad seleccionada: ${text}`, 'success');
        }

        function selectSubject(subject) {
            document.getElementById('newTaskSubject').value = subject;
            document.getElementById('selectedSubjectText').textContent = subject;
            
            // Close dropdown
            const dropdown = document.getElementById('subjectDropdown');
            dropdown.querySelector('.dropdown-trigger').classList.remove('active');
            dropdown.querySelector('.dropdown-menu').classList.remove('show');
            
            showNotification(`Materia seleccionada: ${subject}`, 'success');
        }

        // Enhanced selectDate function for dropdown calendar
        function selectDate(date) {
            selectedDate = new Date(date);
            const dateStr = date.toLocaleDateString('es-ES', { 
                weekday: 'long', 
                year: 'numeric', 
                month: 'long', 
                day: 'numeric' 
            });
            
            document.getElementById('newTaskDate').value = formatDateForInput(date);
            document.getElementById('selectedDateText').textContent = dateStr;
            
            // Close dropdown
            const dropdown = document.getElementById('dateDropdown');
            dropdown.querySelector('.dropdown-trigger').classList.remove('active');
            dropdown.querySelector('.dropdown-menu').classList.remove('show');
            
            // Remove overlay
            const overlay = document.querySelector('.calendar-dropdown-overlay');
            if (overlay) {
                overlay.remove();
            }
            
            renderCalendar();
            showNotification(`Fecha seleccionada: ${dateStr}`, 'success');
        }

        // Close dropdowns when clicking outside
        document.addEventListener('click', function(event) {
            if (!event.target.closest('.custom-dropdown') && !event.target.closest('.calendar-dropdown-overlay')) {
                document.querySelectorAll('.custom-dropdown').forEach(dropdown => {
                    dropdown.querySelector('.dropdown-trigger').classList.remove('active');
                    dropdown.querySelector('.dropdown-menu').classList.remove('show');
                });
                
                // Remove overlay
                const overlay = document.querySelector('.calendar-dropdown-overlay');
                if (overlay) {
                    overlay.remove();
                }
            }
        });

        // Enhanced clearCreateForm function
        function clearCreateForm() {
            document.getElementById('createTaskForm').reset();
            
            // Reset dropdown displays
            document.getElementById('selectedDateText').textContent = 'Seleccionar fecha';
            document.getElementById('selectedPriorityText').textContent = 'Seleccionar prioridad';
            document.getElementById('selectedSubjectText').textContent = 'Seleccionar materia';
            
            // Reset hidden inputs
            document.getElementById('newTaskDate').value = '';
            document.getElementById('newTaskPriority').value = '';
            document.getElementById('newTaskSubject').value = '';
            
            // Close all dropdowns
            document.querySelectorAll('.custom-dropdown').forEach(dropdown => {
                dropdown.querySelector('.dropdown-trigger').classList.remove('active');
                dropdown.querySelector('.dropdown-menu').classList.remove('show');
            });
            
            setDefaultDate();
            showNotification('🗑️ Formulario limpiado', 'info');
        }

        // Load saved preferences on startup
        document.addEventListener('DOMContentLoaded', function() {
            const savedTheme = localStorage.getItem('taskmaster_theme') || 'palette1';
            const savedFontSize = localStorage.getItem('taskmaster_font_size') || 'medium';
            
            changeTheme(savedTheme);
            changeFontSize(savedFontSize);
            
            // Initialize dark mode after a short delay to ensure elements are loaded
            setTimeout(initializeDarkMode, 100);
        });
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'97c35b6ec656cc79',t:'MTc1NzM4NjAwNi4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>

