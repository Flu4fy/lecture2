#include <iostream>
#include <cstring> 

class FooString {
    char* buf;
public:
    FooString(char* tbuf);
    FooString();
    ~FooString(); 
    
    int length(); 
    void show();
};

FooString::FooString(char* tbuf) {
    int len = std::strlen(tbuf); //получаем длину строки
    buf = new char[len + 1]; // выделяем память для буфера, включая 0-терминатор
    
    std::strcpy(buf, tbuf); // копируем переданную строку в буфер
}

FooString::FooString() {
    buf = nullptr; // устанавливаем указатель на ноль
}

FooString::~FooString() {
    delete[] buf; // освобождаем выделенную память
}

int FooString::length() {
    return std::strlen(buf); // возвращаем длину строки
}

void FooString::show() {
    std::cout << buf << std::endl; // выводим содержимое буфера
}

// модульные тесты для проверки работы метода length()
void testLength() {
    FooString str("Hello");
    
    int len = str.length();
    if (len == 5) {
        std::cout << "Тест 1: Пройден" << std::endl;
    } else {
        std::cout << "Тест 1: Не пройден" << std::endl;
    }
    
    FooString emptyStr;
    len = emptyStr.length();
    if (len == 0) {
        std::cout << "Тест 2: Пройден" << std::endl;
    } else {
        std::cout << "Тест 2: Не пройден" << std::endl;
    }
}

int main() {
    // тестирование
    testLength();

    return 0;
}
