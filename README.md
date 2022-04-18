# GU_IOS_2393
GeekBrains homework
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