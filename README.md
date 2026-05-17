# pandas_data_engineering-21
data preprocessing and optimization with pandas
🚗 Pandas Data Engineering — School 21
Буткемп по анализу и обработке данных на Python. Реальный датасет автомобилей, штрафов и логов активности пользователей.
📋 Описание
Практические задания по работе с данными: загрузка из разных форматов, очистка, агрегации, обогащение и оптимизация производительности pandas.
📁 Структура проекта
├── data/
│   ├── auto.json          # Данные об автомобилях (725 записей)
│   ├── fines.csv          # Штрафы водителей (930 записей)
│   ├── owners.csv         # Владельцы автомобилей
│   └── feed-views.log     # Логи активности пользователей (1072 события)
│
├── notebooks/
│   ├── load_and_save.ipynb      # Загрузка и сохранение данных
│   ├── basic_operations.ipynb   # Базовые операции с DataFrame
│   ├── selects_n_aggs.ipynb     # Выборки и агрегации
│   ├── preprocessing.ipynb      # Предобработка и очистка данных
│   ├── enrichment.ipynb         # Обогащение данных
│   └── optimizations.ipynb      # Оптимизация производительности
🔧 Темы и навыки
Загрузка данных (load_and_save)

pd.read_csv с параметрами: sep, skiprows, skipfooter, index_col
Чтение tab-separated и semicolon-separated файлов
Сохранение в CSV с кастомным разделителем

Предобработка (preprocessing)

Удаление дубликатов: drop_duplicates(subset=[...])
Работа с пропусками: dropna, ffill, fillna(mean)
Парсинг строк: apply(lambda x: x.split()[0])
Чтение JSON: pd.read_json(orient='records')

Оптимизация памяти (optimizations)

Сравнение скорости итераций: loop vs iterrows vs apply vs vectorization vs numpy
Результат: numpy в 900x быстрее обычного цикла
Downcasting: float64 → float32, int64 → uint8/uint16
Категориальные типы: object → category (снижение памяти с 182 KB до 61 KB — в 3x)

Агрегации (selects_n_aggs)

groupby, agg, pivot_table
Фильтрация и выборки

Обогащение данных (enrichment)

Объединение таблиц: merge, join
Работа с временными рядами
🚀 Запуск
bash
git clone https://github.com/твой-ник/pandas-s21
cd pandas-s21
pip install pandas numpy jupyter
jupyter notebook
📚 Контекст
Проект выполнен в рамках буткемпа по Data Science в School 21 (Школа 21) — образовательный проект Сбербанка на основе методологии École 42.
