.PHONY: dev prod down stop bash magento magento-console install deploy-dumps
ARG=

dev:
	docker-compose -f docker-compose.yml -f docker-compose-dev.yml up -d
prod:
	docker-compose up -d
down:
	docker-compose down
stop:
	docker-compose stop

bash:
	docker exec -it magento2web bash
magento:
	docker exec -it magento2web bin/magento $(ARG)
install:
	docker exec -it magento2web m2install.sh -f -s composer -v $(ARG)
deploy-dumps:
	docker exec -it magento2web m2install.sh -f
magento-console:
	docker exec -it magento2web n98-magerun2 dev:console