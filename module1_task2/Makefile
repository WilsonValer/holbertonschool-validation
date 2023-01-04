POST_TITLE = Who are we
POST_NAME = who-are-we
build:	## create a rule to build the webpage and create the file /dist
	@hugo
clean:	## create a rule `clean` to clenup all directory /dist
	@rm -rf dist/*
post:	## Create a new blog post whose filename and title come from the environment variables POST_TITLE and POST_NAME 
	@hugo new posts/$(POST_NAME).md
	@sed -i 's/title:.*/title: $(POST_TITLE)/' content/posts/$(POST_NAME).md
	@sed -i 's/draft:.*/draft: "false"/' content/posts/$(POST_NAME).md
help:	## command help
	@echo "build : create a rule to build the webpage and create the file /dist"
	@echo "clean: create a rule `clean` to clenup all directory /dist"
	@echo "post: Create a new blog post whose filename"
	@echo "help: command to help about the usage the proyect"
