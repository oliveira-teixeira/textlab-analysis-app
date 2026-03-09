# TextLab - App para Análise Textual Gratuito

<p align="center">
  <img src="https://img.shields.io/badge/React-18.2-61DAFB?style=flat-square&logo=react" alt="React">
  <img src="https://img.shields.io/badge/Tailwind-3.4-38B2AC?style=flat-square&logo=tailwind-css" alt="Tailwind">
  <img src="https://img.shields.io/badge/License-MIT-green.svg?style=flat-square" alt="MIT License">
  <img src="https://img.shields.io/badge/PT--BR-English-blue?style=flat-square" alt="Languages">
</p>

Ferramenta gratuita e open-source para análise textual em português e inglês, inspirada no IRaMuTeQ. Desenvolvida por **Lucas Oliveira Teixeira** (UFABC) com auxílio de Claude (Anthropic).

## ✨ Funcionalidades

### 📥 Importação Multi-formato
- **PDF** (via pdf.js)
- **Word** (.docx via mammoth.js, .doc via extração ASCII)
- **Excel** (.xlsx, .xls via SheetJS)
- **Rich Text** (.rtf)
- **HTML, JSON, XML, TXT, MD, CSV, TSV, LOG**

### 📊 Análises Disponíveis

| Análise | Descrição |
|---------|-----------|
| **Estatísticas** | Contadores, top 30 palavras, distribuição de frequências |
| **Nuvem de Palavras** | WordCloud SVG interativo com clique para análise de incidências |
| **Rede de Similitude** | Grafo de coocorrência SVG (100 conexões mais fortes) |
| **CHD/Reinert** | Classificação hierárquica descendente em 5 classes |
| **KWIC** | Keyword in Context - concordância textual |
| **Codificação Qualitativa** | Livro de códigos com 10 categorias e ~40 códigos |

### 🧹 Opções de Limpeza
- Remoção de números e pontuação
- Conversão para minúsculas
- Remoção de stopwords (PT: ~750, EN: ~100)
- **Agrupamento morfológico** (gênero, plural, typos via Levenshtein)
- Tamanho mínimo de palavra configurável

### 📤 Exportações
- **IRaMuTeQ** (.txt) - Corpus formatado
- **Frequências** (.tsv)
- **Coocorrências** (.tsv)
- **Análise Completa** (.json)
- **Incidências por Palavra** (.csv)
- **Relatório Científico** (.md) com metodologia e código Python
- **Codificação Qualitativa** (.csv e .json)

## 🚀 Quick Start

### Uso no Claude.ai (Recomendado)
1. Copie o conteúdo de `src/App.jsx`
2. Cole em um novo chat no [claude.ai](https://claude.ai)
3. O preview será renderizado automaticamente

### Desenvolvimento Local
```bash
# Clone o repositório
git clone https://github.com/SEU_USUARIO/textlab-analysis-app.git
cd textlab-analysis-app

# Instale as dependências
npm install

# Inicie o servidor de desenvolvimento
npm run dev
```

## 📁 Estrutura do Projeto

```
textlab-analysis-app/
├── src/
│   └── App.jsx          # Componente principal (single-file)
├── package.json
├── README.md
├── LICENSE
├── vite.config.js
├── tailwind.config.js
├── postcss.config.js
└── index.html
```

## 🎨 Stack Tecnológica

- **React 18** (hooks: useState, useCallback, useMemo, useEffect)
- **Tailwind CSS** (dark theme)
- **Lucide React** (ícones)
- **Lodash** (utilitários)
- **SVG puro** (visualizações)

### Bibliotecas Carregadas Dinamicamente (via CDN)
- **pdf.js v2.16.105** - Extração de PDF
- **mammoth.js v1.6.0** - Extração de DOCX
- **SheetJS v0.18.5** - Extração de Excel

## 🔬 Algoritmos Implementados

### Nuvem de Palavras
- Espiral de Arquimedes com detecção de colisão
- Escala logarítmica para tamanhos
- 15% das palavras rotacionadas (-90°)
- Gradiente de cores por frequência

### Agrupamento Morfológico
```javascript
// Normalização portuguesa
normalizePortugueseWord(word)
// Detecção de typos via Levenshtein
levenshteinDistance(str1, str2)
// Agrupamento de variações
areWordVariations(word1, word2, maxTypoDistance = 1)
```

### CHD/Reinert Simplificado
- 5 classes temáticas
- Chi² calculado para cada termo
- Segmentação automática do corpus

## 🤝 Contribuições

Contribuições são bem-vindas! Por favor:

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/nova-feature`)
3. Commit suas mudanças (`git commit -m 'Adiciona nova feature'`)
4. Push para a branch (`git push origin feature/nova-feature`)
5. Abra um Pull Request

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 🙏 Créditos

- **Lucas Oliveira Teixeira** - Desenvolvimento e conceito
- **Claude (Anthropic)** - Assistência no desenvolvimento
- **UFABC** - Universidade Federal do ABC

---

<p align="center">
  Desenvolvido com ❤️ para a comunidade de pesquisa qualitativa
</p>
