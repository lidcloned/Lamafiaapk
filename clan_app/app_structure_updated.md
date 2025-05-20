# Estrutura Atualizada do Aplicativo de Gerenciamento de Clã

## Visão Geral
Este documento detalha a estrutura e funcionalidades do aplicativo de gerenciamento de clã desenvolvido em Flutter, com interface inspirada no Discord, mas personalizada para as necessidades específicas do clã.

## Sistema de Hierarquia e Permissões

### Níveis de Acesso
- **Dono Principal**: Acesso total a todas as funcionalidades e configurações
- **Administradores/Co-donos**: Pessoas designadas pelo dono com permissões avançadas
- **Membros Regulares**: Acesso limitado às funcionalidades básicas

### Permissões por Nível
1. **Dono Principal**:
   - Gerenciar administradores (adicionar/remover)
   - Configurar todos os aspectos do aplicativo
   - Acesso a todas as funcionalidades administrativas
   - Validação final de missões
   - Visualização de todas as estatísticas e relatórios

2. **Administradores/Co-donos**:
   - Gerenciar membros regulares
   - Criar e editar questionários
   - Moderar o chat
   - Criar e validar missões
   - Acesso a relatórios e estatísticas

3. **Membros Regulares**:
   - Login e gerenciamento do próprio perfil
   - Registro de ponto (entrada/saída)
   - Preenchimento de formulários
   - Sugestão de missões (sem poder de validação)
   - Participação no chat
   - Visualização de estatísticas pessoais

## Módulos Principais

### 1. Autenticação e Perfil
- **Registro de Usuário**: Formulário para novos membros com validação
- **Login**: Sistema seguro de autenticação
- **Perfil do Usuário**: 
  - Nome no jogo
  - Número do WhatsApp
  - Nível atual
  - Horas de jogo
  - Cargo atual
  - Foto de perfil (opcional)
  - Histórico de atividades

### 2. Sistema de Ponto
- **Registro de Entrada**: Marcação de início de sessão de jogo
- **Registro de Saída**: Marcação de fim de sessão de jogo
- **Painel de Status**: Lista em tempo real de membros online/offline
- **Histórico de Pontos**: Registro de todas as sessões anteriores
- **Estatísticas de Tempo**: Cálculo de horas jogadas por dia/semana/mês

### 3. Questionários e Formulários
- **Questionário para Novatos**: Perguntas introdutórias para novos membros
- **Formulários Diários**: Check-in diário para membros ativos
- **Criação de Formulários**: Interface para administradores criarem novos questionários
- **Histórico de Respostas**: Armazenamento e visualização de respostas anteriores

### 4. Sistema de Missões
- **Criação de Missões**: Interface para qualquer membro criar sugestões de missões
- **Validação de Missões**: Painel exclusivo para dono/administradores aprovarem missões
- **Mural de Missões**: Exibição de missões ativas por setor/cargo
- **Progresso de Missões**: Acompanhamento de status e conclusão
- **Recompensas**: Sistema para atribuir benefícios por missões concluídas

### 5. Chat Interno
- **Canais de Chat**: Divisão por tópicos/setores
- **Mensagens Diretas**: Comunicação privada entre membros
- **Compartilhamento de Mídia**: Envio de imagens/vídeos
- **Histórico de Conversas**: Armazenamento de mensagens anteriores
- **Menções**: Sistema para marcar membros específicos

### 6. Notificações
- **Alertas de Missões**: Notificações sobre novas missões ou atualizações
- **Lembretes de Ponto**: Alertas para registrar entrada/saída
- **Mensagens Importantes**: Comunicados da administração
- **Configurações de Notificação**: Personalização por tipo de alerta

### 7. Estatísticas e Relatórios
- **Dashboard Individual**: Estatísticas pessoais de cada membro
- **Visão Geral do Clã**: Métricas coletivas de desempenho
- **Relatórios Periódicos**: Geração de resumos semanais/mensais
- **Gráficos de Progresso**: Visualização de evolução ao longo do tempo

### 8. Administração
- **Gestão de Cargos**: Criação e atribuição de funções
- **Gestão de Permissões**: Promoção/rebaixamento de membros
- **Moderação de Conteúdo**: Controle de mensagens e missões
- **Configurações do App**: Personalização de aparência e funcionalidades
- **Backup de Dados**: Exportação e importação de informações

## Arquitetura Técnica

### Frontend (Flutter)
- **Widgets Personalizados**: Componentes reutilizáveis com estilo Discord
- **Gerenciamento de Estado**: Provider para controle de estado da aplicação
- **Navegação**: Sistema de rotas para transição entre telas
- **Temas**: Modo claro/escuro e personalização de cores

### Backend (Firebase)
- **Authentication**: Sistema seguro de autenticação de usuários
- **Firestore**: Banco de dados NoSQL para armazenamento de dados
- **Storage**: Armazenamento de mídias (fotos, vídeos)
- **Cloud Functions**: Lógica de servidor para validações e processamentos
- **Cloud Messaging**: Sistema de notificações push

### Integração
- **API REST**: Endpoints para comunicação com serviços externos
- **WebSockets**: Comunicação em tempo real para chat e atualizações
- **Offline Mode**: Funcionalidade básica sem conexão com internet

## Fluxos de Usuário

### Fluxo de Registro e Onboarding
1. Download e instalação do APK
2. Tela de boas-vindas
3. Registro com informações básicas
4. Questionário inicial para novatos
5. Tutorial de funcionalidades principais
6. Acesso ao dashboard principal

### Fluxo de Ponto Diário
1. Login no aplicativo
2. Registro de entrada no jogo
3. Notificação periódica durante sessão
4. Registro de saída do jogo
5. Visualização de estatísticas da sessão

### Fluxo de Missões
1. Visualização do mural de missões
2. Seleção de missão compatível com cargo
3. Aceitação e início da missão
4. Atualização de progresso
5. Submissão para validação
6. Recebimento de recompensa após aprovação

### Fluxo de Administração
1. Login como dono ou administrador
2. Acesso ao painel administrativo
3. Gerenciamento de membros e permissões
4. Validação de missões pendentes
5. Criação/edição de questionários
6. Visualização de relatórios e estatísticas

## Considerações de Design
- Interface inspirada no Discord, com adaptações para necessidades específicas do clã
- Esquema de cores personalizável
- Design responsivo para diferentes tamanhos de tela
- Acessibilidade para diferentes necessidades
- Otimização de performance para dispositivos de entrada

## Plano de Expansão Futura
- Integração com API do jogo (se disponível)
- Sistema de ranqueamento e competições internas
- Eventos programados com calendário
- Módulo de recrutamento com formulários específicos
- Integração com plataformas de streaming
