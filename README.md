Лабораторная работа № 3.
====
Классы. Наследование. Создание простых иерархий.
----
Спроектировать и реализовать иерархию классов для игры в шахматы.  
В качестве варианта использования рассмотреть задачу анализа ситуации на поле. В задаче участвует несколько черных фигур (любого вида) и одна белая – король. Провести анализ положения белого короля в условии хода белых фигур - шах, пат, мат или белому королю ничего не угрожает.  
В иерархии классов реализовать:
-	проверку попадания фигуры на доску;
-	проверку установки фигуры на свободную клетку;
-	отслеживание количества экземпляров каждого вида фигур.  
Разработанная иерархия должна допускать использование: 

```c++
int main() 
{
	TKing bKing(black,’h’,5);
	THorse bHorse1(black,’c’,2);
	TKing bKing2(black,’a’,1);	// эта строчка работать не должна, потому что двух
			  		// одинаковых королей быть не может
	THorse bHorse2(black,’с’,2);	// эта строчка работать не должна, потому что клетка
			  		// с2 уже занята
	THorse bHorse3(black,’z’,20);	// эта строчка работать не должна из-за 
			  		// неправильных координат

	TFigure *figures[32];
	figures[0]=&bKing;
	figures[1]=&bHorse;

	/*for (int i = 0; i < 32; i++)
		figures[i]->mapStep();*/

	TKing wKing(white,’a’,4);
	cout << endl << wKing.Situation();

	return 0;
}
```

В тестовой программе информацию о черных фигурах считывать из файла, координаты белого короля получать с клавиатуры.  
Для удобства проверки правильности работы программы реализовать метод вывода доски на экран.  
 
Контрольные точки  
1.	Прокомментировать по программе использование основных принципов ООП.  
2.	Пояснить назначение абстрактных классов, виртуальных функций.  
3.	Проследить правильную организацию исключений.  


*Можно использовать с# или Java
