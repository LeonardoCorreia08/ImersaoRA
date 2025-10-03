# ImersaoRA
Imersão em Realidade Aumentada — explorando experiências interativas que conectam o mundo físico ao digital.

Segue os projetos :

[Leon](https://leon3dv2.netlify.app/)

[Cloud](https://cloudff7.netlify.app/)

# Realidade Aumentada (RA)

## Índice
- [O que é Realidade Aumentada?](#o-que-é-realidade-aumentada)
- [Contínuo de Realidade-Virtualidade](#contínuo-de-realidade-virtualidade)
- [Requisitos Técnicos da RA](#requisitos-técnicos-da-ra)
- [Tecnologias Fundamentais](#tecnologias-fundamentais)
- [RA vs Realidade Mista](#ra-vs-realidade-mista)
- [Aplicações Práticas](#aplicações-práticas)
- [Glossário Técnico](#glossário-técnico)
- [Referências](#referências)

---

## O que é Realidade Aumentada?

Realidade Aumentada (RA) é uma tecnologia que sobrepõe gráficos bidimensionais ou tridimensionais à cena real em tempo real. Diferentemente da Realidade Virtual, que substitui completamente o ambiente físico, a RA **adiciona** elementos digitais ao mundo real.

### Três Requisitos Essenciais da RA:

1. **Combinação real-virtual**
   - Objetos digitais aparecem integrados ao ambiente físico
   - Exemplo: Um modelo 3D de molécula fixo sobre uma mesa real

2. **Alinhamento espacial preciso (tracking)**
   - O sistema calcula continuamente posição e orientação da câmera
   - Mantém objetos virtuais ancorados no lugar correto
   - Utiliza marcadores visuais (QR codes) ou SLAM

3. **Atualização contínua**
   - Composição reage instantaneamente ao movimento
   - Evita desalinhamento perceptível
   - Taxa de quadros mínima: 60 FPS

---

## Contínuo de Realidade-Virtualidade

Proposto por Milgram e Kishino (1994), o contínuo organiza experiências imersivas em um espectro:

```
[Ambiente Real] → [RA] → [RM] → [VA] → [RV]
     100% Real         Híbrido        100% Virtual
```

### Posições no Espectro:

| Tecnologia | Descrição | Exemplo |
|------------|-----------|---------|
| **Ambiente Real** | Mundo físico puro, sem elementos digitais | Câmeras de segurança |
| **RA** | Sobreposição digital sobre o real | Pokémon GO, filtros Instagram |
| **RM** | RA + física realista (colisões, sombras) | Microsoft HoloLens |
| **VA** | Elementos reais em cenário virtual | Chroma key em estúdios TV |
| **RV** | Ambiente 100% sintético | Meta Quest, PS-VR2 |

---

## Requisitos Técnicos da RA

### Hardware Mínimo:

- **Câmera**: Captura do ambiente real
- **Processador**: CPU moderna (últimos 3-5 anos)
- **GPU**: Para renderização em tempo real
- **Sensores**: Giroscópio, acelerômetro (em móveis)
- **Tela**: Display para composição da imagem

### Desempenho Recomendado:

| Métrica | Mínimo | Recomendado | Ideal |
|---------|---------|-------------|-------|
| **FPS** | 30 | 60 | 90+ |
| **Latência** | <50ms | <20ms | <10ms |
| **Resolução** | 720p | 1080p | 4K |

---

## Tecnologias Fundamentais

### 1. Tracking (Rastreamento)

Estimativa contínua de posição e orientação do dispositivo.

**Tipos:**
- **Marker-based**: Usa padrões visuais reconhecíveis (QR codes, marcador Hiro)
- **Markerless**: SLAM, reconhecimento de superfícies planas
- **6DOF**: Seis graus de liberdade (x, y, z + pitch, yaw, roll)

### 2. SLAM (Simultaneous Localization and Mapping)

Constrói mapa do ambiente enquanto calcula trajetória da câmera.

**Vantagens:**
- Não requer marcadores físicos
- Funciona em ambientes variados
- Permite persistência de objetos virtuais

**Limitações:**
- Exige texturas visíveis no ambiente
- Maior consumo de processamento

### 3. Detecção de Superfícies

Identifica planos horizontais/verticais para ancoragem de objetos.

**Aplicações:**
- Posicionar móveis virtuais no chão
- Fixar quadros em paredes
- Criar experiências de piso interativo

---

## RA vs Realidade Mista

### Realidade Aumentada (RA):
- Sobreposição visual simples
- Sem interação física realista
- Objetos podem "flutuar" ou atravessar superfícies
- Iluminação independente do ambiente

### Realidade Mista (RM):
- Comportamento físico coerente
- Colisões com superfícies reais
- Sombras e iluminação adaptadas
- Oclusão bidirecional (objetos reais ocultam virtuais)

**Exemplo prático:**
- **RA**: Filtro de óculos no Instagram (não interage com luz real)
- **RM**: HoloLens posicionando ferramenta virtual que "para" na bancada

---

## Aplicações Práticas

### Educação
- Visualização de modelos anatômicos 3D
- Experimentos científicos virtuais
- Reconstruções históricas

### Indústria
- Manutenção assistida (sobreposição de instruções)
- Controle de qualidade visual
- Treinamento operacional

### Varejo
- Experimentação virtual de produtos
- Visualização de móveis em casa
- Provadores virtuais

### Entretenimento
- Jogos baseados em localização (Pokémon GO)
- Filtros de redes sociais
- Experiências artísticas interativas

### Saúde
- Visualização de veias para punção
- Planejamento cirúrgico
- Reabilitação física gamificada

---

## Glossário Técnico

### Tracking
Estimativa contínua da posição e orientação da câmera ou headset em relação ao ambiente, mantendo conteúdo virtual ancorado.

### Oclusão
Processo onde objeto virtual fica parcial ou totalmente escondido por objeto real, preservando ordem de profundidade.

### SLAM
**Simultaneous Localization and Mapping** - Método que constrói mapa do ambiente enquanto calcula trajetória da câmera, dispensando marcadores.

### Malha 3D Densa
Modelo detalhado do espaço capturado por sensores de profundidade, permitindo colisões físicas e sombras coerentes.

### Latência
Tempo total (em milissegundos) entre movimento real do usuário e atualização da imagem virtual. Atrasos acima de 20ms comprometem alinhamento.

### Presença
Sensação subjetiva de "estar dentro" do ambiente digital. Depende de campo de visão, taxa de quadros e latência.

### Taxa de Quadros (Frame Rate)
Número de imagens completas exibidas por segundo. Em XR, taxas inferiores a 60 FPS geram tremor.

### Áudio Espacial
Técnica que posiciona sons em coordenadas 3D ao redor do ouvinte, simulando distância e direção.

### GPU
**Unidade de Processamento Gráfico** - Circuito especializado em cálculos paralelos para renderizar imagens 2D e 3D em tempo real.

---

## Referências

AZUMA, R. T. A survey of augmented reality. **Presence: Teleoperators and Virtual Environments**, v. 6, n. 4, p. 355-385, 1997.

DURRANT-WHYTE, H.; BAILEY, T. Simultaneous localization and mapping: part I. **IEEE Robotics & Automation Magazine**, v. 13, n. 2, p. 99-110, 2006.

MILGRAM, P.; KISHINO, F. A taxonomy of mixed reality visual displays. **IEICE Transactions on Information and Systems**, v. 77, n. 12, p. 1321-1329, 1994.

---

## Licença

Este documento é fornecido para fins educacionais.

## Contato

Para dúvidas ou sugestões sobre este material, consulte os canais de suporte do curso.
