# github_hw_2
1. На локальном репозитории сделать ветки для:
- Postman
- Jmeter
- CheckLists
- Bug Reports
- SQL
- Charles
- Mobile testing

`git clone git@github.com:olyacenko/github_hw_2.git` - скопировать удаленный репозиторий в локальный

`git branch postman`

`git branch jmeter`

`git branch checklists`

`git branch bug_reports`

`git branch sql`

`git branch charles`

`git branch mobile_testing`

----

2. Запушить все ветки на внешний репозиторий -  

`git push -u origin  bug_reports charles checklists jmeter mobile_testing postman sql`

----

3. В ветке Bug Reports сделать текстовый документ со структурой баг репорта - 

`git checkout bug_reports` - переключиться на ветку  bug_reports ;

`vim bug_report_pattern.txt` ;

`i` - начать редактирование ;

ввести текст в формате txt ;

клавишa `esc` - выйти из режима редактирования ;

клавиши `shift+:` - назначить команду ;

`wq` - записать и закрыть редактор

----

4. Запушить структуру багрепорта на внешний репозиторий - 

`git add bug_report_pattern.txt` => `git commit -m 'add bug_report_pattern.txt'` => `git push `

----

5. Вмержить ветку Bag Reports в Main -

`git checkout main` => `git merge bug_reports`

----

6. Запушить main на внешний репозиторий - `git push` 

----

7. В ветке CheckLists набросать структуру чек листа. -

`git checkout checklists` - переключиться на ветку checklists ;

`vim checklist_pattern.txt` ;

`i` - начать редактирование ;

ввести текст в формате txt ;

клавишa `esc` - выйти из режима редактирования ;

клавиши `shift+:` - назначить команду ;

`wq` - записать и закрыть редактор

----

8. Запушить структуру на внешний репозиторий - 

`git add checklist_pattern.txt` => `git commit -m 'add checklist_pattern.txt'` => `git push`

----

9. На внешнем репозитории сделать Pull Request ветки CheckLists в main - 

Зайти в  ` Pull requests` => 

`create a pull request` => 

в «Compare changes» выбрать ветки : `base: main` `compare: checklists` => 

`create pull request` => 

`create pull request` => 

`merge pull request` => 

`confirm merge`

----

10. Синхронизировать Внешнюю и Локальную ветки Main -

`git checkout main` => `git pull`
