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
flowchart TD
-- file created --> A [untracked];
A -- git add --> B [staged+tracked];
B -- git commit --> C [committed+tracked];
B -- changed --> D [modified+tracked];
D -- git add --> B;
C -- changed --> D;
``` 