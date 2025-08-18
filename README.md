<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Prime Distribution Group</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            color: #333;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            line-height: 1.6;
        }
        header {
            background-color: #001f3f;
            color: white;
            text-align: center;
            padding: 20px;
            position: relative;
        }
        header img {
            max-width: 40%;
            height: auto;
        }
        #lang-selector {
            position: absolute;
            top: 20px;
            right: 20px;
        }
        main {
            max-width: 1200px;
            margin: 20px auto;
            padding: 20px;
            background: white;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        section {
            margin-bottom: 40px;
        }
        h1, h2 {
            color: #001f3f;
        }
        #title {
            color: white;
        }
        footer {
            text-align: center;
            padding: 10px;
            background-color: #001f3f;
            color: white;
        }
        .contact-info {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 10px;
        }
        .banner-image {
            max-width: 100%;
            height: auto;
            display: block;
            margin: 20px auto;
        }
    </style>
</head>
<body>
    <header>
        <img src="logo.png" alt="Prime Distribution Group">
        <h1 id="title">Prime Distribution Group</h1>
        <select id="lang-selector" onchange="changeLanguage(this.value)">
            <option value="pl">Polski</option>
            <option value="en">English</option>
            <option value="de">Deutsch</option>
            <option value="zh">中文 (简体)</option>
        </select>
    </header>
    <main>
        <section id="about-us">
            <h2 id="about-title">O nas</h2>
            <p id="desc1"></p>
            <p id="desc2"></p>
            <p id="desc3"></p>
        </section>
        <section id="import">
            <h2 id="import-title"></h2>
            <p id="import1"></p>
            <p id="import2"></p>
            <p id="import3"></p>
            <p id="import4"></p>
            <p id="import5"></p>
        </section>
        <section id="import-scale">
            <h2 id="scale-title"></h2>
            <p id="scale-desc1"></p>
            <h3 id="scale-params-title"></h3>
            <ul>
                <li id="scale-param1"></li>
                <li id="scale-param2"></li>
            </ul>
            <h3 id="scale-coop-title"></h3>
            <ul>
                <li id="scale-coop1"></li>
                <li id="scale-coop2"></li>
                <li id="scale-coop3"></li>
                <li id="scale-coop4"></li>
            </ul>
            <h3 id="scale-benefits-title"></h3>
            <ul>
                <li id="scale-benefit1"></li>
                <li id="scale-benefit2"></li>
                <li id="scale-benefit3"></li>
            </ul>
        </section>
        <section id="payment-methods">
            <h2 id="payment-title"></h2>
            <p id="payment-desc"></p>
        </section>
        <img src="containers_airplane.png" alt="Shipping containers and airplane" class="banner-image">
    </main>
    <footer>
        <div class="contact-info">
            <span id="email"></span>
            <span id="instagram"></span>
            <span id="location"></span>
        </div>
        <p id="copyright"></p>
    </footer>
    <script>
        const translations = {
            pl: {
                title: "Prime Distribution Group",
                aboutTitle: "O nas",
                desc1: "Prime Distribution Group to nowoczesna hurtownia internetowa o niezwykle szerokim wyborze asortymentu. W naszej ofercie znajdują się m.in. akcesoria elektroniczne, sprzęt komputerowy, gadżety, RTV i AGD, artykuły fotograficzne oraz wiele innych praktycznych i oryginalnych produktów. Towary sprowadzamy głównie z rynków azjatyckich, w szczególności z Chin, dzięki czemu jesteśmy w stanie zapewnić naszym klientom konkurencyjne ceny.",
                desc2: "Jesteśmy zlokalizowani w Polsce co pozwala nam utrzymywać krótkie terminy dostaw, co przekłada się na szybkie terminy realizacji zamówień. W przeciwieństwie do wielu innych hurtowni, które sprowadzają niewielkie partie towarów w wyższych cenach, my możemy zaoferować atrakcyjniejsze warunki zakupu dzięki bezpośredniemu importowi i długoletnim relacjom z producentami.",
                desc3: "Wieloletnie doświadczenie, rozbudowana sieć kontaktów oraz sprawdzony model współpracy z fabrykami zagranicznymi sprawiają, że nasza hurtownia zapewnia wyjątkowo korzystny stosunek ceny do jakości. Dzięki nam zyskują Państwo wygodny dostęp do szerokiego wachlarza artykułów w jednym miejscu – bez potrzeby przeszukiwania wielu różnych sklepów. Prime Distribution Group to jedno z najlepiej zaopatrzonych centrów dystrybucji on-line, oferujące towar w cenach hurtowych, dostępny od ręki.",
                importTitle: "Import produktów z Chin – Prime Distribution Group",
                import1: "Od wielu lat specjalizujemy się w sprowadzaniu towarów z Chin, co pozwala nam oferować naszym partnerom biznesowym szeroki wybór produktów w atrakcyjnych cenach. Regularnie monitorujemy trendy konsumenckie w Polsce i na bieżąco dostosowujemy nasz asortyment, aby odpowiadał aktualnym potrzebom rynku. Każda nowa dostawa to okazja do wzbogacenia oferty o ciekawe nowości.",
                import2: "Aby maksymalnie ułatwić zakupy, nasza hurtownia internetowa została przejrzyście podzielona na kategorie tematyczne. Znajdą tu Państwo m.in.: elektronikę i akcesoria komputerowe, sprzęt do konsol i tabletów, produkty dla domu i ogrodu, akcesoria motoryzacyjne, oświetlenie, odzież, obuwie i biżuterię, artykuły sportowe i turystyczne, sprzęt multimedialny, gadżety, gry, instrumenty muzyczne, grillów i pieców oraz akcesoria z nimi związane. W ofercie nie brakuje również kategorii takich jak uroda, zdrowie, czy produkty dla zwierząt.",
                import3: "Dodatkowo przygotowaliśmy zakładki Nowości, Bestsellery oraz Promocje, aby szybciej dotrzeć do najciekawszych propozycji. Każdy artykuł opatrzony jest szczegółowym opisem, zdjęciami, informacjami o cenie oraz dostępności. Proces zakupowy został zaprojektowany w taki sposób, aby był szybki, wygodny i intuicyjny – wystarczy dodać wybrane produkty do koszyka i sfinalizować zamówienie kilkoma kliknięciami.",
                import4: "Oferujemy także możliwość porównywania i obserwowania interesujących Państwa towarów, co ułatwia podejmowanie decyzji zakupowych. W przypadku dodatkowych pytań, nasz zespół pozostaje do dyspozycji i chętnie udzieli niezbędnych informacji.",
                import5: "Współpraca z nami to gwarancja, że Państwa oferta handlowa stanie się bardziej atrakcyjna, a konkurencyjne ceny pozytywnie zaskoczą klientów.",
                scaleTitle: "Skala importu",
                scaleDesc1: "Jesteśmy dużym importerem hurtowym. Budujemy długoterminowe relacje oparte na stabilnych i powtarzalnych zamówieniach. Standardowe zamówienia realizujemy jako FCL (Full Container Load) – kilka pełnych kontenerów jednego produktu w jednym zleceniu (mix 40’HC/40’ i 20’), zapewniając powtarzalną jakość, stabilne ceny i szybki obrót. FCL nadaje się do dużych wolumenów, minimalizując przeładunki w porównaniu z LCL.",
                scaleParamsTitle: "Parametry referencyjne:",
                scaleParam1: "20’ (1 TEU): ~33 m³, do 10-11 palet EUR.",
                scaleParam2: "40’/40’HC (2 TEU): ~67-76 m³ (HC wyższy), do 20-25 palet EUR.",
                scaleCoopTitle: "Współpraca z dostawcami",
                scaleCoop1: "Ramowe zamówienia z harmonogramem załadunków (kilka kontenerów per slot).",
                scaleCoop2: "Preferowane Incoterms®: FOB/CIF (morski); możliwe DAP w UE (reguły ICC definiujące podział kosztów/ryzyka).",
                scaleCoop3: "Konsolidacja w FCL jednej SKU lub miksy wariantów – bez pośrednich przeładunków.",
                scaleCoop4: "Kontrola jakości (QC/inspection) przed załadunkiem.",
                scaleBenefitsTitle: "Korzyści dla partnerów w Chinach",
                scaleBenefit1: "Przewidywalna produkcja (ciągłe serie, pełne załadunki).",
                scaleBenefit2: "Niższy koszt jednostkowy (pełna kubatura, mniej przeładunków).",
                scaleBenefit3: "Szybsze obroty dzięki stałym slotom i odprawie w UE.",
                paymentTitle: "Metody Płatności",
                paymentDesc: "W Prime Distribution Group dbamy o bezpieczeństwo oraz wygodę transakcji, oferując naszym partnerom biznesowym sprawdzone i bezpieczne metody płatności. Dla zapewnienia najwyższego poziomu ochrony zarówno dla kupujących, jak i sprzedających, korzystamy z usługi escrow. Escrow to zaufana forma zabezpieczenia płatności, która polega na tym, że środki są przechowywane przez niezależnego pośrednika do momentu spełnienia warunków transakcji. Dopiero po ich weryfikacji środki zostają przekazane sprzedającemu, co zapewnia obie strony, że transakcja zostanie zrealizowana zgodnie z umową. Dzięki temu minimalizujemy ryzyko zarówno dla kupujących, jak i sprzedających, co jest szczególnie istotne w przypadku międzynarodowych transakcji. W przypadku jakichkolwiek pytań dotyczących metod płatności lub szczegółów współpracy, nasz zespół jest do Państwa dyspozycji, gotowy udzielić wszelkich niezbędnych informacji.",
                email: 'Email: <a href="mailto:primedistributiongrouppl@gmail.com">primedistributiongrouppl@gmail.com</a>',
                instagram: 'Instagram: <a href="https://www.instagram.com/primedistributiongroup/">@primedistributiongroup</a>',
                location: 'Siedziba: Polska',
                copyright: "&copy; 2025 Prime Distribution Group. Wszelkie prawa zastrzeżone."
            },
            en: {
                title: "Prime Distribution Group",
                aboutTitle: "About Us",
                desc1: "Prime Distribution Group is a modern online wholesale store with an extremely wide range of products. Our offer includes, among others, electronic accessories, computer equipment, gadgets, RTV and AGD, photographic articles, and many other practical and original products. We import goods mainly from Asian markets, particularly from China, which allows us to provide our customers with competitive prices.",
                desc2: "We are located in Poland, which allows us to maintain short delivery times, translating into fast order fulfillment times. Unlike many other wholesalers who import small batches of goods at higher prices, we can offer more attractive purchase conditions thanks to direct import and long-term relationships with manufacturers.",
                desc3: "Years of experience, an extensive network of contacts, and a proven model of cooperation with foreign factories make our wholesale store provide an exceptionally favorable price-to-quality ratio. Thanks to us, you gain convenient access to a wide range of articles in one place – without the need to search many different stores. Prime Distribution Group is one of the best-stocked online distribution centers, offering goods at wholesale prices, available immediately.",
                importTitle: "Import of Products from China – Prime Distribution Group",
                import1: "For many years, we have specialized in importing goods from China, which allows us to offer our business partners a wide selection of products at attractive prices. We regularly monitor consumer trends in Poland and continuously adjust our assortment to meet current market needs. Each new delivery is an opportunity to enrich the offer with interesting novelties.",
                import2: "To maximize shopping convenience, our online wholesale store has been clearly divided into thematic categories. You will find here, among others: electronics and computer accessories, equipment for consoles and tablets, products for home and garden, automotive accessories, lighting, clothing, footwear and jewelry, sports and tourist articles, multimedia equipment, gadgets, games, musical instruments, grills and ovens along with related accessories. The offer also includes categories such as beauty, health, or pet products.",
                import3: "Additionally, we have prepared tabs for New Arrivals, Bestsellers, and Promotions to quickly reach the most interesting proposals. Each article is provided with a detailed description, photos, price information, and availability. The purchasing process has been designed to be fast, convenient, and intuitive – just add selected products to the cart and finalize the order with a few clicks.",
                import4: "We also offer the possibility of comparing and observing items of interest, which facilitates making purchasing decisions. In case of additional questions, our team is at your disposal and will gladly provide the necessary information.",
                import5: "Cooperation with us is a guarantee that your commercial offer will become more attractive, and competitive prices will positively surprise customers.",
                scaleTitle: "Import Scale",
                scaleDesc1: "We are a large wholesale importer. We build long-term relationships based on stable and repeatable orders. Standard orders are executed as FCL (Full Container Load) – several full containers of one product in one order (mix 40’HC/40’ and 20’), ensuring consistent quality, stable prices, and fast turnover. FCL is suitable for large volumes, minimizing transshipments compared to LCL.",
                scaleParamsTitle: "Reference parameters:",
                scaleParam1: "20’ (1 TEU): ~33 m³, up to 10-11 EUR pallets.",
                scaleParam2: "40’/40’HC (2 TEU): ~67-76 m³ (HC higher), up to 20-25 EUR pallets.",
                scaleCoopTitle: "Cooperation with suppliers",
                scaleCoop1: "Framework orders with loading schedule (several containers per slot).",
                scaleCoop2: "Preferred Incoterms®: FOB/CIF (sea); possible DAP in EU (ICC rules defining cost/risk division).",
                scaleCoop3: "Consolidation in FCL one SKU or mixes of variants – without intermediate transshipments.",
                scaleCoop4: "Quality control (QC/inspection) before loading.",
                scaleBenefitsTitle: "Benefits for partners in China",
                scaleBenefit1: "Predictable production (continuous series, full loads).",
                scaleBenefit2: "Lower unit cost (full cubature, fewer transshipments).",
                scaleBenefit3: "Faster turnovers thanks to fixed slots and clearance in EU.",
                paymentTitle: "Payment Methods",
                paymentDesc: "At Prime Distribution Group, we prioritize the security and convenience of transactions, offering our business partners proven and safe payment methods. To ensure the highest level of protection for both buyers and sellers, we use escrow services. Escrow is a trusted form of payment security where funds are held by an independent intermediary until the transaction conditions are met. Only after verification are the funds released to the seller, ensuring both parties that the transaction will be completed as agreed. This minimizes risk for both buyers and sellers, which is particularly important in international transactions. If you have any questions regarding payment methods or cooperation details, our team is at your disposal, ready to provide all necessary information.",
                email: 'Email: <a href="mailto:primedistributiongrouppl@gmail.com">primedistributiongrouppl@gmail.com</a>',
                instagram: 'Instagram: <a href="https://www.instagram.com/primedistributiongroup/">@primedistributiongroup</a>',
                location: 'Location: Poland',
                copyright: "&copy; 2025 Prime Distribution Group. All rights reserved."
            },
            de: {
                title: "Prime Distribution Group",
                aboutTitle: "Über uns",
                desc1: "Prime Distribution Group ist ein modernes Online-Großhandelsgeschäft mit einer extrem breiten Palette an Produkten. Unser Angebot umfasst unter anderem elektronisches Zubehör, Computergeräte, Gadgets, RTV und AGD, fotografische Artikel sowie viele andere praktische und originelle Produkte. Wir importieren Waren hauptsächlich von asiatischen Märkten, insbesondere aus China, was uns ermöglicht, unseren Kunden wettbewerbsfähige Preise anzubieten.",
                desc2: "Wir sind in Polen ansässig, was uns ermöglicht, kurze Lieferzeiten einzuhalten, was sich in schnellen Auftragsabwicklungszeiten niederschlägt. Im Gegensatz zu vielen anderen Großhändlern, die kleine Mengen an Waren zu höheren Preisen importieren, können wir attraktivere Einkaufsbedingungen bieten dank direktem Import und langjährigen Beziehungen zu Herstellern.",
                desc3: "Jahrelange Erfahrung, ein umfangreiches Netzwerk von Kontakten und ein bewährtes Kooperationsmodell mit ausländischen Fabriken sorgen dafür, dass unser Großhandelsgeschäft ein außergewöhnlich günstiges Preis-Leistungs-Verhältnis bietet. Dank uns erhalten Sie bequemen Zugang zu einer breiten Palette von Artikeln an einem Ort – ohne die Notwendigkeit, viele verschiedene Geschäfte zu durchsuchen. Prime Distribution Group ist eines der bestbestückten Online-Verteilungszentren, das Waren zu Großhandelspreisen anbietet, die sofort verfügbar sind.",
                importTitle: "Import von Produkten aus China – Prime Distribution Group",
                import1: "Seit vielen Jahren spezialisieren wir uns auf den Import von Waren aus China, was uns ermöglicht, unseren Geschäftspartnern eine breite Auswahl an Produkten zu attraktiven Preisen anzubieten. Wir überwachen regelmäßig Verbrauchertrends in Polen und passen unser Sortiment laufend an die aktuellen Marktanforderungen an. Jede neue Lieferung ist eine Gelegenheit, das Angebot um interessante Neuheiten zu erweitern.",
                import2: "Um den Einkauf maximal zu erleichtern, ist unser Online-Großhandelsgeschäft klar in thematische Kategorien unterteilt. Sie finden hier unter anderem: Elektronik und Computerzubehör, Ausrüstung für Konsolen und Tablets, Produkte für Haus und Garten, Autozubehör, Beleuchtung, Kleidung, Schuhe und Schmuck, Sport- und Touristenartikel, Multimedia-Ausrüstung, Gadgets, Spiele, Musikinstrumente, Grills und Öfen sowie damit verbundene Zubehörteile. Das Angebot umfasst auch Kategorien wie Schönheit, Gesundheit oder Produkte für Tiere.",
                import3: "Zusätzlich haben wir Tabs für Neuheiten, Bestseller und Aktionen vorbereitet, um schneller zu den interessantesten Vorschlägen zu gelangen. Jeder Artikel ist mit einer detaillierten Beschreibung, Fotos, Preisinformationen und Verfügbarkeit versehen. Der Kaufprozess ist so gestaltet, dass er schnell, bequem und intuitiv ist – einfach die ausgewählten Produkte in den Warenkorb legen und die Bestellung mit wenigen Klicks abschließen.",
                import4: "Wir bieten auch die Möglichkeit, interessierende Waren zu vergleichen und zu beobachten, was die Kaufentscheidungen erleichtert. Bei zusätzlichen Fragen steht unser Team zur Verfügung und gibt gerne die notwendigen Informationen.",
                import5: "Die Zusammenarbeit mit uns ist eine Garantie dafür, dass Ihr Handelsangebot attraktiver wird und wettbewerbsfähige Preise die Kunden positiv überraschen.",
                scaleTitle: "Importskala",
                scaleDesc1: "Wir sind ein großer Großhandelsimporteur. Wir bauen langfristige Beziehungen auf, die auf stabilen und wiederholbaren Bestellungen basieren. Standardbestellungen werden als FCL (Full Container Load) ausgeführt – mehrere volle Container eines Produkts in einer Bestellung (Mix 40’HC/40’ und 20’), um konsistente Qualität, stabile Preise und schnellen Umsatz zu gewährleisten. FCL eignet sich für große Volumina und minimiert Umladungen im Vergleich zu LCL.",
                scaleParamsTitle: "Referenzparameter:",
                scaleParam1: "20’ (1 TEU): ~33 m³, bis zu 10-11 EUR-Paletten.",
                scaleParam2: "40’/40’HC (2 TEU): ~67-76 m³ (HC höher), bis zu 20-25 EUR-Paletten.",
                scaleCoopTitle: "Zusammenarbeit mit Lieferanten",
                scaleCoop1: "Rahmenbestellungen mit Ladezeitplan (mehrere Container pro Slot).",
                scaleCoop2: "Bevorzugte Incoterms®: FOB/CIF (See); möglich DAP in der EU (ICC-Regeln, die Kosten-/Risikoverteilung definieren).",
                scaleCoop3: "Konsolidierung in FCL einer SKU oder Variantenmischungen – ohne Zwischenumladen.",
                scaleCoop4: "Qualitätskontrolle (QC/Inspection) vor dem Laden.",
                scaleBenefitsTitle: "Vorteile für Partner in China",
                scaleBenefit1: "Vorhersehbare Produktion (kontinuierliche Serien, volle Ladungen).",
                scaleBenefit2: "Niedrigere Stückkosten (volle Kubatur, weniger Umladungen).",
                scaleBenefit3: "Schnellere Umsätze dank fester Slots und Zollabfertigung in der EU.",
                paymentTitle: "Zahlungsmethoden",
                paymentDesc: "Bei Prime Distribution Group legen wir Wert auf die Sicherheit und Bequemlichkeit von Transaktionen und bieten unseren Geschäftspartnern bewährte und sichere Zahlungsmethoden an. Um den höchsten Schutz für Käufer und Verkäufer zu gewährleisten, nutzen wir den Escrow-Service. Escrow ist eine vertrauenswürdige Form der Zahlungssicherung, bei der die Mittel von einem unabhängigen Vermittler gehalten werden, bis die Transaktionsbedingungen erfüllt sind. Erst nach Überprüfung werden die Mittel an den Verkäufer freigegeben, was beide Parteien sicherstellt, dass die Transaktion vertragsgemäß abgeschlossen wird. Dadurch minimieren wir das Risiko für Käufer und Verkäufer, was besonders bei internationalen Transaktionen wichtig ist. Bei Fragen zu Zahlungsmethoden oder Kooperationsdetails steht unser Team zur Verfügung und gibt gerne alle notwendigen Informationen.",
                email: 'E-Mail: <a href="mailto:primedistributiongrouppl@gmail.com">primedistributiongrouppl@gmail.com</a>',
                instagram: 'Instagram: <a href="https://www.instagram.com/primedistributiongroup/">@primedistributiongroup</a>',
                location: 'Sitz: Polen',
                copyright: "&copy; 2025 Prime Distribution Group. Alle Rechte vorbehalten."
            },
            zh: {
                title: "Prime Distribution Group",
                aboutTitle: "关于我们",
                desc1: "Prime Distribution Group 是一家现代化的在线批发商店，拥有极其广泛的产品选择。我们的产品包括电子配件、计算机设备、小工具、RTV 和 AGD、摄影用品以及许多其他实用和原创产品。我们主要从亚洲市场进口商品，特别是从中国，这使我们能够为客户提供具有竞争力的价格。",
                desc2: "我们位于波兰，这使我们能够保持较短的交货时间，从而实现快速的订单履行时间。与许多其他批发商不同，他们以更高的价格进口小批量商品，我们可以通过直接进口和与制造商的长期关系提供更具吸引力的购买条件。",
                desc3: "多年的经验、广泛的联系网络以及与外国工厂的成熟合作模式，使我们的批发商店提供异常优惠的价格质量比。多亏了我们，您可以在一个地方方便地访问广泛的文章范围 – 无需搜索许多不同的商店。Prime Distribution Group 是库存最充足的在线分销中心之一，提供批发价格的商品，即时可用。",
                importTitle: "从中国进口产品 – Prime Distribution Group",
                import1: "多年来，我们专注于从中国进口商品，这使我们能够为我们的商业伙伴提供广泛的产品选择，以吸引人的价格。我们定期监测波兰的消费趋势，并不断调整我们的产品范围，以满足当前的市场需求。每一次新交货都是丰富产品范围的有趣新奇事物的机会。",
                import2: "为了最大限度地便利购物，我们的在线批发商店被清晰地分为主题类别。您将在这里找到：电子产品和计算机配件、游戏机和平板电脑设备、家用和花园产品、汽车配件、照明、服装、鞋类和珠宝、体育和旅游用品、多媒体设备、小工具、游戏、乐器、烧烤炉和烤箱以及相关配件。产品还包括美容、健康或宠物产品等类别。",
                import3: "此外，我们准备了新品、畅销品和促销标签，以便更快地访问最有趣的提议。每件物品都附有详细描述、照片、价格信息和可用性。购买过程设计得快速、方便和直观 – 只需将选定的产品添加到购物车并通过几次点击完成订单。",
                import4: "我们还提供比较和观察感兴趣物品的可能性，这有助于做出购买决定。如果有其他问题，我们的团队随时为您服务，并乐意提供必要的信息。",
                import5: "与我们合作是保证您的商业报价变得更有吸引力，而竞争性价格将积极惊喜客户。",
                scaleTitle: "进口规模",
                scaleDesc1: "我们是一家大型批发进口商。我们基于稳定和可重复的订单建立长期关系。标准订单作为FCL（Full Container Load）执行 – 一个订单中几个完整集装箱的一个产品（混合40’HC/40’和20’），确保一致的质量、稳定的价格和快速周转。FCL适用于大批量，相比LCL最小化转运。",
                scaleParamsTitle: "参考参数：",
                scaleParam1: "20’ (1 TEU): ~33 m³, 最多10-11个EUR托盘。",
                scaleParam2: "40’/40’HC (2 TEU): ~67-76 m³ (HC更高), 最多20-25个EUR托盘。",
                scaleCoopTitle: "与供应商合作",
                scaleCoop1: "框架订单，带有装载时间表（每个槽位几个集装箱）。",
                scaleCoop2: "首选Incoterms®: FOB/CIF（海运）；欧盟内可能DAP（ICC规则定义成本/风险分配）。",
                scaleCoop3: "FCL中一个SKU或变体混合的整合 – 无中间转运。",
                scaleCoop4: "装载前的质量控制（QC/检查）。",
                scaleBenefitsTitle: "对中国伙伴的好处",
                scaleBenefit1: "可预测的生产（连续系列，满载）。",
                scaleBenefit2: "更低的单位成本（满立方体，更少转运）。",
                scaleBenefit3: "通过固定槽位和欧盟清关实现更快的周转。",
                paymentTitle: "支付方式",
                paymentDesc: "在 Prime Distribution Group，我们重视交易的安全性和便利性，为我们的商业伙伴提供经过验证的安全支付方式。为了确保买卖双方最高水平的保护，我们使用托管服务。托管是一种可信的支付保障形式，资金由独立中介持有，直到交易条件满足。只有在验证后，资金才释放给卖方，确保双方交易按约定完成。这最小化了买卖双方的风险，这在国际交易中尤为重要。如果您对支付方式或合作细节有任何疑问，我们的团队随时为您服务，愿意提供所有必要信息。",
                email: '电子邮件: <a href="mailto:primedistributiongrouppl@gmail.com">primedistributiongrouppl@gmail.com</a>',
                instagram: 'Instagram: <a href="https://www.instagram.com/primedistributiongroup/">@primedistributiongroup</a>',
                location: '位置: 波兰',
                copyright: "&copy; 2025 Prime Distribution Group。保留所有权利。"
            }
        };

        function changeLanguage(lang) {
            localStorage.setItem('lang', lang);
            location.reload();
        }

        window.onload = function() {
            const lang = localStorage.getItem('lang') || 'pl';
            document.getElementById('lang-selector').value = lang;
            const texts = translations[lang];
            document.getElementById('title').innerText = texts.title;
            document.getElementById('about-title').innerText = texts.aboutTitle;
            document.getElementById('desc1').innerText = texts.desc1;
            document.getElementById('desc2').innerText = texts.desc2;
            document.getElementById('desc3').innerText = texts.desc3;
            document.getElementById('import-title').innerText = texts.importTitle;
            document.getElementById('import1').innerText = texts.import1;
            document.getElementById('import2').innerText = texts.import2;
            document.getElementById('import3').innerText = texts.import3;
            document.getElementById('import4').innerText = texts.import4;
            document.getElementById('import5').innerText = texts.import5;
            document.getElementById('scale-title').innerText = texts.scaleTitle;
            document.getElementById('scale-desc1').innerText = texts.scaleDesc1;
            document.getElementById('scale-params-title').innerText = texts.scaleParamsTitle;
            document.getElementById('scale-param1').innerText = texts.scaleParam1;
            document.getElementById('scale-param2').innerText = texts.scaleParam2;
            document.getElementById('scale-coop-title').innerText = texts.scaleCoopTitle;
            document.getElementById('scale-coop1').innerText = texts.scaleCoop1;
            document.getElementById('scale-coop2').innerText = texts.scaleCoop2;
            document.getElementById('scale-coop3').innerText = texts.scaleCoop3;
            document.getElementById('scale-coop4').innerText = texts.scaleCoop4;
            document.getElementById('scale-benefits-title').innerText = texts.scaleBenefitsTitle;
            document.getElementById('scale-benefit1').innerText = texts.scaleBenefit1;
            document.getElementById('scale-benefit2').innerText = texts.scaleBenefit2;
            document.getElementById('scale-benefit3').innerText = texts.scaleBenefit3;
            document.getElementById('payment-title').innerText = texts.paymentTitle;
            document.getElementById('payment-desc').innerText = texts.paymentDesc;
            document.getElementById('email').innerHTML = texts.email;
            document.getElementById('instagram').innerHTML = texts.instagram;
            document.getElementById('location').innerHTML = texts.location;
            document.getElementById('copyright').innerHTML = texts.copyright;
        };
    </script>
</body>
</html>
