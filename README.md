# esglog-website
Site corporativo ESGLOG - Consultoria em Logística
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ESGLOG - Consultoria Estratégica em Logística Integrada</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --green-primary: #2D7B4D;
            --teal-primary: #1A5E6F;
            --gray-50: #f8f9fa;
            --gray-100: #e9ecef;
            --gray-200: #dee2e6;
            --gray-600: #495057;
            --gray-800: #212529;
            --white: #ffffff;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--gray-800);
            background: var(--white);
        }

        header {
            background: var(--white);
            border-bottom: 1px solid var(--gray-100);
            padding: 1.5rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            font-weight: 700;
            font-size: 1.5rem;
            color: var(--gray-800);
        }

        .logo-icon {
            width: 36px;
            height: 36px;
            background: linear-gradient(135deg, var(--green-primary) 0%, var(--teal-primary) 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-weight: 800;
        }

        nav {
            display: flex;
            gap: 2.5rem;
        }

        nav a {
            text-decoration: none;
            color: var(--gray-600);
            font-size: 0.95rem;
            transition: color 0.3s;
        }

        nav a:hover {
            color: var(--green-primary);
        }

        .hero {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            padding: 6rem 0;
            text-align: center;
        }

        .hero-content h1 {
            font-size: 3rem;
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: 1rem;
            color: var(--gray-800);
        }

        .hero-subtitle {
            font-size: 1.25rem;
            color: var(--teal-primary);
            margin-bottom: 0.5rem;
            font-weight: 600;
        }

        .hero-description {
            font-size: 1.1rem;
            color: var(--gray-600);
            max-width: 700px;
            margin: 2rem auto;
            line-height: 1.8;
        }

        .hero-services {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 1.5rem;
            flex-wrap: wrap;
            font-weight: 500;
            font-size: 0.95rem;
            color: var(--gray-600);
        }

        .hero-services span {
            padding: 0.5rem 1rem;
            background: var(--white);
            border: 1px solid var(--gray-200);
            border-radius: 20px;
        }

        .cta-group {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            margin-top: 3rem;
            flex-wrap: wrap;
        }

        .cta-primary {
            background: var(--green-primary);
            color: var(--white);
            padding: 1rem 2.5rem;
            border: none;
            border-radius: 4px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: background 0.3s;
            text-decoration: none;
            display: inline-block;
        }

        .cta-primary:hover {
            background: #1e5838;
        }

        .cta-secondary {
            background: var(--white);
            color: var(--teal-primary);
            padding: 1rem 2.5rem;
            border: 2px solid var(--teal-primary);
            border-radius: 4px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            text-decoration: none;
            display: inline-block;
        }

        .cta-secondary:hover {
            background: var(--teal-primary);
            color: var(--white);
        }

        section {
            padding: 4rem 0;
        }

        section h2 {
            font-size: 2.2rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            color: var(--gray-800);
        }

        .section-subtitle {
            font-size: 1.1rem;
            color: var(--gray-600);
            margin-bottom: 3rem;
        }

        .processo {
            background: var(--gray-50);
        }

        .processo-steps {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
            gap: 1.5rem;
            margin-bottom: 3rem;
        }

        .step {
            background: var(--white);
            padding: 2rem;
            border-radius: 4px;
            border: 1px solid var(--gray-200);
            text-align: center;
            transition: all 0.3s;
            position: relative;
        }

        .step:hover {
            border-color: var(--green-primary);
            box-shadow: 0 4px 12px rgba(45, 123, 77, 0.1);
        }

        .step-number {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, var(--green-primary), var(--teal-primary));
            color: var(--white);
            font-size: 1.5rem;
            font-weight: 700;
            border-radius: 50%;
            margin-bottom: 1rem;
        }

        .step-text {
            font-weight: 600;
            color: var(--gray-800);
            font-size: 1rem;
        }

        .step-arrow {
            display: none;
            position: absolute;
            right: -15px;
            top: 50%;
            transform: translateY(-50%);
            color: var(--green-primary);
            font-size: 1.5rem;
            font-weight: bold;
        }

        @media (min-width: 768px) {
            .step-arrow {
                display: block;
            }
            .processo-steps {
                grid-template-columns: repeat(6, 1fr);
            }
            .step:last-child .step-arrow {
                display: none;
            }
        }

        .solucoes {
            background: var(--white);
        }

        .solucoes-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .solucao-card {
            background: var(--white);
            border: 1px solid var(--gray-200);
            border-radius: 4px;
            padding: 2rem;
            transition: all 0.3s;
        }

        .solucao-card:hover {
            border-color: var(--teal-primary);
            box-shadow: 0 8px 24px rgba(26, 94, 111, 0.12);
            transform: translateY(-2px);
        }

        .solucao-title {
            font-size: 1.25rem;
            font-weight: 700;
            color: var(--gray-800);
            margin-bottom: 1rem;
            padding-bottom: 1rem;
            border-bottom: 2px solid var(--green-primary);
        }

        .solucao-items {
            list-style: none;
        }

        .solucao-items li {
            padding: 0.5rem 0;
            color: var(--gray-600);
            font-size: 0.95rem;
        }

        .solucao-items li:before {
            content: "→ ";
            color: var(--teal-primary);
            font-weight: bold;
            margin-right: 0.5rem;
        }

        .rede {
            background: var(--gray-50);
        }

        .rede-intro {
            text-align: center;
            margin-bottom: 3rem;
        }

        .rede-intro p {
            font-size: 1.1rem;
            color: var(--gray-600);
            max-width: 600px;
            margin: 0 auto;
            line-height: 1.8;
        }

        .parceiros-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
            margin-bottom: 3rem;
        }

        .parceiro-tipo {
            background: var(--white);
            padding: 1.5rem;
            border-radius: 4px;
            border-left: 4px solid var(--green-primary);
            font-weight: 600;
            color: var(--gray-800);
            text-align: center;
        }

        .funcionamento {
            background: var(--white);
        }

        .fluxo-container {
            background: var(--gray-50);
            padding: 2rem;
            border-radius: 4px;
            margin-bottom: 2rem;
        }

        .fluxo-item {
            display: flex;
            gap: 1.5rem;
            margin-bottom: 1.5rem;
            align-items: flex-start;
        }

        .fluxo-numero {
            flex-shrink: 0;
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: var(--teal-primary);
            color: var(--white);
            border-radius: 50%;
            font-weight: 700;
            font-size: 1.1rem;
        }

        .fluxo-texto {
            flex: 1;
        }

        .fluxo-texto h4 {
            color: var(--gray-800);
            margin-bottom: 0.25rem;
            font-weight: 600;
        }

        .fluxo-texto p {
            color: var(--gray-600);
            font-size: 0.95rem;
        }

        .diferenciais {
            background: var(--gray-50);
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 1.5rem;
            padding: 2rem;
            border-radius: 4px;
            margin-bottom: 2rem;
        }

        .diferencial-item {
            display: flex;
            gap: 1rem;
            align-items: flex-start;
        }

        .diferencial-check {
            flex-shrink: 0;
            color: var(--green-primary);
            font-weight: bold;
            font-size: 1.5rem;
            margin-top: 0.25rem;
        }

        .diferencial-texto {
            color: var(--gray-800);
            font-weight: 500;
            font-size: 0.95rem;
            line-height: 1.4;
        }

        .chamada-final {
            background: linear-gradient(135deg, var(--green-primary), var(--teal-primary));
            color: var(--white);
            text-align: center;
            padding: 4rem 2rem;
        }

        .chamada-final h2 {
            color: var(--white);
            font-size: 2.2rem;
            margin-bottom: 1.5rem;
        }

        .chamada-final p {
            font-size: 1.1rem;
            max-width: 700px;
            margin: 0 auto 2rem;
            line-height: 1.8;
            opacity: 0.95;
        }

        footer {
            background: var(--gray-800);
            color: var(--white);
            text-align: center;
            padding: 2rem 0;
            font-size: 0.9rem;
            margin-top: 4rem;
        }

        @media (max-width: 768px) {
            .hero-content h1 {
                font-size: 2rem;
            }

            nav {
                display: none;
            }

            .container {
                padding: 0 1rem;
            }

            section {
                padding: 2rem 0;
            }

            section h2 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container header-content">
            <div class="logo">
                <div class="logo-icon">E</div>
                <span>ESGLOG</span>
            </div>
            <nav>
                <a href="#como-trabalhamos">Como trabalhamos</a>
                <a href="#solucoes">Soluções</a>
                <a href="#rede">Rede</a>
                <a href="#contato">Contato</a>
            </nav>
        </div>
    </header>

    <main>
        <section class="hero">
            <div class="container">
                <div class="hero-content">
                    <div class="hero-subtitle">Consultoria Estratégica em Logística Integrada</div>
                    <h1>Inteligência que conecta toda a cadeia logística</h1>
                    <div class="hero-services">
                        <span>Transporte</span>
                        <span>Armazenagem</span>
                        <span>Comércio Exterior</span>
                        <span>Supply Chain</span>
                        <span>ESG</span>
                    </div>
                    <p class="hero-description">
                        Da estratégia à operação, entregamos soluções logísticas através de uma rede de parceiros homologados.
                    </p>
                    <div class="cta-group">
                        <button class="cta-primary">Solicitar Diagnóstico Logístico</button>
                        <button class="cta-secondary">Fale com um Especialista</button>
                    </div>
                </div>
            </div>
        </section>

        <section class="processo" id="como-trabalhamos">
            <div class="container">
                <h2>Como trabalhamos</h2>
                <p class="section-subtitle">Seis etapas que garantem eficiência e resultados</p>
                
                <div class="processo-steps">
                    <div class="step">
                        <div class="step-number">1</div>
                        <div class="step-text">Entendemos sua necessidade</div>
                        <div class="step-arrow">→</div>
                    </div>
                    <div class="step">
                        <div class="step-number">2</div>
                        <div class="step-text">Desenvolvemos a solução</div>
                        <div class="step-arrow">→</div>
                    </div>
                    <div class="step">
                        <div class="step-number">3</div>
                        <div class="step-text">Selecionamos o parceiro ideal</div>
                        <div class="step-arrow">→</div>
                    </div>
                    <div class="step">
                        <div class="step-number">4</div>
                        <div class="step-text">Negociamos as melhores condições</div>
                        <div class="step-arrow">→</div>
                    </div>
                    <div class="step">
                        <div class="step-number">5</div>
                        <div class="step-text">Gerenciamos toda a operação</div>
                        <div class="step-arrow">→</div>
                    </div>
                    <div class="step">
                        <div class="step-number">6</div>
                        <div class="step-text">Monitoramos indicadores e resultados</div>
                    </div>
                </div>
            </div>
        </section>

        <section class="solucoes" id="solucoes">
            <div class="container">
                <h2>Nossas soluções</h2>
                <p class="section-subtitle">Portfólio completo de serviços logísticos</p>
                
                <div class="solucoes-grid">
                    <div class="solucao-card">
                        <div class="solucao-title">Transporte Rodoviário</div>
                        <ul class="solucao-items">
                            <li>Carga lotação</li>
                            <li>Carga fracionada</li>
                            <li>Containers</li>
                            <li>Carga projeto</li>
                            <li>Produtos perigosos</li>
                            <li>Carga refrigerada</li>
                        </ul>
                    </div>

                    <div class="solucao-card">
                        <div class="solucao-title">Armazenagem</div>
                        <ul class="solucao-items">
                            <li>Centros de distribuição</li>
                            <li>REDEX</li>
                            <li>Cross Docking</li>
                            <li>Transit Point</li>
                            <li>Gestão de estoques</li>
                            <li>Fulfillment</li>
                        </ul>
                    </div>

                    <div class="solucao-card">
                        <div class="solucao-title">Comércio Exterior</div>
                        <ul class="solucao-items">
                            <li>Despacho aduaneiro</li>
                            <li>Importação</li>
                            <li>Exportação</li>
                            <li>Frete internacional</li>
                            <li>Frete marítimo</li>
                            <li>Frete aéreo</li>
                        </ul>
                    </div>

                    <div class="solucao-card">
                        <div class="solucao-title">Consultoria</div>
                        <ul class="solucao-items">
                            <li>Supply chain</li>
                            <li>BIDs</li>
                            <li>Custos logísticos</li>
                            <li>KPIs</li>
                            <li>Planejamento</li>
                            <li>Torre de controle</li>
                        </ul>
                    </div>

                    <div class="solucao-card">
                        <div class="solucao-title">ESG & Sustentabilidade</div>
                        <ul class="solucao-items">
                            <li>Inventário de carbono</li>
                            <li>Escopo 3</li>
                            <li>ISO 14083</li>
                            <li>Descarbonização</li>
                            <li>Indicadores ESG</li>
                            <li>Relatórios</li>
                        </ul>
                    </div>

                    <div class="solucao-card">
                        <div class="solucao-title">Cabotagem</div>
                        <ul class="solucao-items">
                            <li>Transporte costeiro</li>
                            <li>Consolidação de cargas</li>
                            <li>Operações portuárias</li>
                            <li>Rastreamento</li>
                            <li>Documentação</li>
                            <li>Assessoria</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <section class="rede" id="rede">
            <div class="container">
                <h2>Rede ESGLOG</h2>
                <div class="rede-intro">
                    <p>Uma rede nacional de parceiros homologados. A ESGLOG possui uma rede de empresas criteriosamente selecionadas para atender operações logísticas em todo o Brasil e no mercado internacional.</p>
                </div>

                <div class="parceiros-grid">
                    <div class="parceiro-tipo">Transportadoras</div>
                    <div class="parceiro-tipo">Operadores Logísticos</div>
                    <div class="parceiro-tipo">Armazéns Gerais</div>
                    <div class="parceiro-tipo">Centros de Distribuição</div>
                    <div class="parceiro-tipo">Freight Forwarders</div>
                    <div class="parceiro-tipo">NVOCC</div>
                    <div class="parceiro-tipo">Despachantes Aduaneiros</div>
                    <div class="parceiro-tipo">Armadores</div>
                    <div class="parceiro-tipo">Transporte Internacional</div>
                    <div class="parceiro-tipo">Empresas de Tecnologia</div>
                    <div class="parceiro-tipo">Consultorias Especializadas</div>
                </div>
            </div>
        </section>

        <section class="funcionamento" id="funcionamento">
            <div class="container">
                <h2>Como funciona</h2>
                <p class="section-subtitle">Um processo estruturado e transparente</p>

                <div class="fluxo-container">
                    <div class="fluxo-item">
                        <div class="fluxo-numero">1</div>
                        <div class="fluxo-texto">
                            <h4>Demanda do cliente</h4>
                            <p>O cliente envia sua demanda para a ESGLOG com detalhes da operação logística necessária.</p>
                        </div>
                    </div>

                    <div class="fluxo-item">
                        <div class="fluxo-numero">2</div>
                        <div class="fluxo-texto">
                            <h4>Diagnóstico técnico</h4>
                            <p>Nossa equipe realiza uma análise profunda da necessidade, identificando os melhores caminhos.</p>
                        </div>
                    </div>

                    <div class="fluxo-item">
                        <div class="fluxo-numero">3</div>
                        <div class="fluxo-texto">
                            <h4>Seleção de parceiros</h4>
                            <p>Selecionamos os parceiros homologados que melhor atendem aos requisitos técnicos e operacionais.</p>
                        </div>
                    </div>

                    <div class="fluxo-item">
                        <div class="fluxo-numero">4</div>
                        <div class="fluxo-texto">
                            <h4>Negociação</h4>
                            <p>Negociamos as melhores condições comerciais e operacionais para o cliente.</p>
                        </div>
                    </div>

                    <div class="fluxo-item">
                        <div class="fluxo-numero">5</div>
                        <div class="fluxo-texto">
                            <h4>Gerenciamento operacional</h4>
                            <p>Gerenciamos toda a operação com controle de qualidade e governança.</p>
                        </div>
                    </div>

                    <div class="fluxo-item">
                        <div class="fluxo-numero">6</div>
                        <div class="fluxo-texto">
                            <h4>Monitoramento e resultados</h4>
                            <p>Acompanhamos indicadores, apresentamos relatórios e garantimos contínua melhoria.</p>
                        </div>
                    </div>
                </div>

                <h3 style="margin-top: 3rem; margin-bottom: 1.5rem; font-size: 1.5rem;">Diferenciais ESGLOG</h3>
                <div class="diferenciais">
                    <div class="diferencial-item">
                        <div class="diferencial-check">✓</div>
                        <div class="diferencial-texto">Independência na escolha dos parceiros</div>
                    </div>
                    <div class="diferencial-item">
                        <div class="diferencial-check">✓</div>
                        <div class="diferencial-texto">Rede nacional homologada</div>
                    </div>
                    <div class="diferencial-item">
                        <div class="diferencial-check">✓</div>
                        <div class="diferencial-texto">Especialistas em supply chain</div>
                    </div>
                    <div class="diferencial-item">
                        <div class="diferencial-check">✓</div>
                        <div class="diferencial-texto">Gestão completa de projetos</div>
                    </div>
                    <div class="diferencial-item">
                        <div class="diferencial-check">✓</div>
                        <div class="diferencial-texto">Governança operacional</div>
                    </div>
                    <div class="diferencial-item">
                        <div class="diferencial-check">✓</div>
                        <div class="diferencial-texto">Inteligência de dados</div>
                    </div>
                    <div class="diferencial-item">
                        <div class="diferencial-check">✓</div>
                        <div class="diferencial-texto">ESG aplicado à logística</div>
                    </div>
                    <div class="diferencial-item">
                        <div class="diferencial-check">✓</div>
                        <div class="diferencial-texto">Torre de controle</div>
                    </div>
                    <div class="diferencial-item">
                        <div class="diferencial-check">✓</div>
                        <div class="diferencial-texto">Gestão por indicadores</div>
                    </div>
                    <div class="diferencial-item">
                        <div class="diferencial-check">✓</div>
                        <div class="diferencial-texto">Atendimento consultivo</div>
                    </div>
                </div>
            </div>
        </section>

        <section class="chamada-final" id="contato">
            <div class="container">
                <h2>Sua operação logística merece inteligência e governança</h2>
                <p>A ESGLOG conecta sua empresa às melhores soluções logísticas do mercado, gerenciando cada etapa com transparência, eficiência e foco em resultados.</p>
                <button class="cta-primary" style="background: var(--white); color: var(--green-primary);">Solicite um diagnóstico sem compromisso</button>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <p>&copy; 2024 ESGLOG - Consultoria Estratégica em Logística Integrada. Todos os direitos reservados.</p>
            <p style="margin-top: 0.5rem; font-size: 0.85rem;">Santos, SP | Brasil</p>
        </div>
    </footer>

    <script>
        // Smooth scroll para links de navegação
        document.querySelectorAll('nav a').forEach(link => {
            link.addEventListener('click', (e) => {
                const href = link.getAttribute('href');
                if (href.startsWith('#')) {
                    e.preventDefault();
                    const target = document.querySelector(href);
                    if (target) {
                        target.scrollIntoView({ behavior: 'smooth' });
                    }
                }
            });
        });

        // CTAs que podem ser convertidos em links
        document.querySelectorAll('button').forEach(btn => {
            btn.addEventListener('click', function() {
                alert('Clique: ' + this.textContent + '\n\nConfigure um formulário ou integração com seu CRM aqui.');
            });
        });
    </script>
</body>
</html>
