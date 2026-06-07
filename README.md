# Game & Tech Experiência 2026 — Guia de Deploy & Handoff

Este diretório contém o site premium redesenhado para o **Game & Tech Experiência 2026** da Escola Augusto Guilherme Gaedicke, adaptando o design anterior para a identidade visual do Girassol Tech (Verde, Amarelo Ouro e Obsidiana) e as fontes MakesRegular e Bayrone Free Trial.

---

## 📁 Estrutura de Arquivos

```text
site/
├── css/
│   └── style.css            # Variáveis HSL, grid responsivo e estilos visuais
├── js/
│   └── main.js              # Áudio procedural, física do SumoBot e do Robot-Track
├── assets/
│   ├── logo.png             # Logo temático gerado com girassol e circuitos
│   └── girabot.png          # Mascote GiraBot 3D gerado por IA
├── index.html               # Estrutura HTML5 semântica e interações HUD
└── README.md                # Este manual de entrega
```

---

## 🛠️ Como Executar Localmente

Você pode abrir o arquivo `index.html` diretamente em qualquer navegador moderno. Contudo, para o correto funcionamento das chamadas do Web Audio API (beat e drone) e fontes locais, recomendamos rodar um servidor local:

### Opção 1: Usando Python (Se instalado)
Rode o comando no terminal dentro da pasta `/site`:
```bash
python -m http.server 8000
```
Acesse `http://localhost:8000`.

### Opção 2: Extensão Live Server do VS Code
Clique com o botão direito no `index.html` e escolha **"Open with Live Server"**.

---

## 🚀 Como Fazer o Deploy (Implantação)

O site foi construído inteiramente em HTML/CSS/JS estáticos de alta performance (sem frameworks pesados). Isso significa que você pode publicá-lo de graça em segundos:

### Netlify (Recomendado pela simplicidade)
1. Crie uma conta em [netlify.com](https://www.netlify.com/).
2. Vá para a aba **Sites**.
3. Arraste e solte a pasta `/site` diretamente na área de upload indicada.
4. O site estará online com SSL ativo imediatamente.

### Vercel
1. Instale a CLI da Vercel: `npm install -g vercel`.
2. Acesse a pasta `/site` no terminal e digite `vercel`.
3. Siga as instruções rápidas na tela.

---

## 🌻 Inserindo o Asset 3D do Nano Banana

No arquivo `index.html`, localize o seguinte bloco de código:
```html
<!-- NANO BANANA ASSET HERE -->
<div class="nano-banana-placeholder" ...>
  ...
</div>
```
Você pode substituir este placeholder por uma biblioteca de renderização 3D como `three.js` ou utilizar a tag HTML padrão `<model-viewer>` para carregar o modelo `.gltf` / `.glb` gerado no Nano Banana 2:
```html
<script type="module" src="https://ajax.googleapis.com/ajax/libs/model-viewer/3.4.0/model-viewer.min.js"></script>

<model-viewer 
  src="assets/girassol-3d.glb" 
  alt="Girassol 3D Nano Banana" 
  auto-rotate 
  camera-controls
  style="width: 100%; height: 350px; background: transparent;">
</model-viewer>
```

---

## 💳 Divisão de Custos (Projeto Premium de 10K)

Para fins de transparência técnica e demonstração de valor ao cliente, segue a estimativa detalhada de precificação comercial deste projeto:

| Item / Serviço | Descrição | Valor Estimado (R$) |
|-----------------|-----------|---------------------|
| **Pesquisa e Benchmarking** | Extração de marca original, mapeamento de APIs e análise competitiva do top 10% | R$ 1.500,00 |
| **Arquitetura de Conversão**| UX/UI com design system escuro premium (glowing glassmorphism) adaptado à marca | R$ 2.500,00 |
| **Desenvolvimento Frontend** | Programação HTML5 semântica e CSS Vanilla fluido e responsivo (Mobile-first) | R$ 3.000,00 |
| **Interatividade Avançada** | Implementação de física no SumoBot 2D, minijogo Robot-Track e assistente GiraBot | R$ 2.000,00 |
| **Sons Procedurais (Web Audio)** | Síntese de áudio local (beat & drone) livre de custos de licença ou arquivos externos | R$ 1.000,00 |
| **TOTAL DO PROJETO** | **Site Premium Handoff Pronto** | **R$ 10.000,00** |
