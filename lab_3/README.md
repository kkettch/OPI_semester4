# lab_3
Выполнение лабораторной работы №3. Основы Программной Инженерии. 4-ый семестр. Университет ИТМО. 

## Задание | Вариант - 432321

Написать сценарий для утилиты Apache Ant, реализующий компиляцию, тестирование и упаковку в jar-архив кода проекта из лабораторной работы №3 по дисциплине "Веб-программирование".

Каждый этап должен быть выделен в отдельный блок сценария; все переменные и константы, используемые в сценарии, должны быть вынесены в отдельный файл параметров; MANIFEST.MF должен содержать информацию о версии и о запускаемом классе. <br />

Cценарий должен реализовывать следующие цели (targets): <br />

- **compile** - компиляция исходных кодов проекта.  <br />
- **build** - компиляция исходных кодов проекта и их упаковка в исполняемый jar-архив. Компиляцию исходных кодов реализовать посредством вызова цели compile. <br />
- **clean** - удаление скомпилированных классов проекта и всех временных файлов (если они есть). <br />
- **test** - запуск junit-тестов проекта. Перед запуском тестов необходимо осуществить сборку проекта (цель build). <br />
- **music** - воспроизведение музыки по завершению сборки (цель build). <br />
- **doc** - добавление в MANIFEST.MF MD5 и SHA-1 файлов проекта, а также генерация и добавление в архив javadoc по всем классам проекта. <br />
- **native2ascii** - преобразование native2ascii для копий файлов локализации (для тестирования сценария все строковые параметры необходимо вынести из классов в файлы локализации). <br />
- **xml** - валидация всех xml-файлов в проекте. <br />
- **env** - осуществляет сборку и запуск программы в альтернативных окружениях; окружение задается версией java и набором аргументов виртуальной машины в файле параметров. <br />
- **team** - осуществляет получение из git-репозитория 4 предыдущих ревизий, их сборку (по аналогии с основной) и упаковку получившихся jar-файлов в zip-архив. Сборку реализовать посредством вызова цели build. <br />
- **alt** - создаёт альтернативную версию программы с измененными именами переменных и классов (используя задание replace/replaceregexp в файлах параметров) и упаковывает её в jar-архив. Для создания jar-архива использует цель build. <br />
- **history** - если проект не удаётся скомпилировать (цель compile), загружается предыдущая версия из репозитория git. Операция повторяется до тех пор, пока проект не удастся собрать, либо не будет получена самая первая ревизия из репозитория. Если такая ревизия найдена, то формируется файл, содержащий результат операции diff для всех файлов, измёненных в ревизии, следующей непосредственно за последней работающей. <br />
