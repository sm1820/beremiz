===========================================
 Настройка окружения и сборка документации
===========================================


-----------------------------------
По умолчанию: Использование Docker
-----------------------------------

Для упрощения установки на различные платформы предполагается использование `docker-контейнера <https://hub.docker.com/r/jubnzv1/sphinx-build/>`_, содержащего необходимые для сборки пакеты.

1. `Установить Docker <https://docs.docker.com/install/>`_

2. Загрузить исходники Beremiz::

      git clone https://github.com/jubnzv/beremiz beremiz

3. Для сборки документации::

      cd beremiz/doc
      make -f Makefile.docker

Сгенерированные документы в форматах `pdf` и `html` будут расположны в директории `beremiz/doc/build`.

---------------------------------------------------
Альтернатива: Нативная установка (Debian GNU/Linux)
---------------------------------------------------

Для Debian Stretch потребуется установить следующие пакеты::

	apt-get -y install make \
		    python2.7 \
		    python-sphinx \
		    python-sphinx-rtd-theme \
		    doxygen \
		    graphviz \
		    python-breathe \
		    breathe-doc \
		    texlive-base \
		    texlive-latex-base \
		    texlive-lang-cyrillic \
		    texlive-fonts-recommended \
		    texlive-generic-extra \
		    texlive-latex-extra \
		    texlive-latex-recommended

После этого сборка может быть запущена нативно::

     cd beremiz/doc
     make html latexpdf
