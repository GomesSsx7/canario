# Plano de melhorias — controle de criatório

Esta branch **não deve ser publicada nem mesclada na main** até confirmar se contém exatamente o aplicativo de produção. O projeto tem apenas `claucriatorio.html` e persiste dados via `localStorage`; o site público mencionado pelo proprietário usa autenticação e pagamentos, que **não aparecem neste arquivo**.

## Verificações antes de publicar
- Confirmar a origem do deploy atualmente em produção, incluindo o arquivo de entrada.
- Identificar código do login, cobrança e renovação; não mexer no valor de R$ 70 sem autorização específica.
- Exportar backup do plantel, testar restauração e verificar telas no celular.
- Testar teclado, formulários, números e datas, criação/edição/exclusão de aves, casais, ninhadas, saúde, financeiro e exportações.
- Verificar URL canônica e domínio correto antes de permitir indexação.

## 20 pontos do pedido
| Item | Situação/decisão |
|---|---|
| 1. Política de privacidade | Pendente: identificar controlador, contato e fluxos reais de dados para texto correto conforme LGPD |
| 2. Termos de uso | Pendente: regras comerciais, cancelamento e assinatura reais |
| 3. CTA limpa | Pendente no site comercial, inexistente no arquivo |
| 4. Perguntas frequentes | Pendente: respostas verificadas sobre assinatura e suporte |
| 5. robots.txt | Pendente: validar origem do deploy e domínio de produção |
| 6. sitemap.xml | Pendente: validar quais URLs públicas devem ser indexadas |
| 7. 404 personalizada | Pendente no site público; depende da configuração de rotas |
| 8. Texto alternativo | Revisão parcial de controles; auditoria visual ainda necessária |
| 9. Análises | Pendente: ferramenta aprovada e consentimento para rastreadores opcionais |
| 10. Meta títulos | Aplicado título descritivo ao arquivo nesta branch |
| 11. Meta descrição | Aplicada descrição inicial nesta branch |
| 12. Compartilhamento social | Pendente: URL canônica e imagem oficial |
| 13. Favicon | Pendente: ativo de marca oficial |
| 14. URLs canônicas | Pendente: confirmar URLs finais |
| 15. Consentimentos de cookies | Não criar banner fictício: auditar cookies e trackers usados em produção primeiro |
| 16. Versão mobile | CSS responsivo pré-existente; testes em dispositivos pendentes |
| 17. Acessibilidade | Melhorias de teclado, diálogo e avisos aplicadas parcialmente |
| 18. Formulários de teste | Pendente: testes completos sem dados reais |
| 19. Links quebrados | Pendente: rastrear site real e corrigir links confirmados |
| 20. Desempenho | Pendente: medições antes/depois na versão publicada |

## Correções implementadas nesta branch
- Datas locais sem deslocamento UTC ao criar e avançar datas.
- Rejeição de datas impossíveis.
- Verificação estrutural antes de carregar dados locais em memória.
- Atalho de pular ao conteúdo, rótulos de navegação, feedback acessível e gerenciamento básico de foco de modais.
- Título e descrição mais claros; `noindex` temporário no arquivo isolado, para evitar indexação indevida da versão errada.

**Atenção:** a presença de `noindex` é provisória, intencional e deve ser revista quando o projeto correto e a URL final forem confirmados.
