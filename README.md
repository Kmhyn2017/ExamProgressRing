# ExamProgressRing 구현 예제
---
### Xaml코드  
```
<StackPanel Grid.Row="1" Grid.Column="0">
          <ProgressRing x:Name="ProgressRing" Height="60" Width="60" Margin="10"/>
</StackPanel>
<StackPanel Grid.Row="1" Grid.Column="1" Margin="100,10,0,10">
         <ToggleSwitch x:Name="ProgressToggle" Header="토글 스위치" OffContent="작동하기" OnContent="작동 중" 
                      IsOn="True" Visibility="Visible" Toggled="ProgressToggle_Toggled" />
</StackPanel>
```          
#### 행 1에 프로그래스 링과 토글 버튼을 놓아줍니다. 열 0에는 프로그래스 링이 들어가고,   
#### 열 1에는 토글버튼을 놓아줍니다.   
#### 토글은 IsOn으로 켜짐으로 하여 프로그래스 링이 보이도록 합니다.   
---
이제 기능 구현을 위한 Xaml.cpp를 작성해줍니다.   
   
---
### Xaml.cpp
```
if (ProgressToggle().IsOn()==true) {
    ProgressRing().IsActive(true);
    ProgressRing().Visibility();
}
else {
    ProgressRing().IsActive(false);
}
```
#### 토글버튼이 켜저 있다면 프로그래스 링을 작동 시키고 링이 보이게합니다.
#### 그렇지 않다면 링을 작동 시키지않고 대기합니다.
---
### 실행화면
![제목 없는 동영상 - Clipchamp로 제작](https://user-images.githubusercontent.com/92089428/206246034-91397409-b0ce-41b0-8fe2-ad5efd1492e6.gif)
---
