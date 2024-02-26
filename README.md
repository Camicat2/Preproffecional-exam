# Анализ профессий
файл с данными:
`https://drive.google.com/file/d/1sdQk4lgkEzUVoOu1JuF0EzByEj8yYa70/view?usp=drive_link`
## описание проекта
### задание 2
import csv
size = 23456789
with open(r'/home/student/Загрузки/vacancy.csv', encoding = 'utf-8') as file:
    reader = csv.reader(file, delimiter=';', quotechar='"')
    work_list = list(reader)[1:]
    for salary, work_type, company_size, role, company in work_list:
        if 'классный руководитель' in role and int(company_size) < int(size):
            size = company_size
            a = (f'в компании {company} есть заданная профессия:{role}, з/п в такой компании составит: {salary}, количество человек {company_size}')
print(a)

# #метод быстрой сортировки
# def ins_sort(arr):
#     for i in range(len(arr)):
#         cursor = arr[pos]
#         pos = i
#         while pos > 0 and arr[pos - 1] > cursor:
#             arr[pos] = arr[pos - 1]
#             pos -= 1
#         arr[pos] = cursor
#     return arr
 добавление в сортировку
# import csv
# with open(r'/home/student/Загрузки/vacancy.csv', encoding='utf-8') as file:
#     reader = list(csv.reader(file, delimiter=',', quotechar='"'))
#     for i in range(len(reader)):
#         # reader = list(csv.DictReader(file, delimiter=',', quotechar='"'))
#         pos = i
#         for company_size in reader:
#         # cursor = reader[pos]
#             while pos > 0 and reader[pos - 1] > company_size:
#                 reader[pos] = reader[pos - 1]
#                 pos -= 1
#             reader[pos] = company_size
#         print(reader)
#         break

### задание №3
#### описание аргументов
- **reader**
- **work_list** - создаваемый список
- **company_name** - название интересующей компании
- **count** - счётчик
- **salary, work_type, company_size, role, company**: зарплата, тип, размер компании, роль, компания соответственно (взято из 'файл с данными')
     
      `import csv` 
  
      `with open(r'/home/student/Загрузки/vacancy.csv', encoding = 'utf-8') as file:` - открытие файла с помощью кодировки UTF - 8
  
          `reader = csv.reader(file, delimiter=';', quotechar='"')`
          
          `work_list = list(reader)[1:]`
          
          `company_name = input('')` - запрашивается название компании
          
          `count = 0` - счётчик
          
          `for salary, work_type, company_size, role, company in work_list:`
          
              `while company_name != 'None':` - пока пользователем не ввелось 'None' цикл не завершается
                  
                  `if company_name in company:`
                  
                      `print(f'в компании {company} есть заданная профессия:{role}, з/п в такой компании составит: {salary}, количество человек {company_size}')`
                      
                      `company_name = input('')` - после вывода информации о прошлой компании запрашивается название новой
                      
                  `elif company_name not in company:`
                  
                      `count += 1` - предложеных компаний всего 200 соответственно когда счетчик достигает 200 компания не найдена
                      
                      `if count >= 200:`
                          `count == 0` - счётчик обнуляется
                      
                          `print('К сожалению ничего не удалось найти :(')`
                          
                          `company_name = input('')`
  


                    
## Как запустить проект
## Как использовать
