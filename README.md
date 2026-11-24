# Oráculo Semanal

Aplicação web estática de tarô em arquivo único (`index.html`) onde o usuário acessa toda semana e sorteia aleatoriamente uma carta dentre as 78 cartas do baralho tradicional (22 Arcanos Maiores e 56 Arcanos Menores).

As ilustrações de referência e os significados das cartas nas posições normal e invertida são baseados no guia [Ezra Card — Lista de significados das cartas de tarô](https://ezracard.com/pt/tarot-card-meanings-list/).

## Funcionalidades

- **Sorteio semanal com trava por ciclo:** libera 1 carta aleatória por semana (de segunda a domingo, seguindo a semana ISO) e salva o resultado localmente no navegador até a virada da próxima segunda-feira às 00:00, com contagem regressiva em tempo real.
- **Leitura normal e invertida:** opção para incluir ou não cartas invertidas no sorteio. Todas as cartas são exibidas inicialmente na posição direita para facilitar a leitura da ilustração, com selo indicando **Posição Invertida** e botão opcional para girar a arte em 180°.
- **Baralho completo ilustrado (78 cartas):** aba dedicada com busca por nome ou palavra-chave, filtros por grupo (Arcanos Maiores, Paus, Copas, Espadas e Pentáculos) e modal detalhado com ambos os significados e contexto do naipe.
- **Diário e histórico semanal:** campo de anotação pessoal salvo automaticamente para a semana vigente e aba de histórico com todas as leituras registradas.
- **Modo de simulação e cópia rápida:** botão **Testar sorteio** para simular novas cartas sem sobrescrever a carta oficial da semana, além de botão para copiar a leitura para a área de transferência.
- **Dark mode e Light mode:** tema escuro minimalista ativo por padrão, com alternador no cabeçalho para modo claro e persistência da preferência em `localStorage`.

## Tecnologias

- HTML5, CSS3 e JavaScript (arquivo único, sem etapa de build)
- [Tailwind CSS](https://www.google.com/search?q=https%3A%2F%2Ftailwindcss.com%2F) via CDN (`3.4.17`)
- [Lucide Icons](https://www.google.com/search?q=https%3A%2F%2Flucide.dev%2F) via CDN (`0.460.0`)
- Armazenamento local via `localStorage`

## Estrutura do Projeto

```text
oraculo_semanal_v1/
├── index.html   # Aplicação completa (HTML, estilos, lógica e base das 78 cartas)
└── README.md    # Documentação do projeto
```

## Como Executar Localmente

1. Clone o repositório:
   ```bash
   git clone https://github.com/RobsonLost/oraculo_semanal_v1.git
   cd oraculo_semanal_v1
   ```
2. Abra o arquivo `index.html` diretamente no navegador ou utilize a extensão **Live Server** no VS Code.

## Deploy e Atualização na Vercel

O projeto é estático e não exige comando de build nem variáveis de ambiente.

1. Conecte o repositório `RobsonLost/oraculo_semanal_v1` na [Vercel](https://www.google.com/search?q=https%3A%2F%2Fvercel.com%2F) mantendo o diretório raiz padrão.
2. Sempre que alterar o projeto localmente, envie a atualização para disparar o deploy automático:
   ```bash
   git add .
   git commit -m "Descreva sua atualizacao"
   git push origin main
   ```

## Créditos e Referência

- Cartas e significados: [Ezra Card — Lista rápida com os significados das 78 cartas de tarô](https://ezracard.com/pt/tarot-card-meanings-list/)
