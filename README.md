# Tips

First start:

1.Create Tips repository on git hub

2.Init local and push to Github
echo "# Tips" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/dunght163/Tips.git
git push -u origin master

#note: using 'https://github.com/dunght163' for username/email. If configed SSH, using 'git@github.com:dunght163'

3.Config user.name/user.email
git config user.name <your username>
git config user.email <your mail>
