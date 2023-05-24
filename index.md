<html>
  <body>
    <form name="person" onSubmit = f()>
      ФИО: <input type = "text" name="fio"><br><br>
      Дата рождения: <input type = "text" name="birthday"><br><br>
      Должность: <select name= "position" size= "1" ><br>
        <option name= "director" >Директор</option>
        <option selected name= "manager" >Менеджер</option>
      </select><br><br>
      Оклад: <input type = "text" name="salary"><br><br>
      Пол: <input type= "radio" name = "sex" id= "sex" value= "Мужской">Мужской
      <br>
      <input type= "radio" name="sex" id= "sex" value= "Женский" checked>Женский
      <br>
      <br>
      <input type = "submit" value = "save">
    </form>
    <script>
      function f(){
	  fio = person.fio.value
	  birthday = person.birthday.value
	  index_position = person.position.selectedIndex
	  salary = person.salary.value
	  sex = document.getElementById('sex').value
	  S = "<table border=1><tr><th>ФИО</th><th>День рождения</th><th>Должность</th><th>Оклад</th><th>Пол</th><tr>"
	  S+="<tr><td>"+fio+"</td><td>"+birthday+"</td><td>"+index_position+"</td><td>"+salary+"</td><td>"+sex+"</td></tr></table>"
	  document.write(S)
      }
    </script>
  </body>
</html>
