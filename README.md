<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Меню | Капучино оттенки | Ресторан</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #d9c7b3;  /* фон — тёплый капучино с молочным отливом */
            font-family: 'Inter', 'Segoe UI', 'Roboto', system-ui, -apple-system, 'Helvetica Neue', sans-serif;
            padding: 2rem 1.5rem;
            color: #2b211b;
        }

        /* главный контейнер — матовый, сливочно-кофейный */
        .menu-container {
            max-width: 1280px;
            margin: 0 auto;
            background: #fbf7f0;  /* основа цвета latte */
            border-radius: 36px;
            box-shadow: 0 25px 45px -12px rgba(60, 40, 25, 0.35);
            overflow: hidden;
            border: 1px solid #e2cfb6;
        }

        /* внутренний отступ, без шапки (строгость) */
        .menu-inner {
            padding: 2.2rem 2rem 2.5rem;
        }

        /* категории с акцентами под капучино */
        .category {
            margin-bottom: 2.8rem;
        }

        .category-title {
            font-family: 'Georgia', 'Times New Roman', serif;
            font-size: 1.65rem;
            font-weight: 600;
            color: #7b4a2e;  /* тёмно-коричневый, как кортado */
            border-left: 6px solid #bb8b64;
            padding-left: 20px;
            margin-bottom: 1.4rem;
            display: flex;
            align-items: center;
            gap: 12px;
            flex-wrap: wrap;
            letter-spacing: -0.2px;
        }

        .category-title span {
            font-size: 0.7rem;
            background: #ede3d5;
            padding: 4px 12px;
            border-radius: 50px;
            font-weight: 500;
            color: #8f623f;
            font-family: system-ui, sans-serif;
            letter-spacing: normal;
        }

        /* сетка блюд */
        .items-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(290px, 1fr));
            gap: 12px 20px;
        }

        /* карточка блюда — строгая, но благородная */
        .menu-item {
            display: flex;
            justify-content: space-between;
            align-items: baseline;
            background: #ffffff;
            padding: 12px 18px;
            border-radius: 20px;
            border: 1px solid #e5d5c0;
            transition: all 0.2s ease;
            cursor: default;
            box-shadow: 0 1px 2px rgba(0,0,0,0.02);
        }

        .menu-item:hover {
            background: #fef7ef;
            border-color: #cfa97e;
            transform: translateX(3px);
        }

        .item-name {
            font-weight: 600;
            font-size: 1rem;
            color: #38281d;
            letter-spacing: -0.2px;
            word-break: break-word;
        }

        .item-price {
            font-weight: 700;
            font-size: 1rem;
            color: #a56338;
            background: #f5ebe0;
            padding: 3px 12px;
            border-radius: 60px;
            white-space: nowrap;
            margin-left: 16px;
            font-family: 'JetBrains Mono', monospace, 'Courier New';
        }

        /* блок напитков с более глубоким кофейным подтоном */
        .drinks-wrap {
            background: #fdf9f2;
            border-radius: 28px;
            padding: 0.8rem 0.5rem 0.5rem 0.8rem;
            border: 1px solid #e0ceb4;
        }

        /* футер — сдержанный, эспрессо-оттенок */
        .footer-thin {
            margin-top: 2rem;
            text-align: center;
            font-size: 0.7rem;
            color: #a27b59;
            border-top: 1px solid #e4d3be;
            padding-top: 1.6rem;
            letter-spacing: 0.3px;
        }

        @media (max-width: 650px) {
            body {
                padding: 1rem;
            }
            .menu-inner {
                padding: 1.5rem;
            }
            .category-title {
                font-size: 1.4rem;
            }
            .menu-item {
                padding: 10px 14px;
            }
            .item-name {
                font-size: 0.92rem;
            }
        }
    </style>
</head>
<body>
<div class="menu-container">
    <div class="menu-inner">

        <!-- ЗАВТРАКИ / СУПЫ / ГОРЯЧИЕ БЛЮДА -->
        <div class="category">
            <div class="category-title">
                ЗАВТРАКИ · СУПЫ · ГОРЯЧИЕ БЛЮДА
                <span>домашний уют</span>
            </div>
            <div class="items-grid">
                <div class="menu-item"><div class="item-name">Шорпа</div><div class="item-price">400₽</div></div>
                <div class="menu-item"><div class="item-name">Латман</div><div class="item-price">400₽</div></div>
                <div class="menu-item"><div class="item-name">Манты</div><div class="item-price">400₽</div></div>
                <div class="menu-item"><div class="item-name">Омлет</div><div class="item-price">250₽</div></div>
                <div class="menu-item"><div class="item-name">Шакшука</div><div class="item-price">250₽</div></div>
                <div class="menu-item"><div class="item-name">Яичница</div><div class="item-price">150₽</div></div>
                <div class="menu-item"><div class="item-name">Блины 3 шт с ягодами</div><div class="item-price">230₽</div></div>
                <div class="menu-item"><div class="item-name">Сырники</div><div class="item-price">250₽</div></div>
                <div class="menu-item"><div class="item-name">Каши (в ассортименте)</div><div class="item-price">100₽</div></div>
            </div>
        </div>

        <!-- ХЫЧИНЫ БАЛКАРСКИЕ -->
        <div class="category">
            <div class="category-title">
                ХЫЧИНЫ БАЛКАРСКИЕ
                <span>традиционная выпечка</span>
            </div>
            <div class="items-grid">
                <div class="menu-item"><div class="item-name">Хычины с мясом</div><div class="item-price">250₽</div></div>
                <div class="menu-item"><div class="item-name">Хычины (сыр, зелень)</div><div class="item-price">180₽</div></div>
                <div class="menu-item"><div class="item-name">Хычины (сыр, картошка)</div><div class="item-price">180₽</div></div>
            </div>
        </div>

        <!-- САЛАТЫ (точная структура из PDF + дубль хычин) -->
        <div class="category">
            <div class="category-title">
                САЛАТЫ И НАРЕЗКИ
                <span>свежесть</span>
            </div>
            <div class="items-grid">
                <div class="menu-item"><div class="item-name">Хычины (сыр, картошка)</div><div class="item-price">180₽</div></div>
                <div class="menu-item"><div class="item-name">Овощи (нарезка)</div><div class="item-price">450₽</div></div>
                <div class="menu-item"><div class="item-name">Салат овощной</div><div class="item-price">200₽</div></div>
                <div class="menu-item"><div class="item-name">Морковный салат</div><div class="item-price">120₽</div></div>
                <div class="menu-item"><div class="item-name">Свекольный салат</div><div class="item-price">150₽</div></div>
                <div class="menu-item"><div class="item-name">Греческий салат</div><div class="item-price">350₽</div></div>
            </div>
        </div>

        <!-- ЧЕБУРЕКИ -->
        <div class="category">
            <div class="category-title">
                ЧЕБУРЕКИ
                <span>хрустящие, золотистые</span>
            </div>
            <div class="items-grid">
                <div class="menu-item"><div class="item-name">Чебуреки с сыром</div><div class="item-price">200₽</div></div>
                <div class="menu-item"><div class="item-name">Чебуреки с мясом</div><div class="item-price">230₽</div></div>
            </div>
        </div>

        <!-- ШАШЛЫК / БЛЮДА НА МАНГАЛЕ (капучино-стиль: сдержанно) -->
        <div class="category">
            <div class="category-title">
                ШАШЛЫК · БЛЮДА НА МАНГАЛЕ
                <span>уголь, аромат дыма</span>
            </div>
            <div class="items-grid">
                <div class="menu-item"><div class="item-name">Баранина мякоть</div><div class="item-price">1000₽</div></div>
                <div class="menu-item"><div class="item-name">Баранина спинка</div><div class="item-price">900₽</div></div>
                <div class="menu-item"><div class="item-name">Тепятина мякоть</div><div class="item-price">1000₽</div></div>
                <div class="menu-item"><div class="item-name">Куриный шашлык</div><div class="item-price">700₽</div></div>
                <div class="menu-item"><div class="item-name">Жау-баур</div><div class="item-price">400₽</div></div>
                <div class="menu-item"><div class="item-name">Форель порц</div><div class="item-price">800₽</div></div>
                <div class="menu-item"><div class="item-name">Люля</div><div class="item-price">300₽</div></div>
                <div class="menu-item"><div class="item-name">Овощи на мангале</div><div class="item-price">450₽</div></div>
                <div class="menu-item"><div class="item-name">Карп</div><div class="item-price">750₽</div></div>
                <div class="menu-item"><div class="item-name">Грибы на мангале</div><div class="item-price">350₽</div></div>
            </div>
        </div>

        <!-- НАПИТКИ — оттенок молочной пенки -->
        <div class="category">
            <div class="category-title">
                НАПИТКИ
                <span>облепиха, травы, классика</span>
            </div>
            <div class="drinks-wrap">
                <div class="items-grid">
                    <div class="menu-item"><div class="item-name">Чай облепиховый 500мл</div><div class="item-price">250₽</div></div>
                    <div class="menu-item"><div class="item-name">Чай травяной 500мл</div><div class="item-price">200₽</div></div>
                    <div class="menu-item"><div class="item-name">Чай черный</div><div class="item-price">30₽</div></div>
                    <div class="menu-item"><div class="item-name">Чай зеленый</div><div class="item-price">30₽</div></div>
                    <div class="menu-item"><div class="item-name">Кофе</div><div class="item-price">80₽</div></div>
                    <div class="menu-item"><div class="item-name">Лимонад</div><div class="item-price">80₽</div></div>
                    <div class="menu-item"><div class="item-name">Айран</div><div class="item-price">50₽</div></div>
                </div>
            </div>
        </div>

        <div class="footer-thin">
            ⋆ все блюда и цены в точности из оригинального меню ⋆
        </div>
    </div>
</div>
</body>
</html>
