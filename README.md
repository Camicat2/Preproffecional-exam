# Анализ профессий
файл с данными:
`https://drive.google.com/file/d/1sdQk4lgkEzUVoOu1JuF0EzByEj8yYa70/view?usp=drive_link`
## описание проекта
### задание №3

      `import csv` 
  
      `with open(r'/home/student/Загрузки/vacancy.csv', encoding = 'utf-8') as file:` - открытие файла с помощью кодировки UTF - 8
  
          `reader = csv.reader(file, delimiter=';', quotechar='"')`
          
          `work_list = list(reader)[1:]`
          
          `company_name = input('')`
          
          `count = 0`
          
          `for salary, work_type, company_size, role, company in work_list:`
          
              `while company_name != 'None':`
                  
                  `if company_name in company:`
                  
                      `print(f'в компании {company} есть заданная профессия:{role}, з/п в такой компании составит: {salary}, количество человек {company_size}')`
                      
                      `company_name = input('')`
                      
                  `elif company_name not in company:`
                  
                      `count += 1`
                      
                      `if count >= 200:`
                      
                          `print('К сожалению ничего не удалось найти :(')`
                          
                          `company_name = input('')`
                    
## Как запустить проект
## Как использовать
