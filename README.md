# Teste de Conteúdo — Fluxo de Fechar uma Ocorrência

## 1. Tela(s) analisada(s)

**Fluxo composto por 3 telas:**

1. **Lista de ocorrências** (`/lista-ocorrencias`) — exibe as ocorrências ativas e o histórico de ocorrências encerradas. ![Tela 1 - Listagem Ocorrências](/fluxo1.png)
2. **Detalhamento da ocorrência** (`/lista-ocorrencias/lista-rastreadores`) — exibe os recursos alocados por base, os botões "Pausar"/"Despausar" e "Finalizar ocorrência". ![Tela 2 - Detalhamento Ocorrência](/fluxo2.png)
3. **Tela de confirmação** (`/lista-ocorrencias/lista-rastreadores/finalizada`) — exibe o texto "Ocorrência finalizada com sucesso" e a mensagem "A ocorrência foi encerrada e registrada no histórico.", com as opções "Voltar" e "Menu". ![Tela 3 - Finalização Confirmada](/fluxo3.png)

**Contexto:** O usuário precisa encerrar uma ocorrência de incêndio após a situação ser controlada, registrando-a no histórico do sistema.

## 2. Tipo de teste

**Tipo:** Conteúdo

**O que será testado:** Se os textos, rótulos e mensagens presentes no fluxo de finalização comunicam de forma clara ao usuário o que acontece ao clicar em "Finalizar ocorrência", qual é o estado resultante e quais ações ficam disponíveis após o encerramento.

## 3. Conjunto de perguntas (técnica do funil)

As perguntas seguem a lógica do funil — partindo de percepções amplas e abertas e afunilando para compreensões específicas sobre o conteúdo da interface.

| # | Nível do funil | Tela de origem | Pergunta | Intenção |
|---|---|---|---|---|
| 1 | Abertura (exploratória) | Lista de ocorrências (`/lista-ocorrencias`) | Olhando para esta tela de lista de ocorrências, o que você entende que está sendo mostrado aqui? O que cada seção representa? | Captar a primeira impressão do usuário sobre a organização da tela, sem direcionar para nenhuma ação. Permite avaliar se a divisão em duas listas e os rótulos "Ocorrências ativas" e "Histórico" comunicam claramente a diferença entre ocorrências em andamento e encerradas. |
| 2 | Direcionamento (tarefa orientada) | Lista de ocorrências (`/lista-ocorrencias`) | Seu objetivo agora é encerrar uma ocorrência que já foi controlada. A partir do que você vê nesta tela, como você faria isso? | Observar o caminho mental que o usuário traça a partir do conteúdo visível — se ele identifica que deve selecionar uma ocorrência ativa, se os rótulos e badges de status orientam a navegação, ou se hesita sem saber por onde começar. Revela se o conteúdo da listagem dá pistas suficientes sobre o fluxo de encerramento. |
| 3 | Foco (intermediária-específica) | Detalhamento da ocorrência (`/lista-ocorrencias/lista-rastreadores`) | Agora que você chegou na tela de detalhamento e vê o botão "Finalizar ocorrência", o que você espera que aconteça ao clicar nele? Essa ação pode ser desfeita? | Avaliar se o rótulo "Finalizar ocorrência" comunica a consequência da ação (encerramento definitivo e registro no histórico) ou se gera dúvida — por exemplo, o usuário pode achar que apenas gera um relatório, ou não saber se a ação é reversível. |
| 4 | Específica | Tela de confirmação (`/lista-ocorrencias/lista-rastreadores/finalizada`) | Após o clique, você vê a mensagem "Ocorrência finalizada com sucesso — A ocorrência foi encerrada e registrada no histórico." Essa informação é suficiente? Faltou algo que você gostaria de ver neste momento? | Verificar se o conteúdo da tela de confirmação transmite segurança e completude, ou se o usuário sente falta de informações como data/hora de encerramento, resumo dos recursos mobilizados ou próximos passos. |
| 5 | Fechamento (reflexiva) | Lista de ocorrências (`/lista-ocorrencias`) — seção "Histórico" | Voltando à lista de ocorrências, a ocorrência agora aparece no "Histórico" com o badge "Resolvida". Esse termo faz sentido pra você? Usaria outra palavra? | Testar se a terminologia "Resolvida" é natural para o domínio do usuário. Em contextos de combate a incêndio, termos como "Controlada", "Encerrada" ou "Extinta" podem ser mais familiares e transmitir melhor o estado final. |

## 4. Objetivo do teste

Descobrir se o conteúdo textual do fluxo de encerramento (rótulos de botões, mensagens de confirmação e badges de status) é compreendido sem ambiguidade pelo usuário, ou se a terminologia utilizada gera hesitação ou interpretações incorretas.

## 5. Ação ou entendimento esperado

O usuário deve compreender, apenas pela leitura dos textos da interface, que ao clicar em "Finalizar ocorrência" a ocorrência será permanentemente encerrada e passará a constar no histórico com status "Resolvida", sem necessidade de explicação externa.
