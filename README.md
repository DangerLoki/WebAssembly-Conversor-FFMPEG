# ConverterFFMPEG

Aplicação web para conversão de imagens diretamente no navegador usando **FFmpeg via WebAssembly**, sem envio de arquivos para uma API externa.

## Visão geral

Este projeto foi desenvolvido para demonstrar uma abordagem **client-side** de processamento de arquivos, com foco em privacidade, simplicidade de uso e integração de tecnologia avançada no navegador.

A aplicação permite selecionar uma imagem, visualizar um preview e realizar a conversão localmente, gerando o arquivo final para download.

## Status

**Projeto em desenvolvimento**

A versão atual está focada em **conversão de imagens**. Expansões futuras podem incluir novos formatos, controles de qualidade e suporte a conversão de vídeo.

## Funcionalidades atuais

- Upload de imagem
- Suporte a drag-and-drop
- Preview do arquivo selecionado
- Conversão local no navegador
- Download do arquivo convertido

## Stack

- JavaScript
- HTML
- CSS
- Node.js
- Express
- `@ffmpeg/ffmpeg`

## Decisões técnicas

### Por que WebAssembly
WebAssembly foi utilizado para executar processamento de mídia diretamente no navegador com desempenho superior ao de abordagens puramente interpretadas em JavaScript. Isso permite trazer uma ferramenta tradicionalmente nativa para o ambiente web de forma prática.

### Por que FFmpeg no navegador
FFmpeg foi escolhido por ser uma solução consolidada para processamento e conversão de mídia. Executá-lo no browser permite aproveitar sua robustez sem depender de backend dedicado para conversão.

### Por que processamento client-side
A conversão local evita o envio do arquivo para servidores externos, o que traz vantagens em:

- privacidade dos dados
- redução de dependência de API
- menor custo de infraestrutura
- arquitetura mais simples para testes e demonstração

## Limitações conhecidas

- O carregamento inicial pode ser mais lento devido à inicialização do FFmpeg em WebAssembly
- Conversões mais pesadas dependem diretamente do hardware do usuário
- O navegador impõe limites práticos de memória e processamento
- A versão atual está focada em imagem, não em fluxos mais pesados de vídeo

## Habilidades demonstradas

- Integração de biblioteca complexa no front-end
- Processamento de arquivos no navegador
- Manipulação de upload e preview de arquivos
- Processamento client-side
- Estruturação de interface para fluxo de conversão
- Experiência do usuário com drag-and-drop
- Organização de projeto web com separação entre servidor e front-end
- Aplicação prática de WebAssembly
- Uso de ferramenta de mídia em ambiente web

## Estrutura do projeto

```bash
WebAssembly-Conversor-FFMPEG/
├── public/
├── build/
├── server.js
├── package.json
└── README.md
````

## Como executar

```bash
npm install
node server.js
```

A aplicação ficará disponível localmente em:

```bash
http://localhost:8080
```

## Objetivo no portfólio

Este projeto faz parte do meu portfólio para demonstrar capacidade de construir soluções web que integrem interface, processamento local de arquivos e tecnologias voltadas a performance no navegador.
