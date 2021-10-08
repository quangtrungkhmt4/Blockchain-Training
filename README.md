# Solidity Basic

## Data types(Kiểu dữ liệu)
- bool: Kiểu dữ liệu logic
- int/uint: Kiểu dữ liệu số nguyên
- fixed/unfixed: Kiểu dữ liệu số thập phân
- string: Kiểu dữ liệu chuỗi
- struct: Kiểu dữ liệu cấu trúc, bao gồm nhiều thành phần bên trong
- address: Mỗi Ethereum blockchain ví như một account, address là một chuỗi định dạng duy nhất trỏ đến địa chỉ của account đó
```
    uint dnaDigits = 16;
    int number = 10;
    bool isCheck = true;
    string data = "tutorial";
    struct Zombie {
        string name;
        uint dna;
    }
    address ckAddress = 0x06012c8cf97BEaD5deAe237070F9587f8E7A266d;
```

## Variables(Biến)
- State Variables: Biến khai báo và lưu trữ trong Contract
- Local Variables: Biến được khai báo trong function và có giá trị trong khi function được thực thi
```
contract ZombieFactory {
    uint dnaDigits = 16; -- State Variables
    
    function _generateRandomDna(string memory _str) private view returns (uint) {
        uint rand = uint(keccak256(abi.encodePacked(_str)));  -- Local Variables
        return rand % dnaModulus;
    }
}
```

## Operator(Toán tử)
- Toán tử toán học
    -- Subtraction(-)
        ```
        uint dnaDigits = 16 - 10;
        ```
        
    -- Addition(+)
        ```
        uint dnaDigits = 16 + 10;
        ```
        
    -- Multiplication(*)
        ```
        uint dnaDigits = 16 * 10;
        ```
        
    -- Division(/)
        ```
        uint dnaDigits = 10 / 2;
        ```
        
    -- Modulus(%)
        ```
        uint dnaDigits = 10 / 3;
        ```
        
    -- Increment(++)
        ```
        uint dnaDigits = 10;
        dnaDigits++;
        ```
        
    -- Decrement(--)
        ```
        uint dnaDigits = 10;
        dnaDigits--;
        ```
- Toán tử so sánh
 -- Equal(`==`)
 -- Not Equal(`!=`)
 -- Greater than(`>`)
 -- Less than(`<`)
 -- Greater than or Equal to(`>=`)
 -- Less than or Equal to(`<=`)

- Toán tử logic
 -- Logical AND(`&&`)
 -- Logical OR(`||`)
 -- Logical NOT(`!`)

## Loops(Vòng lặp)
- While Loop
    ```
        uint count;
        while (count < 10) {
            count++;
        }
    ```
- Do - While loop
    ```
        uint count;
        do{
            count--;
         }while(count > 0) ;
            count++;
        }
    ```
- For loop
    ```
        uint count;
        for(uint i=0; i<5; i++){
            count++;
        }
    ```
    
## Arrays(Mảng)
- Mảng tĩnh: Mảng với kích thước phần tử được cấu hình trước
    ```
    uint numbers[10];
    ```
- Mảng động: Mảng với kích thước phần tử không được cấu hình trước
    ```
    uint numbers[];
    ```
- Khởi tạo mảng
    ```
    uint numbers[5] = [1, 2, 3, 4, 5];
    uint balance[] = new uint[](5);
    ```
- Thêm phần tử vào mảng
    ```
    uint[] numbers;
    numbers.push(5);
    numbers.push(10);
    numbers.push(15);
    ```

## Mappings
Mapping là một cặp key-value để lưu trữ và truy xuất dữ liệu
