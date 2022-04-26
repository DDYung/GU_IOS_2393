# GU_IOS_2393
GeekBrains homework
Lesson 1

Домашнее задание №1

Задание 1. Решить квадратное уравнение.

import Swift
import Foundation

//ах²+bх+с=0 — вид квадратного уравнения

var a: Float = 1 // теперь в переменной a хранится коэффициент A уравнения 
var b: Float = 2 // теперь в переменной b хранится коэффициент B уравнения 
var c: Float = 3 // теперь в переменной c хранится коэффициент C уравнения 

// подставляем формулу дискриминанта, чтобы понять, сколько корней в уравнении
var discriminant = (b*b) - (4*a*c)

if discriminant<0 {
    print("Уравнение не имеет корней")
} 
else if discriminant==0 {
    b=b*(-b)
    let oneRoot: Float = b/2*a
    print("Уравнение имеет один корень \(oneRoot)")   
} 
else {
    b=b*(-b)
    let firstRoot: Float = (b+sqrt(discriminant))/(2*a)
    let secondRoot: Float = (b-sqrt(discriminant))/(2*a)
    print("Уравнение имеет два корня, x1=\(firstRoot), x2=\(secondRoot)")
}

Задание 2. Даны катеты прямоугольного треугольника. Найти площадь, периметр и гипотенузу треугольника.

var cathetusOne = 5 // переменная будет хранить значение первого катета
var cathetusTwo = 8 // переменная будет хранить значение второго катета

var S = (cathetusOne*cathetusTwo)*1/2 // результат вычисления площади треугольника записываем в переменную S
print ("Площадь треугольника равна \(S)")

var hypotenuse: Float = sqrt(Float(cathetusOne*cathetusOne)+Float(cathetusTwo*cathetusTwo)) // находим гипотенузу по теореме Пифагора
print ("Гипотенуза треугольника равна \(hypotenuse)")

var perimeter: Float = Float(cathetusOne+cathetusTwo)+(hypotenuse)// находим периметр треугольника
print ("Периметр треугольника равен \(perimeter)")

Домашнее задание №2

Задание 1. Написать функцию, которая определяет, четное число или нет.

var anyValue: Int = 10 // здесь будет точка входа, где мы задаем число (четное либо нечетное). 
                    // !Внимание, по правилам математики 0 также является четным числом, поэтому под него не писался отдельный кейс.

func isEvenOrNot (_ param: Int) // В функции параметр, который принимает значение, которое мы вводим в anyValue 
{
let specialArg = 2; // это константа, которая хранит число 2 на которое мы делим входной параметр
let specialArg1 = "четное" // строковая переменная для вывода результата для четного числа
let specialArg2 = "нечетное" // строковая переменная для вывода результата для нечетного числа
let result: Float = Float(param%specialArg) // записываем результат в result, если у нас есть остаток от деления, это нечетное число
if result == 0 {
print ("Введенное число \(specialArg1)") // если нет остатка от деления, выводим строку
}
else
{print ("Введенное число \(specialArg2)") // если есть остаток от деления, выводим строку
}
}

isEvenOrNot (anyValue)

Задание 2. Написать функцию, которая определяет, делится ли число без остатка на 3.

var putNumber = 30// здесь будет точка входа, где мы задаем число

func splitNum (_ param: Int) {
let specialArg = 3; // это константа, которая хранит число 3 на которое мы делим входной параметр
let result: Float = Float(param%specialArg) // записываем результат в result, если у нас есть остаток от деления, то входной параметр не делится на 3 без остатка
if result == 0  {
print ("Введенное число делится на 3 без остатка")} // если результат деления с остатком равен нулю, выводим уведомление  
else {
print ("Введенное число не делится на 3 без остатка") // если результат деления с остатком не равен нулю, выводим уведомление 
}
}

splitNum(putNumber) // запуск функции с входным параметром, которое мы задаем

Задание 3. Создать возрастающий массив из 100 чисел

Вариант 1.
var number1 = [Int] (0..<101) // создаем массив number1 со значениями от 0 до 100
print(number1) // выводим массив

Вариант 2.
var number2: [Int] = []// создаем массив number2
for i in 0...100 {
    number2.append(i) //с помощью метода append добавляем по одному элементу в массив до числа 100
}
print (number2)// выводим массив

Задание 4. Удалить из этого массива все четные числа и все числа, которые не делятся на 3.

var numbers = Array(1...100) // создаем массив, можно как у вас, результат тот же

for number in numbers { // итерируемся по массиву numbers
if number % 2 == 0 { // проверяем что число четное, вместо проверки можно использовать прямо вашу функцию
numbers.remove(at: numbers.firstIndex(of: number)!) // чтобы удалить конкретный элемент – функцией firstIndex(of:) мы ищем индекс нужного элемента, а функция remove(at:) удаляет элемент по этому индексу
} else if number % 3 != 0 {
numbers.remove(at: numbers.firstIndex(of: number)!)
}
}

Домашнее задание №3
1. Описать несколько структур – любой легковой автомобиль SportCar и любой грузовик TrunkCar.
2. Структуры должны содержать марку авто, год выпуска, объем багажника/кузова, запущен ли двигатель, открыты ли окна, заполненный объем багажника.
3. Описать перечисление с возможными действиями с автомобилем: запустить/заглушить двигатель, открыть/закрыть окна, погрузить/выгрузить из кузова/багажника груз определенного объема.
4. Добавить в структуры метод с одним аргументом типа перечисления, который будет менять свойства структуры в зависимости от действия.
5. Инициализировать несколько экземпляров структур. Применить к ним различные действия.
6. Вывести значения свойств экземпляров в консоль.

import Swift
import Foundation

struct sportCar { // создаем структуру и несколько полей с разными типами
	let name: String
	let made: Int
	let trunkValue: Float
	let trunkValueUsed: Int
	var isEngineOn: Bool
	var areWindowsOpen: Bool
    
    enum CarProperties {
        case turnEngineOn 
        case turnEngineOff
        case openTheWindows
        case closeTheWindows
        }

    //func changeMethod (CarProperties) {     // пока не разобрался как это работает
    //} 
}    	

var carCondition: sportCar.CarProperties = .turnEngineOff // создаем экземпляр класса и присваиваем ему значение из перечисления

switch carCondition { // набор случаев для состояния автомобиля
    case .turnEngineOn:
    print("Двигатель включен")
    case .turnEngineOff:
    print("Двигатель выключен")
    case .openTheWindows: 
    print ("Окна открыты")
    case .closeTheWindows:
    print("Окна закрыты")
}

let lamborghini = sportCar(name: "Lamborghini", made: 2021, trunkValue: 100.00, trunkValueUsed: 38, isEngineOn: false , areWindowsOpen: true) // инициализируем экземпляр структуры

print (lamborghini) // распечатаем весь экземпляр структуры для проверки

