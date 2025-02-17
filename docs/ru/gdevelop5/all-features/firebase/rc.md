---
title: настройка с помощью Firebase
---
#Удаленная настройка с помощью Firebase 

!!! tip

    Перед использованием любой функции Firebase не забудьте [настроить его правильно с помощью краткого руководства](/ru/gdevelop5/all-features/firebase/quickstart).

Firebase RC (сокращение от Remote Configuration) позволяет создавать [переменные](/gdevelop5/ all-features/ variables), которые можно изменять в панели управления Firebase без необходимости обновлять игру.
Вы также можете изменить их для определенной группы людей.
Например, вы можете изменить цену на что-то в магазине для активных пользователей удаленно во время проведения рекламной акции.
Вы также можете использовать это для удаленного включения и отключения экспериментальных функций, если они слишком нестабильны и их требуется отключить,
без необходимости публиковать обновление с исправленной настройкой.
!!! note

    Указание групп людей может потребовать аутентификацию и аналитику, чтобы Firebase могла различать группы игроков.

## Подготовка

В этой статье объясняется, как установить RC в проект и как это использовать.
Вот с чего мы начинаем:
![](/gdevelop5/all-features/firebase/rc1.png)
![](/gdevelop5/all-features/firebase/rc2.png)

Это простой кликер где вы можете получать и тратить деньги. Теперь мы можем начать добавлять RC для динамической настройки.

## Добавление значений по умолчанию

Прежде всего, мы должны установить некоторые значения по умолчанию.
Эти значения по умолчанию должны содержать значение по умолчанию для каждой из настраиваемых переменных.
Они используются, когда нет сети для обновления значения переменных или когда они еще не завершили загрузку.

!!! warning
    
        
    Это не обязательный шаг, но всё же рекомендуется это сделать, чтобы избежать ошибки у игроков у которых конфигурация ещё не загрузилась или у игроков у которых нету доступа к интернету.
    

Мы можем сделать это, создав структуру, содержащую значения по умолчанию:
![](/gdevelop5/all-features/firebase/rc3.png)
А затем установив его по умолчанию:
![](/gdevelop5/all-features/firebase/rc4.png)
Как видите, в этом примере мы используем 2 переменные: одну, чтобы решить, сколько денег вы выиграете, а другую - сколько вы проиграете при нажатии кнопок.

## Настройка Firebase

Теперь нам нужно также настроить Firebase. Перейдите на панель инструментов приложений, а затем на удаленную настройку:
![](/gdevelop5/all-features/firebase/rc5.png)
Теперь вы можете установить некоторые переменные. Установите те, которые вы назначили по умолчанию:
![](/gdevelop5/all-features/firebase/rc6.png)
!!! danger
    
        
    Не забудьте сохранить изменения!
    ![](/gdevelop5/all-features/firebase/rc7.png)
    

## Добавление синхронизации

Это расширение позволяет вам управлять синхронизацией удаленной конфигурации, как вы хотите.
Лучше всего использовать действие «принудительная синхронизация» для события, которое будет происходить регулярно.
Для этого вы можете использовать таймер или сделать это в начале сцены, на которую часто переключают.

!!! danger
    
        
    Хотя вы, вероятно, хотите часто синхронизировать конфигурацию, не синхронизируйте ее слишком часто!
    В противном случае Firebase отключит вас по тайм-ауту, чтобы предотвратить DDoS-атаки по всем выполненным запросам.
    

!!! note
    
        
    Вы также можете использовать действие «установить интервал автоматического обновления», но, согласно некоторым тестам, оно не очень надежно.
    

Мы можем, например, использовать здесь нажатия кнопок, поскольку они будут происходить часто, но не слишком часто:
![](/gdevelop5/all-features/firebase/rc8.png)

## Замените статические значения конфигурацией

Теперь нам просто нужно заменить ранее статические значения на значения из удаленной конфигурации:
![](/gdevelop5/all-features/firebase/rc9.png)

### Адаптируйте остальную игру к модульности

Не забывайте, что некоторые вещи, которые могли быть статичными, теперь являются динамическими, и для поддержки этой модульности необходимо добавить некоторые действия.
В нашем примере был статический текст, показывающий, сколько денег вы теряете, покупая «зелья». Теперь вы можете обновить этот текст, чтобы показать правильное значение:
![](/gdevelop5/all-features/firebase/rc10.png)

## Используйте консоль Firebase, чтобы изменить значения

Теперь вы должны закончить настройку.
Вам нужно только изменить значения в консоли Firebase, чтобы увидеть, как они обновляются в реальном времени (или, точнее, всякий раз, когда игра синхронизирует удаленную конфигурацию) в вашей игре.