# Путевая точка

!["В этом направлении!" - "Нет, в этом!"](oredict:oc:waypoint)

Главное не что это такое, а как это использовать. [Навигационное улучшение](../item/navigationUpgrade.md) может обнаруживать путевые точки, что позволяет устройствам с этим улучшением ориентироваться в игровом мире. Это можно использовать для написания программ для [роботов](robot.md) и [дронов](../item/drone.md).

Обратите внимание, что актуальным местоположением считается *блок перед путевой точкой* (выделен с помощью частиц), именно это местоположение будет передано, при запросе его навигационным улучшением. Это позволяет поместить путевую точку рядом или над сундуком и позволит обратиться к путевой точке "над сундуком", без необходимости вращения самой точки.

Путевая точка имеет два параметра, которые могут быть использованы при ее опросе навигационным улучшением: уровень редстоун-сигнала, который получает точка и изменяемое имя. Имя это строка, состоящая из 32 символов, оно может быть изменено через интерфейс или через API. Эти два параметра могут быть использованы устройством, для определения, что можно сделать с путевой точкой. Например, сортировочная программа может использовать блоки с высоким уровнем редстоун-сигнала как входные, а с низким как выходные.