# CivisBR — Dados para o Cidadão

Civic tech brasileira que cruza bases de dados governamentais com inteligência artificial para revelar o que os números escondem — e entregar transparência de verdade para quem paga a conta.

**Site:** https://civisbr.github.io · **GitHub Org:** https://github.com/civisBR

---

## O que é o CivisBR

O Brasil tem leis de transparência exemplares. O problema é que os dados existem, mas estão espalhados em dezenas de portais, em formatos incompatíveis, sem cruzamento entre si.

O CivisBR conecta essas fontes com IA para transformar planilhas complexas em respostas claras: o município está gastando bem? Os repasses chegaram? Os preços pagos são compatíveis com o mercado?

Não somos um partido, não temos patrocinador, não temos agenda política. Somos código aberto, dados abertos e LAI.

---

## Projetos

### 💊 MedAudit SUS
**Repositório:** [`civisBR/medicamentos-sus-sorocaba-sp`](https://github.com/civisBR/medicamentos-sus-sorocaba-sp)

Cruza as notas de empenho de medicamentos da Prefeitura de Sorocaba com o Banco de Preços em Saúde do Ministério da Saúde. Quando o preço pago está 30% ou mais acima da mediana nacional, um alerta é gerado e analisado por IA.

`Python` · `Claude API` · `BPS/MS` · `CATMAT` · `BrasilAPI`

---

### 🏥 RepasseSUS
**Repositório:** [`civisBR/repasses-saude-sorocaba-sp`](https://github.com/civisBR/repasses-saude-sorocaba-sp)

Painel público atualizado automaticamente que mostra quanto o governo federal repassou para a saúde de Sorocaba, por programa (PAB, CAPS, SAMU, Farmácia Básica), e compara com municípios de porte similar.

`HTML/JS` · `GitHub Pages` · `FNS/MS` · `SIOPS` · `Chart.js`

---

## Como funciona

```
01 COLETA        Scripts Python coletam dados dos portais públicos —
                 transparência municipal, Portal Federal, DATASUS e BPS.

02 NORMALIZAÇÃO  Nomes padronizados com fuzzy matching, unidades convertidas,
                 CNPJs enriquecidos — tudo pronto para comparação.

03 ANÁLISE       Os casos críticos são enviados para o Claude API, que produz
                 um relatório narrativo priorizando o que merece investigação.

04 PUBLICAÇÃO    CSV, HTML e painel interativo publicados abertamente —
                 para jornalistas, vereadores e qualquer cidadão usar.
```

---

## Fontes de dados

| Sigla | Nome | O que fornece |
|---|---|---|
| BPS/MS | Banco de Preços em Saúde | Preços de referência de medicamentos |
| FNS/MS | Fundo Nacional de Saúde | Repasses federais por programa |
| SIOPS | Orçamentos Públicos em Saúde | Declaração de gastos municipais em saúde |
| Portal Transparência | Governo Federal | Transferências da União aos municípios |
| TCE-SP | Tribunal de Contas de SP | Contratos e licitações das prefeituras paulistas |
| BrasilAPI | Receita Federal | Dados cadastrais de fornecedores (CNPJ) |

---

## Adaptando para outro município

Todo o código é aberto, documentado e pensado para ser replicado. Se você é de outra cidade:

1. Faça fork do repositório que deseja adaptar
2. Ajuste o código IBGE do município no arquivo de configuração
3. Substitua o portal de transparência local (a maioria usa o mesmo padrão TCE-SP)
4. Atualize as chaves de API necessárias (Claude API, BrasilAPI)
5. Publique no GitHub Pages — custo zero

---

## Princípios

- **Transparência radical** — todo dado é público, todo código é aberto
- **Sem acusação** — apontamos inconsistências para investigação; acusar é trabalho do Ministério Público
- **IA a serviço do cidadão** — modelos de linguagem transformam dados brutos em relatórios legíveis
- **Foco municipal** — começamos por Sorocaba, onde o impacto de um real mal gasto é sentido na UBS do bairro

---

## Aviso legal

Os dados utilizados são 100% públicos, coletados de fontes governamentais oficiais conforme a **Lei de Acesso à Informação (Lei 12.527/2011)**. Este projeto não acusa ninguém — aponta inconsistências para investigação. Toda conclusão deve ser verificada com os documentos originais.

Denúncias formais: [CGU Fala.BR](https://falabr.cgu.gov.br) · [TCE-SP](https://www.tce.sp.gov.br)

---

## Licença

MIT License — veja [LICENSE](LICENSE) para detalhes.

Código aberto · Dados públicos · Feito com ♥ em Sorocaba, SP
