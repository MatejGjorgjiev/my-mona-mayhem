<!-- l10n-sync: source-file="workshop/06-bonus.md" -->
# 🎉 Bônus e extensões

---

Você criou um app de batalhas do GitHub totalmente funcional! Agora é hora de avançar com estes **desafios abertos**.

<!-- track:vscode:start -->
Use o **Agent Mode** em todos eles: descreva o que você quer e deixe o Copilot ajudar na criação.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Use o Copilot CLI em todos eles: combine o contexto com `@file`, `/plan`, o modo normal e `/review`, conforme necessário.
<!-- track:cli:end -->

---

## 🏆 Desafio 1: Faixa do vencedor

Depois que os dois gráficos de contribuições forem carregados, compare os totais e anuncie o vencedor.

**O que criar:**
- Compare o total de contribuições dos dois usuários
- Exiba **"🏆 {username} WINS! 🏆"** com um estilo comemorativo se houver um vencedor
- Exiba **"🤝 IT'S A TIE! 🤝"** se as contribuições forem iguais
- Adicione uma animação ou confete para dar mais destaque

**Sugestão de prompt:**
> After both users' contribution data loads, compare total contributions and display a winner banner. Show "🏆 {username} WINS! 🏆" if one user has more contributions, or "🤝 IT'S A TIE! 🤝" if equal. Make it visually exciting with CSS animations.

---

## 🏆 Desafio 2: Contador de sequência

Calcule e exiba a maior sequência consecutiva de contribuições de cada usuário.

**O que criar:**
- Analise os dados de contribuição dia a dia
- Encontre a maior sequência de dias consecutivos com pelo menos uma contribuição
- Destaque a quantidade de dias da sequência de cada usuário
- Destaque quem tem a sequência mais longa

**Sugestão de prompt:**
> Add a streak counter feature that analyzes each user's contribution data to find their longest consecutive contribution streak. Display "🔥 Longest Streak: X days" for each user below their contribution graph.

---

## 🏆 Desafio 3: Histórico de batalhas

Persista os resultados das batalhas para que os usuários possam consultar os confrontos anteriores.

**O que criar:**
- Salve cada resultado em `localStorage` (nomes de usuário, totais, vencedor e data e hora)
- Adicione uma seção **"Recent Battles"** abaixo da área principal da batalha
- Mostre os últimos 5–10 confrontos e seus resultados
- Adicione um botão "Clear History"

**Sugestão de prompt:**
> Save battle results to localStorage after each comparison. Add a "Recent Battles" section that displays the last 10 battles with usernames, contribution totals, the winner, and when the battle happened. Include a "Clear History" button.

---

## 🏆 Desafio 4: Efeitos sonoros

Adicione efeitos sonoros de fliperama retrô usando a Web Audio API, sem arquivos externos.

**O que criar:**
- Som de **moeda inserida** quando o botão "Battle!" for clicado
- Som de **power-up** quando os resultados forem carregados com sucesso
- Som de **explosão** em caso de erro (usuário não encontrado ou falha da API)
- Botão para ativar ou desativar o som

**Sugestão de prompt:**
> Add retro arcade sound effects using the Web Audio API (no audio files). Play a coin insert sound on battle start, a power-up sound when results load, and an explosion sound on errors. Generate the sounds programmatically with oscillators and gain nodes. Include a mute toggle.

---

## 🏆 Desafio 5: Sequência de batalha animada

Crie suspense com uma contagem regressiva dramática antes de revelar os resultados.

**O que criar:**
- Quando "Battle!" for clicado, exiba uma sobreposição em tela cheia
- Anime: **"3..."** → **"2..."** → **"1..."** → **"⚡ FIGHT! ⚡"**
- Em seguida, revele os gráficos de contribuições com uma entrada dramática
- Use animações CSS ou temporização em JavaScript

**Sugestão de prompt:**
> Add an animated battle sequence when the user clicks "Battle!". Show a countdown overlay: "3..." then "2..." then "1..." then "⚡ FIGHT! ⚡" with each step lasting about 1 second. After the countdown, reveal the results with a slide-in animation.

---

## 🏆 Desafio 6: Legenda de contribuições

Adicione uma legenda de escala de cores que corresponda à paleta do gráfico de contribuições.

**O que criar:**
- Uma legenda horizontal com os níveis de intensidade das contribuições
- Rótulos de **"Less"** a **"More"**
- Use a paleta real da resposta da API de contribuições do GitHub
- Posicione-a perto dos gráficos

**Sugestão de prompt:**
> Add a contribution legend below the graphs showing the color scale from the API's color palette. Display a row of colored squares ranging from "Less" (lightest) to "More" (darkest), matching the actual contribution level colors returned by the API.

---

## 🏆 Desafio 7: Compartilhar resultados

Permita que os usuários compartilhem os resultados da batalha com um só clique.

**O que criar:**
- Um botão **"📋 Share Results"** exibido depois de uma batalha
- Copie um resumo formatado em texto para a área de transferência
- Inclua os nomes de usuário, os totais de contribuições e o vencedor
- Mostre brevemente a confirmação "Copied!"

**Sugestão de prompt:**
> Add a "📋 Share Results" button that copies a formatted battle summary to the clipboard. The summary should include both usernames, their contribution totals, and who won. Use the Clipboard API and show a brief "Copied to clipboard!" confirmation.

---

<!-- track:cli:start -->
## 💻 Extras do CLI

Se quiser explorar mais recursos do Copilot CLI depois do workshop principal:

- Use `copilot -p "Write a conventional commit message for the current git diff"` para gerar uma resposta rápida que você pode colar no Git.
- Execute `/share file` para salvar a sessão como Markdown e consultar depois.
- Use `/session` e `/session plan` para verificar como o CLI acompanha seu trabalho atual.
<!-- track:cli:end -->

## 🎊 Parabéns!

Você concluiu o workshop **Mona Mayhem: GitHub Battle**! Veja o que você realizou:

### O que você criou

- ✅ Um **aplicativo web com várias páginas** a partir de uma especificação de design
- ✅ Uma **página inicial** com tema de fliperama retrô e layout responsivo
- ✅ Uma **arena de batalha** que busca e compara dados reais de contribuições do GitHub
- ✅ **Gráficos de contribuições interativos** com níveis de atividade indicados por cores
- ✅ Melhorias no **tratamento de erros, estados de carregamento e acessibilidade**
- ✅ Um **design responsivo** que funciona em diferentes dispositivos

### O que você praticou

| Habilidade | Prática |
|---|---|
| **Engenharia de contexto** | Fornecer ao Copilot os arquivos, as instruções e as restrições adequadas |
| **Planejamento** | Gerar e refinar planos de implementação antes de programar |
| **Codificação agêntica** | Delegar ao Copilot tarefas com várias etapas e arquivos |
| **Iteração de design** | Partir de uma direção visual e refiná-la até chegar a um resultado polido |
| **Disciplina de revisão** | Inspecionar alterações geradas por IA antes de registrá-las |

### 🚀 Continue aprendendo

- 📺 [Canal do VS Code no YouTube](https://www.youtube.com/@code) — Dicas, tutoriais e novidades
- 📖 [Documentação do GitHub Copilot](https://docs.github.com/en/copilot) — Documentação e guias oficiais
- 💻 [Documentação do GitHub Copilot CLI](https://docs.github.com/en/copilot/how-tos/copilot-cli) — Instalação, comandos slash e boas práticas
- 🌟 [Awesome GitHub Copilot](https://github.com/stefanprodan/awesome-github-copilot) — Recursos e exemplos da comunidade
- 🛠️ [Workshops do Copilot Dev Days](https://github.com/github/copilot-dev-days) — Mais workshops práticos

---

## 🙏 Obrigado!

Obrigado por participar deste workshop! Você viu como o GitHub Copilot pode acelerar todas as etapas do desenvolvimento — do planejamento e design à implementação e ao polimento. As técnicas praticadas aqui servem para qualquer projeto, framework ou escala. Agora, crie algo incrível! 🚀
