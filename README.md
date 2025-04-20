# TreinoTracker

O TreinoTracker é uma aplicação HTML de página única desenvolvida para ajudar você a acompanhar seu plano de treino semanal. Com uma interface simples e organizada, permite gerenciar exercícios, registrar séries, monitorar a duração do treino e consultar um glossário de termos técnicos de musculação. Ideal para quem segue uma rotina estruturada de força e cardio na academia.

## Funcionalidades

- **Plano de Treino Semanal**: Treinos organizados de segunda a domingo, incluindo musculação (ex.: Pernas, Peito, Costas) e cardio (ex.: Corrida, Futebol, HIIT).
- **Iniciar Treino**: Botão “Iniciar Treino” aparece após selecionar um dia, carregando os exercícios e iniciando o temporizador.
- **Acompanhamento de Exercícios**: Registre séries com botões de incrementar/diminuir e marque como concluído com checkboxes.
- **Finalizar Treino**: Botão “Finalizar Treino” só aparece quando todos os exercícios estão marcados como concluídos.
- **Temporizador de Treino**: Monitora a duração total da sessão, iniciada ao clicar em “Iniciar Treino”.
- **Temporizador HIIT**: Temporizador para o treino intervalado de alta intensidade (HIIT) de sexta-feira (30s corrida/30s caminhada, 10–12 ciclos).
- **Salvamento do Último Treino**: Salva o último treino concluído (dia, data, duração e exercícios) usando `localStorage`.
- **Glossário de Termos Técnicos**: Explica termos como “excêntrico”, “concêntrico” e “FCmáx” para iniciantes.
- **Modo Escuro**: Alterne entre temas claro e escuro com um botão, com preferências salvas no `localStorage` e suporte à configuração do sistema (`prefers-color-scheme`).
- **Design Responsivo**: Interface limpa e adaptável para dispositivos móveis, estilizada com Tailwind CSS.
- **Pesquisa Fácil de Exercícios**: Nomes dos exercícios são destacados e fáceis de copiar para buscar tutoriais ou vídeos online.

## Instalação

### Pré-requisitos

- Um navegador moderno (ex.: Chrome, Firefox, Safari).
- Opcional: Um servidor local (ex.: `http.server` do Python) para testar a funcionalidade de `localStorage`.

### Passos

1. **Clonar o Repositório**:

   ```bash
   git clone https://github.com/dbelarmino/treino-tracker.git
   cd treino-tracker
   ```

2. **Abrir o Aplicativo**:

   - Abra o arquivo `index.html` diretamente no navegador (ex.: clique duplo ou arraste para o Chrome).
   - Alternativamente, hospede localmente para evitar restrições de `localStorage`:
     ```bash
     python3 -m http.server 8000
     ```
     Acesse `http://localhost:8000` no navegador.

## Uso

1. **Alternar Modo Escuro**:

   - Clique no botão com ícone de sol/lua no canto superior direito para alternar entre os modos claro e escuro.
   - A preferência é salva automaticamente e respeita a configuração do sistema.

2. **Selecionar e Iniciar um Treino**:

   - Escolha um dia de treino no menu suspenso (ex.: “Segunda: Pernas + Abdômen”).
   - Clique no botão “Iniciar Treino” para carregar os exercícios e iniciar o temporizador.

3. **Acompanhar Exercícios**:

   - Para cada exercício (ex.: “Agachamento Livre”):
     - Incremente/diminua o contador de séries com os botões `+`/`-`.
     - Ao completar todas as séries (ex.: 4/4), o checkbox “Concluído” é habilitado (borda verde).
     - Marque “Concluído” para indicar que terminou (adiciona um risco no cartão).
   - Copie o nome do exercício (ex.: “Supino Reto”) selecionando o texto e colando em uma pesquisa na web (ex.: Google ou YouTube) para encontrar tutoriais.

4. **Usar o Temporizador HIIT** (Sexta-feira):

   - No exercício “HIIT”, clique em “Iniciar HIIT” para começar os ciclos de 30s corrida/30s caminhada.
   - Pause ou feche o modal conforme necessário.
   - Após concluir o HIIT, a série é marcada automaticamente como concluída.

5. **Finalizar o Treino**:

   - O botão “Finalizar Treino” aparece apenas quando todos os exercícios estão marcados como concluídos.
   - Clique para salvar os detalhes (dia, data, duração, exercícios concluídos) no `localStorage`.
   - Veja o último treino na seção “Último Treino”.

6. **Consultar o Glossário**:
   - Role até a seção “Glossário de Termos Técnicos” para entender termos como “FCmáx” ou “déficit leve”.

## Tecnologias

- **HTML5**: Estrutura da aplicação de página única.
- **JavaScript**: Lógica para acompanhamento de treinos, temporizadores, `localStorage` e modo escuro.
- **Tailwind CSS**: Estilização responsiva com suporte a modo escuro via CDN (`https://cdn.tailwindcss.com`).

## Estrutura do Repositório

```
treino-tracker/
├── index.html          # Página principal do aplicativo
└── screenshots/        # (Opcional) Capturas de tela para o README
```

## Contribuição

Contribuições são bem-vindas! Para contribuir:

1. Faça um fork do repositório.
2. Crie uma branch para sua funcionalidade (`git checkout -b feature/nova-funcionalidade`).
3. Commit suas alterações (`git commit -m "Adiciona nova-funcionalidade"`).
4. Envie para a branch (`git push origin feature/nova-funcionalidade`).
5. Abra um Pull Request.

Certifique-se de que seu código segue o estilo existente e inclui testes, se aplicável.

## Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo [LICENSE](LICENSE) para detalhes.

## Contato

Para dúvidas ou sugestões, entre em contato com o mantenedor:

- GitHub: [@dbelarmino](https://github.com/dbelarmino)
- Email: douglas.belarr@gmail.com

Bons treinos com o TreinoTracker! 💪
