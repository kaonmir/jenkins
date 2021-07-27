node {
    def hello = 'Hello jojoldu' // 변수선언
    stage ('npm test') {
        npm i
        npm test
    }

    stage ('print') {
        print(hello) // 함수 + 변수 사용
    }
}

// 함수 선언 (반환 타입이 없기 때문에 void로 선언, 있다면 def로 선언하면 됨)
void print(message) {
    echo "${message}"
}