<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TaskMaster AI - Gestión Inteligente</title>
    
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --bg-color: #F0F8FF;
            --primary-color: #1E90FF;
            --secondary-color: #98FB98;
            --accent-color: #87CEEB;
            --text-color: #2F4F4F;
            --card-bg: #FFFFFF;
            --border-color: #B0E0E6;
            --shadow-color: rgba(30, 144, 255, 0.2);
            --glow-color: rgba(30, 144, 255, 0.4);
            --success-color: #32CD32;
            --warning-color: #FFD700;
            --danger-color: #FF4500;
            --overdue-color: #DC143C;
        }

        [data-theme="palette2"] {
            --bg-color: #FFFACD;
            --primary-color: #FFD700;
            --secondary-color: #FFA500;
            --accent-color: #FFFF99;
            --text-color: #8B4513;
            --card-bg: #FFFFFF;
            --border-color: #F0E68C;
            --shadow-color: rgba(255, 215, 0, 0.3);
            --glow-color: rgba(255, 215, 0, 0.5);
            --success-color: #32CD32;
            --warning-color: #FF8C00;
            --danger-color: #FF4500;
            --overdue-color: #DC143C;
        }

        [data-theme="palette3"] {
            --bg-color: #E6F0FA;
            --primary-color: #3CB371;
            --secondary-color: #20B2AA;
            --accent-color: #98FB98;
            --text-color: #006400;
            --card-bg: #FFFFFF;
            --border-color: #90EE90;
            --shadow-color: rgba(60, 179, 113, 0.3);
            --glow-color: rgba(60, 179, 113, 0.5);
            --success-color: #32CD32;
            --warning-color: #FFD700;
            --danger-color: #FF4500;
            --overdue-color: #DC143C;
        }

        [data-theme="palette4"] {
            --bg-color: #E6E6FA;
            --primary-color: #6A5ACD;
            --secondary-color: #BA55D3;
            --accent-color: #DDA0DD;
            --text-color: #4B0082;
            --card-bg: #FFFFFF;
            --border-color: #D8BFD8;
            --shadow-color: rgba(106, 90, 205, 0.3);
            --glow-color: rgba(106, 90, 205, 0.5);
            --success-color: #32CD32;
            --warning-color: #FFD700;
            --danger-color: #FF4500;
            --overdue-color: #DC143C;
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

