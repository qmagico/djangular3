# Recrutamento back-end do QMágico

Olá amigo back-end. Bem vindo ao processo de recrutamento do QMágico.
Este projeto é um esqueleto de aplicação web, construído usando Django e AngularJS.
Se vc [se cadastrou no nosso site](CADE_O_LINK_DO_PROCESSO_SELETIVO), em breve vamos te mandar uma missão: construir uma aplicação web baseada neste projeto.
No email, que vc vai receber, haverá mais detalhes dos requisitos, e qual o prazo que a gente espera que vc entregue alguma coisa.
Mas vc pode - e deve - já ir se adiantando e estudando a estrutura deste projeto. Nos links abaixo você vai encontrar alguns vídeos que vão te ajudar nessa caminhada.

Observações importantes:
* Durante a execução da missão, **não faça fork** deste projeto. Projetos no Github são públicos e não queremos que os trabalhos dos candidatos influenciem uns aos outros.
* Conhecimento prévio de AngularJS vai ajudar muito, **mas não é obrigatório** pra completar a missão.
* Algum conhecimento prévio de Python **será necessário** pra completar a missão.
* A estrutura deste projeto é bastante semelhante aos projetos "de verdade" que temos aqui.
* Mesmo que vc não seja aprovado pra trabalhar com a gente na sua primeira tentativa, temos certeza que o aprendizado deste processo vai valer a pena o esforço!
* E se você não quiser participar do nosso processo mas quiser usar este projeto como base pros seus próprios projetos, vai em frente! Modéstia parte, o projeto tá bem feitinho e deverá te ajudar bastante! :-)
* A qualquer momento, se vc tiver problemas ou dúvidas, crie uma issue aqui no repo. Vamos tentar responder sempre que possível.


Videos e artigos que vão te ajudar:

* [Overview do setup](http://youtu.be/RvgZkrofgcU)
* [Arquitetura do projeto](https://www.youtube.com/watch?v=XarTMSK2Fq8)

# Setup do sistema operacional

As instruções abaixo são pra linux (ubuntu/debian). Se vc usa outro sistema operacional, a gente recomenda que vc crie uma VM usando Virtualbox ou algo parecido. Ou então fica à vontade pra mandar o pull request com o `setup_win.md` ou `setup_mac.md` ;-)

Vc vai precisar instalar algumas coisas no seu sistema operacional pra que tudo funcione direitinho. É bem possível que algumas dessas coisas vc já tenha instalado. Só precisa fazer isso uma vez na vida.

* 1) Instala esse monte coisa aí com o apt-get (node, npm, o postgres e umas bibliotecas aih)

```bash
sudo apt-get install python3-dev nodejs npm postgresql-9.3 postgresql-server-dev-all
```

* 2) Instala o gulp

```shell
sudo npm install -g gulp
```

* 3) Certifique-se que vc tem o python3 (meu ubuntu já veio com o python 2 e o 3, sendo que o 2 é o default)

* 4) Instale o virtualenvwrapper, [de acordo com as instruções que tem no site](http://virtualenvwrapper.readthedocs.org/en/latest/install.html)

# Setup do projeto

Agora vc precisa fazer o setup do projeto. Isso significa que se vc tivesse outro projeto desse, ia ter que fazer essas coisas de novo.

* 1) Cria o banco de dados e o usuario no postgres

```bash
sudo su postgres  #
createuser -d -SRP djangular3  # poe a senha djangular3
createdb -O djangular3 djangular3
exit  # Volta pro seu usuario

# Se vc quiser mudar o nome do banco/usuario/senha,
# tem que mexer no arquivo djangular3/settings.py
```

* 2) Cria o virtualenv do projeto e baixa as dependências do python

```shell
mkvirtualenv --python=/usr/bin/python3 djangular3  
# Renomeia esse djangular3 pro nome do seu projeto
deactivate  # So pra mostrar como sai do virtualenv
workon djangular3  # Entra no venv de novo
pip install -r requirements.txt
```

* 3) Cria as tabelas no banco

```shell
./manage.py migrate
```

* 4) Cria um superusuario no seu banco

```shell
./manage.py createsuperuser
```

* 5) Baixa as dependências pra build do frontend

```shell
cd frontend
npm install
```

* 6) Importa as funções do dev.sh pro seu bash

```shell
cd ..
. dev.sh  # Nao esquece desse pontinho ae
devhelp  # Esses comandos agora devem estar todos funcionando
#  Esse help aih eh a melhor parte. Ele vai te ajudar daqui pra frente.
#  Cuida dele pro seu projeto ficar sempre com os comandinhos atualizados!!
```
