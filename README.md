# HidroSábio — Monitoramento de Consumo Hídrico (ODS 6)

Dashboard web para acompanhar o consumo de água por ambiente (cozinha, banheiro, jardim etc.), ligado à **ODS 6 da ONU — Água Potável e Saneamento**. A ideia é tornar o consumo visível, avisar quando um ambiente passa do limite e incentivar o uso consciente da água.

## Funcionalidades

- **Início & ODS 6** — apresentação da ODS 6, configurações base (como o preço da água), economizômetro e indicadores do valor da água.
- **Dashboard** — gráfico de consumo por ambiente e fila de alertas de consumo excessivo.
- **Sensor IoT & Ambientes** — cadastro de ambientes com limite de consumo diário e um simulador de sensor IoT para registrar leituras.
- **Histórico** — registro consolidado de todas as leituras, com opção de limpar.
- **Relatórios** — gerador de relatório técnico, com cópia do texto ou download do arquivo.

Os dados ficam em memória no navegador (são recarregados com dados de exemplo ao abrir a página). Internamente o projeto usa as classes `Ambiente` e `FilaAlertas` (uma fila FIFO: o alerta mais antigo é resolvido primeiro).

## Tecnologias

- HTML + JavaScript
- Tailwind CSS v4
- Vite (servidor de desenvolvimento e build)
- Ícones [Lucide](https://lucide.dev)

## Como rodar

Pré-requisito: [Node.js](https://nodejs.org) 18 ou superior.

```bash
npm install
npm run dev
```

Acesse `http://localhost:3000`.

Para gerar a versão de produção na pasta `dist/`:

```bash
npm run build
npm run preview
```
