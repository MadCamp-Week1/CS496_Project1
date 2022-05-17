# Peach10
Peach10 is an gaming app that allows you to save and share records achieved while playing games.

## Developers
Dayun Cha  
Wonjae Lee

## Abstract
- Contacts
- Gallery
- Simple puzzle game

## Usage
### Contact tab
- You can get all the contacts stored on the device.
- You can add, delete, edit, search contacts in the contact tab.
- You can move to a phone app or a text app with the contact information.

<img src="https://user-images.githubusercontent.com/96765048/148054259-9863ffcc-52d5-44b0-933a-232dc57f459b.jpeg"  width="200" height="444"/> <img src="https://user-images.githubusercontent.com/96765048/148054328-68c96e9b-e208-4cd2-9360-af002c2070f7.jpeg"  width="200" height="444"/> <img src="https://user-images.githubusercontent.com/96765048/148054372-06dc369c-8c27-4536-9471-a7eeb7ee9ca3.jpeg"  width="200" height="444"/> <img src="https://user-images.githubusercontent.com/96765048/148054481-6553d830-1638-4448-a257-ef38adee8e7c.jpeg"  width="200" height="444"/>

### Gallery tab 
- You can bring up the pictures on the device.
- You can swipe to delete the images from the gallery tab. (It won't be deleted from your phone.)

<img src="https://user-images.githubusercontent.com/96765048/148055651-2aad21fb-7e33-4727-b6c0-ab145e061ab4.jpeg"  width="200" height="444"/> <img src="https://user-images.githubusercontent.com/96765048/148055733-a6ce2991-c993-4ed0-8547-bd04ce7cd675.jpeg"  width="200" height="444"/> <img src="https://user-images.githubusercontent.com/96765048/148055765-bd5c2320-f363-4504-96a6-af3f65e5cc53.jpeg"  width="200" height="444"/> 

### Game tab 
- You can play a simple game.
- After the game, you can share the score using contact tab.(Automatically, the score is stored in the gallery tab.)


<img src="https://user-images.githubusercontent.com/96765048/148054549-85e1f4d8-9af2-40e0-ab3e-6be4f6f54931.jpeg"  width="190" height="424"/> <img src="https://user-images.githubusercontent.com/96765048/148054597-54bcbd5b-4aed-4a9d-854b-3d0dbcde41d2.jpeg"  width="190" height="424"/>  <img src="https://user-images.githubusercontent.com/96765048/148054649-0a65d391-2de6-48d4-a007-f62c74ec686b.jpeg"  width="190" height="424"/>  <img src="https://user-images.githubusercontent.com/96765048/148054685-206d80ab-1ceb-49f1-a420-2c8ac6487b63.jpeg"  width="190" height="424"/> <img src="https://user-images.githubusercontent.com/96765048/148054720-c815ccdc-fe6e-4f05-81f7-807b7589ead6.jpeg"  width="190" height="424"/>

## Development process
### Contact
- Used recyclerview
- Used searchview
- Used contactcontract
### Gallery
- Used gridview
- Used photoview library
- Used jsonobject to load saved status
- Used viewpager
### Game
- Used tableview




License
--------

    Copyright 2018 Chris Banes

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
입사 후 약 한 달 동안은 스플 안드로이드에서 이용하는 기술 스택을 익히고 스플의 코드를 이해하는 과정을 거쳤습니다. 온보딩 과제가 끝난 후에는 스프린트에 참여하며 처음으로 실제 스플 프로젝트에서 작업을 할 수 있게 되었습니다. 첫 스프린트를 진행하면서 git flow 전략도 실제로 사용해보고, 저희가 구현한 기능들이 QA를 거쳐 플레이스토어에 릴리즈되는 것까지 경험해볼 수 있었습니다.

그리고 저희는 애자일의 방법 중 하나로 한 컴퓨터를 가지고 번갈아가며 코딩을 하고 다른 한명은 이를 지켜보며 검토를 해주는 방식인 페어프로그래밍 방식을 사용하여 스프린트를 진행하였습니다.

# 컨텐츠 인턴 스프린트

첫 스프린트에서는 효과음 On/Off 기능을 구현하는 것과 자연어 입력 에디터 창 구현 및 키보드 컨트롤을 구현하는 것을 진행했습니다.

## 효과음 On/Off 기능 구현

효과음 버튼을 만든 후, 해당 버튼을 눌렀을 때 효과음만을 켜고 끌 수 있도록 하는 기능을 구현하는 피쳐였습니다. 기존 코드에 효과음 on/off를 위한 함수는 구현되어있었지만 배경음 버튼에 통합되어 실행되고 있는 상태였습니다. 그래서 배경음 버튼과 분리하는 작업을 진행했습니다.

효과음 켜진 상태             |  효과음 꺼진 상태             |  배경음과 효과음 모두 있는 경우 |  배경음 껐을 때
:-------------------------:|:-------------------------:|:-------------------------:|:-------------------------:
<img src="https://user-images.githubusercontent.com/68413811/168750277-543ec44f-3153-4972-a135-d3a7201a120d.jpg"/>  |  <img src="https://user-images.githubusercontent.com/68413811/168750588-c2c08f70-03e0-417b-bd68-ae7f4944a638.png"/>  |  <img src="https://user-images.githubusercontent.com/68413811/168750641-40268e52-38ab-4f89-9752-5a13b5e3a58c.png"/>  |  <img src="https://user-images.githubusercontent.com/68413811/168750677-3670c9c8-2c39-4c82-96e1-df8663bf452b.png"/>

우선 아래와 같이 ViewModel에 효과음의 on/off 상태를 관리할 수 있는 LiveData를 추가 했고, 이 상태를 Fragment에서 옵저빙 할 수 있도록 했습니다.  

```kotlin
private val _effectBtnState = MutableLiveData(SoundBtnState.ON)
val effectBtnState: LiveData<SoundBtnState> = _effectBtnState
```

Fragment에서는 추가한 효과음 버튼 UI에 OnClickListener를 설정하여 효과음 버튼을 클릭한 경우 효과음의 state 값을 바꾸고, 토스트를 띄울 수 있도록 추가했습니다. 추가적으로 배경음 버튼에서 효과음을 처리하는 부분은 삭제하고, 배경음 버튼을 클릭했을 때 배경음 on/off에 대한 토스트를 띄우는 코드를 추가했습니다.

해당 피쳐의 가장 중요한 기능인 효과음을 실제로 끄는 기능은 아래 코드와 같이 작품의 스크립트를 처리할 때, Effect 타입을 만난 경우 효과음 state가 ON인 경우에만 효과음 이벤트를 전달할 수 있도록 구현했습니다.

```kotlin
private fun procNextChat(
        item: ScriptEntity?,
        currentList: MutableList<Chat>,
        isAutoScroll: Boolean = false
    ) {
        ...
        when (item) {
			...
            is ScriptEntity.Effect -> {
                if (item.isBgm) {
                    ...
                } else if (item.isVib) {
                    ...
                } else {  // Effect가 효과음인 경우
                    if (effectBtnState.value == SoundBtnState.ON) {
                        _soundEffectOnEvent.value = Event(item.text)
                    }
                    nextChat()
                }
            }
			...
		}
		...
	}
```

해당 피쳐 구현을 진행하며 채팅 화면에 효과음 버튼을 새로 추가했는데, 이를 진행하면서 디자인 요구사항도 고려하여 구현을 진행했어야 했습니다. 효과음 버튼은 모든 작품에 나타나지만, 배경음 버튼은 배경음이 있는 작품에서만 나타날 수 있도록 구현을 진행했습니다. 이때 주의해야할 점은 사진과 같이 아이콘과 parent view의 top 사이의 거리와 두 아이콘 사이의 거리가 다르다는 것이었습니다. 그래서 배경음이 있는 경우와 없는 경우에 따라 효과음 버튼의 marginTop을 다르게 지정해주는 방식으로 구현했습니다.

<img width="82" alt="스크린샷 2022-05-09 오후 3 18 30" src="https://user-images.githubusercontent.com/68413811/168751824-a8c5ce21-8be3-49e1-aa66-15414d2cbe06.png">

```kotlin
override fun observeUi() {
	with(viewModel) {
		...
		observe(hasBgm) {
		    binding.soundButton.visibility = if (it) View.VISIBLE else View.GONE
						
			// 배경음악 존재 여부에 따라 버튼 margin 값 설정
		    val marginTopWithBgm = 8f.dpToPx(requireContext())
	        val marginTopWithoutBgm = 12f.dpToPx(requireContext())
		    val marginRight = 16f.dpToPx(requireContext())
	        if (it) {
	            (binding.effectButton.layoutParams as ViewGroup.MarginLayoutParams).apply {
	                setMargins(0, marginTopWithBgm, marginRight, 0)
			    }
	        } else {
	            (binding.effectButton.layoutParams as ViewGroup.MarginLayoutParams).apply {
	                setMargins(0, marginTopWithoutBgm, marginRight, 0)
	            }
	        }
       }
				...
	}
}
```

---

## 자연어 입력 에디터 창 구현 및 키보드 컨트롤

이 피쳐에서는 사용자가 자연어 입력으로 답변을 할 수 있도록 자연어를 입력할 수 있는 에디터 창을 구현하였습니다. 이 피쳐는 당장 작품에서 나타나는 기능은 아니기 때문에 자연어 입력창을 강제로 띄워 개발한 피쳐를 확인했고, 입력창 View의 상태를 invisible로 설정하여 현재의 앱에서는 보이지 않는 상태입니다.  
<img src="https://user-images.githubusercontent.com/68413811/168751978-b86929f7-1d8b-44d8-a7ea-33b579c60621.gif"  width="270"/>

위와 같이 입력창을 클릭하면 키보드가 올라와 사용자가 직접 대사를 입력할 수 있습니다. 해당 피쳐의 세부적인 기능은 다음과 같습니다.  

1. 입력칸에 글자가 있을 시 ✖️ 아이콘을 표시하고, 아이콘 클릭 시 입력한 글자를 삭제한다.
2. 한 글자 이상, 최대 글자 수 미만 작성 시 보내기 버튼 활성화시키고, 이외의 경우에는 비활성화 시킨다.
3. 보내기 버튼의 왼쪽에 **입력한 글자 수 /  최대 글자 수**를 표시한다.
4. 입력한 글자 수가 최대 입력 글자 수에 도달하면 더 이상 글자를 입력하지 못하게 하고 입력창 하단에 경고 문구를 표시한다.
5. 입력 가능한 최대 글자 수는 설정 가능하다.
6. 키보드가 올라가면 하단 배경은 따라 올라오지 않고, 채팅과 입력창은 키보드 위로 올라오도록 구현한다.

해당 기능들을 구현하기 위해 우선 입력창을 위한 Custom View를 만들었습니다. 입력 칸에 글자 개수에 따라 변화가 일어나는 기능들을 위해 EditText View에 doOnTextChanged 콜백을 달아 UI 변화를 처리했습니다.

```kotlin
// ChatInputView
editText.doOnTextChanged{text, _, _, _->
	if (text.isNullOrBlank()) {    // 입력한 내용이 없을 때
	    // Count 값 0/max 로 설정
        val countString = "0/$maxCount"
        textCount.text= countString
		// 보내기 버튼 비활성화
		chatSend.setImageResource(R.drawable.ic_chat_send_disabled)
		// ✖️ 버튼 비활성화
        changeViews(false)
	 } else {    // 입력한 내용이 있을 때
	    // Count값 입력한 글자 수로 설정
        val count = text.length
        val countString = "$count/$maxCount"
        textCount.text = countString
		// 보내기 버튼 활성화
        chatSend.setImageResource(R.drawable.ic_chat_send_enabled)
		// ✖️ 버튼 활성화
        changeViews(true)

		// 입력 글자 수가 최대를 넘었는지 확인하여 UI 변경
        if (count >= maxCount) {
		    changeViewOverCount(true)
        } else {
            changeViewOverCount(false)
        }
    }
}
```

그리고 입력창의 Custom View를 구현할 때, 이미 구현되어 있는 댓글 입력창의 Custom View를 참고하여 구현했는데, 세부적인 기능은 다르지만 입력창이라는 근본적인 속성은 동일하기때문에 많은 양의 코드가 중복되는 문제가 있었습니다. 따라서 두 입력창의 공통적인 요소를 CommentInputView라는 추상클래스로 분리했고, 각 입력창은 이를 상속받도록 하여 중복되는 코드들을 제거할 수 있었습니다.

이 피쳐를 개발하면서 가장 어려웠던 부분은 채팅화면에서 키보드가 올라올 때, 모든 화면이 키보드 위로 함께 밀려나는 이슈였습니다. 
<img src="https://user-images.githubusercontent.com/68413811/168752352-523217eb-444a-4388-8eb7-e17b713a7864.gif"  width="270"/>

이슈가 발생했던 화면의 상태는 위와 같습니다. 

구글링을 통해 AndroidMenifest에서 `windowSoftInputMode` 라는 옵션을 이용하여 키보드가 올라올 때, 배경의 레이아웃을 조절해줄 수 있다는 것을 발견하였습니다. 하지만 이 옵션을 수정하니 입력창까지 키보드에 가려지는 것은 물론 채팅도 일부분 가려지는 경우가 발생했습니다.

고민을 해본 결과, 키보드가 올라올 때 하단 배경이 사라지도록 설정하면 요구사항을 만족할 수 있다는 점을 깨달았습니다. 그래서 리스너를 달아 키보드가 올라오는 경우 하단 배경의 visibility를 GONE으로 변경했습니다. 하지만 배경 이미지만 사라진 채로 이미지가 차지하던 공간은 그대로 남아있는 문제가 발생했습니다.

하단 배경과 관련된 뷰를 모두 없앴는데 왜 공간은 사라지지 않는지 한참 고민하며 코드를 다시 살펴보던 중 채팅을 띄우는 RecyclerView의 아래 부분에 하단 배경의 높이만큼 padding이 설정되어있는 것을 발견했습니다. 그래서 키보드가 올라온 경우에는 RecyclerView 아래쪽 padding의 크기가 EditText의 높이를 기준으로 변경될 수 있도록 코드를 수정하여 이슈를 해결하였습니다.

```kotlin
// ChatFragment
chatInputView.setOnEditTextClickListener {
	// keyboard 안보일 때 visibility = View.Visible
	// keyboard 보일 때 visibility = View.Gone
	val visibility = if (it) View.VISIBLE else View.GONE
	imgChatBackground.visibility = visibility
    imgChatBackgroundOverlay.visibility = visibility
    backgroundBottom.visibility = visibility

    val height = (displayWidth * 240f / 375f).toInt()
    val paddingBottom = (resources.displayMetrics.density * 14f).toInt()
    val chatInputViewHeight = chatInputView.height
		
	// keyboard 보임 여부에 따라 채팅 recyclerView의 padding 설정 
	if (it) {  //keyboard 안보일 때
        recyclerChat.setPadding(0, 0, 0, height + paddingBottom)
    } else {  //keyboard 보일 때
        recyclerChat.setPadding(0, 0, 0, paddingBottom + chatInputViewHeight)
    }

    recyclerChat.scrollToPosition(adapter.itemCount- 1)
}
```

---

# 20220429 스파이크

## 내 수치 단위 표시
<img width="300" src="https://user-images.githubusercontent.com/68413811/168752594-c9975f9b-6248-44f1-99d3-fbe882456f91.png">

인턴 스프린트를 마무리한 후 내 수치화면에서 나타나는 수치에 단위를 표시할 수 있도록 해주는 간단한 스파이크 피쳐를 개발을 진행했습니다. 

서버에서 새로 추가된 속성의 단위를 갖고 있는 unit 이라는 필드를 받아와 화면에 띄워주면 되는 간단한 기능이지만, data layer와 usecase layer 등 여러 레이어를 거치며 데이터가 계속 가공되어 전달되기 때문에 처음에 데이터의 흐름을 파악하는 부분에서 조금 헤매었습니다.

이후 진행하는 스프린트에서도 계속해서 데이터를 주고받는 작업이 포함되는데, 전체적인 흐름은 거의 비슷하기 때문에 스플 안드로이드 앱에서 데이터가 전달되는 흐름을 정리해보았습니다.  
<img src="https://user-images.githubusercontent.com/68413811/168753128-5415ae8a-bb5f-4a2d-b0d0-c1fe7a3f669f.png"  width="700"/>

1. 스플에서는 데이터를 주고받기 위한 쿼리 언어로 REST API가 아닌 GraphQL을 사용합니다. GraphQL에서 Query를 통해 Read를 수행할 수 있고, Mutation을 통해 Create, Update, Delete를 수행할 수 있습니다.
2. ApiService에서는 GraphQL API를 호출하여 데이터를 가져오는데, 이렇게 GraphQL을 통해 받아오는 데이터는 가공되지 않은 Dto의 형태를 띠고 있습니다.
3. 그리고 중간 레이어로 UseCase layer가 존재하여 Dto 형태의 데이터를 여러가지 Mapper를 통해 중간 가공하여 Entity 형태로 만들어줍니다.
4. 그러면 ViewModel에서는 Entity 형태의 데이터를 받아와 View에 뿌려주기 용이한 형태인 Model 로 최종 가공을 해주고, LiveData에 최종적인 형태의 데이터를 세팅해주게 됩니다.
5. 최종적으로 Fragment 와 같은 View에서는 ViewModel의 LiveData를 Observing 하고 있다가 데이터가 들어오면 View를 렌더링해주게 됩니다.  
    <img src="https://user-images.githubusercontent.com/68413811/168753148-1d840e1c-98e2-4043-a980-edef712ee649.png"  width="700"/>

    

위의 그림에서 서버로부터 다이얼로그 뷰까지 내 수치 값이 전달되는 과정을 간단하게 나타내보았습니다. 여기서 저희는 unit 이라는 String 값을 이러한 데이터 흐름을 따라 계속 전달해주었습니다.

그래서 최종적으로 View에 도달한 데이터를 숫자 뒤에 그대로 붙여주면 완성입니다.

---

# 220503 컨텐츠 스프린트

스파이크가 마무리 된 후에는 스플 컨텐츠 개발팀의 다음 스프린트에 함께 참여했습니다.

저희는 이 스프린트에서 사용자의 타입을 선택할 수 있는 온보딩 팝업을 추가하였고, 온보딩 팝업이 끝날 때 선택된 데이터가 서버에 저장될 수 있도록 하는 부분을 담당했습니다. 그리고 그 기능을 마무리한 이후 추가적으로 선택지 확률 다시보기 팝업을 구현하였습니다.

## 온보딩 팝업 유저타입 추가 및 서버 데이터 변경 및 전송

해당 피쳐는 유저 타입을 추가하여 일반 선택 형태의 온보딩 팝업과 별개로 내부에서 유저 타입을 선택할 수 있도록 구현하는 것이었습니다. 또한, 선택한 유저 타입에 따라 이후에 나타나는 온보딩 팝업을 제어할 수 있도록 해야 했습니다. 해당 피쳐의 목표는 다음과 같습니다.

1. 유저 타입을 정의하고 온보딩 팝업에 유저타입을 추가할 수 있도록 수정
2. 마지막 온보딩 팝업에서 “시작하기"를 눌렀을 때, 서버에 선택된 유저타입 데이터 전송

### 유저 타입 정의 및 온보딩 팝업 수정

온보딩 팝업에 대한 데이터도 위에서 설명드렸던 흐름과 비슷한 과정을 거쳐 전달됩니다. 아래의 그림에서는 온보딩 팝업 관련 데이터가 가공 되는 과정을 간단히 정리하였습니다.  
 <img src="https://user-images.githubusercontent.com/68413811/168753535-d1f38884-e92e-4251-9039-abfeef2d7fe8.png"  width="400"/>



온보딩 팝업 데이터가 GraphQL의 쿼리로부터 ChatOnBoardingDialog까지 전달되는 흐름에 따라 각 데이터 타입에서 playerClassId와 playerClass.name이라는 유저 타입 정보를 추가로 받아올 수 있도록 수정해주었습니다. 

- 이때, 유저 타입 팝업의 경우 아래 코드와 같이 기존 온보딩 팝업의 OnBoardingChoice.Text 를 재사용하여 playerClassName을 선택지 텍스트로 렌더링 할 수 있도록 처리해주었습니다.
    
    ```kotlin
    // OnBoardingPopupChoiceMapper
    if (item.playerClassId != null) {
    	return OnBoardingChoice.Text(
    		...
    		text = item.playerClassName ?: "",
    	)
    }
    ```
    

작품의 온보딩 팝업에서는 특정 선택지를 선택할때마다 해당 선택지에 종속되어있는 속성값들이 내부적으로 저장되고, 저장된 속성값에 따라 이후에 나타날 팝업이 달라지게 됩니다. 저희는 속성값 뿐만이 아니라 선택한 유저 타입에 따라서도 이후 나타나는 팝업을 제어할 수 있도록 구현해야했습니다.

이를 위해서는 우선 이해해야할 변수가 몇가지 있습니다.

1. descriptionEffect : 온보딩 팝업의 각 선택지 데이터에는 descriptionEffect 라는 `Map<String, Int>` 타입의 필드가 존재하며, 해당 선택지가 영향을 주는 속성값들을 나타냅니다. Map의 key로는 해당 선택지를 선택했을 때 얻게되는 속성값의 종류가 들어가고 value로는 속성값의 수치가 들어가게 됩니다.
2. visibleConditions : 각 온보딩 팝업에는 visibleConditions 라는 `List<Map<String, Any>>` 타입의 필드가 존재하며, 해당 온보딩 팝업이 나타나기 위한 조건들을 나타냅니다. 
    
    이 필드에는 아래와 같은 json 형태가 List<Map<String, Any>> 형태로 변환된 값이 들어가게 되고, Map의 key로는 “property”, “value”, “inequality” 의 세가지 값이 들어가게 됩니다. 
    
    커뮤니케이션을 통해 서버에서 유저 타입에 따른 조건은 visibleConditions에서 아래와 같은 형태로 내려주기로 하였습니다.
    
    ```json
    "visibleConditions": [
      { // 속성 일 때,
        "property": "귀여움",
         "value": 10,
         "inequality": "Equal"
       },
    	{// 사용자 클래스 일 때,
        "property": "__playerClass__", //유저타입의 경우 property는 무조건 이 단어!
         "value": 1,
         "inequality": "Equal"  //ex) NotEqual..
       },
    ]
    ```
    

기존 온보딩 팝업에서는 selectedResult의 descriptionEffect에 현재까지 선택한 속성들을 저장하고 다음에 띄울 온보딩 팝업을 선택할 때, 온보딩 팝업의 visibleCondition과 비교하여 온보딩 팝업을 제어하고 있었습니다. 

그래서 저희는 선택지에 대한 데이터가 가공되는 경로에서 다음과 같이 선택지의 descriptionEffect에 <”__playerClass_”, playerClassId> 쌍을 추가적으로 넣어주었습니다.

```kotlin
descriptionEffect = descriptionEffect?.apply {
	descriptionEffect[PLAYER_CLASS] = choice.playerClassId!!
} ?: mapOf(PLAYER_CLASS to choice.playerClassId!!)
```

이렇게 하면 기존에 descriptionEffect를 통해 속성값에 따라 온보딩 팝업을 제어하던 로직을 그대로 사용하여 유저 타입에 따라 온보딩 팝업을 제어하는 일도 함께 처리할 수 있게 됩니다.

### 서버 데이터 변경 및 전송

서버 데이터 변경 및 전송 단계에서는 위에서 저장한 playerClassId를 StartStoryMutation의 인자로 전달하여 서버에 온보딩 팝업에서 선택된 유저 타입 정보를 저장하는 작업을 진행했습니다. 이후 플레이그라운드에서 내가 선택한 유저 타입이 잘 저장 되었는지 확인하는 과정을 거쳤습니다.  

 <img src="https://user-images.githubusercontent.com/68413811/168753637-793cc4e4-f803-4737-b5a0-e68af8f00e49.png"  width="700"/>

위의 그림에서 온보딩 팝업을 마무리하고 시작하기 버튼을 클릭 했을 때의 데이터 전송 경로를 간단히 정리해보았습니다.

1. ChatOnBoardingDialog에서는 onResultEvent를 옵저빙하고, 이벤트가 전달된 경우 Fragment에서 전달된 onConfirmClick 콜백 함수에 온보딩 팝업의 결과를 전달합니다.
2. onConfirmClick에서는 ViewModel의 startFirstEpisode() 함수를 호출합니다.
3. 이후 UseCase → ApiService → GraphQL의 순서로 playerClassId를 인자로 전달하여 최종적으로 서버에 데이터를 전송할 수 있도록 구현했습니다.  

서버에 저장된 데이터 확인을 위한 쿼리             | 좌측 쿼리의 결과        
:-------------------------:|:-------------------------:
<img src="https://user-images.githubusercontent.com/68413811/168753998-86841ce5-d123-4b7b-b03d-dc6ebbf1b922.png"/>  |  <img src="https://user-images.githubusercontent.com/68413811/168754013-fa9ab566-640e-4f99-98b7-e99d14d9637b.png"/>

서버에 사용자가 선택한 유저 타입 정보가 잘 저장 되었는지 확인하는 과정은 플레이그라운드에서 쿼리를 찍어서 확인하는 방식으로 진행했습니다.

---

## 선택지 확률 다시보기 팝업

선택지 확률 다시보기 팝업 피쳐에서는 확률 다시 보기 아이콘을 클릭했을 때, 해당 선택지에 대한 확률 정보를 팝업으로 띄워주는 기능을 구현해야 했습니다. 해당 피쳐의 요구 기능은 다음과 같습니다.

1. 선택지 확률 다시보기 팝업 구현
2. 선택지 확률 데이터를 서버에서 가져와 다시보기 팝업에 표시

### 선택지 확률 다시보기 팝업 레이아웃 구현

선택지 확률 다시 보기 팝업은 왼쪽 사진과 같이 경문님께서 작업하신 선택지 확률 레이아웃을 이용하여 구현을 하였는데, 이때 xml이 아닌 Compose로 UI를 구현했습니다. 

스토리 진행 중 선택지 확률 표시 화면 | 선택지 확률 다시보기 팝업 화면        
:-------------------------:|:-------------------------:
<img src="https://user-images.githubusercontent.com/68413811/168754318-f15c287d-1f1b-46ea-a762-a7452aef7b0e.png"/>  |  <img src="https://user-images.githubusercontent.com/68413811/168754329-d66f6b4a-9cfd-4cbb-be87-ff5ecef2ee67.png"/>

위의 진행 화면과 같이 스토리 진행 중 전체 화면으로 나타나는 선택지 확률 표시 UI와 확률 다시 보기 팝업 UI에서 선택지 제목 및 확률을 표시하는 흰색 창은 동일한 UI를 사용하고 있습니다. 그런데 처음에는 Compose를 사용하는 이유를 제대로 이해하지 못하고 위의 두 사진의 흰색 창의 코드를 중복하여 작성하였습니다. 이 피쳐에 대한 코드 리뷰를 받은 후, 공통되는 UI를 별개의 Composable 함수로 분리하여 재사용할 수 있도록 코드를 수정하여 Compose가 UI를 재사용하는 경우에 매우 유리함을 깨달을 수 있었습니다. 

- 아래의 코드와 같이 두 화면에서 모두 사용하는 공통된 UI는 LayoutSelectedWithPercents에 구현하여 각 화면에 맞게 데이터와 modifier를 인자로 주어 화면을 그릴 수 있도록 하였습니다.

```kotlin
// 선택지 확률 다시보기 팝업 UI
@Composable
fun LayoutSelectedWithPercentsDialog(viewModel: ChatViewModel = viewModel()) {
    val data = viewModel.showSelectedWithPercentDialogEvent.observeAsState()
    data.value?.getContentIfNotHandled()?.let{
		ConstraintLayout(
            ...
        ){
			val (imgCancel, dialogLayout) = createRefs()

			Image(
              ...
	        )
					
			// 공통된 UI 이용
			**LayoutSelectedWithPercents**(
                onTypeListener = { type ->
				    viewModel.onPercentDialogType(type)
			    },
                  data =it,
                  modifier = Modifier
                    .constrainAs(dialogLayout){
						...
					}
					.padding(start = 20.dp, top = 36.dp, end = 20.dp, bottom = 20.dp)
            )
		}
    }
}
```

팝업에 띄우는 데이터는 ViewModel에 더미데이터를 넣어주었고, Compose UI에서 Event을 옵저빙하여 이벤트 발생 시 ViewModel의 데이터를 팝업에 표시할 수 있도록 했습니다.

하지만 이 과정에서 ChatViewModel의 데이터가 Dialog에 제대로 전달 되지 않는 문제가 발생했습니다. Dialog에 만들어진 ViewModel이 ChatFragment에서 만들어진 객체와 별개로 새로 생성되어 생긴 문제였습니다. 이를 해결하기 위해 Dialog에 ViewModel을 직접 주입해주어 같은 객체가 사용될 수 있도록 하였습니다.

### 선택지 확률 다시보기 API 통신 및 팝업에 표시

<img src="https://user-images.githubusercontent.com/68413811/168754550-4dce88f5-82c0-4a1f-ad4b-980208ee1475.png"  width="700"/>


앞의 태스크에서는 선택지 확률 다시보기 UI만 구현하였기 때문에 API 통신을 통해 서버에서 실제 데이터를 가져오는 작업이 필요했습니다. 서버 측에서 getUserChoiceResult라는 쿼리를 통해 선택지 확률에 대한 데이터를 받아볼 수 있도록 작업해주셨기 때문에, 저희는 앞서 진행했던 피쳐에서처럼 여러 layer에 걸쳐 쿼리의 인자를 전달하고, 리턴된 데이터를 잘 가공하여 가져오는 작업을 수행하였습니다.

위에 데이터를 가져오는 흐름을 나타낸 것과 같이 왼쪽 화살표를 따라가며 인자들을 전달하여 순차적으로 데이터를 요청하면, 오른쪽 화살표 순서대로 선택지 확률 통계에 대한 가공된 데이터가 최종적으로는 Dialog에 전달되고 이것이 반영된 Dialog가 보이게 됩니다!

# 띵스플로우에서 일하며 느낀점

### [민서]

  회사에서 인턴을 해보는 것이 처음이라 띵플에 와서 경험한 모든 것이 새롭게 다가왔습니다. 인턴 기간 동안 실제 스플의 컨텐츠 스프린트에 직접 참여하며, 계획회의부터 개발 후 QA를 진행하고 실제 저희가 개발한 피쳐가 앱에 릴리즈 되는 과정까지 모두 경험해 볼 수 있어서 신기하기도 했고, 이 과정에서 많은 것을 배울 수 있었던 것 같습니다.

  온보딩이 끝난 후 스프린트에 참여하여 개발을 진행할 때에는 페어프로그래밍 방식으로 개발을 진행해보는 경험을 해볼 수 있었는데요, 페어프로그래밍으로 개발을 진행하면서 다윤님과 많은 커뮤니케이션을 하며 개발을 진행했습니다. 이렇게 함께 코딩을 하면서 다양한 아이디어를 공유하며 더 나은 코드를 짤 수 있었던 것 같습니다. 그리고 스프린트를 진행하면서 커뮤니케이션을 통해서 협업하는 방법도 배울 수 있었습니다. 하나의 피쳐를 만들기 위해서 기획, 디자인, 개발이 모두 얽혀있기에 함께 개발을 진행하는 안드로이드 개발자 뿐만 아니라 다른 직무의 팀원과도 원활한 소통을 진행하면서 개발을 진행하는 것이 중요하다는 점을 깨달을 수 있었습니다. 스프린트 계획회의, 데일리 스크럼, 슬랙을 통한 소통을 통해 피쳐를 개발하는 데에 있어 더 나은 방법을 고민하는 과정의 중요성을 직접 느낄 수 있었습니다.

  그리고 실제로 운영되는 안드로이드 앱 개발에 참여하고, 코드 리뷰를 통해서 안드로이드 개발에 대해서도 많이 배울 수 있었습니다. 온보딩 과제를 통해 처음 들어 본 안드로이드 기술 스택들도 익힐 수 있었고, 스플 코드를 이해하며 실제로 앱에서는 공부한 기술 스택들이 어떻게 활용되고 있는지 확인할 수 있었습니다. 그리고 스플 앱 개발에 참여하면서 과제에서 익혔던 내용을 적용해보면서 실제 안드로이드 개발에 대해서 배울 수 있었던 것 같습니다.

  띵스플로우에서 인턴으로 보낸 시간이 정말 빠르게 지나간 것 같습니다. 인턴을 시작하기 전에는 걱정도 많았는데, 스플 컨텐츠 개발팀에서 일을 하면서 정말 즐거웠고, 새로운 경험을 통해서 많이 배우고 성장할 수 있었던 것 같습니다. 저의 첫 인턴 생활을 띵플에서 좋은 사람들과 함께 할 수 있어서 정말 행복했고, 앞으로도 평생 잊지 못 할 경험이 될 것 같습니다!

### **[다윤]**

  띵스플로우에서 인턴을 시작한지 어느새 두달이 지났네요. 몰입캠프에서 강연을 통해 처음으로 띵스플로우라는 회사를 접하고 관심을 갖게되었는데, 이렇게 짧은 기간이지만 인턴으로 함께할 수 있게 되어 정말 행복했고 잊지 못할 경험이 될 것 같습니다.

  지금 생각해보면 처음 인턴을 시작할때는 거의 아무것도 모르던 상태였고, 무려 코틀린조차 알지 못해서 자바로만 안드로이드 앱 개발을 해봤던 상태였습니다. 인턴을 시작하고 한달동안은 여러가지 기술스택을 공부하고, 온보딩 과제를 수행했습니다. 그리고 제가 짠 코드를 실무자에게 리뷰받고, 또 제가 다른 사람의 코드리뷰를 하며 배울만한 점을 찾으며 안드로이드 앱 개발의 기초를 쌓을 수 있었던 것 같습니다.

 그리고 온보딩 기간이 끝나고 실제 스토리플레이의 기능을 구현하며 스프린트에 참여하게 되었는데요..! 온보딩을 통해 열심히 공부했지만, 실제 상용화되는 앱 개발에 참여하는 것은 처음이라 기대반 걱정반인 마음이었습니다😂  그런데 다행히도 같이 인턴을 시작하신 민서님과 페어프로그래밍을 할 수 있게 되어 좀 더 편안한 마음으로 참여할 수 있었고 더 재미있게 인턴 기간을 보낼 수 있었던 것 같습니다!

 또 학교 수업에서 이론으로만 배웠던 애자일에 대해서도 데일리스크럼, 백로그그루밍, 스프린트등을 통해 직접 경험해볼 수 있었고, 다양한 직무에서 일하는 사람들과도 협업해보고 현직에서 어떻게 일이 진행되는지 가까이서 지켜볼 수 있는 좋은 기회였습니다. 특히 git flow 전략이나, CI/CD, lint check와 같이 이전에는 알지 못했던 부분들을 실제로 사용해보는 경험도 새로웠습니다!

 살면서 처음으로 해본 회사생활이어서 걱정이 많았는데, 많은 분들이 언제나 친절하게 대해주시고 모르는 부분이 있으면 잘 알려주셔서 잘 적응할 수 있었던 것 같습니다.

스토리플레이 안드로이드 개발자로 띵스플로우에서 보낸 두달동안 많이 배우고 성장할 수 있었고, 띵스플로우를 떠나더라도 계속 스토리플레이를 지켜보며 응원하겠습니다!! 🥳
