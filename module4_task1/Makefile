# Implement the next steps for the actual Go-Hugo website's source code
build: ## Generate the website from markdown and config files in the 'dist/' folder
	@apt install ./hugo.deb
	@hugo
	@touch awesome-api
clean: ## Cleanup the content of the 'dist/' folder
	@rm -Rf dist/*

post: ## Create a new blog post using POST_TITLE and POST_NAME env variables
	@rm -Rf content/posts/$(POST_NAME).md
	@hugo new posts/$(POST_NAME).md
	@sed -i 's/title:.*/title: $(POST_TITLE)/' content/posts/$(POST_NAME).md
	@sed -i 's/draft:.*/draft: "false"/' content/posts/$(POST_NAME).md

package: ## Produce a zip file containing the 'dist/' folder
	@make build
	@mkdir -p dist
	@zip -r awesome-website.zip  dist/

build-docker: ## Define a docekr image
	@docker build -t awesome:build -f ./build/Dockerfile .

lint: ## Check markdown files for any syntax mistake
	@apt install curl -y
	@curl --silent --location https://deb.nodesource.com/setup_16.x | bash -
	@apt install nodejs -y
	@npm install -g markdownlint-cli 1>&2
	@markdownlint README.md DEPLOY.md

unit-tests: ## Run unit-tets of the project
	@touch coverage-units.out
integration-tests: ## Run integration-tests of the project
	@touch coverage-integrations.out

validate: ## Validate the project

help: ## Show this help usage
	@echo "Usage: make <command>"
	@echo "-----"
	@fgrep -h "##" Makefile | fgrep -v fgrep | sed -e 's/\\$$//' | sed -e 's/##//' | head -9
