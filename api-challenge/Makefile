DCMP = docker-compose

clean:
		sudo chown -R $(USER):$(USER) .
		find . -name "*.pyc" -exec rm -rf {} \;
		find . -type d -empty -delete;
		rm -rf htmlcov/
		rm -rf .coverage
		rm -rf *.log

build:
		${DCMP} build

migrate:
	 	${DCMP} run api sh -c 'cd src && python migrate.py db upgrade'

test:
		${DCMP} run api coverage run --omit="**migrations**,**tests**,**__init__.py**" --source='./src/' -m pytest -q

report:
		${DCMP} run api coverage report -m

start:
		${DCMP} up

startd:
		${DCMP} up -d

prune:
		docker container prune -f

stop:
		${DCMP} stop

execute:
		${MAKE} clean
		${MAKE} build
		${MAKE} migrate
		# ${MAKE} test
		# ${MAKE} report
		${MAKE} startd
		${MAKE} prune
