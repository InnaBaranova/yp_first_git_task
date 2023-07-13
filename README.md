# Something I know about GIT already

-------

### Синхронизируем локальные и удаленный репозитории

- 'git add --all' - подготовили все файлы для коммита

- 'git commit -m' - закоммитили файлы с комментарием

- 'git push'- отправить изменения на удалённый репозиторий

**'git push -u origin master'**- первый раз используем эту команду: флаг -u и параметр origin (имя удалённого репозитория) и master (название текущей ветки). Флаг -u свяжет локальную ветку с одноимённой удалённой.

__________

### File git statuses

```mermaid
-- "file created" --> untracked;  
untracked -- "git add" --> staged+tracked;
  staged+tracked    -- "git commit" --> committed+tracked;
stage -- "changed --> modified+tracked;
modified+tracked -- "git add" --> staged+tracked;
committed+tracked -- "changed" --> modified+tracked;
``` 