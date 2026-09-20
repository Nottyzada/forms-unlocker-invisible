# Forms Unlocker Invisible

Userscript para uso em páginas do Google Forms. Ele pode ser instalado no navegador com [Tampermonkey](https://www.tampermonkey.net/) ou [Violentmonkey](https://violentmonkey.github.io/).

> **Aviso de uso responsável:** use este script somente em formulários, contas e dispositivos para os quais você tem autorização. Não o utilize para burlar regras de avaliações, controles institucionais, políticas de uma escola/empresa ou restrições de segurança. O comportamento do Google Forms pode mudar a qualquer momento, e o projeto não garante compatibilidade futura.

## Arquivos

- [`script.js`](./script.js): userscript principal.
- `README.md`: este tutorial.

## Requisitos

- Google Chrome, Chromium, Microsoft Edge, Firefox ou outro navegador compatível com extensões de userscript.
- Tampermonkey ou Violentmonkey instalado.
- Acesso autorizado ao Google Forms que será utilizado.

## Instalação com Tampermonkey

1. Instale o [Tampermonkey](https://www.tampermonkey.net/) para o seu navegador.
2. Abra o menu da extensão e escolha **Create a new script** / **Criar um novo script**.
3. Apague o conteúdo de exemplo que aparece no editor.
4. Abra o arquivo [`script.js`](./script.js) deste repositório, copie todo o conteúdo e cole no editor do Tampermonkey.
5. Salve com **Ctrl + S** ou pelo menu **File > Save**.
6. Abra o painel do Tampermonkey e confirme que **Forms Unlocker Invisible** está com o interruptor ativado.

### Instalação direta pelo GitHub

Se o repositório publicar o arquivo como conteúdo bruto, você também pode abrir o arquivo `script.js` no GitHub, clicar em **Raw** e confirmar a instalação no Tampermonkey. Antes de confirmar, confira o código e o endereço do repositório.

## Instalação com Violentmonkey

1. Instale o [Violentmonkey](https://violentmonkey.github.io/) para o seu navegador.
2. Clique no ícone da extensão e selecione **New** / **Novo**.
3. Remova o conteúdo padrão do editor.
4. Copie todo o conteúdo de [`script.js`](./script.js) e cole no editor.
5. Clique em **Save** ou use **Ctrl + S**.
6. No painel do Violentmonkey, confirme que o script está habilitado.

Para instalar diretamente, abra `script.js` em sua versão **Raw** no GitHub. O Violentmonkey deverá reconhecer o cabeçalho `// ==UserScript==` e mostrar a tela de instalação.

## Como ativar

1. Abra o painel do Tampermonkey ou Violentmonkey.
2. Localize **Forms Unlocker Invisible**.
3. Deixe o script como **Enabled/Ativado**.
4. Verifique se o navegador permite a execução da extensão em `docs.google.com`.
5. Recarregue a página do Google Forms depois de ativar ou alterar o script.

O cabeçalho do script limita a execução a páginas com o endereço `docs.google.com/forms/`. Ele não deve ser executado em outros sites.

## Como usar

1. Com o userscript ativado, abra o formulário autorizado no Google Forms.
2. Aguarde o carregamento completo da página.
3. Quando aplicável, o script adicionará um botão invisível de **Bypass** no canto inferior esquerdo da janela. A área clicável tem aproximadamente 64 × 64 pixels.
4. Clique uma vez nessa área para acionar a ação. A página será recarregada com o marcador `#gfu` na URL.
5. Se o formulário continuar bloqueado, recarregue a página manualmente e verifique os passos de solução de problemas abaixo.

### Posição exata do botão

O botão fica no **canto inferior esquerdo da janela**, sobre a pequena área destacada na imagem abaixo. Clique dentro do quadrado indicado pela seta; como o botão é invisível, não haverá um texto visível sobre ele.

![Posição do botão invisível no Google Forms](./CliqueA.png)

> A área clicável acompanha a janela do navegador, não o conteúdo central do formulário. Se você redimensionar a janela ou alterar o zoom, procure novamente o canto inferior esquerdo.

O botão é intencionalmente invisível; isso não significa que o script esteja desativado. Em algumas situações o script também mostra uma mensagem informando que um *User Agent Spoofer* é necessário. Só instale ferramentas adicionais se você confiar nelas e tiver autorização para usá-las.

## Verificar se está funcionando

- No painel do gerenciador, o script deve aparecer como ativado.
- Na página, abra as ferramentas de desenvolvedor com **F12**, vá à aba **Console** e procure a mensagem `Initialized`.
- Confirme que o endereço é um Google Forms e que a extensão tem permissão para executar scripts nesse domínio.

## Solução de problemas

### O script não aparece no painel
Confira se o arquivo foi salvo com o cabeçalho completo `// ==UserScript==` no início e se a extensão correta está instalada.

### O script está ativado, mas nada acontece
Recarregue a página, confirme o domínio e desative temporariamente outros userscripts que alterem o Google Forms. O Google atualiza a estrutura interna das páginas com frequência, o que pode quebrar seletores usados pelo script.

### O botão invisível não responde
Clique na área inferior esquerda da janela, recarregue a página e tente novamente. Se houver zoom diferente de 100%, a posição percebida pode variar.

### Aparece a mensagem sobre User Agent Spoofer
Essa mensagem indica que o fluxo detectado pelo script exige uma configuração adicional. Consulte a documentação indicada pelo próprio script e use qualquer ferramenta somente em um ambiente autorizado.

### O Google Forms mostra um erro
Abra o Console do navegador, copie o erro sem incluir dados pessoais e abra uma [issue](https://github.com/Nottyzada/forms-unlocker-invisible/issues) descrevendo navegador, versão, sistema operacional e URL sem informações privadas.

## Desinstalação

- **Tampermonkey:** abra o painel, localize o script, escolha o ícone de lixeira e confirme.
- **Violentmonkey:** abra o painel, localize o script, escolha **Remove/Delete** e confirme.

## Desenvolvimento e contribuições

Alterações podem ser propostas por pull request. Ao relatar um problema, não envie respostas de formulários, tokens, endereços de e-mail ou outros dados pessoais.

## Licença

Nenhuma licença foi definida neste repositório. Até que uma licença seja adicionada, todos os direitos permanecem com o autor.
