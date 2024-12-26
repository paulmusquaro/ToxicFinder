# toxic_finder

# Опис проекту ...

# Інструкції по установці і запуску застусунку ...

# Команда:
* П.Коржов - скрам майстер
* Т.Дзвінчук - тім лід
* М.Соболь - розробник
* М.Шотурма - розробник
* О.Лозовий - розробник
* О.Сазонець - розробник

# Структура проекту:
* README.md - документація проекту. Виконавець Т.Дзвінчук.
* requirements.txt - перелік залежностей для проекту. Виконавець Т.Дзвінчук, П.Коржов.
* train_data.ipynb - попередня обробка тренувальних даних. Виконавець О.Лозовий. Фінальний результат зберегти у файл train_data.csv
* test_data.ipynb - попередня обробка тестових даних. Виконавець О.Лозовий. Фінальний результат зберегти у файл test_data.csv
* train_data.csv - оброблені тренувальні дані, готові до передачі у моделі для навчання.
* test_data.csv - оброблені тестові дані для фінальної оцінки та вибору найкращої моделі. 
* model_1.ipynb, model_2.ipynb, model_3.ipynb, model_4.ipynb - альтернативні версій створення і навчання моделі. Створені і навчені моделі зберігаємо у файли model_1.h5, model_2.h5, model_3.h5, model_4.h5 відповідно. Виконавці - М.Соболь, Т.Дзвінчук, М.Сазонець, М.Шотурма
* model_1.h5, model_2.h5, model_3.h5, model_4.h5 - навчені моделі
* estimate.ipynb - оценка чотирьох моделей, візуалізація. Вибір моделі, що демонструє найкращі результати та збереження її у файл best_model.h5. Виконавець О.Сазонець
* best_model.h5 - найкраща модель
* app.py - застосунок для оцінки коментарів за рівнем токсичності. Виконавець М. Шорутма
* Dockerfile - файл для створення Docker-образу. Містить усі інструкції для встановлення залежностей, копіювання коду та запуску програми. Виконавець П.Коржов.
* docker-compose.yml - файл для автоматизації розгортання проекту в середовищі Docker. Містить опис сервісів, мереж та томів, необхідних для роботи. Виконавець П.Коржов.

***

# Системні вимоги

- Python 3.9
- 


## Покрокові Git команди для роботи з репозиторієм [toxic_finder](https://github.com/T-Dzv/toxic_finder.git)

Цей посібник допоможе вам покроково зрозуміти, як працювати з репозиторієм на GitHub. Почнемо з клонування репозиторію і завершимо створенням гілки та її завантаженням на віддалений репозиторій.


### 1. **Клонування репозиторію**
Це дозволить скопіювати репозиторій `toxic_finder` на ваш комп'ютер.

```bash
git clone https://github.com/T-Dzv/toxic_finder.git
```

- **Результат:** Локальна копія репозиторію буде створена в папці `toxic_finder`.


### 2. **Перехід у папку репозиторію**
Перейдіть у створену папку, щоб працювати з репозиторієм.

```bash
cd toxic_finder
```

- **Результат:** Ви тепер працюєте всередині репозиторію.


### 3. **Перевірка статусу репозиторію**
Перевірте поточний стан репозиторію (які файли змінені, чи є щось для коміту).

```bash
git status
```

- **Результат:** Ви побачите, чи є зміни або нові файли, які потрібно додати.


### 4. **Створення нової гілки**
Щоб працювати над окремим завданням чи функцією, створіть нову гілку.

```bash
git branch new_feature
```

- **`new_feature`:** Назва гілки (можете змінити на іншу, відповідно до вашої задачі).


### 5. **Перехід у нову гілку**
Після створення гілки перейдіть у неї.

```bash
git checkout new_feature
```

Або, починаючи з Git 2.23+, можна створити і перейти в нову гілку одночасно:

```bash
git switch -c new_feature
```

- **Результат:** Ви тепер працюєте в новій гілці.


### 6. **Внесення змін у проект**
- Редагуйте, додавайте або видаляйте файли в проєкті.
- Після внесення змін виконайте наступні кроки, щоб зберегти їх у Git.


### 7. **Додавання файлів до індексу**
Додайте змінені або нові файли до індексу (staging area).

```bash
git add .
```

- **`git add .`:** Додає всі змінені файли.
- **Альтернативно:** Можна додати конкретний файл:
  ```bash
  git add filename
  ```


### 8. **Створення коміту**
Збережіть ваші зміни в історії гілки.

```bash
git commit -m "Додано нову функцію"
```

- **`-m "Додано нову функцію"`:** Короткий опис змін.


### 9. **Перевірка гілок**
Перевірте, в якій гілці ви зараз перебуваєте, та перелік усіх доступних гілок.

```bash
git branch
```

- **Результат:** Поточна гілка буде позначена зірочкою `*`.


### 10. **Завантаження гілки на віддалений репозиторій**
Щоб завантажити нову гілку на GitHub, скористайтеся командою:

```bash
git push origin new_feature
```

- **`origin`:** Це стандартна назва віддаленого репозиторію.
- **`new_feature`:** Назва вашої гілки.


### 11. **Створення Pull Request (PR) на GitHub**
1. Відкрийте репозиторій на GitHub: [toxic_finder](https://github.com/T-Dzv/toxic_finder.git).
2. Перейдіть у вкладку **Pull Requests**.
3. Натисніть **New Pull Request**.
4. Виберіть вашу гілку `new_feature` для злиття в основну гілку (зазвичай `main`).
5. Додайте опис змін і натисніть **Create Pull Request**.

***

## Додаткові корисні команди

#### Відправити зміни до існуючої гілки
Якщо вже створили гілку на GitHub і хочете лише оновити її:

```bash
git push
```

#### Перейти на гілку `main`
```bash
git checkout main
```
#### Команда, що оновить ваш локальний репозиторій останніми змінами з `main` із віддаленого репозиторію
```bash
git pull origin main
```

#### **Скасувати останній коміт, але зберегти зміни в індексі (staging area):**
Якщо ви хочете скасувати коміт і залишити файли готовими для повторного коміту:

```bash
git reset --soft HEAD~1
```

- **`HEAD~1`** означає "останній коміт".
- **Результат:** зміни залишаться в індексі (`staging area`), і ви зможете зробити новий коміт.


#### **Скасувати останній коміт і повернути зміни в робочу директорію:**
Ця команда знімає зміни з індексу і повертає їх до робочої директорії:

```bash
git reset --mixed HEAD~1
```

- **Результат:** зміни повернуться до робочої директорії, але не будуть у staging.



#### **Скасувати останній коміт і видалити всі зміни (небезпечний варіант):**
Це скасовує останній коміт і повністю видаляє всі внесені зміни:

```bash
git reset --hard HEAD~1
```

- **Увага:** Використовуйте цю команду обережно, оскільки зміни буде втрачено назавжди.



#### **Скасувати певний коміт у середині історії:**
Якщо вам потрібно скасувати конкретний коміт (наприклад, серед попередніх), використовуйте:

```bash
git revert <commit_hash>
```

- Замість `<commit_hash>` вкажіть хеш коміту, який потрібно скасувати (знайдіть його через `git log`).
- **Результат:** Git створить новий коміт, який скасує зміни з обраного коміту.


#### **Скасувати останній коміт, якщо він уже завантажений на віддалений репозиторій:**
Якщо ви вже зробили `git push`, то:

1. Скасуйте коміт локально (будь-який з варіантів вище).
2. Завантажте зміни на сервер із примусовим перезаписом:

   ```bash
   git push origin branch_name --force
   ```

   (Замість `branch_name` вкажіть вашу гілку, наприклад, `main` або `feature_branch`.)


#### **Переглянути історію комітів:**
Щоб знайти потрібний коміт для скасування, скористайтеся:

```bash
git log
```

- Для короткого формату:

  ```bash
  git log --oneline
  ```

***

## Conda (Налаштування та Віртуальне середовище)

Щоб зробити проєкт відтворюваним і забезпечити зручне управління пакетами, у цьому проєкті використовується Conda як менеджер пакетів і середовища (бажано щоб на вашому диску `C` було не менше 20 гігабайт). Нижче наведені кроки для налаштування середовища:



1. **Встановіть Conda:** Якщо Conda ще не встановлена, ви можете завантажити її з офіційного сайту [Anaconda](https://www.anaconda.com/products/individual):

    - Перейдіть за посиланням;
    - Впишіть ваш gmail;
    - Натисніть кнопку Submit;
    - Перейдіть на пошту що вказали;
    - Оберіть відповідний Anaconda Installer (якщо тут наприклад пише Python 3.12 або інший який у вас встановлений локально, не зважайте на це взагалі);
    - Запустіть завантажений `.exe` файл з правами адміністратора;
    - Під час встановлення ніякі галочки не тиснемо, все залишаємо як є;
    - Після завантаження запуститься ANACONDA.NAVIGATOR, але він нам не потрібен, його можна просто закрити;

    - Все, `conda` має бути додана в `PATH`, щоб це перевірити, відкрийте звичайну командну строку та виконайте наступну команду: `conda --version`
    - Якщо все добре, має вивистись версія `conda`, але якщо пише щось по типу що команду не розпізнано, значить `conda` не було додано в `PATH`, і вам треба зробити це вручну.


2. **Створіть нове середовище:** Після того як ви вже склонували репозиторій, відкрийте термінал у відповідній дерикторії з проектом і виконайте наступну команду, щоб створити нове середовище Conda з Python 3.9:

    ```bash
    conda create --name new_conda_env python=3.9
    ```


3. **Активуйте середовище:** Після створення середовища активуйте його за допомогою команди:

    ```bash
    conda activate new_conda_env
    ```


4. **Встановіть необхідні пакети:**

    ```bash
    conda install jupyter numpy matplotlib seaborn pandas scikit-learn tensorflow keras transformers
    ```


5. **Запустіть Jupyter Notebook:**

    ```bash
    jupyter notebook
    ```


**Наступного разу під час роботи з проектом, буде достатньо виконати лище команди №3 та №5**
