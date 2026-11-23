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

Os executáveis ainda não têm assinatura de desenvolvedor, então o sistema avisa na primeira abertura de cada versão.

**macOS** — aviso "A Apple não pôde verificar se o 'LLM Doc.app' está livre de malware":

1. Arraste o LLM Doc para **Aplicativos** e tente abri-lo uma vez; no aviso, clique em **Concluído**
   (não em "Mover para o Lixo").
2. Abra **Ajustes do Sistema → Privacidade e Segurança** e role até o fim.
3. Ao lado de "O 'LLM Doc' foi bloqueado…", clique em **Abrir Mesmo Assim** e confirme com a senha ou o Touch ID.
4. Abra o LLM Doc de novo e clique em **Abrir**.

Desde o macOS 15, o antigo "botão direito → Abrir" não libera mais o app. Alternativa pelo Terminal, que tira
só deste app a marca de "baixado da internet":

```bash
xattr -dr com.apple.quarantine "/Applications/LLM Doc.app"
```

**Windows** — aviso "O Windows protegeu o computador": *Mais informações* → *Executar assim mesmo*.

Confira, se quiser, que o arquivo baixado é o publicado: as somas SHA-256 estão em `SHA256SUMS.txt` na página
da versão (`shasum -a 256 arquivo` no macOS; `certutil -hashfile arquivo SHA256` no Windows).

## Privacidade

O LLM Doc roda só no seu computador (endereço 127.0.0.1) e guarda as chaves de API cifradas no
cofre do sistema. Prontuários só saem para o provedor de IA escolhido, com nome, CPF, telefone,
endereço e outros dados identificadores trocados por marcadores; com IA local (Ollama), nada sai.
Ao abrir, o programa consulta este repositório só para saber se há versão nova.
