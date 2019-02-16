# homework
{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Лабораторне заняття №1"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 1 Перестановки"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### 1.1 Використовуючи власну функцію"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 1,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "def permute(A):\n",
    "    if len(A)==1:\n",
    "        return [tuple(A)]\n",
    "    permutations = []\n",
    "    for x in A:\n",
    "        for y in permute(A-{x}):\n",
    "            permutations.append((x,)+y)\n",
    "    return permutations"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "A = {1, 2, 3}"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 9,
   "metadata": {
    "collapsed": false
   },
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Перестановки множини {1, 2, 3}: {(3, 1, 2), (1, 3, 2), (3, 2, 1), (2, 3, 1), (1, 2, 3), (2, 1, 3)}\n",
      "Кількість перестановок:  6\n"
     ]
    }
   ],
   "source": [
    "# Використовуючи власну функцію\n",
    "permute_all = set(permute(A))\n",
    "print(\"Перестановки множини {}: {}\".format(A,permute_all))\n",
    "print(\"Кількість перестановок: \", len(permute_all))"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### 1.2 Використовуючи бібліотеку `itertools`"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "from itertools import permutations"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "A = {1, 2, 3}"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 10,
   "metadata": {
    "collapsed": false
   },
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Перестановки множини {1, 2, 3}: {(3, 1, 2), (1, 3, 2), (3, 2, 1), (2, 3, 1), (1, 2, 3), (2, 1, 3)}\n",
      "Кількість перестановок:  6\n"
     ]
    }
   ],
   "source": [
    "# Використовуючи бібліотеку itertools\n",
    "permute_all = set(permutations(A))\n",
    "print(\"Перестановки множини {}: {}\".format(A,permute_all))\n",
    "print(\"Кількість перестановок: \", len(permute_all))"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### 1.3 Задача\n",
    "Виведіть всі можливі перестановки та порахуйте їх кількість від таких множин:\n",
    "- {1, 3, 5}\n",
    "- {1, 2, 3, 4}\n",
    "- {1, 2, 2, 1}\n",
    "\n",
    "Порахуйте кількість перестановок таких множин:\n",
    "- {1, 2, 3, 4, 5}\n",
    "- {1, 2, 3, 4, 5, 6, 7}\n",
    "- {1, 3, 5, 7, 9, 11, 13, 15, 17, 19}"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 7,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# Місце для Вашого коду\n",
    "\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### 1.4 Задача\n",
    "Виведіть всі можливі перестановки без нерухомих точок та порахуйте їх кількість від таких множин:\n",
    "- {1, 2, 3}\n",
    "- {1, 2, 3, 4}\n",
    "- {1, 3, 5, 7}\n",
    "- {1, 2, 2, 1}\n",
    "\n",
    "_Перестановка без нерухомих точок_ - це така перестановка, в якій позиція кожного елементу не збігається з його позицією в початковій множині.\n",
    "**Приклад.** Для множини {1, 2, 3, 4, 5}:\n",
    "- {4, 1, 5, 2, 3} - перестановка без нерухомих точок\n",
    "- {4, **2**, 1, 3, **5**} - перестановка з нерухомими точками"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 8,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# Місце для Вашого коду\n",
    "\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### 1.5 Задача\n",
    "Виведіть всі можливі перестановки, в яких перші $4$ елементи зростають, а наступні спадають, та порахуйте їх кількість від таких множин:\n",
    "- {1, 2, 3, 4, 5, 6, 7, 8}\n",
    "- {1, 2, 3, 4, 5, 6, 7, 8, 9, 10}"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 8,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# Місце для Вашого коду\n",
    "\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 2 Часткові перестановки"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### 2.1 Використовуючи бібліотеку `itertools`"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 12,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "A = {1, 2, 3}\n",
    "k = 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 14,
   "metadata": {
    "collapsed": false
   },
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Перестановки довжини 2 множини {1, 2, 3}: [(1, 2), (1, 3), (2, 1), (2, 3), (3, 1), (3, 2)]\n",
      "Кількість таких перестановок: 6\n"
     ]
    }
   ],
   "source": [
    "# перестановки довжини k множини A\n",
    "permute_k = list(permutations(A, k))\n",
    "print(\"Перестановки довжини {} множини {}: {}\".format(k,A,permute_k))\n",
    "print(\"Кількість таких перестановок: {}\".format(len(permute_k)))"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### 2.2 Задача\n",
    "Нехай $n$ - розмір множини, $k$ - розмір перестановок.\n",
    "Виведіть всі можливі часткові перестановки та порахуйте їх кількість для таких параметрів:\n",
    "- $n = 4, k = 2$\n",
    "- $n = 4, k = 3$\n",
    "- $n = 5, k = 2$\n",
    "\n",
    "Порахуйте кількість часткових перестановок для таких параметрів:\n",
    "- $n = 6, k = 2$\n",
    "- $n = 6, k = 4$\n",
    "- $n = 8, k = 4$"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 15,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# Місце для Вашого коду\n",
    "\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 3 Комбінації без повторень"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### 3.1 Використовуючи бібліотеку `itertools`"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 16,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "from itertools import combinations"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 18,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "A = {1, 2, 3}\n",
    "k = 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 19,
   "metadata": {
    "collapsed": false
   },
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Комбінації довжини 2 множини {1, 2, 3}: [(1, 2), (1, 3), (2, 3)]\n",
      "Кількість таких комбінацій: 3\n"
     ]
    }
   ],
   "source": [
    "# комбінації довжини k множини A\n",
    "choose_k = list(combinations(A,k))\n",
    "print(\"Комбінації довжини {} множини {}: {}\".format(k,A,choose_k))\n",
    "print(\"Кількість таких комбінацій: {}\".format(len(choose_k)  ))"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### 3.2 Задача\n",
    "Нехай $n$ - розмір множини, $k$ - розмір комбінацій.\n",
    "Виведіть всі можливі комбінації без повторень та порахуйте їх кількість для таких параметрів:\n",
    "- $n = 4, k = 2$\n",
    "- $n = 4, k = 3$\n",
    "- $n = 5, k = 2$\n",
    "\n",
    "Порахуйте кількість комбінацій без повторень для таких параметрів:\n",
    "- $n = 6, k = 2$\n",
    "- $n = 6, k = 4$\n",
    "- $n = 8, k = 4$"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 20,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# Місце для Вашого коду\n",
    "\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### 3.3 Задача\n",
    "Нехай $A$ - множина з $10$ елементів, кожен з яких є цілим числом від $1$ до $100$.\n",
    "Тобто $$A = \\{ a_i \\}_{i = 1}^{10},\\\\ 1 \\leq a_i \\leq 100, \\quad i = 1, \\ldots, 10.$$\n",
    "Скільки елементів може бути в множині, яка складається із попарних сум елементів множини $A$?\n",
    "$$B = \\{ b_k \\, \\colon \\, b_k = a_i + a_j, \\quad a_i, a_j \\in A, \\, 1 \\leq i, j \\leq 10, \\, i \\neq j \\}_{k = 1}^{\\textbf{?}}$$"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 20,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# Місце для Вашого коду\n",
    "\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 4 Комбінації з повтореннями"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### 4.1 Використовуючи бібліотеку `itertools`"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 22,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "from itertools import combinations_with_replacement"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 21,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "A = {1, 2, 3}\n",
    "k = 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 23,
   "metadata": {
    "collapsed": false
   },
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Комбінації довжини 2 множини {1, 2, 3}: [(1, 1), (1, 2), (1, 3), (2, 2), (2, 3), (3, 3)]\n",
      "Кількість таких комбінацій: 6\n"
     ]
    }
   ],
   "source": [
    "# комбінації довжини k множини A\n",
    "choose_k = list(combinations_with_replacement(A,k))\n",
    "print(\"Комбінації довжини {} множини {}: {}\".format(k,A,choose_k))\n",
    "print(\"Кількість таких комбінацій: {}\".format(len(choose_k)  ))"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### 4.2 Задача\n",
    "Нехай $n$ - розмір множини, $k$ - розмір комбінацій.\n",
    "Виведіть всі можливі комбінації з повтореннями та порахуйте їх кількість для таких параметрів:\n",
    "- $n = 4, k = 2$\n",
    "- $n = 4, k = 3$\n",
    "- $n = 5, k = 2$\n",
    "\n",
    "Порахуйте кількість комбінацій з повтореннями для таких параметрів:\n",
    "- $n = 6, k = 2$\n",
    "- $n = 6, k = 4$\n",
    "- $n = 8, k = 4$"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 20,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# Місце для Вашого коду\n",
    "\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### 4.3 Задача\n",
    "Скільки існує 6-цифрових наборів таких, що сума перших трьох цифр дорівнює сумі останніх трьох?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 24,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# Місце для Вашого коду\n",
    "\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### 4.4 Задача\n",
    "Скільки існує 6-цифрових чисел, в яких дві однакові цифри не стоять поряд?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 24,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# Місце для Вашого коду\n",
    "\n"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.6.1"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 0
}
