# Auditor de Core Web Vitals e Performance de Carregamento

[![Teste Core Web Vitals](https://img.shields.io/badge/TAVARDT-Core%20Web%20Vitals-5b3cf5.svg)](https://tools.tavardt.com/br/teste-core-web-vitals/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Analise de TTFB, compressao de dados, recursos bloqueantes de renderizacao e prevencao de deslocamento de layout (CLS).

Desenvolvido e mantido pela divisao de engenharia de performance web e experiencia do usuario da **TAVARDT**.

***

## Capacidades de Auditoria de Core Web Vitals

* **Analise de Latencia e TTFB**: Medicao precisa do tempo de resposta inicial do servidor (Time to First Byte) e eficiencia de borda.
* **Inspecao de Recursos Bloqueantes de Renderizacao**: Identificacao de folhas de estilo e scripts sincronicamente carregados no `<head>` que retardam o First Contentful Paint (FCP).
* **Diagnostico de Estabilidade Visual (CLS)**: Verificacao de dimensoes explicitas (`width`/`height`) e carregamento postergado (`loading="lazy"`) em imagens para evitar mudancas abruptas de layout.
* **Avaliacao de Compressao e Payload**: Deteccao de suporte e ativacao de algoritmos modernos de compressao (Brotli e Gzip).
* **Indice de Performance W3C**: Nota tecnica quantitativa de 0 a 100 com recomendacoes de otimizacao priorizadas.

***

## Instalacao e Execucao

Requer Python 3.8 ou superior sem necessidade de bibliotecas externas adicionais.

```bash
git clone https://github.com/TAVARDT-Brasil/core-web-vitals-tester-br.git
cd core-web-vitals-tester-br
python cwv_tester.py https://empresa.com.br
```

Para gerar a saida em formato estruturado JSON para esteiras de integracao continua:

```bash
python cwv_tester.py https://empresa.com.br -json
```

***

## Diagnostico Completo na Web

Para auditoria aprofundada de velocidade e simulacao de dispositivos:

* **Teste de Core Web Vitals Oficial**
* **[Portal Corporativo TAVARDT](https://ag.tavardt.com/br/)**

***

## Consultoria em Otimizacao de Performance Web

Para aceleracao de carregamento e conformidade com Diretrizes de Experiencia de Pagina Google e W3C, consulte os especialistas da **TAVARDT**.

***

## Links Úteis

* **Portal Corporativo:** https://ag.tavardt.com/br/
* **Suíte de Diagnósticos:** https://tools.tavardt.com/br/
* **Contato Técnico:** https://ag.tavardt.com/br/contato/

***

### Licença
Distribuído sob a Licença MIT. Consulte o arquivo [LICENSE](LICENSE) para obter detalhes completos.

***

© 2026 TAVARDT. Todos os direitos reservados.
