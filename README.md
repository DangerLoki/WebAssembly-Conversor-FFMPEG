````md
# ConverterFFMPEG

Uma ferramenta web simples para **converter imagens no navegador** usando **FFmpeg (WebAssembly)** — sem depender de API externa.

> ✅ Conversão client-side (privacidade: o arquivo não precisa sair da sua máquina)  
> ✅ Interface básica com upload/drag-and-drop e preview  
> ✅ Gera arquivo convertido para download

---

## O que este projeto faz

- Permite enviar uma imagem (upload ou arrastar/soltar)
- Mostra um preview do arquivo selecionado
- Converte a imagem para um formato de saída (ex.: JPG) usando FFmpeg rodando no browser
- Faz o download do arquivo convertido

> **Obs.:** apesar do nome “ConverterFFMPEG”, a versão atual está focada em **conversão de imagem**. (Vídeo ainda é um passo futuro.)

---

## Stack

- **Node.js + Express** (servidor simples para servir os arquivos)
- **HTML/CSS/JavaScript** (front-end)
- **@ffmpeg/ffmpeg** (FFmpeg via WebAssembly no navegador)

---

## Como rodar localmente

### Pré-requisitos
- **Node.js** instalado (versão LTS recomendada)

### Instalação
```bash
npm install
````

### Executar

```bash
node server.js
```

Acesse no navegador:

* `http://localhost:8080`

---

## Como usar

1. Abra a página no navegador
2. Arraste uma imagem para a área de drop **ou** selecione via botão de upload
3. Clique para converter (quando disponível no fluxo da página)
4. Baixe o arquivo convertido

---

## Estrutura do projeto

* `server.js` — servidor Express (static hosting)
* `public/` — arquivos do front-end

  * `public/index.html` — página principal
  * `public/style.css` — estilos
  * `public/js/` — scripts (upload, preview, conversão)
* `build/` — artefatos/bundle (se aplicável)

---

## Pontos a melhorar (roadmap)

* [ ] Ajustar input para respeitar a extensão real do arquivo (PNG/JPG/WebP etc.)
* [ ] Melhorar UX: loader/progresso durante `ffmpeg.load()` e `ffmpeg.run()`
* [ ] Permitir escolher formato de saída (JPG/PNG/WebP)
* [ ] Permitir configurar qualidade/resolução
* [ ] (Futuro) Conversão de vídeo/áudio e presets

---

## Limitações conhecidas

* A primeira execução pode ser mais lenta por causa do carregamento do FFmpeg (WASM)
* Conversões pesadas podem variar conforme o hardware do usuário (CPU/RAM)
