# EN

## MediaCutters
The repository offers two GNU/Linux Bash scripts to simplify time-based video/audio parts deletion via ffmpeg. 
To use them ensure that the following dependencies are installed:
- ffmpeg
- libglib2.0-bin or an alternative containing gio executable (to move input files to Trash after processing)

Scripts are designed to operate as follows:
1. Open terminal in a directory containing video or audio files to cut/trim.
2. Type &lt;script name&gt; &lt;start time&gt; &lt;end time&gt; &lt;file name&gt; replacing parameters in brackets with actual values. Pro tip: use can use Tab for filename autocompletion.
3. The original file is deleted and replaced with a new one ending with `.cut` suffix before an extension.

## cutm Script
The script is intended for deleting the middle part in a media file based on provided start time, end time and file name. `m` stands for **m**iddle.

Here are examples of parameter values for start time and end time:
- `30` (30 seconds)
- `1:12` (1 minute and 12 seconds)
- `2:33:17` (2 hours, 33 minutes and 17 seconds)

cutm usage examples:
- `cutm 45 01:30 "sample video.mkv"` replaces the original video file with "sample video.cut.mkv" file where a part from 45s to 1min 30s is removed.
- `cutm 5:44 8:59 "sample audio.opus"` replaces the original audio file with "sample audio.cut.opus" file where a part from 5min 44s to 8min 59s is removed.

## cutse Script
The script is intended for deleting the beginning and/or ending part in a media file based on provided start time, end time and file name. `se` stands for **s**tart/**e**nd.

Here are examples of parameter values for start time and end time:
- `-` (do not cut from a beginning/end)
- `30` (30 seconds)
- `1:12` (1 minute and 12 seconds)
- `2:33:17` (2 hours, 33 minutes and 17 seconds)

cutse usage examples:
- `cutse - 2:25:50 "sample audio.mp3"` replaces the original audio file with "sample audio.cut.mp3" file where everything after 2h 25min 50s is removed.
- `cutse 50 - "sample video.mkv"` replaces the original video file with "sample video.cut.mkv" file where everything before 50s is removed.
- `cutse 45 10:30 "sample video.mp4"` replaces the original video file with "sample video.cut.mp4" file where everything before 45s and after 10min 30s is removed.
- `cutse 5:44 03:08:00 "sample audio.opus` replaces the original audio file with "sample audio.cut.opus" file where everything before 5min 44s and after 3h 8min 0s is removed.


# UK

## MediaCutters
Репозиторій містить два Bash-скрипти для GNU/Linux, які спрощують видалення частин відео/аудіо за часом за допомогою ffmpeg.  
Щоб використовувати їх, переконайтеся, що встановлено такі залежності:
- ffmpeg
- libglib2.0-bin або альтернативний пакет, що містить виконуваний файл gio (щоб переміщати вхідні файли до Смітника після обробки)

Скрипти розраховані на такий спосіб використання:
1. Відкрийте термінал у каталозі, що містить відео- або аудіофайли, які потрібно обрізати.
2. Введіть &lt;назва скрипта&gt; &lt;час початку&gt; &lt;час кінця&gt; &lt;назва файлу&gt; замінивши частини в дужках на справжні значення. Порада: ви можете використовувати Tab для автодоповнення назви файлу.
3. Оригінальний файл видаляється і замінюється новим із суфіксом `.cut` перед розширенням.

## cutm Script
Цей скрипт призначений для видалення середини медіафайлу на основі заданих часу початку, часу кінця та назви файлу. `m` означає **m**iddle (середина).

Ось приклади значень параметрів для часу початку і часу кінця:
- `30` (30 секунд)
- `1:12` (1 хвилина 12 секунд)
- `2:33:17` (2 години, 33 хвилини і 17 секунд)

Приклади використання cutm:
- `cutm 45 01:30 "зразок відео.mkv"` замінює оригінальний відеофайл на файл "зразок відео.cut.mkv", з якого видалено частину від 45 с до 1 хв 30 с.
- `cutm 5:44 8:59 "зразок аудіо.opus"` замінює оригінальний аудіофайл на файл "зразок аудіо.cut.opus", з якого видалено частину від 5 хв 44 с до 8 хв 59 с.

## cutse Script
Цей скрипт призначений для видалення початкової та/або кінцевої частини медіафайлу на основі заданих часу початку, часу кінця та імені файлу. `se` означає **s**tart/**e**nd (початок/кінець).

Ось приклади значень параметрів для часу початку і часу завершення:
- `-` (не обрізати початок/кінець)
- `30` (30 секунд)
- `01:12` (1 хвилина 12 секунд)
- `2:33:17` (2 години, 33 хвилини і 17 секунд)

Приклади використання cutse:
- `cutse - 2:25:50 "зразок аудіо.mp3"` замінює оригінальний аудіофайл на файл "зразок аудіо.cut.mp3", з якого видалено все після 2 год 25 хв 50 с.
- `cutse 50 - "зразок відео.mkv"` замінює оригінальний відеофайл на файл "зразок відео.cut.mkv", з якого видалено все до 50 с.
- `cutse 45 10:30 "зразок відео.mp4"` замінює оригінальний відеофайл на файл "зразок відео.cut.mp4", з якого видалено все до 45 с і після 10 хв 30 с.
- `cutse 5:44 03:08:00 "зразок аудіо.opus"` замінює оригінальний аудіофайл на файл "зразок аудіо.cut.opus", з якого видалено все до 5 хв 44 с і після 3 год 8 хв 0 с.
