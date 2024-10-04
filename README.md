Этот проект по предсказанию пола на основе следующих датафреймов:
train_labels.csv:
    - «user_id» - id пользователя;
    - «target» - пол пользователя (1 / 0).
 
train.csv, test.csv;
    - «request_ts» - server timestamp of request;
    - «user_id» - id пользователя (см. п.1);
    - «referer» - url, где показывается реклама. В данном случае захэшировано 2 части url:
        1) domain - домен урла;
        2) path - все что после domain. Например, https://a758bf6/1432d3f1, a 758bf6 - domain, 1432d3f1 - path.
    - «geo_id» - id geo;
    - «user_agent» - строка user_agent.
 
referer_vectors.csv:
    - «component0» - … - «component9» - числа, которые несут в себе информацию о url. Их нельзя как-либо интерпретировать;
    - «referer» - url, где показывается реклама (см. п.2).
 
geo_info.csv:
    - «geo_id» - id geo (см. п.2);
    - «country_id» - id страны;
    - «region_id» - id региона;
    - «timezone» - часовой пояс для geo.


Требования
Для каждого пользователя (user) из файла test_users.csv необходимо предсказать пол. Их рекламные запросы лежат в файле test.csv.

Формат вывода
Формат вывода соответствует train_labels.csv.


https://cups.online/ru/workareas/innopolis_open_ai/1004/1923?is_sandbox=1 - ссылка для скачивания датафреймов
