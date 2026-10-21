# Campos Pass — Plataforma nacional de turismo

## Estado confirmado do repositório (21/10/2026)
- `index.html` é um protótipo mobile em HTML/CSS/JS com páginas de início, mapa, pass, perfil e conteúdos de Campos do Jordão.
- Há interações de demonstração (alertas, ofertas simuladas, clima e perfil fictícios). **Não** são reservas ou benefícios confirmados.
- `marketplace.html` é a primeira vitrine nacional e apresentação de afiliados/parceiros. Não coleta dados em backend, não processa pagamentos nem cria contas.

## Visão do produto
Marketplace de destinos, meios de hospedagem, experiências e serviços turísticos, com usuários turistas, fornecedores, afiliados e administração. Começar por Campos do Jordão, evoluir para Brasil e depois destinos internacionais, sem prometer cobertura universal antes de ter catálogo e fornecedores.

## Modelo de monetização
1. Comissão sobre vendas confirmadas e elegíveis, pactuada por fornecedor.
2. Repasse de parte da comissão aos afiliados, sempre com aprovação e regras de estorno.
3. Mensalidades opcionais de recursos B2B e anúncios patrocinados identificados.
4. Plano VIP opcional somente após benefícios contratuais reais.

## Banco de dados e segurança (Supabase/Postgres)
Tabelas sugeridas: profiles (roles), destinations, providers, listings, inventory, bookings, payments, affiliate_profiles, affiliate_links, referral_clicks, attributions, commissions, payouts, reviews, partner_contracts, audit_logs. Usar RLS por papel, política explícita para informações sensíveis, consentimento LGPD, logs imutáveis para comissões e segregação por fornecedor. Validar preços, estoque, assinatura de webhooks e atribuição no backend; nunca no front-end. Não guardar cartão de crédito diretamente.

## Regras iniciais de atribuição (a confirmar comercial e juridicamente)
- Link de afiliado com token opaco persistido em banco; janela de atribuição configurável.
- Comissão calculada sobre base contratual líquida apropriada, após confirmação, taxas aplicáveis, cancelamentos e chargebacks.
- Exibir status pendente/aprovada/paga/estornada, demonstrativos e regras de saque.
- Prevenir fraudes, autoindicações e cliques artificiais.

## Roadmap de entrega
**Fase 1 — MVP público:** catálogo real de Campos do Jordão, painel de administração, cadastro de fornecedores, páginas de produto, busca, SEO e PWA instalável. Não publicar produtos sem autorização.
**Fase 2 — Comércio:** autenticação, calendário e estoque, checkout via provedor de pagamentos/marketplace, confirmação e cancelamento, vouchers válidos e atendimento.
**Fase 3 — Afiliados:** cadastro verificado, links rastreáveis, atribuição backend, comissões, relatórios, aprovação e repasses.
**Fase 4 — Escala:** novas cidades e destinos, avaliações verificadas, assinaturas, personalização, idiomas e app Android/iOS.

## Publicação nas lojas
Site/PWA é o começo. Android pode exigir wrapper confiável e requisitos específicos da Play Store; iOS requer empacotamento nativo e atendimento às políticas da App Store. Contas de desenvolvedor, metadados, privacidade, testes e aprovação das lojas são etapas separadas; presença no GitHub Pages não equivale a publicação.

## Antes de vender
Conseguir parceiros e contratos, definir responsável legal da operação, revisar Cadastur e obrigações conforme a atividade, CDC, LGPD, emissão fiscal e regras de intermediação. Não anunciar cashback ou descontos sem fonte de custeio formal e condições de uso.
