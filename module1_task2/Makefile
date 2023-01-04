POST_TITLE = Who are we
POST_NAME = who-are-we
build: ## create a rule to build the webpage and create the file /dist
	hugo
clean: ## create a rule `clean` to clenup all directory /dist
	rm -rf dist/*
post: ## Create a new blog post whose filename and title come from the environment variables POST_TITLE and POST_NAME 
	hugo new posts/$(POST_NAME)
help:
	hugo help
