# Проект 4. Задача классификации клиентов банка

## Оглавление  
[1. Описание проекта](.README.md#Описание-проекта)  
[2. Какой кейс решаем?](.README.md#Какой-кейс-решаем)  
[3. Краткая информация о данных](.README.md#Краткая-информация-о-данных)  
[4. Этапы работы над проектом](.README.md#Этапы-работы-над-проектом)  
[5. Результат](.README.md#Результат)    
[6. Выводы](.README.md#Выводы) 

### Описание проекта    
Вам предоставили данные о последней маркетинговой кампании, которую проводил банк: задачей было привлечь клиентов для открытия депозита. Вы должны проанализировать эти данные, выявить закономерность и найти решающие факторы, повлиявшие на то, что клиент вложил деньги именно в этот банк. Если вы сможете это сделать, то поднимете доходы банка и поможете понять целевую аудиторию, которую необходимо привлекать путём рекламы и различных предложений.

:arrow_up:[к оглавлению](_)


### Какой кейс решаем?    
Бизнес-задача: определить характеристики, по которым можно выявить клиентов, более склонных к открытию депозита в банке, и за счёт этого повысить результативность маркетинговой кампании.

Техническая задача для вас как для специалиста в Data Science: построить модель машинного обучения, которая на основе предложенных характеристик клиента будет предсказывать, воспользуется он предложением об открытии депозита или нет.

**Наши основные цели:**  
- Исследование данных, а не просто вычисление метрик и создание визуализаций.
- Попробовать выявить характерные черты для потенциальных клиентов, чтобы чётко очертить ЦА и увеличить прибыль банка.
- Использовать разные инструменты для повышения качества прогноза

**Метрика качества**     
Результаты оцениваются метриками классификации accuracy, precision и f1-score


### Краткая информация о данных
<p>Данные о клиентах банка:

- age (возраст);
- job (сфера занятости);
- marital (семейное положение);
- education (уровень образования);
- default (имеется ли просроченный кредит);
- housing (имеется ли кредит на жильё);
- loan (имеется ли кредит на личные нужды);
- balance (баланс).
<br /><br /> Данные, связанные с последним контактом в контексте текущей маркетинговой кампании:

- contact (тип контакта с клиентом);
- month (месяц, в котором был последний контакт);
- day (день, в который был последний контакт);
- duration (продолжительность контакта в секундах).
<br /><br /> Прочие признаки:

- campaign (количество контактов с этим клиентом в течение текущей кампании);
- pdays (количество пропущенных дней с момента последней маркетинговой кампании до контакта в текущей кампании);
- previous (количество контактов до текущей кампании)
- poutcome (результат прошлой маркетинговой кампании).<br /><br />
И, разумеется, наша целевая переменная deposit, которая определяет, согласится ли клиент открыть депозит в банке. Именно её мы будем пытаться предсказать в данном кейсе.</p>
  
:arrow_up:[к оглавлению](.README.md#Оглавление)


### Этапы работы над проектом  
Проект будет состоять из пяти частей:

1. Первичная обработка данных

В рамках этой части нам предстоит обработать пропуски и выбросы в данных. Это необходимо для дальнейшей работы с ними.

2. Разведывательный анализ данных (EDA)

Нам необходимо будет исследовать данные, нащупать первые закономерности и выдвинуть гипотезы.

3. Отбор и преобразование признаков

На этом этапе мы перекодируем и преобразуем данные таким образом, чтобы их можно было использовать при решении задачи классификации. Если на первом этапе мы лишь избавили данные от ненужных артефактов, то на этом шаге совершим действия, более важные для подготовки данных к задаче классификации, уже понимая их структуру.

4. Решение задачи классификации: логистическая регрессия и решающие деревья

На данном этапе мы построим свою первую прогностическую модель и оценим её качество. Научимся подбирать оптимальные параметры модели для того, чтобы получить наилучший результат для конкретного алгоритма.

5. Решение задачи классификации: ансамбли моделей и построение прогноза

:arrow_up:[к оглавлению](.README.md#Оглавление)


### Результаты:  

Метрика accuracy(доля правильных ответов) на финальной модели составила 0.83, что является очень хорошим показателем качества модели.
Способность отделять клиентов, которые наверняка откроют депозит от отказавшихся (метрика precision) составила также - 0.83
И комбинация двух метрик Precision и Recall, то есть метрика f1-score составила также 0.83
:arrow_up:[к оглавлению](.README.md#Оглавление)


### Выводы:  

- Мы использовали большое количество алгоритмов машинного обучения для итогового предсказания откроет клиент свой депозит в банке или нет. Среди них самыми эффективными в плане качества оказались Стэкинг, Случайный Лес с оптимизированными гиперпараметрами через Optuna и в конце имплементация градиентного бустинга от Яндекса CatBoost. Все эти алгоритмы дают одинаково хороший показатель accuracy при правильной настройки гиперпараметры.


:arrow_up:[к оглавлению](.README.md#Оглавление)


Если информация по этому проекту покажется вам интересной или полезной, то я буду очень вам благодарен, если отметите репозиторий и профиль ⭐️⭐️⭐️-дами