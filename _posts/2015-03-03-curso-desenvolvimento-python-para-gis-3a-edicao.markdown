---
layout: post
title:  "Curso Desenvolvimento Python para GIS 3a Edi&ccedil;&atilde;o"
date:   2015-03-03 16:39:00
categories: curso python gis
---

Ol&aacute; pessoal

Hoje comeca a terceira turma do curso [Desenvolvimento Python para GIS][geocursos-python], uma parceria com o Fernando Quadro da Geocursos que tem sido muito bacana. O curso &eacute; totalmente m&atilde;o na massa, ent&atilde;o &eacute; fundamental garantir que todos os participantes tenham acesso a um ambiente com as ferramentas e dados que s&atilde;o utilizados durante o curso.

Nesta edi&ccedil;&atilde;o eu decidi publicar parte das informa&ccedil;&otilde;es no meu blog (n&atilde;o &eacute; realmente um blog, esta mais para um rascunho de id&eacute;ias que estou iniciando agora). Espero que este texto possa ajudar os participantes desta edicao, ex-alunos, futuros alunos e a todos os interessados no assunto.

Não existe restrição de ambiente para assistir o curso, mas os exemplos utilizam o ambiente Linux. Sendo assim, o primeiro passo do curso é configurar um ambiente Linux que possa ser utilizado durante o curso. Nós utilizamos o [Vagrant][vagrant] com [VirtualBox][virtualbox] pela facilidade de instalação e configuração e também por serem gratuitos.

**Instalação do VirtualBox**

O VirtualBox é um gerenciador de máquinas virtuais criado pela antiga Sun, atual Oracle. Durante o curso nós vamos utiliza-lo de forma indireta, através do Vagrant.

Durante o processo de instalação são feitas várias perguntas para autorizar a instalação de devices do VirtualBox. Simplemente aceite todas, o que permitirá o uso de dispositivos usb entre outros nas máquinas virtuais.

![Instalação do VirtualBox]({{ site.url }}/downloads/Untitled01.png)

![Instalação do VirtualBox]({{ site.url }}/downloads/Untitled02.png)

![Instalação do VirtualBox]({{ site.url }}/downloads/Untitled03.png)

![Instalação do VirtualBox]({{ site.url }}/downloads/Untitled04.png)

![Instalação do VirtualBox]({{ site.url }}/downloads/Untitled05.png)

![Instalação do VirtualBox]({{ site.url }}/downloads/Untitled06.png)

![Instalação do VirtualBox]({{ site.url }}/downloads/Untitled07.png)

**Instalação do Vagrant**

O Vagrant é um gerenciador de máquinas virtuais que foca em criar processos simplificados para criação manual e automática destas máquinas. O Vagrant é programa muito útil quando precisamos criar uma máquina virtual rapidamente ou se queremos por exemplo criar várias máquinas com as mesmas configurações.

![Instalação do Vagrant]({{ site.url }}/downloads/Untitled08.png)

![Instalação do Vagrant]({{ site.url }}/downloads/Untitled09.png)

![Instalação do Vagrant]({{ site.url }}/downloads/Untitled10.png)

![Instalação do Vagrant]({{ site.url }}/downloads/Untitled11.png)

![Instalação do Vagrant]({{ site.url }}/downloads/Untitled12.png)

Após a instalação do Vagrant (provavelmente você vai precisar reiniciar o computador antes de seguir adiante), abra um prompt de comando (Programas -> Acessórios -> Prompt de comando) e digite os comandos a seguir.

{% highlight sh %}
C:\Users\roberto> cd Documents

C:\Users\roberto\Documents> mkdir vm

C:\Users\roberto\Documents> cd vm

C:\Users\roberto\Documents\vm> vagrant init hashicorp/precise32

C:\Users\roberto\Documents\vm> vagrant up
{% endhighlight %}

Os comandos abaixo vão criar uma pasta **vm** dentro da pasta **Documents**, criar uma máquina virtual baseada no modelo hashicorp/precise32 e inicia-la. O primeiro processo de inicialização pode demorar algum tempo porque o Vagrant vai copiar este modelo para o computador local (aproximadamente 200MB). A inicialização das próximas máquinas será muito mais rápido porque a cópia será local.

Após a inicialização da máquina virtual, você deverá ver as seguintes mensagens em seu prompt de comando.

![Instalação do Vagrant]({{ site.url }}/downloads/Untitled13.png)


[geocursos-python]: http://www.geocursos.com.br/python
[vagrant]: http://www.vagrantup.com
[virtualbox]: https://www.virtualbox.org

