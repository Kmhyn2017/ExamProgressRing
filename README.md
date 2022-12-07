# ExamProgressRing

Xaml코드
<StackPanel Grid.Row="1" Grid.Column="0">
            <ProgressRing x:Name="ProgressRing" Height="60" Width="60" Margin="10"/>
            </StackPanel>
            <StackPanel Grid.Row="1" Grid.Column="1" Margin="100,10,0,10">
                <ToggleSwitch x:Name="ProgressToggle" Header="토글 스위치" OffContent="작동하기" OnContent="작동 중" 
                              IsOn="True" Visibility="Visible" Toggled="ProgressToggle_Toggled" />
            </StackPanel>
