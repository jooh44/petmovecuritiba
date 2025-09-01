# PetMove Curitiba - Landing Page

## 📋 Visão Geral
Landing page para a clínica veterinária **PetMove Curitiba**, focada em atendimento domiciliar e cuidados especializados para pets. O projeto utiliza HTML, CSS e JavaScript com animações em anime.js.

## 🎨 Design e Identidade Visual

### Paleta de Cores
- **Vermelho Principal**: `#dc3545` (CTA buttons, highlights)  
- **Bege/Dourado**: `#f8d5a2` (accents, backgrounds)
- **Branco**: `#ffffff` (backgrounds, cards)
- **Cinza Escuro**: `#333333` (textos principais)
- **Cinza Médio**: `#666666` (textos secundários)

### Tipografia
- **Font Principal**: System fonts (Arial, sans-serif)
- **Hierarquia**: H1, H2, H3 com diferentes pesos e tamanhos responsivos

## 🏗️ Estrutura do Projeto

```
LP2/
├── index.html.html      # Arquivo principal HTML
├── styles.css           # Estilos principais
├── images/
│   ├── iconografia.png  # Referência para badges com duplo círculo
│   └── [outras imagens]
└── README.md           # Este arquivo
```

## 🔧 Funcionalidades Principais

### 1. **Seção Hero**
- Background com gradiente
- Animações SVG com anime.js
- CTA principal "Agende uma Consulta"
- Responsivo para desktop, tablet e mobile

### 2. **Seção Diferenciais Unificada**
- Combina "Nossos Diferenciais" + "Saúde e Longevidade dos Pets"
- **Cards octogonais** com clip-path personalizado
- **Duplo círculo interno** (inspirado na iconografia.png)
- **Background geométrico sutil** com círculos vazados
- Grid responsivo 2x2 (desktop) → 1 coluna (mobile)

### 3. **Seção de Depoimentos**
- **Sistema ticker dual** com animações CSS
- **Primeiro ticker**: scroll para esquerda
- **Segundo ticker**: scroll reverso (direita)
- Cards verticais estilo Aumivet
- Fade gradual nas laterais
- Auto-loop infinito

### 4. **Animações e Interatividade**
- **Anime.js** para SVG animations na hero
- **Intersection Observer** para trigger de animações
- **CSS keyframes** para tickers e hover effects
- **Responsive animations** com diferentes velocidades

## 📱 Responsividade

### Breakpoints
- **Desktop**: > 768px
- **Tablet**: 481px - 768px  
- **Mobile**: ≤ 480px

### Adaptações Mobile
- Header colapse para hambúrguer
- Cards diferenciais empilhados (1 coluna)
- SVGs hero adaptados para mobile viewport
- Ticker velocidade reduzida
- Background geométrico simplificado

## 🎭 Elementos de Design Específicos

### Cards Diferenciais - Formato Octogonal
```css
clip-path: polygon(8px 0, calc(100% - 8px) 0, 100% 8px, 100% calc(100% - 8px), calc(100% - 8px) 100%, 8px 100%, 0 calc(100% - 8px), 0 8px);
```

### Duplo Círculo (Inspirado na Iconografia)
- **Círculo externo**: Border vermelho (#dc3545)
- **Círculo interno**: Background bege (#f8d5a2) com pseudo-elementos
- Efeito criado com `::before` e `::after`

### Background Geométrico Sutil
- Círculos vazados com `radial-gradient`
- Opacidade baixa (0.04-0.08)
- Cores da paleta (vermelho/bege)
- Posicionamento pseudo-aleatório

## 🔄 Sistema de Ticker (Depoimentos)

### Funcionamento
```css
@keyframes testimonials-scroll {
    0% { transform: translateX(0); }
    100% { transform: translateX(-50%); }
}

@keyframes testimonials-scroll-reverse {
    0% { transform: translateX(-50%); }
    100% { transform: translateX(0); }
}
```

### Características
- **Duração**: 60s para loop completo
- **Direções**: Normal + Reversa
- **Fade lateral**: 60px desktop, 40px tablet, 20px mobile
- **Gap entre cards**: 40px
- **Conteúdo duplicado** para loop seamless

## 🚀 Tecnologias Utilizadas

- **HTML5**: Estrutura semântica
- **CSS3**: 
  - Flexbox & Grid
  - Custom Properties (CSS Variables)
  - Clip-path para formas customizadas
  - Keyframes para animações
  - Media queries para responsividade
- **JavaScript ES6+**:
  - Intersection Observer API
  - Anime.js para SVG animations
  - Event listeners responsivos

## 📝 Histórico de Implementação

### Versão Atual (v2.0)
1. ✅ **Badges com duplo círculo** - Inspirado na iconografia.png
2. ✅ **Seção unificada** - Diferenciais + Saúde em uma seção
3. ✅ **Sistema de depoimentos ticker** - Dual direction com fade
4. ✅ **Background geométrico sutil** - Elementos circulares inspirados nas badges
5. ✅ **Responsividade completa** - Desktop, tablet, mobile
6. ✅ **Animações otimizadas** - Performance e acessibilidade

### Removido/Deprecado
- ❌ SVG animations na seção diferenciais (substituído por background CSS)
- ❌ Hover effects nos cards diferenciais
- ❌ Estatísticas numéricas (substituídas por depoimentos)

## 🎯 Objetivos de Conversão

### CTAs Principais
1. **Hero**: "Agende uma Consulta" 
2. **Header**: Botão de contato
3. **Footer**: Informações de contato

### Foco no Usuário
- **Atendimento domiciliar** como diferencial principal
- **Cuidado especializado** para pets
- **Conveniência** e **qualidade** do serviço
- **Depoimentos reais** para credibilidade

## 🔧 Comandos de Desenvolvimento

### Estrutura de Arquivos
```bash
# Visualizar estrutura
tree LP2/

# Servir localmente (opcional)
python -m http.server 8000
```

### CSS Architecture
- **Mobile-first** approach
- **BEM-like** naming convention para classes
- **Custom properties** para cores e espaçamentos
- **Modular CSS** por seções

## 📊 Performance e SEO

### Otimizações
- **CSS minification** ready
- **Image optimization** para backgrounds
- **Lazy loading** preparado para imagens
- **Semantic HTML** para SEO
- **Meta tags** estruturadas

### Acessibilidade
- **Contrast ratios** WCAG compliant
- **Keyboard navigation** ready
- **Screen reader** friendly
- **Reduced motion** queries implementadas

## 🐛 Debug e Troubleshooting

### Problemas Comuns

1. **Cards com bordas cortadas**
   - Verificar `overflow: visible` nos containers
   - Confirmar `clip-path` não está conflitando

2. **Ticker parado ou quebrado**
   - Verificar se conteúdo está duplicado
   - Confirmar animations CSS estão carregando

3. **SVG hero não aparece**
   - Verificar console para erros anime.js
   - Confirmar Intersection Observer está funcionando

4. **Responsividade quebrada**
   - Verificar media queries na ordem correta
   - Confirmar breakpoints consistentes

## 🔮 Próximos Passos Sugeridos

### Melhorias Futuras
- [ ] Implementar lazy loading para imagens
- [ ] Adicionar Google Analytics/Meta Pixel
- [ ] Integração com WhatsApp API
- [ ] Formulário de contato funcional
- [ ] Sistema de agendamento online
- [ ] Blog/artigos sobre cuidados pet

### Performance
- [ ] Critical CSS inline
- [ ] Image optimization automática  
- [ ] Service Worker para cache
- [ ] Bundle size optimization

---

## 📞 Contato e Suporte

**Desenvolvido para**: PetMove Curitiba
**Tecnologias**: HTML5, CSS3, JavaScript ES6+, Anime.js
**Status**: Produção Ready ✅

---

*Última atualização: Janeiro 2025*