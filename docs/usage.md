### Пример использования

```python
import moss_cappa

userid = 123456789 # Необходимо указать собственный userid

m = moss_cappa.Moss(lang='python', user_id=userid)

# Добавление файлов для проверки (используется символ подстановки '*')
m.add_files('submissions/*.py')

# Отправка файлов на проверку
moss_url = m.send_file(
    lambda file, 
    display_name: print('x', end='', flush=True)
)
print()

print (f'URL: {moss_url}')

# Обработка полученных результатов
result = m.process_url(url=moss_url)
print(f'Plagiarism percentage: {result}')
```

## Совместимость с версиями Python

* [Python](http://www.python.com) - v3
