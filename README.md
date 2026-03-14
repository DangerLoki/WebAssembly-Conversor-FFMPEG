# ConverterFFMPEG

Aplicação web para conversão de mídia diretamente no navegador, utilizando **FFmpeg via WebAssembly** e processamento **client-side**, sem dependência de upload para uma API externa.

## Demo

Acesse a aplicação publicada:

[converterffmpeg-static.onrender.com](https://converterffmpeg-static.onrender.com/#)

## Visão geral

Este projeto foi desenvolvido para demonstrar processamento de arquivos no navegador com foco em privacidade, experiência do usuário e integração de tecnologias avançadas no front-end.

A aplicação permite converter **imagens e vídeos** localmente no browser, sem envio dos arquivos para um servidor de processamento.

## Status

**Projeto em desenvolvimento**

A aplicação já possui uma versão funcional publicada. Atualmente, a conversão de imagens apresenta melhor desempenho, enquanto a conversão de vídeos funciona, mas ainda possui limitações de velocidade por depender da execução do FFmpeg em WebAssembly no navegador.

## Funcionalidades atuais

- Conversão de imagens no navegador
- Conversão de vídeos no navegador
- Upload de arquivos
- Suporte a drag-and-drop
- Conversão local com FFmpeg WebAssembly
- Seleção de formatos de saída
- Download do arquivo convertido

## Stack

- JavaScript
- HTML
- CSS
- Node.js
- Express
- `@ffmpeg/ffmpeg`
- WebAssembly

## Decisões técnicas

### Por que WebAssembly
WebAssembly foi utilizado para permitir a execução de processamento de mídia diretamente no navegador com desempenho superior ao de soluções puramente em JavaScript.

### Por que FFmpeg no browser
FFmpeg foi escolhido por ser uma ferramenta consolidada para conversão de mídia. Sua execução no navegador permite reaproveitar uma solução robusta sem depender de backend dedicado para processar arquivos.

### Por que processamento client-side
A conversão local foi adotada para evitar envio de arquivos a servidores externos, o que traz vantagens como:

- maior privacidade
- menor dependência de infraestrutura
- redução de custo de backend
- arquitetura mais simples para demonstração e uso local

## Trade-offs e limitações

A principal limitação atual está na **conversão de vídeos**.

Embora funcional, esse processo pode ser mais lento porque:

- o FFmpeg roda no navegador via WebAssembly
- processamento de vídeo exige muito mais CPU e memória que conversão de imagem
- o desempenho depende diretamente do hardware do usuário
- o ambiente do navegador possui limitações práticas em comparação com execução nativa

Ou seja, a solução privilegia **execução local e privacidade**, mas com custo de desempenho em operações mais pesadas.

## Habilidades demonstradas

- Integração de biblioteca complexa no front-end
- Processamento de arquivos no navegador
- Conversão de mídia client-side
- Manipulação de upload e preview de arquivos
- Aplicação prática de WebAssembly
- Integração de FFmpeg em aplicação web
- Tratamento de fluxo de conversão no front-end
- Experiência do usuário com drag-and-drop
- Estruturação de solução web com foco em performance e privacidade
- Avaliação de trade-offs entre arquitetura local e processamento pesado

## Como executar localmente

```bash
npm install
node server.js

A aplicação ficará disponível localmente em:

```bash
http://localhost:8080
```

## Objetivo no portfólio

Este projeto faz parte do meu portfólio para demonstrar capacidade de construir soluções web que integrem interface, processamento local de arquivos e tecnologias voltadas a performance no navegador.
