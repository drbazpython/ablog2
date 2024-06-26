.PHONY:

DJANGO_PROJECT := blogproject

all:
	@echo "Hello $(LOGNAME), nothing to do by default"
	@echo "Try 'make help'"

pip-install-dev:
	pip install --upgrade pip pip-tools
	pip-sync requirements.txt requirements-dev.txt

pip-install:
	pip install --upgrade pip pip-tools
	pip-sync requirements.txt

pip-update:
	pip install --upgrade pip pip-tools
	pip-compile requirements.in
	pip-compile requirements-dev.in
	pip-sync requirements.txt requirements-dev.txt

server:
	make opensite
	python3 manage.py runserver

opensite:
	open http://127.0.0.1:8000/

admin:
	open http://127.0.0.1:8000/admin