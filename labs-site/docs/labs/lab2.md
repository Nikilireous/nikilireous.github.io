# Лабораторная работа №2.

## Тема
Численные вычисления и анализ данных с использованием NumPy.

## Цели работы
- Узнать о возможностях использования библиотек NumPy, Pandas, Matplotlib, Seaborn.
- Освоить базовые методы представленных библиотек.

## Задачи
### Создание массива
```python
def create_vector() -> np.ndarray:
    return np.arange(10)
```
Реализовано с помощью базового функционала библиотеки.


### Создание матрицы
```python
def create_matrix() -> np.ndarray[tuple[float]]:
    return np.random.rand(5,5)
```
Реализовано с помощью базового функционала библиотеки.


### Преобразование вектора
```python
def reshape_vector(vec: np.ndarray) -> np.ndarray:
    return vec.reshape(2,5)
```
Реализовано с помощью базового функционала библиотеки.


### Транспонирование матрицы
```python
def transpose_matrix(mat: np.ndarray) -> np.ndarray:
    return mat.T
```
Реализовано с помощью базового функционала библиотеки.


### Сложение векторов одинаковой длины
```python
def vector_add(a: np.ndarray, b: np.ndarray) -> np.ndarray:
    return a + b
```
Реализовано с помощью базового функционала библиотеки.


### Умножение вектора на число
```python
def scalar_multiply(vec: np.ndarray, scalar: float | int) -> np.ndarray:
    return vec * scalar
```
Реализовано с помощью базового функционала библиотеки.


### Поэлементное умножение
```python
def elementwise_multiply(a: np.ndarray, b: np.ndarray) -> np.ndarray:
    return a * b
```
Реализовано с помощью базового функционала библиотеки.


### Скалярное произведение
```python
def dot_product(a: np.ndarray, b: np.ndarray) -> float:
    return np.dot(a, b)
```
Реализовано с помощью базового функционала библиотеки.


### Умножение матриц
```python
def matrix_multiply(a: np.ndarray, b: np.ndarray) -> np.ndarray:
    return a @ b
```
Реализовано с помощью базового функционала библиотеки.


### Определитель матрицы
```python
def matrix_determinant(a: np.ndarray) -> float:
    return np.linalg.det(a)
```
Реализовано с помощью базового функционала библиотеки.


### Обратная матрица
```python
def matrix_inverse(a: np.ndarray) -> np.ndarray:
    return np.linalg.inv(a)
```
Реализовано с помощью базового функционала библиотеки.


### Решение системы вида: Ax = b
```python
def solve_linear_system(a: np.ndarray, b: np.ndarray) -> np.ndarray:
    return np.linalg.solve(a, b)
```
Реализовано с помощью базового функционала библиотеки.


### Получение NumPy массива из CSV-файла
```python
def load_dataset(path: str = "data/students_scores.csv") -> np.ndarray:
    return pd.read_csv(path).to_numpy()
```
Реализовано с помощью базового функционала библиотеки.


### Получение некоторых характеристических данных массива
```python
def statistical_analysis(data: np.ndarray) -> dict:
        return {
        "mean": np.mean(data),
        "median": np.median(data),
        "std": np.std(data),
        "min": np.min(data),
        "max": np.max(data),
        "25": np.percentile(data, 25),
        "75": np.percentile(data, 75)
    }
```
Реализовано с помощью базового функционала библиотеки.


### Min-Max нормализация
```python
def normalize_data(data: np.ndarray) -> np.ndarray:
    return (data - np.min(data)) / (float(np.max(data)) - np.min(data))
```
Воспроизведена формула Min-Max нормализации для массива данных.


### Построение гистограммы распределения
```python
def plot_histogram(data: np.ndarray) -> None:
    plt.hist(data)
    plt.title("Гистограмма распределения оценок по математике.")
    plt.xlabel("Оценка")
    plt.ylabel("Количество учащихся, получивших оценку")

    plt.savefig("plots/histogram.png")
    plt.close()
```
Реализовано с помощью базового функционала библиотеки.


### Построение тепловой карты корреляции
```python
def plot_heatmap(matrix: np.ndarray) -> None:
    sns.heatmap(matrix)
    plt.title("Тепловая карта корреляции предметов")

    plt.savefig("plots/heatmap.png")
    plt.close()
```
Реализовано с помощью базового функционала библиотеки.


### Построение графика зависимости
```python
def plot_line(x: np.ndarray, y: np.ndarray) -> None:
    plt.plot(x, y, "bo")
    plt.title("График студентов и их оценок")
    plt.xlabel("Номер студента")
    plt.ylabel("Оценки")

    plt.savefig("plots/students_marks.png")
    plt.close()
```
Реализовано с помощью базового функционала библиотеки.


## Вывод
Были достигнуты все поставленные задачи:

- Получены знания о работе названных выше библиотек.
- Отработаны основные функции для взаимодействия с массивами (векторами, матрицами).
- Построены различные графики с помощью библиотек визуализаций.


***[Ссылка на репозиторий](https://github.com/Nikilireous/Python-Labs/Semester-2/Task-2)***