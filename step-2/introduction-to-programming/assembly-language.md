# Assembly Language

Assembly Language란 컴퓨터 프로세서를 다루기 위한 가장 기본적인 언어입니다. 소프트웨어 개발자는 Assembly Language를 이용하여 오로지 CPU가 수행해야 할 직접적인 작업에 관한 내용만을 명령내릴 수 있습니다.

Assembly Language는 일반적으로 함수나 변수와 같은 편의를 위한 고차원적인 기능들은 가지고 있지 않습니다. 그리고 또한 일반적으로 CPU의 종류에 따라 Assembly Language는 다릅니다. Assembly Language는 Machine Language와 같은 구조나 명령어들을 갖고 있지만, 소프트웨어 개발자는 숫자가 아닌 이름을 이용해서 작업을 할 수 있습니다. Assembly Language는 소프트웨어 개발자가 성능적인 필요에 따라 혹은 고차원 언어에서 수행 불가능한 명령어들을 사용하고 싶을때 유용하기도 합니다.

![Assembly](https://s3.ap-northeast-2.amazonaws.com/bootcamp-prep-assets/images/assembly.gif)

### Assembly Language는 왜 유용한가?

Machine Language는 숫자들로만 이루어져 있어 사람이 읽고 이해하기는 힘듭니다. Assembly Language를 이용하면, 소프트웨어 엔지니어는 Machine Language의 내용들을 사람이 읽고 이해할 수 있는 방식으로 거의 동일하게 작업할 수 있습니다.

단점은 컴퓨터가 수행하는 모든 작업을 세부적으로 명시해주어야만 한다는 것이고, 장점으로는 소프트웨어 개발자가 컴퓨터의 모든 작업 실행에 대한 전권을 갖고 있다는 점입니다.

### 왜 Assembly Language는 "Low-level" Language인가?

Assembly Language는 컴퓨터가 수행하는 모든 작업에 대해 1:1로 대응하는 수준으로 명령을 내리고 작업을 해야하므로 Low-level Language입니다. 일반적으로 Assembly Language 프로그램은 한 줄에 최대 한 가지의 명령을 컴퓨터에게 내립니다.

### Assembly Language는 어떻게 "High-level" Language와 다른가?

High-level Language는 Low-level Language의 기능들을 조금 더 추상화하여 우리에게 제공해줍니다. 그래서 소프트웨어 엔지니어는 어떻게 작업을 해야하는지보다는 무엇을 해야하는지에 더욱 집중할 수 있습니다. 이런 특징은 소프트웨어 엔지니어의 작업을 훨씬 쉽고 수월하게 해줍니다.

High-level Language로 쓰여진 프로그램은 Assembly로 쓰여진 프로그램에 비해 절대적으로 성능이 떨어질 수 밖에 없는 태생적 한계가 있기도 합니다. High-level Language로는 Python, Java, Javascript, Clojure 등이 있습니다.
