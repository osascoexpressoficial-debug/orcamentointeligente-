# Osasco Express App 🛵

Sistema de gestão logística para restaurantes — Dashboard, Orçamento IA e Proposta Comercial.

## Arquivos do projeto

```
osasco-express-app/
├── src/
│   ├── index.html          ← Shell do app (navegação entre telas)
│   ├── dashboard.html      ← Dashboard Fratelli (dados reais Jan-Fev/2026)
│   ├── oe_orcamento.html   ← Sistema de orçamento inteligente
│   └── proposta_oe.html    ← Proposta comercial visual
├── public/
│   ├── manifest.json       ← Config PWA (ícone, nome, cores)
│   ├── sw.js               ← Service Worker (cache offline)
│   └── icons/              ← Ícones do app (gerar abaixo)
├── package.json
└── capacitor.config.json
```

---

## 🌐 Opção 1 — Testar no celular agora (sem instalar nada)

Suba para o **GitHub Pages** e abra no celular:

1. Crie um repositório no GitHub
2. Suba todos os arquivos
3. Vá em `Settings → Pages → Deploy from branch → main`
4. Acesse `https://SEU-USUARIO.github.io/osasco-express-app/src/`
5. No iPhone/Android: menu do browser → **"Adicionar à Tela de Início"**

Já funciona como app com ícone na tela inicial!

---

## 📱 Opção 2 — App nativo iOS e Android (publicar na App Store / Play Store)

### Pré-requisitos
- Node.js 18+ instalado
- Para iOS: Mac com Xcode instalado
- Para Android: Android Studio instalado

### Passo a passo

```bash
# 1. Instalar dependências
npm install

# 2. Inicializar Capacitor
npm run cap:init

# 3. Adicionar plataformas
npm run cap:add:ios       # só no Mac
npm run cap:add:android

# 4. Sincronizar arquivos
npm run cap:sync

# 5. Abrir no IDE nativo
npm run cap:open:ios      # abre Xcode
npm run cap:open:android  # abre Android Studio

# 6. No Xcode/Android Studio: rodar no simulador ou dispositivo real
```

### Gerar ícones do app

Crie uma imagem 1024×1024px com o logo e use o site:
👉 **https://www.appicon.co** — gera todos os tamanhos automaticamente

Coloque os arquivos em `public/icons/`:
- `icon-192.png` (192×192)
- `icon-512.png` (512×512)

---

## 🏗️ Estrutura técnica

| Tecnologia | Uso |
|---|---|
| HTML/CSS/JS puro | Todas as telas do app |
| Capacitor 5 | Wrapper nativo iOS e Android |
| PWA (manifest + SW) | Instalação via browser sem app store |
| SheetJS | Leitura de planilhas .xlsx localmente |
| Chart.js | Gráficos no dashboard e proposta |

---

## 📋 Telas do app

### 1. Dashboard Fratelli
Análise completa de Jan-Fev/2026: 1.865 pedidos, cancelamentos, recompras, horários de pico, proposta OE integrada.

### 2. Orçamento IA
Atendimento de qualquer restaurante: formulário + upload de planilhas iFood/99Food → análise local com SheetJS → diagnóstico + entregadores + proposta.

### 3. Proposta OE
Proposta comercial visual com dashboard de dados reais, ROI calculado, tabela de preços e contrato digital.

---

## 📞 Contato
- contato@osascoexpress.com.br
- (11) 98666-1784
- Av. Diogo Antônio Feijó, 855 – KM18, Osasco/SP
