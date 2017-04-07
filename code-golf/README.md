# Code Golf
Competition to write the shortest and fastest programs to solve problems in a variety of languages, including Javascript, Python, C++, and Java. It is built on Python 3.5 and Flask and uses a SQLAlchemy instance.

### Setup
Install dependencies using and deploy using: 
```shell
pip install -r requirements.txt
python app.py
```

### Endpoints
POST `/golf/:task_id/answer?code=<CODE>&username=<USERNAME>`
Submit a response on task `task_id`

GET `/golf/:answer_id/answer_info`
Returns all data about one user submission id `answer_id` as a JSON

POST `/golf/task?name=<NAME>&desc_link=<DESC_LINK>&test_link=<TEST_LINK>`
Submit a task as a title and links `desc_link` and `test_link`

GET `/golf/:task_id/task_info?order=<ORDER>`
Returns all data about one task, including responses sorted by `<ORDER>`
Order is optional `latest`, `fastest`, `shortest` and is `fastest` by default
