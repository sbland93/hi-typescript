# hi-typescript

## tsconfig.json
tsconfig.json
어떻게 컴파일 될지

## tsc
tsc를 통해서 ts -> js를 만들 수 있다.

## interface, class
interface와 class로 객체의 타입을 관리할 수 있는데,
interface는 생성되는 js에 표현되지 않는다.
class는 표현된다.



### 코드 예시


#### 일반 함수
`
const sayHi = (name:string, age:Number, gender:string):string => {
    return `Hello ${name}, you are ${age}, you are a ${gender}!!!!`;
}
`

#### 인터페이스 사용
`

interface Human {
    name: string;
    age: number;
    gender: string;
}

const person = {
    name : "seungbeom",
    age : 24,
    gender : "male",
}

const sayHi = (person:Human):string => {
    return `Hello ${person.name}, you are ${person.age}, you are a ${person.gender}!!!!`;
}
`
#### 클래스 사용
`
class Human {
    public name: string;
    public age: number;
    public gender: string;
    constructor(name: string, age: number, gender:string){
        this.name = name;
        this.age = age;
        this.gender = gender;
    }
}

const lynn = new Human("Lynn", 18, "female");

const sayHi = (person:Human):string => {
    return `Hello ${person.name}, you are ${person.age}, you are a ${person.gender}!!!!`;
}

console.log(sayHi(lynn));
`