![image](https://github.com/Sunyoungs/writeup/assets/128673666/cb5d7b72-66a2-436a-b38f-1877be52c067) ![image](https://github.com/Sunyoungs/SWING/assets/128673666/8d630535-a4fe-4c5a-a12f-9e4616cda066)

문제를 들어가면 다음의 화면처럼 주소 하나만 나와있다.

마우스 스크롤을 내리라길래 무작정 스크롤 내려봤더니 겨우 1퍼센트가 찼었다.

저번 Click Master에서 자동으로 클릭되는 매크로.. 비슷한 함수를 사용해야 했던 기억이 있어서 마우스 스크롤도 관련 함수가 있나 찾아봤더니, pyautogui라는 함수를 통해 자동으로 마우스를 사용자 조종할 수 있다고 한다.

pyautogui에서 마우스 스크롤을 내리는 코드는 pyautogui.scroll(-N)이며, 이를 사용하기 위해 selenium을 통해 문제의 주소를 열고 스크롤을 무한 반복 하도록 코드를 짜면 되지 않을까 싶었다.

```python
from selenium import webdriver
import pyautogui

driver = webdriver.Chrome()

driver.get('http://3.39.177.195:12312/')

while True:
    pyautogui.scroll(-1000000000)
```

다음과 같은 코드를 짜봤다.

seleiunm의 deriver.get 코드를 통해 문제 주소의 인터넷 창을 열도록 했고, while True로 pyautogui.scroll 함수를 무한 반복 하도록 했다;

![image](https://github.com/Sunyoungs/SWING/assets/128673666/739e2e21-a78d-47e6-8171-ee68f9ff325b) ![image](https://github.com/Sunyoungs/SWING/assets/128673666/a41a5af1-e6a7-4c74-8c1d-15b4334cbc8f)

코드를 실행하자 다음과 같이 인터넷 창이 떴고, 시간이 지나면서 스크롤 상태가 늘어나는 것을 볼 수 있다.

100퍼센트가 될 때까지 기다렸더니 팝업 창과 함께 FLAG 값이 나왔다.

![image](https://github.com/Sunyoungs/SWING/assets/128673666/70790ce2-89e2-4216-aa1c-c580727658dc) ![image](https://github.com/Sunyoungs/SWING/assets/128673666/2666a1e7-5be6-4549-a799-3d20a71a773d)

**hspace{wOw_ScrO1l_m4ST3r}**
