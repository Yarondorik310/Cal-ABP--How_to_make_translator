В этом проекте я хочу рассказать вам, как сделать перевод на разные языки в игре Cats are Liquid - A Better Place. Но для начала надо ознакомиться с тем, как это вообще работает.

У нас есть файлы, которые нам обязательно нужны, остальные не трогаем. Это ini-файл en-US.uilang, который находится по пути «Steam\steamapps\common\Cats are Liquid - A Better Place\CaL-ABP-Windows_Data\StreamingAssets\lang\en-US.uilang» и множество ini-файлов en-US.lang, коорые находятся по пути «Steam\steamapps\common\Cats are Liquid - A Better Place\CaL-ABP-Windows_Data\StreamingAssets\Official Maps\» а дальше в каждой папке 'Room' (Я прикрепил их чтобы даже те, у кого не было игры, могли делать перевод). en-US.uilang отвечает за весь текст в интерфейсе игры, а en-US.lang за субтитры в мирах. Если вы хотите сделать перевод, то вам понадобятся все эти файлы.

en-US.lang работает так: он создаёт переменную, которая означает какой-либо текст, а игра с помощью этих файлов переводит переменную в набор слов. Например:

	"STORY_1": "The cat had just arrived to this world.",
	"STORY_2": "It was built by her and her friends.",
	"STORY_3": "It was still incomplete.",
	"STORY_4": "But she knew how to fix that."

Название переменных изменять нельзя, а вот их значение можно как вздумается. Когда я делал перевод на русский язык, я сделал его так:

	"STORY_1": "Кошка только что появилась на свет.",
	"STORY_2": "Это место был построено ею и ее друзьями.",
	"STORY_3": "Оно все еще было незавершенным.",
	"STORY_4": "Но она знала, как это исправить."

(Вы можете делать перевод на любые другие языки, чтобы расширить аудиторию игры, но если вам интересен русификатор, вот ссылка: https://yarondorik.itch.io/cats-are-liquid-a-better-place-rus-local).

В этих файлах могут встречаться такие наборы символов, как '[1.2]' и '|'. [1.2] делает задержку в секундах между текстом до неё и после. А | переносит текст после неё на следующую стоку. Например:

	"STORY_1": "Everything still felt a bit dull.",
	"STORY_2": "Too[1.2] boxy.",
	"STORY_3": "The cat got another idea.",
	"STORY_4": "That’s better."

С переводом:

	"STORY_1": "Все по-прежнему казалось немного скучным.",
	"STORY_2": "Слишком[1.2] квадрантым.",
	"STORY_3": "Кошке пришла в голову другая идея.",
	"STORY_4": "Так-то лучше."

А с '|':

	"STORY_1": "The rooms were starting to get|a bit more difficult.",
	"STORY_2": "At least the consequences for failing|weren’t that bad.",
	"STORY_3": "The cat could just respawn.",
	"STORY_4": "And get right back to it."

И перевод:

	"STORY_1": "С комнатами становилось|немного сложнее.",
	"STORY_2": "По крайней мере, последствия неудачи|были не такими уж плохими.",
	"STORY_3": "Кошка могла просто возродиться.",
	"STORY_4": "И сразу же идти дальше."

Наконец, зная всё это, вы можете изменять текст и переводить его на другие языки.

Теперь изучим файл en-US.uilang. Он, как я вам уже сказал, переводит текст в самом интерфейсе игры. Этот файл тоже действует по принципу с переменными, но на этот раз их гораздо больше, и все они в одном en-US.uilang. В нём такое начало:

    "LANG_NAME": "English (US)",
    "LANG_NAME_ENGLISH": "English (US)",
    "LANG_CODE_IEFT": "en-US",

Его мы не трогаеи, а берём все значения переменных, что ниже. Там могут встречаться такие наборы символов, как '\n', '\n\n' и '%AMOUNT%'. \n - это переход на следующую строку, \n\n, как вы поняли на две строки, а %AMOUNT% переводить нельзя, это тоже переменная. Вот пример:

    "SHARESCREEN_CHECKSFAILED_LIST_ANDOTHERS": "and %AMOUNT% others.",

Перевод:

    "SHARESCREEN_CHECKSFAILED_LIST_ANDOTHERS": "и %AMOUNT% другие.",

\n:

    "LEVELSELECTSCREEN_PACKMENU": "P\nA\nC\nK\nS",

Перевод:

    "LEVELSELECTSCREEN_PACKMENU": "П\nА\nК\nИ",

\n\n:

    "INTRO_WARNING_DESCRIPTION": "This game contains flashing visuals that can be harmful to viewers with photosensitive epilepsy.\n\nThese visuals can be disabled in the settings menu.",

Перевод:

    "INTRO_WARNING_DESCRIPTION": "Эта игра содержит мигающие визуальные эффекты, которые могут быть опасны для зрителей с эпилепсией.\n\nЭти визуальные эффекты можно отключить в меню настроек.",

Наконец, зная всё это, вы можете изменять текст и переводить его на другие языки.



Если вы сделали перевод, вы можете его опубликовать, НО:
1. Вы должны указать этот сайт, чтобы другие, увидев ваш перевод, могли сделать другой свой, например: 'Сделано благодаря 'https://github.com/Yarondorik310/Cal-ABP--How_to_make_translator.git'', или по лубому другому способу.
2. Вам нужно упомянуть '@Yarondorik' рядом с ссылкой на этот сайт, чтобы другие могли знать, к кому, если что, обращаться, например: 'Сделано благодаря Yarondorik и 'https://github.com/Yarondorik310/Cal-ABP--How_to_make_translator.git''
Тепрь свободно распространяйте перевод и делайте игру и айдиторию Cats Are Liquid лучше!
