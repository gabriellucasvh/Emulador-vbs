# Iniciando o Emulador do Android Studio Sem Janela de Terminal
## Objetivo
Este documento orienta o usuário sobre como iniciar o emulador do Android Studio sem abrir uma janela de terminal, utilizando um script em VBS (Visual Basic Script).

## Pré-requisitos
- Android Studio instalado com o SDK do Android.
- Um emulador configurado (neste exemplo, o emulador é chamado Pixel_8_API_35).
### Passos para Criar um Script VBS
1. **Abrir um Editor de Texto:**

- Use o Bloco de Notas ou qualquer outro editor de texto de sua escolha.
2. **Inserir o Código:**

- Copie e cole o seguinte código no editor de texto:

```
Set WshShell = CreateObject("WScript.Shell")
WshShell.Run """C:\Users\"seu-usuario"\AppData\Local\Android\Sdk\emulator\emulator.exe"" -avd Pixel_8_API_35", 0
```
- Explicação do Código:
  - `Set WshShell = CreateObject("WScript.Shell")`: Cria uma instância do objeto `WScript.Shell,`que permite executar comandos no sistema.

  - `WshShell.Run`: Executa o comando especificado.
  - `"""C:\Users\"seu-usuario"\AppData\Local\Android\Sdk\emulator\emulator.exe"" -avd Pixel_8_API_35"`: O caminho para o executável do emulador com o parâmetro para iniciar o emulador especificado.
  - `, 0`: Este parâmetro instrui o script a executar o comando sem abrir uma janela de terminal.
3. **Salvar o Arquivo:**

- Clique em **Arquivo > Salvar Como.**
- No campo "Nome do arquivo", insira iniciar_emulador.vbs.
- No campo "Tipo", selecione "Todos os arquivos".
- Salve o arquivo em um local acessível, como a área de trabalho.
### Criar um Atalho para o Script VBS
1. **Criar Atalho:**
- Clique com o botão direito no arquivo iniciar_emulador.vbs e selecione Criar atalho.
2. **Mover o Atalho:**
- Mova o atalho recém-criado para a área de trabalho ou para o local de sua preferência.
## Executando o Emulador
- Para iniciar o emulador:
  - Dê um duplo clique no atalho que você criou para o script VBS.
## Considerações Finais
- Este método permite que o emulador do Android Studio seja iniciado sem que uma janela de terminal apareça, proporcionando uma experiência mais limpa e direta.

- Certifique-se de que o caminho para o executável do emulador e o nome do emulador estejam corretos para evitar erros de execução.
