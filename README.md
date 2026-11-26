<p align="center">
  <a href="https://ag.tavardt.com/br/">
    <img src="https://ag.tavardt.com/img/tavardt-banner.png" alt="TAVARDT" width="1024" />
  </a>
</p>

# Auditor de Core Web Vitals e Velocidade de Pagina

[![Teste Core Web Vitals](https://img.shields.io/badge/TAVARDT-Core%20Web%20Vitals-5b3cf5.svg)](https://tools.tavardt.com/br/teste-core-web-vitals/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Auditoria de latencia TTFB, compressao HTTP, recursos bloqueadores de renderizacao e estabilidade visual CLS.

Desenvolvido e mantido pela divisao de engenharia de performance web e auditoria de infraestrutura da **TAVARDT**.

***

## Vetores de Risco e Impacto Operacional em Web Performance

Tempos de resposta lentos do servidor e recursos bloqueadores de renderizacao prejudicam o posicionamento organico no Google sob os sinais de Page Experience. Quando plataformas apresentam alto TTFB e arquivos descompactados, as taxas de rejeicao disparam no Brasil.

Layouts instaveis desprovidos de dimensoes de imagem explicitas provocam saltos bruscos que degradam gravemente o indice Cumulative Layout Shift. A auditoria continua protege o investimento em midia e assegura taxas superiores de conversao.

***

## Capacidades Centrais de Auditoria Tecnica

* **Medicao de Alta Precisao de TTFB**: Calculo de latencia de resposta inicial via contadores de alta resolucao, alertando para atrasos acima de 600 ms e gargalos criticos superiores a 1200 ms.
* **Inspecao de Compressao HTTP**: Checagem de transmissao de dados sob padroes Brotli ou Gzip, penalizando o envio de dados descompactados em 15 pontos.
* **Deteccao de Recursos Bloqueadores**: Identificacao de folhas de estilo CSS e scripts JS sincronos no `<head>` sem atributos async, defer ou module.
* **Auditoria de Estabilidade Visual (CLS)**: Varredura de tags `<img>` sem atributos explicitos de largura e altura para neutralizar deslocamentos de layout.
* **Identificacao de Resource Hints**: Reconhecimento de diretivas preconnect e preload estrategicas para aceleracao de conexoes prioritarias.
* **Indice de Performance W3C**: Metrica quantitativa de 0 a 100 categorizando a pagina em GOOD (FAST), NEEDS IMPROVEMENT ou POOR (SLOW).

***

## Instalacao e Execucao

Requer Python 3.8 ou superior sem dependencias externas adicionais.

```bash
git clone https://github.com/TAVARDT-Brasil/core-web-vitals-tester-br.git
cd core-web-vitals-tester-br
python cwv_tester.py https://empresa.com.br
```

Para gerar a saida em formato estruturado JSON em esteiras de CI/CD:

```bash
python cwv_tester.py https://empresa.com.br -j
```

***

## Perguntas Frequentes (FAQ Tecnico)

### 1. Qual o impacto de um Time to First Byte (TTFB) elevado na pontuacao de Core Web Vitals?
O TTFB atrasa o inicio do carregamento de todos os recursos subsequentes, comprometendo diretamente as metricas de LCP e FCP. Quando o servidor demora mais de 600 milissegundos para responder, o validador penaliza a pontuacao e alerta para gargalos de cache.

### 2. Como os recursos JavaScript e CSS no head afetam o bloqueio de renderizacao?
Scripts sincronos e folhas de estilo sem atributos assincronos interrompem a construcao da arvore DOM pelo navegador. O auditor contabiliza ativos que nao utilizam async, defer ou type=module, sinalizando a necessidade de postergar codigos nao essenciais.

### 3. Por que imagens sem atributos explicitos de largura e altura agravam o Cumulative Layout Shift?
Sem dimensoes de largura e altura declaradas no HTML, o navegador nao consegue reservar espaco antecipado para a imagem na tela. Isso provoca deslocamentos visuais repentinos durante o carregamento, prejudicando a pontuacao de estabilidade visual e a usabilidade.

### 4. Qual a relevancia da compressao HTTP via Brotli ou Gzip no desempenho de carregamento?
A compactacao de texto via Brotli ou Gzip reduz o tamanho do payload HTML transferido pela rede em ate setenta por cento. A ausencia de compressao ativa consome largura de banda excessiva e gera deducao imediata na avaliacao de velocidade.

### 5. De que maneira o uso de resource hints como preconnect e preload otimiza a entrega do site?
As diretivas preconnect e preload antecipam resolucoes DNS e inicializam downloads de fontes e imagens criticas antes da requisicao natural. O validador identifica esses aceleradores estruturais para certificar que o navegador prioriza os ativos de maior impacto.

***

## Consultoria em Performance Web e Otimizacao de Velocidade

Para estruturacao de arquiteturas de alta velocidade e conformidade com padroes do W3C, consulte a equipe tecnica da **TAVARDT**.

***

## Links Uteis

* **Portal Corporativo:** https://ag.tavardt.com/br/
* **Suite de Diagnosticos:** https://tools.tavardt.com/br/
* **Contato Tecnico:** https://ag.tavardt.com/br/contato/

***

### Licenca
Distribuido sob a Licenca MIT. Consulte o arquivo LICENSE para termos completos.

***

© 2026 TAVARDT. Todos os direitos reservados.
