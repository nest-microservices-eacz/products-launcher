## Dev

1. Clone repository 
2. Create a .env based on the .env.example file 
3. Execute the following command `docker compose up --build `



### Steps to Create Git Submodules

1. **Create a new repository on GitHub**  
2. **Clone the repository to your local machine**  
3. **Add the submodule**, where `repository_url` is the URL of the repository and `directory_name` is the name of the folder where you want the submodule to be saved (this folder should not already exist in the project):  
   ```bash
   git submodule add <repository_url> <directory_name>


4. Add the changes to the repository (git add, git commit, git push). Example:
Ej:
```
git add .
git commit -m "Add submodule"
git push
```
5. Initialize and update submodules. When someone clones the repository for the first time, they must run the following command to initialize and update the submodules:
```
git submodule update --init --recursive
```
6. To update the references of the submodules:
```
git submodule update --remote
```


## Important
If you are working on the repository that contains the submodules:

First, update and push the submodule.

Then, update and push the main repository.

If you do it the other way around, you will lose the references to the submodules in the main repository and will have to resolve conflicts.

