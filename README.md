# Компілятор F#, базова бібліотека F#, та інструменти редагування Ф#
[![Build Status](https://dev.azure.com/dnceng-public/public/_apis/build/status/dotnet/fsharp/fsharp-ci?branchName=main)](https://dev.azure.com/dnceng-public/public/_build/latest?definitionId=90&branchName=main)
[![Help Wanted](https://img.shields.io/github/issues/dotnet/fsharp/help%20wanted?style=flat-square&color=%232EA043&label=help%20wanted)](https://github.com/dotnet/fsharp/labels/help%20wanted)

Ця гілка для роботи над локалізованою версією F#.
Мета цього єксперіменту створити 

- [ ] Створити локалізовану мову програмування
    - [x] Пропонувати переклад ключових слів
    - [ ] Пропонувати переклад псевдо-ключових слів таких як async/None/Some/int/float
    - [ ] Зробити приклади базових мовних конструкцій
    - [ ] Створити локалізовану на українську мову базову бібліотеку
- [ ] Створити локалізовани інструменти редагування
    - [ ] Візуал Студія
      - [x] Розробка
      - [ ] Упакування
    - [ ] Іонід
      - [ ] Розробка
      - [ ] Упакування
    - [ ] Райдер
      - [ ] Розробка
      - [ ] Упакування
    - [x] .NET Polyglot Notebooks
      - [x] [Розробка](https://github.com/kant2002/fsharp-kernel-ua)
      - [x] [Упакування](https://www.nuget.org/packages/DotNetInteractive.FSharp.Ukrainian)
- [ ] Перекласти декілька відомих проектів на українську
    - [ ] Мати можливість роботи с консолью
    - [ ] Мати можливість робити запроси до веб
    - [ ] Мати можливість роботи з файлами
    - [ ] Мати можливість роботи з базами даних
    - [ ] Мати можливість створення десктопних програм
    - [ ] Мати можливість створення веб-додатків

Лише частина роботи буде розміщена у цьому репозіторії, інші частини роботи будуть проводиться у форках відповідних проектів.

Ми запрошуємо вас зробити внесок у майбутні випуски Ф# компілятра, базової біблітеки, та інструментів. Розробка цього репозіторія може проводитися на будь якій ОС яка підтримує [.NET](https://dotnet.microsoft.com/).

Ви також повинні мати встановлений .NET 7 SDK [звідси](https://dotnet.microsoft.com/download/dotnet/7.0).

## Нащо ций діалект

Коли я створював цей діалект моя мотивація була полегшити перші місяці(або роки) навчання програмуванню та процедурному мисленню. За свою кар'єру, я дуже часто бачив помилки коли
люди плутали цілі використання тієї, чи іншої концепції у програмуванні. Я вважаю що це на сам перед тому що коли люди вчаться програмуванню, вони вчать англійску мову 
водночас, потім вони читають статі на англійскій, і використовують сленг. Як на мене це робить навчання не англомовним людям більш важким, і якщо людина із социально-вразливого
шару суспільства, це додає що один бар'єр, яких як на мене і так забагато. Наприклад є Scratch, має безліч перекладів на інші мови, чому ми не можемо зробити так 
само із мовами програмування? Також я не можу відкинути аргументи що навчатися краще якійсь індустріальній мові. Саме тому (а також тому що це було відносно легко зробити) з'явився цей діалект F# 
де ви можете писати як на F# або цілком на українскій.

## Внести вклад

### Швидкий старт на Windows

Збудувати із командної строки:

```shell
build.cmd
```

The build depends on an installation of Visual Studio. To build the compiler without this dependency use:

```shell
build.cmd -noVisualStudio
```

Після того як збудова завершена, відкрийте або `FSharp.sln` або `VisualFSharp.sln` у редакторі на ваш смак. Остання рішення більше але воно включає Ф# інструменти для Visual Studio та супутню інфраструктуру.

### Швидкий старт на Linux або macOS

Збудувати із командної строки:

```shell
./build.sh
```

Після того як збудова завершена, відкрийте `FSharp.sln` у редакторі на ваш смак.

### Документація для співвкладників

* The [Compiler Documentation](docs/index.md) is essential reading for any larger contributions to the F# compiler codebase and contains links to learning videos, architecture diagrams and other resources.

* The same docs are also published as the [The F# Compiler Guide](https://fsharp.github.io/fsharp-compiler-docs/). It also contains the public searchable docs for FSharp.Compiler.Service component.

* See [DEVGUIDE.md](DEVGUIDE.md) for more details on configurations for building the codebase. In practice, you only really need to run `build.cmd`/`build.sh`.

* See [TESTGUIDE.md](TESTGUIDE.md) for information about the various test suites in this codebase and how to run them individually.

### Докуметація для Ф# громади

* [The F# Documentation](https://learn.microsoft.com/dotnet/fsharp/) is the primary documentation for F#. The source for the content is [here](https://github.com/dotnet/docs/tree/main/docs/fsharp).

* [The F# Language Design Process](https://github.com/fsharp/fslang-design/) is the fundamental design process for the language, from [suggestions](https://github.com/fsharp/fslang-suggestions) to completed RFCs.  There are also [tooling RFCs](https://github.com/fsharp/fslang-design/tree/main/tooling) for some topics where cross-community co-operation and visibility is most useful.

* [The F# Language Specification](https://fsharp.org/specs/language-spec/) is an in-depth description of the F# language. This is essential for understanding some behaviors of the F# compiler and some of the rules within the compiler codebase. For example, the order and way name resolution happens is specified here, which greatly impacts how the code in Name Resolutions works and why certain decisions are made.

### Змінені ключові слова

Нижче приведени приклади змінених ключових слів. Італіком відзначені слова, переклад яких є сумнівним.

| F# | Ф# |
| -------- | ---------- |
| abstract | абстрактний |
| and | та |
| as | як |
| assert | ствердити |
| asr | -- |
| base | база |
| begin | *початок* | 
| class | клас |
| const | конст |
| default | *замовчання* |
| delegate | делегат |
| do | зробити |
| done | зроблено |
| downcast | -- |
| downto | -- |
| elif | інякщо |
| else | інакше |
| end | кінець |
| exception | виключення |
| extern | зовнішній |
| false | ложь |
| finally | востаннє |
| fixed | *фіксовано* |
| for | для |
| fun | фун |
| function | функція |
| global | глобальний |
| if | якщо |
| in | у |
| inherit | успадкує |
| inline | інлайн |
| interface | інтерфейс |
| internal | внутрішній |
| land | -- |
| lazy | ледачий |
| let | нехай |
| lor | -- |
| lsl | -- |
| lsr | -- |
| lxor | -- |
| match | *відповідає* |
| member | *член* |
| mod | мод |
| module | модуль |
| mutable | змінливий |
| namespace | простір |
| new | *новий* |
| null | *нуль* |
| of | *з* |
| open | відкрити |
| or | або |
| override | перевизначити |
| private | приватний |
| public | відкритий |
| rec | рек |
| return | повернути |
| sig | сіг |
| static | статичний |
| struct | структ |
| then | тоді |
| to | до |
| true | істина |
| try | спробувати |
| type | тип |
| upcast | -- |
| use | вживати |
| val | знач |
| void | пусто |
| when | коли |
| while | доки |
| with | із |
| yield | поступатися |

Приклади над якими треба розмірковувати як перекласти ключові слова.

```
type x with
	member this.test(name: string) = 
		match name with
			| "1" -> true
			| _ -> false
```

### Тестові проєкти

- [ВеселШарп](https://github.com/kant2002/FunSharp) Весела кросс-платформенна графична біблиотека, базуючаяся на библиотеці із Small Basic, зроблена спеціально для Ф# та C#.

### Ніякий вклад не замалий

Якщо ви знайдете навіть опечатку з одної літери, ми раді прийняти зміни! Навіть якщо кодова база може виглядати лячною для початківців, ми та інші співвкладники будемо раді допомогти вам і надалі.

## Per-build NuGet packages

Per-build [versions](https://dev.azure.com/dnceng/public/_packaging?_a=package&feed=dotnet-tools&view=versions&package=FSharp.Compiler.Service&protocolType=NuGet) of our NuGet packages are available via this URL: `https://pkgs.dev.azure.com/dnceng/public/_packaging/dotnet-tools/nuget/v3/index.json`

## Branches

These are the branches in use:

* `main`
  * Almost all contributions go here.
  * Able to be built, installed and used in the latest public Visual Studio release.
  * May contain updated F# features and logic.
  * Used to build nightly VSIX (see above).

* `release/dev15.9`
  * Long-term servicing branch for VS 2017 update 15.9.x. We do not expect to service that release, but if we do, that's where the changes will go.

* `release/dev17.x`
  * Latest release branch for the particular point release of Visual Studio.
  * Incorporates features and fixes from main up to a particular branch point, then selective cherry-picks.
  * May contain new features that depend on new things or fixes in the corresponding forthcoming Visual Studio release.
  * Gets integrated back into main once the corresponding Visual Studio release is made.

## F# language and core library evolution

Evolution of the F# language and core library follows a process spanning two additional repositories. The process is as follows:

1. Use the [F# language suggestions repo](https://github.com/fsharp/fslang-suggestions/) to search for ideas, vote on ones you like, submit new ideas, and discuss details with the F# community.
2. Ideas that are "approved in principle" are eligible for a new RFC in the [F# language design repo](https://github.com/fsharp/fslang-design). This is where the technical specification and discussion of approved suggestions go.
3. Implementations and testing of an RFC are submitted to this repository.

## License

This project is subject to the MIT License. A copy of this license is in [License.txt](License.txt).

## Code of Conduct

This project has adopted the [Contributor Covenant](https://contributor-covenant.org/) code of conduct to clarify expected behavior in our community. You can read it at [CODE_OF_CONDUCT](CODE_OF_CONDUCT.md).

## Get In Touch

Members of the [F# Software Foundation](https://fsharp.org) are invited to the [FSSF Slack](https://fsharp.org/guides/slack/). You can find support from other contributors in the `#compiler` and `#editor-support` channels.

Additionally, you can use the `#fsharp` tag on Twitter if you have general F# questions, including about this repository. Chances are you'll get multiple responses.

## About F\#

If you're curious about F# itself, check out these links:

* [What is F#](https://learn.microsoft.com/dotnet/fsharp/what-is-fsharp)
* [Get started with F#](https://learn.microsoft.com/dotnet/fsharp/get-started/)
* [F# Software Foundation](https://fsharp.org)
* [F# Testimonials](https://fsharp.org/testimonials)
