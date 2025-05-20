# LAMAFIA - Aplicativo de Gerenciamento de Clã

Este repositório contém o código-fonte do aplicativo LAMAFIA, desenvolvido para gerenciamento de clãs de jogos com interface inspirada no Discord.

## Estrutura do Projeto

O projeto está organizado da seguinte forma:

- `/lib`: Código-fonte principal do aplicativo Flutter
  - `/models`: Modelos de dados (usuário, missões, questionários)
  - `/screens`: Telas do aplicativo
  - `/services`: Serviços de integração com Firebase
  - `/providers`: Gerenciadores de estado
- `/assets`: Recursos como imagens e fontes
- `/documentation.md`: Documentação completa do aplicativo

## Requisitos para Desenvolvimento

- Flutter SDK 3.0.0 ou superior
- Dart 3.0.0 ou superior
- Firebase CLI
- Android Studio ou VS Code com extensões Flutter/Dart

## Como Compilar o APK

Para gerar um APK funcional a partir deste código-fonte:

1. Configure o Firebase:
   ```
   firebase init
   ```

2. Atualize o arquivo `google-services.json` com suas credenciais

3. Execute o comando de build:
   ```
   flutter build apk --release
   ```

4. O APK será gerado em `build/app/outputs/flutter-apk/app-release.apk`

## Funcionalidades Implementadas

- Sistema de autenticação e perfis
- Dashboard principal
- Sistema de ponto (entrada/saída)
- Mural de missões
- Sistema de questionários
- Chat interno
- Gestão de cargos
- Visualização organizacional

## Próximos Passos

Para transformar este projeto em um aplicativo totalmente funcional:

1. Configure um projeto Firebase real
2. Implemente a lógica de backend para autenticação e armazenamento
3. Teste em dispositivos reais
4. Distribua o APK assinado para os membros do clã

## Licença

Este código é fornecido para uso exclusivo do solicitante e não deve ser redistribuído sem autorização.

© 2025 LAMAFIA. Todos os direitos reservados.
