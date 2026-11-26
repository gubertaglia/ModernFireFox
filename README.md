# ModernFireFox

Tema CSS para o Firefox, desenvolvido para Fedora e GNOME. Usa uma paleta neutra clara e escura, reposiciona a barra de endereços acima das abas horizontais e estiliza a barra lateral, o gerenciador de senhas e outras páginas internas.

## Compatibilidade

| Ambiente | Situação na v0.10.3 |
| --- | --- |
| Firefox 160.0 no Fedora 45 | Páginas internas testadas visualmente em perfil temporário na v0.10.1. O painel de notificações atualizado ainda precisa de validação visual. O layout das abas, a barra lateral e os controles do GNOME ainda precisam de validação visual. |
| Firefox 161 no Windows 11 | Barras de navegação e favoritos e painéis de exclusão de dados e de abas validados nos modos claro e escuro. |
| Outros ambientes Linux e macOS | Instalação manual disponível. Aparência e controles de janela ainda sem validação. |
| Firefox ESR, Beta e Nightly | Sem validação. Diferenças na interface podem impedir a aplicação de parte do tema. |

O tema usa seletores internos do Firefox. Atualizações podem mudar a aparência ou exigir uma atualização do CSS. Os botões coloridos da janela são específicos do Linux e dependem de o Firefox desenhar seus próprios controles. O tema funciona sem extensões, inclusive sem Blur my Shell.

## Instalação

1. Extraia `ModernFireFox-v0.10.3.zip`. Se ainda precisar baixar o pacote, use a [release v0.10.3](https://github.com/gubertaglia/ModernFireFox/releases/tag/v0.10.3).
2. Abra `about:support` no Firefox em que você quer instalar o tema. Na linha **Pasta do perfil** ou **Diretório do perfil**, clique no botão para abrir a pasta. Se não abrir, use `about:profiles` e copie o caminho do **Diretório raiz** do perfil em uso.
3. Abra `about:config`, procure `toolkit.legacyUserProfileCustomizations.stylesheets` e defina como `true`.
4. Feche o Firefox por completo. Na pasta do perfil aberta no passo 2, crie a pasta `chrome` se ela ainda não existir.
5. Caso já existam `userChrome.css` ou `userContent.css` dentro de `chrome`, guarde uma cópia dos arquivos antigos em outra pasta. Copie os dois CSS do ZIP diretamente para `chrome`.
6. Abra o Firefox. Confira a barra de abas, abra a barra lateral e visite `about:logins`.

```text
<pasta do perfil>/
  chrome/
    userChrome.css
    userContent.css
```

Use o perfil aberto pelo próprio Firefox. Isso vale também para Flatpak e Snap, que podem guardar o perfil em caminhos diferentes. No Windows, confira se os arquivos terminam em `.css`.

Se o tema carregar parcialmente, selecione **Tema do sistema — automático** em `about:addons` e teste novamente. Para conferir as abas verticais, use a opção do próprio Firefox nas configurações da barra lateral.

## Atualizar ou remover

- **Atualizar.** Feche o Firefox, faça uma cópia dos CSS ativos e substitua os dois pelos da nova versão. Reabra o navegador.
- **Remover.** Feche o Firefox, mova os dois CSS do ModernFireFox para fora de `chrome` e restaure os arquivos anteriores, se houver. Se não usar mais CSS personalizado, você pode restaurar a preferência em `about:config` para o valor padrão.

## Segurança e privacidade

O pacote inclui os dois CSS, este guia e as notas da versão. Os CSS se aplicam à interface e às páginas internas do Firefox, sem scripts, importações ou recursos externos. As regras para `about:logins` alteram cores, bordas e botões.

Se for compartilhar o tema, copie somente os dois CSS e a documentação. A pasta completa do perfil pode conter senhas, cookies, sessões, favoritos e histórico. [O que o Firefox guarda no perfil — Mozilla](https://support.mozilla.org/en-US/kb/profiles-where-firefox-stores-user-data)

[Personalização avançada do Firefox — Mozilla](https://support.mozilla.org/en-US/kb/firefox-advanced-customization-and-configuration)
