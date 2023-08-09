# Instalar o Jupyter Notebook no macOS
Clique nas setinhas para abrir o tópico.
<details><summary>I. TROCAR O DEFAULT SHELL DE .ZSH PARA .BASH</summary>


Hoje, o Mac usa o default shell como ``.zsh``. Eu, particularmente, prefiro o shell ``.bash`` por suportar várias funcionalidades. O primeiro passo seria trocar o shell de ``.zsh`` para ``.bash``.

Vamos ao primeiro passo. 

1. Abra o seu terminal pelo ``command+espaço``;
2. Para você ver que existem vários shells, digite ``cat /etc/shells``;
3. Você estará visualizando os shells existentes. Mas como precisamos setar o shell para ``.bash``, vamos ao próximo passo;
4. Digitar o comando ``chsh -s /bin/bash`` , *dica: ``chsh - s`` significa ``change shell``;
5. Informe a senha do seu Mac e dê enter (é normal não aparecer a senha visivelmente);
6. Pronto!
</p>
</details>

<details><summary>II. INSTALAR PYTHON EM SEU MAC</summary>

Normalmente o seu Mac vem com python instalado de forma nativa. Vamos verificar? Tem que ser a última versão de Python que é o 3.x.

1. No terminal (command+espaço), digite ``which python3``;
2. O terminal deve retornar a mensagem ``/usr/bin/python3``, o que significa que já está instalado!
</p>
</details>

<details><summary>III. INSTALAR O JUPYTER NOTEBOOK USANDO O PIP</summary>

Em vez de usar o Visual Code Studio para codar, prefiro o Jupyter Notebook por ser mais intuitivo e funciona no formato web. 

Pip é um gerenciador de pacotes padrão usado para instalar e gerenciar pacotes de software escritos em Python. Normalmente vem de forma nativa no macOS e usaremos o pip para instalar o jupiter notebook.

Vamos a instalação:

1. No terminal, digite ``pip3 install jupyter``;
2. Vai estar instalando e provavelmente vai acusar que o atual diretório não é um PATH;
3. Vamos ver qual é a variável do seu ambiente (PATH) digitando ``echo $PATH``;
4. Provavelmente deve aparecer a mensagem ``usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin``;
5. Execute este comando para padronizar o PATH ``nano .bash_profile`` ;
6. Copie este comando ``export PATH=$PATH:~/Library/Python/3.9/bin`` e cole;
7. Aperte o Control+O no teclado para confirmar a mudança do path;
8. Aperte ENTER para finalizar a confirmação, Você verá a mensagem ``[Wrote NUMBER linhas]``;
9. Aperte o ``Control+X`` para sair do nano;
10. Saia do terminal e abra novamente o terminal;
11. Digite ``echo $PATH`` ;
12. Deve aparecer a mensagem ``/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/munki:/Users/nomedoseucomputador/Library/Python/3.9/bin`` ;
13. Pronto! O objetivo disso foi para não ter que precisar escrever o ``diretório+jupyter notebook`` toda vez que você for abrir o terminal. Agora pode abrir o jupyter notebook digitando o único comando ``jupyter notebook``;
14. Vai abrir uma nova janela web e enjoy it!
15. Para sair do jupyter, basta apertar ``Control+C`` e depois dê enter em ``y`` no terminal ou clicar em ``Logout`` na web;
16. Para fechar o terminal, aperte ``command+W``.
</p>
</details>

<details><summary>IV. IMPORTAR A BIBLIOTECA DO SLACK</summary>

Para você usar o bot do slack com Python, precisa usar a biblioteca do Slack. O Slack fornece uma API Python Slack rica para integração. Para importar via terminal, digite ``pip3 install slackclient``

Agora é só usar a criatividade no jupyter notebook e dar o ``run``!
</p>
</details>
