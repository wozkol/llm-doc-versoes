# LLM Doc — versões

Instaladores do **LLM Doc**, aplicação que escreve rascunhos de documentos médicos e respostas a
pacientes a partir do prontuário, rodando no próprio computador (Windows e macOS).

Este repositório guarda só as versões publicadas. O código-fonte é privado.

## Baixar

Abra a [versão mais recente](https://github.com/wozkol/llm-doc-versoes/releases/latest) e escolha:

| Arquivo | Sistema |
|---|---|
| `LLM-Doc-<versão>-Instalador-Windows.exe` | Windows 10/11: instala só para o seu usuário, sem pedir administrador |
| `LLM-Doc-<versão>-Windows-portatil.exe` | Windows, sem instalar |
| `LLM-Doc-<versão>-macOS.dmg` | macOS 12 ou mais recente: arraste para Aplicativos |
| `LLM-Doc-<versão>-macOS.zip` | macOS, alternativa ao .dmg |

Os executáveis ainda não têm assinatura de desenvolvedor. Na primeira abertura:

- **Windows:** "O Windows protegeu o computador" → *Mais informações* → *Executar assim mesmo*.
- **macOS:** botão direito no LLM Doc → *Abrir* → *Abrir*.

## Privacidade

O LLM Doc roda só no seu computador (endereço 127.0.0.1) e guarda as chaves de API cifradas no
cofre do sistema. Prontuários só saem para o provedor de IA escolhido, com nome, CPF, telefone,
endereço e outros dados identificadores trocados por marcadores; com IA local (Ollama), nada sai.
Ao abrir, o programa consulta este repositório só para saber se há versão nova.
