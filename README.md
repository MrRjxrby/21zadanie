# 21zadanie
# Практика 21
# Задание 1.
```
import java.util.Arrays;
import java.util.List;

public class ArrayConverter {
    public static <T> List<T> convertToList(T[] array) {
        return Arrays.asList(array);
    }

    public static void main(String[] args) {
        String[] stringArray = {"Hello", "World", "!"};
        List<String> stringList = convertToList(stringArray);
        System.out.println("Список строк: " + stringList);

        Integer[] integerArray = {1, 2, 3, 4, 5};
        List<Integer> integerList = convertToList(integerArray);
        System.out.println("Список чисел: " + integerList);
    }
}
```
# Задание 2
```
import java.util.ArrayList;
import java.util.List;

public class GenericArray<T> {
    private List<T> elements;

    public GenericArray() {
        elements = new ArrayList<>();
    }

    public void addElement(T element) {
        elements.add(element);
    }

    public List<T> getElements() {
        return elements;
    }

    public static void main(String[] args) {
        GenericArray<Object> mixedArray = new GenericArray<>();
        mixedArray.addElement(10);
        mixedArray.addElement("Привет");
        mixedArray.addElement(3.14);
        
        System.out.println("Элементы массива: " + mixedArray.getElements());
    }
}
```
Задание 3
```
public class ArrayRetriever<T> {
    private T[] array;

    public ArrayRetriever(T[] array) {
        this.array = array;
    }

    public T getElement(int index) {
        if (index < 0 || index >= array.length) {
            throw new IndexOutOfBoundsException("Индекс вне диапазона!");
        }
        return array[index];
    }

    public static void main(String[] args) {
        Integer[] numbers = {1, 2, 3, 4, 5};
        ArrayRetriever<Integer> retriever = new ArrayRetriever<>(numbers);
        
        System.out.println("Элемент под индексом 2: " + retriever.getElement(2));
        System.out.println("Элемент под индексом 0: " + retriever.getElement(0));
    }
}

```
