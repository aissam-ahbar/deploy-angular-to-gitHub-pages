# Deploy Angular App to Github

To deploy your application to Github, you first need to create a **Github** account [here](https://github.com/).

## 1) Create a repository in Github ([here](https://github.com/))

Creates your-project-name.git that will have the following origin :

```
https://github.com/your-username/your-project-name.git
```

## 2) Push your changes to remote main branch

```ts
git remote add origin https://github.com/your-username/your-project-name.git
git branch -M main
git push -u origin main
```

## 3) Create local github branch

```ts
git checkout -b gh-pages
```

## 4) Build the project using the GitHub project name

```ts
ng build --output-path docs --base-href /your_project_name/
```

## 5) Create a default not found page (404) - Copy index.html

```ts
cp docs/index.html docs/404.html
```

## 6) Commit and deploy changes

```ts
git add .
git commit -a -m "sparkles: initial deploy to Github page"
git push origin gh-pages
```

## 7) Public from the docs folder on Github

- On the GitHub project page, open Settings
- Select the pages option to configure the site to publish from the docs folder
- Click on **_Save_**

## 8) Open your deployed application link

Your application will be deployed to :
`https://<user_name>.github.io/<project_name>`
