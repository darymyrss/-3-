import re

# Определяем алфавит
alphabet = ['a', 'b']

# Создаем все возможные комбинации длиной до 3 символов
words = [''.join([x, y, z]) for x in alphabet for y in alphabet for z in alphabet]

# Создаем регулярное выражение для поиска слов, не содержащих подстроки "aab"
regex_pattern = r'^(?!.*aab)[ab]+$'

# Находим все подходящие слова
matching_words = [word for word in words if re.match(regex_pattern, word)]

print(matching_words)
