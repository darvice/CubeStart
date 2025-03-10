<h1 align="center">
  <img src="images/banner.svg" alt="Cube Api"/>
  CubeStart
  <br/>
</h1>

<p align="center">
    CLI приложение, которое поможет вам играть в актуальные версии сборок  CubeStudio. <i>Использует Cube-API</i>
</p>

## Что это такое и зачем?

CubeStart - CLI приложение, которое предлагает вам возможность играть в Сезоны CubeStudio с модами, не задумываясь об обновлении их до актуальной версии, оптимизации сборки, переносе конфигов.

## Как это работает?

CubeStart работает совместно с [Cube-API](https://github.com/fadegor05/Cube-API), который передает скомпилированный образ текущей сборки с помощью принципа Restful API, затем CubeStart сравнивает файлы скомпилированный сборки и текущей сборки, а затем обрабатывая эти данные, производит изменения в локальной сборке: скачивает файлы, удаляет их, копирует.

## Как пользоваться CubeStart?

Для начала вам необходимо установить CubeStart себе на устройство, затем запустите его любым удобным для вас способом, например ```.exe``` файлом. Затем откройте данное приложение. Когда вас попросят ввести папку до сборки, создайте в вашем лаунчере сборку с необходимой версией Minecraft и загрузчиком модов, далее укажите путь до созданной лаунчером папки со сборкой. Теперь CubeStart подключиться к Cube-API, если же возникнут проблемы с подключением, то проверьте настройки Брандмауэра, если это не помогло, то скорее всего проблемы на стороне сервера, либо указан неправильный URL-адрес API в ```config.json```, текущий адрес можно узнать у админа CubeStudio. CubeStart сам совершит необходимые действия в директории сборки, чтобы привести ее к актуальному состоянию. Если у вас есть свои моды, которые вы хотите поставить в сборку, то их нужно переместить в папку ```custom_mods```, созданную CubeStart в директории со сборкой. После добавления своих модов, будет необходимо открыть CubeStart, для добавления их в сборку (ВАЖНО, свои моды не нужно удалять после добавления в сборку, иначе они будут убраны из сборки). Также перед каждым входом на сервер стоит открывать CubeStart для поддержания актуальности вашей сборки.

## Последний релиз: 0.1
* Первый запуск и билд приложения ✨
* Доступны базовые функции по обновлению 💼
* Реализована функция для своих модов, используя папку ```custom_mods``` 💫

## Дорожная карта CubeStart
* [X] Первый запуск приложения 🌟
* [X] Возможность обновления, удаления, загрузки модов 🛠️
* [X] Возможность добавления своих, кастомных модов в сборку путем отдельной папки ```custom_mods``` в директории сборки 📂
* [X] Создание .exe файла приложения ⚒️
* [X] Кроссплатформенность (Windows, Linux) 📺
* [ ] Добавить возможность обновления конфигов и других файлов в сборке 💫
* [ ] Добавить возможность авто-загрузки готовых профилей в разные лаунчеры (MultiMC, PrismLauncher, Modrinth App, CurseForge Launcher, TLauncher Legacy) 🍀
* [ ] Реализовать автозапуск сборки после завершения обновлений CubeStart ⚙️
* [ ] Добавить возможность поддержки сразу нескольких обновляемых сборок одновременно (зависит от Cube-API) 🗃️
* [ ] Реализация модульности сборок (отключение некоторых компонентов по выбору, и наоборот добавление некоторых компонентов по желанию) 🎯

## Зависимости
* ```gson```, version = 2.10.1
* ```unirest```, version = 1.4.9
* ```jfiglet```, version = 0.0.9
* ```progressbar```, version = 0.10.0

## Файл конфигурации config.json
```
{
  "instance_id":0, // ID текущей установленной сборки (Не трогать!)
  "instance_version":"0.0.3", // Текущая версия установленной сборки (Не трогать!)
  "instance_directory":"/home/fadegor05/.local/share/PrismLauncher/instances/1.20.1/.minecraft", // Путь до директории вашей сборки
  "apiUrl":"http://cubeshield.ru:8000/api/v1" // Адрес Cube-API (Не изменяйте параметр, если не знаете, что вы делаете!)
}
```

## Полезные ссылки
* Телеграм-канал CubeStudio: https://t.me/+Gphg_BIJEdMwMmFi

###### Not an official Minecraft product. We are in no way affiliated with or endorsed by Mojang Synergies AB, Microsoft Corporation or other rightsholders.