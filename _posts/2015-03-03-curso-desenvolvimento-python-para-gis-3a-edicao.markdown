---
layout: post
title:  "Curso Desenvolvimento Python para GIS 3a Edi&ccedil;&atilde;o"
date:   2015-03-03 16:39:00
categories: curso python gis
---

Ol&aacute; pessoal

Hoje comeca a terceira turma do curso [Desenvolvimento Python para GIS][geocursos-python], uma parceria com o Fernando Quadro da Geocursos que tem sido muito bacana. O curso &eacute; totalmente m&atilde;o na massa, ent&atilde;o &eacute; fundamental garantir que todos os participantes tenham acesso a um ambiente com as ferramentas e dados que s&atilde;o utilizados durante o curso.

Nesta edi&ccedil;&atilde;o eu decidi publicar parte das informa&ccedil;&otilde;es no meu blog (n&atilde;o &eacute; realmente um blog, talvez seja mais um rascunho de id&eacute;ias que estou iniciando agora). Espero que este texto possa ajudar os participantes desta edição, ex-alunos, futuros alunos e a todos os interessados no assunto.

Não existe restrição de ambiente para assistir o curso, mas os exemplos utilizam o ambiente Linux. Sendo assim, o primeiro passo do curso é configurar um ambiente Linux para execução dos exemplos e exercícios. Vamos utilizar o [Vagrant][vagrant] com [VirtualBox][virtualbox] pela facilidade de instalação e configuração e também por serem gratuitos.

**Instalação do VirtualBox**

O [VirtualBox][virtualbox] é um gerenciador de máquinas virtuais criado pela antiga Sun, atual Oracle. Durante o curso nós vamos utiliza-lo de forma indireta, através do [Vagrant][vagrant].

Durante o processo de instalação o programa faz várias perguntas sobre autorização da instalação de dispositivos do [VirtualBox][virtualbox]. Simplemente aceite todas, o que permitirá o uso de dispositivos USB entre outros nas máquinas virtuais.

![Instalação do VirtualBox]({{ site.url }}/downloads/Untitled01.png)

![Instalação do VirtualBox]({{ site.url }}/downloads/Untitled02.png)

![Instalação do VirtualBox]({{ site.url }}/downloads/Untitled03.png)

![Instalação do VirtualBox]({{ site.url }}/downloads/Untitled04.png)

![Instalação do VirtualBox]({{ site.url }}/downloads/Untitled05.png)

![Instalação do VirtualBox]({{ site.url }}/downloads/Untitled06.png)

![Instalação do VirtualBox]({{ site.url }}/downloads/Untitled07.png)

**Instalação do Vagrant**

O [Vagrant][vagrant] é um gerenciador de máquinas virtuais com foco em criar processos simplificados para criação manual e automática destas máquinas. O [Vagrant][vagrant] é programa muito útil quando precisamos criar uma máquina virtual rapidamente ou se queremos criar várias máquinas com as mesmas configurações.

![Instalação do Vagrant]({{ site.url }}/downloads/Untitled08.png)

![Instalação do Vagrant]({{ site.url }}/downloads/Untitled09.png)

![Instalação do Vagrant]({{ site.url }}/downloads/Untitled10.png)

![Instalação do Vagrant]({{ site.url }}/downloads/Untitled11.png)

![Instalação do Vagrant]({{ site.url }}/downloads/Untitled12.png)

Após a instalação do [Vagrant][vagrant] (provavelmente você vai precisar reiniciar o computador antes de seguir adiante), abra um prompt de comando (Programas -> Acessórios -> Prompt de comando) e digite os comandos a seguir.

{% highlight sh %}
C:\Users\roberto> cd Documents

C:\Users\roberto\Documents> mkdir vm

C:\Users\roberto\Documents> cd vm

C:\Users\roberto\Documents\vm> vagrant init hashicorp/precise32

C:\Users\roberto\Documents\vm> vagrant up
{% endhighlight %}

Os comandos abaixo vão 1) criar uma pasta **vm** dentro da pasta **Documents**, 2) criar uma máquina virtual baseada no modelo hashicorp/precise32 e 3) iniciá-la. O primeiro processo de inicialização pode demorar algum tempo porque o [Vagrant][vagrant] vai copiar a imagem modelo para o computador local (aproximadamente 200MB). A inicialização das próximas máquinas será muito mais rápida porque a cópia da imagem já estará no computador.

Após a inicialização da máquina virtual, você deverá ver as seguintes mensagens em seu prompt de comando.

![Instalação do Vagrant]({{ site.url }}/downloads/Untitled13.png)

**Conectando-se a máquina virtual**

Para acessar a máquina virtual, precisamos de um programa que trabalhe com o protocolo SSH. Neste curso vamos utilizar o [Putty][putty], um cliente SSH para Windows que é gratuito e simples.

Para começar, faça o download do programa neste [link][putty-download]. Salve o programa na sua Área de Trabalho (ou Desktop).

![Instalação do Vagrant]({{ site.url }}/downloads/Untitled14.png)

Faça um duplo clique sobre o ícone do Putty para iniciar o programa.

![Instalação do Vagrant]({{ site.url }}/downloads/Untitled15.png)

Preencha os dados solicitados.

```
Host Name (or IP address): localhost
Port: 2222
Saved Sessions: vm
```

Agora, clique no botão **Save** para gravar estes dados no perfil **vm**. A partir de agora basta um duplo clique no perfil **vm** para carregar os dados e abrir uma sessão.

![Instalação do Vagrant]({{ site.url }}/downloads/Untitled16.png)

Na primeira vez que você tentar conectar-se à máquina virtual, o [Putty][putty] irá informar que a chave de segurança não parece ser a correta e perguntar se você confia no servidor. Confirme que sim clicando no botão **Yes**.

![Instalação do Vagrant]({{ site.url }}/downloads/Untitled16.png)

A máquina virtual vai solicitar um usuário e senha para autorizar a conexão. Utilize os dados a seguir.

```
usuário: vagrant
senha: vagrant
```

![Instalação do Vagrant]({{ site.url }}/downloads/Untitled17.png)

Se você chegou até aqui e não ocorreu nenhum problema no caminho, parabéns!!! Você tem a sua disposição uma máquina virtual rodando o sistema operacional Linux, distribuição Ubuntu 14.04.2 LTS.

Espero que este pequeno passo a passo seja útil nos seus estudos.

Abraço,

Roberto

[geocursos-python]: http://www.geocursos.com.br/python
[vagrant]: http://www.vagrantup.com
[virtualbox]: https://www.virtualbox.org
[putty]: http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html
[putty-download]: http://the.earth.li/~sgtatham/putty/latest/x86/putty.exe