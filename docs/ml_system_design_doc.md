# Дизайн документ
## 1. Зачем идем в разработку продукта?
### Бизнес-цель:
* Улучшить производительность языковых моделей (LLM) в задачах вопросов-ответов (QA), понимания текста (MRC) и работы с графами знаний (KGQA) для создания более точных и масштабируемых систем ИИ.
* Увеличение точности и уменьшение количества ошибок моделей за счет интеграции знаний из Knowledge Graphs (KG).
* Повышение конкурентоспособности продукта в сравнении с текущими решениями за счет улучшения интерпретируемости и контекстной релевантности.
### Почему станет лучше:
* Совмещение LLM и KG улучшит понимание модели, что приведет к повышению точности на 20-30% в зависимости от задачи.
* Бизнес получит возможность эффективно решать более сложные вопросы пользователей, требующие мульти-хопового или составного рассуждения.
### Что будем считать успехом:
* Увеличение точности ответов модели (accuracy) на 15%+ для QA/MRC/KGQA.
* Повышение скорости обработки вопросов без значительного увеличения вычислительных затрат.
* Успешное прохождение пилотного использования продукта в реальных условиях.
## 2. Бизнес-требования и ограничения
### Краткое описание бизнес-требований (БТ):
* Разработка мультизадачной системы на базе DRAGON с улучшенной производительностью для QA, MRC и KGQA.
* Ускорение процесса обработки вопросов с сохранением высокой точности.
* Возможность интеграции в существующие бизнес-процессы (например, платформы поддержки клиентов, образовательные системы).
### Бизнес-ограничения:
* Используем только англоязычные данные из-за сложности работы с мультиязычными графами знаний.
* Сроки пилота ограничены 2-3 месяцами.
### Ожидания от итерации:
* Повышение точности модели по ключевым задачам.
* Демонстрация работы на реальных данных из бизнес-сценариев.
### Бизнес-процесс пилота:
* Интеграция модели в существующую систему вопросов-ответов.
* Тестирование на реальных пользователях или примерах из базы знаний компании.
* Что считаем успешным пилотом:
* Достижение 70%+ точности на задачах QA, MRC и KGQA в реальных условиях.
* Положительные отзывы пользователей о работе системы.
### Критерии успеха:
* Точность выше установленного порога.
* Стабильность работы модели при увеличении нагрузки.
* Подготовка базы для масштабирования на новые языки.
## 3. Скоуп проекта
### Входит:
* Разработка мультизадачного фреймворка с объединением задач QA, MRC и KGQA.
* Обучение модели на датасетах CommonsenseQA, DREAM и KQA Pro.
* Подготовка к интеграции в пилотный процесс.
### Не входит:
* Мультиязычные данные.
* Расширение графов знаний за рамки ConceptNet/Wikidata.
### Результат с точки зрения кода:
* Воспроизводимая модель с открытым исходным кодом.
* Документация для интеграции в сторонние системы.
### Технический долг:
* Отложенные задачи по мультиязычной поддержке.
* Возможность улучшения качества генерации сложных вопросов.
## 4. Предпосылки решения
**Данные**: Используются данные из ConceptNet и BookCorpus для предварительного обучения, дополненные CommonsenseQA, DREAM и KQA Pro.
**Горизонт прогноза**: Прогнозируем производительность на 3-6 месяцев вперед.  
**Гранулярность модели**: Отвечает на вопросы с детализацией до сущностей Knowledge Graph.
## 5. Постановка задачи
### С технической точки зрения:
* Реализовать мультизадачную систему (multitask learning), обученную решать QA, MRC и KGQA.
* Интегрировать подходы к улучшению представления текстовых данных и структурированных данных (графов знаний).
* Использовать модели, основанные на RoBERTa-large, с поддержкой различных метрик потерь для каждой задачи.

![schema](/figs/schema.png)


