# test
1. Запустить постман коллекцию Аттестация Issue Финал

2. В коллекции **Аттестация Issue Финал** зайти во вкладку Variables

3. Создать следуюющие значения: 
URL https://api.github.com
owner TataritnsevE
repo test
issuesNumber

4. Нажать кнопку Save

5. Создать первый запрос POST "Создание issues" {{URL}}/repos/{{owner}}/{{repo}}/issues

6. Во вкладке Authorization в в поле "Type" выбрать "Bearer Token" и справа в поле "Token" прописать заранее созданный token в аккаунте на платформе GitHub

7. Далее прописать Body
{
    "title": "Issue 1",
    "body": "Something went wrong",
    "labels": ["bug"],
    "assignee": "TatarintsevE"
}

8. Нажать кнопку "Save"

9. Затем нажать кнопку "Send"

10. Должен получиться ответ на запрос с кодом 201Created и репозитории появляется Issue 1

11. Далее, создаем второй запрос GET {{URL}}/repos/{{owner}}/{{repo}}/issues

12. Во вкладке Authorization в в поле "Type" выбрать "Bearer Token" и справа в поле "Token" прописать заранее созданный token в аккаунте на платформе GitHub

13. Body запроса оставляем пустым

14. Нажимаем кнопку "Save", а после кнопку "Send"

15. Приходит ответ на запрос с кодом 200OK

16. Создаем третий запрос PATCH на редактирование {{URL}}/repos/{{owner}}/{{repo}}/issues/{{issuesNumber}}

17. Во вкладке Authorization в поле "Type" выбрать "Bearer Token" и справа в поле "Token" прописать заранее созданный token в аккаунте на платформе GitHub

18. В Body прописываем
{
    "title": "Issue 2",
    "body": "Something went wrong",
    "labels": ["bug"],
    "assignee": "TatarintsevE"
}

19. Нажать кнопку "Save" и затем нажать кнопку "Send"

20. Должен получиться ответ на запрос с кодом 200OK и репозиторий меняется на Issue 2

21. Затем создаем последний запрос DELETE {{URL}}/repos/{{owner}}/{{repo}}/issues/{{issuesNumber}}/lock

22. Во вкладке Authorization в в поле "Type" выбрать "Bearer Token" и справа в поле "Token" прописать заранее созданный token в аккаунте на платформе GitHub

23. В Body прописываем
{
    "title": "Issue 2",
    "body": "Something went wrong",
    "labels": ["bug"],
    "assignee": "TatarintsevE"
}

24. Нажать кнопку "Save" и затем нажать кнопку "Send"

25. Приходит ответ на запрос с кодом 204No Content





