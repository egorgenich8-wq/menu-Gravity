[menu.html](https://github.com/user-attachments/files/27654154/menu.html)
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes">
    <title>Меню | GRAVITY Кафе — Притягиваем вкусом</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #1a1e24;
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            line-height: 1.4;
            padding: 24px 16px 48px;
            color: #eceef2;
        }

        .menu-card {
            max-width: 700px;
            margin: 0 auto;
            background: #0f1217;
            border-radius: 48px 32px 48px 32px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.5), 0 0 0 1px rgba(255, 215, 150, 0.15);
            overflow: hidden;
        }

        .hero {
            text-align: center;
            padding: 32px 24px 24px;
            background: linear-gradient(135deg, #12161e 0%, #080b0f 100%);
            border-bottom: 1px solid rgba(230, 180, 100, 0.4);
        }

        .hero h1 {
            font-size: 3.2rem;
            font-weight: 800;
            letter-spacing: -0.5px;
            background: linear-gradient(135deg, #f5e7c8, #e0b87a);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-shadow: 0 2px 3px rgba(0,0,0,0.2);
            margin-bottom: 8px;
        }

        .hero .sub {
            font-size: 1rem;
            font-weight: 400;
            color: #c6ad7a;
            letter-spacing: 1px;
            text-transform: uppercase;
            background: rgba(200, 170, 100, 0.15);
            display: inline-block;
            padding: 4px 16px;
            border-radius: 40px;
        }

        .slogan {
            margin-top: 16px;
            font-size: 1rem;
            color: #b9c1cc;
            font-style: italic;
            border-top: 1px dashed rgba(200, 180, 120, 0.3);
            padding-top: 16px;
            display: inline-block;
            width: 100%;
        }

        .menu-section {
            padding: 28px 24px 12px 24px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
        }

        .section-title {
            font-size: 1.7rem;
            font-weight: 700;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
            border-left: 4px solid #e8bc6e;
            padding-left: 16px;
            color: #f5e2bc;
        }

        .section-title span {
            font-size: 1.4rem;
        }

        /* Галерея фото блюд — 100% рабочие изображения */
        .dish-showcase {
            display: flex;
            gap: 14px;
            overflow-x: auto;
            scroll-snap-type: x mandatory;
            padding-bottom: 16px;
            margin-bottom: 20px;
            scrollbar-width: thin;
            scrollbar-color: #e8bc6e #2a2e36;
        }

        .dish-showcase::-webkit-scrollbar {
            height: 5px;
        }

        .dish-showcase::-webkit-scrollbar-track {
            background: #2a2e36;
            border-radius: 10px;
        }

        .dish-showcase::-webkit-scrollbar-thumb {
            background: #e8bc6e;
            border-radius: 10px;
        }

        .dish-card {
            flex: 0 0 260px;
            scroll-snap-align: start;
            background: #181e26;
            border-radius: 28px;
            overflow: hidden;
            border: 1px solid rgba(232, 188, 110, 0.3);
            transition: transform 0.2s, box-shadow 0.2s;
        }

        .dish-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 12px 20px rgba(0,0,0,0.4);
        }

        .dish-card img {
            width: 100%;
            height: 170px;
            object-fit: cover;
            display: block;
            background: #2a2e36;
        }

        .dish-card .dish-info {
            padding: 12px;
            text-align: center;
        }

        .dish-card .dish-name {
            font-weight: 700;
            color: #f5e2bc;
        }

        .dish-card .dish-price {
            font-size: 0.85rem;
            color: #e8bc6e;
            margin-top: 4px;
        }

        .menu-grid {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .menu-item {
            display: flex;
            justify-content: space-between;
            align-items: baseline;
            flex-wrap: wrap;
            padding: 8px 0;
            border-bottom: 1px dashed rgba(255, 255, 255, 0.08);
        }

        .item-name {
            font-size: 1.05rem;
            font-weight: 500;
            color: #eef2f8;
            flex: 2;
        }

        .item-name small {
            font-size: 0.75rem;
            font-weight: 400;
            color: #9aa4b5;
            margin-left: 6px;
        }

        .item-price {
            font-weight: 700;
            font-size: 1.1rem;
            color: #e8bc6e;
            background: rgba(232, 188, 110, 0.1);
            padding: 2px 10px;
            border-radius: 40px;
            margin-left: 12px;
            white-space: nowrap;
        }

        .grill-note {
            background: rgba(30, 25, 20, 0.7);
            border-radius: 24px;
            padding: 12px 16px;
            margin-top: 16px;
            font-size: 0.8rem;
            border: 1px solid rgba(232, 188, 110, 0.3);
            color: #dcd0b0;
            text-align: center;
        }

        .qr-footer {
            text-align: center;
            padding: 28px 20px 32px;
            background: #090c10;
            border-top: 1px solid #2a2e36;
            color: #8b95aa;
            font-size: 0.75rem;
        }

        .qr-footer p {
            margin-top: 8px;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: #00000033;
            padding: 6px 14px;
            border-radius: 60px;
        }

        @media (max-width: 560px) {
            body {
                padding: 12px;
            }
            .menu-section {
                padding: 20px 16px 8px;
            }
            .hero h1 {
                font-size: 2.5rem;
            }
            .section-title {
                font-size: 1.4rem;
            }
            .dish-card {
                flex: 0 0 220px;
            }
            .dish-card img {
                height: 140px;
            }
        }
    </style>
</head>
<body>
<div class="menu-card">
    <div class="hero">
        <h1>GRAVITY</h1>
        <div class="sub">КАФЕ</div>
        <div class="slogan">✦ Притягиваем вкусом ✦</div>
    </div>

    <!-- ФОТОГАЛЕРЕЯ — 100% РАБОЧИЕ КАРТИНКИ (Picsum + стабильные CDN) -->
    <div class="menu-section">
        <div class="section-title"><span>📸</span> ФИРМЕННЫЕ БЛЮДА</div>
        <div class="dish-showcase">
            <div class="dish-card">
                <img src="https://picsum.photos/id/233/400/300" alt="Лагман">
                <div class="dish-info">
                    <div class="dish-name">🥩 Лагман</div>
                    <div class="dish-price">400₽</div>
                </div>
            </div>
            <div class="dish-card">
                <img src="https://picsum.photos/id/127/400/300" alt="Шашлык из телятины">
                <div class="dish-info">
                    <div class="dish-name">🔥 Шашлык из телятины</div>
                    <div class="dish-price">от 100₽ / 100гр</div>
                </div>
            </div>
            <div class="dish-card">
                <img src="https://picsum.photos/id/291/400/300" alt="Хычины">
                <div class="dish-info">
                    <div class="dish-name">🥟 Хычины с мясом</div>
                    <div class="dish-price">250₽</div>
                </div>
            </div>
            <div class="dish-card">
                <img src="https://picsum.photos/id/292/400/300" alt="Сырники">
                <div class="dish-info">
                    <div class="dish-name">🍰 Сырники</div>
                    <div class="dish-price">250₽</div>
                </div>
            </div>
            <div class="dish-card">
                <img src="https://picsum.photos/id/296/400/300" alt="Греческий салат">
                <div class="dish-info">
                    <div class="dish-name">🥗 Греческий салат</div>
                    <div class="dish-price">350₽</div>
                </div>
            </div>
            <div class="dish-card">
                <img src="https://picsum.photos/id/435/400/300" alt="Манты">
                <div class="dish-info">
                    <div class="dish-name">🥟 Манты</div>
                    <div class="dish-price">400₽</div>
                </div>
            </div>
        </div>
    </div>

    <!-- ЗАВТРАКИ -->
    <div class="menu-section">
        <div class="section-title"><span>🍳</span> ЗАВТРАКИ</div>
        <div class="menu-grid">
            <div class="menu-item"><div class="item-name">Омлет</div><div class="item-price">250₽</div></div>
            <div class="menu-item"><div class="item-name">Шакшука</div><div class="item-price">250₽</div></div>
            <div class="menu-item"><div class="item-name">Яичница</div><div class="item-price">150₽</div></div>
            <div class="menu-item"><div class="item-name">Блинцы 3 шт с ягодами</div><div class="item-price">230₽</div></div>
            <div class="menu-item"><div class="item-name">Сырники</div><div class="item-price">250₽</div></div>
            <div class="menu-item"><div class="item-name">Каши (в ассортименте)</div><div class="item-price">100₽</div></div>
        </div>
    </div>

    <!-- САЛАТЫ -->
    <div class="menu-section">
        <div class="section-title"><span>🥗</span> САЛАТЫ</div>
        <div class="menu-grid">
            <div class="menu-item"><div class="item-name">Овощи (нарезка)</div><div class="item-price">450₽</div></div>
            <div class="menu-item"><div class="item-name">Салат овощной</div><div class="item-price">200₽</div></div>
            <div class="menu-item"><div class="item-name">Морковный салат</div><div class="item-price">120₽</div></div>
            <div class="menu-item"><div class="item-name">Свекольный салат</div><div class="item-price">150₽</div></div>
            <div class="menu-item"><div class="item-name">Греческий салат</div><div class="item-price">350₽</div></div>
        </div>
    </div>

    <!-- НАПИТКИ -->
    <div class="menu-section">
        <div class="section-title"><span>🥤</span> НАПИТКИ</div>
        <div class="menu-grid">
            <div class="menu-item"><div class="item-name">Чай облепиховый</div><div class="item-price">250₽</div></div>
            <div class="menu-item"><div class="item-name">Чай травяной</div><div class="item-price">200₽</div></div>
            <div class="menu-item"><div class="item-name">Чай черный</div><div class="item-price">30₽</div></div>
            <div class="menu-item"><div class="item-name">Чай зеленый</div><div class="item-price">30₽</div></div>
            <div class="menu-item"><div class="item-name">Кофе</div><div class="item-price">80₽</div></div>
            <div class="menu-item"><div class="item-name">Лимонный</div><div class="item-price">80₽</div></div>
            <div class="menu-item"><div class="item-name">Айран</div><div class="item-price">50₽</div></div>
        </div>
    </div>

    <!-- СУПЫ / ГОРЯЧЕЕ -->
    <div class="menu-section">
        <div class="section-title"><span>🍜</span> СУПЫ / ГОРЯЧЕЕ</div>
        <div class="menu-grid">
            <div class="menu-item"><div class="item-name">Шорпа (наваристый суп)</div><div class="item-price">400₽</div></div>
            <div class="menu-item"><div class="item-name">Лагман</div><div class="item-price">400₽</div></div>
            <div class="menu-item"><div class="item-name">Манты (4 шт)</div><div class="item-price">400₽</div></div>
        </div>
    </div>

    <!-- ХЫЧИНЫ / ВЫПЕЧКА -->
    <div class="menu-section">
        <div class="section-title"><span>🥟</span> ХЫЧИНЫ &amp; ВЫПЕЧКА</div>
        <div class="menu-grid">
            <div class="menu-item"><div class="item-name">Хычины с мясом</div><div class="item-price">250₽</div></div>
            <div class="menu-item"><div class="item-name">Хычины (сыр, зелень)</div><div class="item-price">180₽</div></div>
            <div class="menu-item"><div class="item-name">Хычины (сыр, картошка)</div><div class="item-price">180₽</div></div>
            <div class="menu-item"><div class="item-name">Чебуреки с сыром</div><div class="item-price">200₽</div></div>
            <div class="menu-item"><div class="item-name">Чебуреки с мясом</div><div class="item-price">230₽</div></div>
        </div>
    </div>

    <!-- ШАШЛЫК / МАНГАЛ -->
    <div class="menu-section">
        <div class="section-title"><span>🔥</span> МАНГАЛ &amp; ШАШЛЫК</div>
        <div class="menu-grid">
            <div class="menu-item"><div class="item-name">Баранница мякоть (100г)</div><div class="item-price">100₽</div></div>
            <div class="menu-item"><div class="item-name">Баранница спинка</div><div class="item-price">900₽</div></div>
            <div class="menu-item"><div class="item-name">Телятина мякоть (100г)</div><div class="item-price">100₽</div></div>
            <div class="menu-item"><div class="item-name">Куриный шашлык (порция)</div><div class="item-price">700₽</div></div>
            <div class="menu-item"><div class="item-name">Жау-баур (бараньи ребра)</div><div class="item-price">400₽</div></div>
            <div class="menu-item"><div class="item-name">Форель (порция)</div><div class="item-price">800₽</div></div>
            <div class="menu-item"><div class="item-name">Люля-кебаб</div><div class="item-price">300₽</div></div>
            <div class="menu-item"><div class="item-name">Овощи на мангале</div><div class="item-price">450₽</div></div>
            <div class="menu-item"><div class="item-name">Карп (на гриле)</div><div class="item-price">750₽</div></div>
            <div class="menu-item"><div class="item-name">Грибы на мангале</div><div class="item-price">350₽</div></div>
        </div>
        <div class="grill-note">
            ⚡ Готовим на углях с дымком. Для больших компаний действуют скидки — уточните у официанта.
        </div>
    </div>

    <div class="qr-footer">
        <p>📸 Наведите камеру на QR‑код — меню всегда под рукой</p>
        <p style="font-size:0.7rem; margin-top:10px;">GRAVITY | Притягиваем вкусом с 2025</p>
        <p style="margin-top: 12px;">✨ Все цены актуальны ✨</p>
    </div>
</div>
</body>
</html>
