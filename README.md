База данных моих скромных рецептов. Зачем это?
1) Прикольно. Готовка бывает веселой, особенно если готовит Гордон Рамзи.
2) Чтобы в чём-то разобраться, надо a) своими словами мочь рассказать, b) обдумать основные проблемы - суть дела, c) разобраться почему основные моменты вообще стали таковыми (т.е. понять причины их появления, эволюционная ретроспектива) и d) используя имеющие знания, закрепить их, реализуя нечто тебе приятное и их включающее.
Значит чтобы получше в SQL стать, надо настругать таблички и позаполнять их.  

Таковыми табличками, под управлением базы данных, будут составляющие процесса приготовления.  
На важный самостоятельный объект будет создаваться своя таблица.  

Что это за объекты?  
Рецепт включает: ингредиенты, время готовки, последовательность шагов (что с ингредиентами делают).  
Значит ингредиенты помещаются в отдельную таблицу (1).  
Последовательность шагов - отдельная таблица - это импровизированная кулинарная книга (2).  
Теперь, что пишется в рецепте - например, взяли мясо (ингредиент (1)) и отбили его или порезали. Но что ж получается, надо ручками в каждую строку подобное писать? А если ошибки будут или решишь по-другому   назвать, то возникнет хаос! Как потом из этого общую информацию извлекать?! Для систематизации декомпозируем шаги готовки и выделим из них группы с общими свойствами, которые станут нашими новыми объектами.  
Получаем такие объекты как духовка (3), плита (4), мультиварка (5), холодная готовка (6) - сюда относятся всякие отбивание, промывания, нарезания, в общем что выполняется человеком, микроволновка (7).  
Затем надо как-то систематизировать сами ингредиенты, у них же тоже общие свойства есть. Таким образом появляется таблица тип ингредиентов (8), в которой содержатся такие вещи как специи, мясо, овощи, рыба и т.д..
Всё это в качестве внешних ключей попадёт в таблицу рецепт (9), каждый из которых имеет своё собственное название, например, мясо по-французски. Но у каждого рецепта есть и свой скромный автор (10).  
Также 
