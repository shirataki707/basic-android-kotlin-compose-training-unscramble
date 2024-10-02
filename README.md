Unscramble app
=================================

Single player game app that displays scrambled words. To play the game, player has to make a
word using all the letters in the displayed scrambled word.
This code demonstrates the Android Architecture component- ViewModel and StateFlow.

Screenshot
----------

<p align="center">
  <img src="https://github.com/user-attachments/assets/9468eaa4-de98-4f68-a044-1152fda92256" width="300">
</p>

Learn
-----
- Architecture
  - - ViewModelとuiStateを用いた単方向データフロー
  
![61eb7bcdcff42227_856](https://github.com/user-attachments/assets/ca31fedb-3736-41f1-adc3-b8f065ec94bb)

- Unit test for ViewModel
  - testImplementationを使うことで、テスト用のライブラリを追加できる(本番のapkには含まれない)
    ```kotlin
    testImplementation("junit:junit:4.13.2")
  - Composeのテストのときは、Bomを使うことでライブラリのバージョンを統一できる
    ```kotlin
    androidTestImplementation(platform("androidx.compose:compose-bom:2023.06.01"))
    androidTestImplementation("androidx.compose.ui:ui-test-junit4")
  - Test Strategy
    - Success path
      - ハッピーパステスト。意図された正常な動作を確認するテスト
    - Error path
      - 意図しないエラーが発生した場合のテスト。網羅が難しいので、単体テストを改善していくことが重要
    - Boundary path
      - アプリがロードされたときのUI状態など。状態の変化を確認するテスト
  - 命名
    - thingUnderTest_TriggerOfTest_ResultOfTest
      - thingUnderTest = gameViewModel
      - TriggerOfTest = CorrectWordGuessed
      - ResultOfTest = ScoreUpdatedAndErrorFlagUnset
  - Test Coverage
    - Testを右クリックして、"Run Test with Coverage"を選択
    - カバー率が表示され、クリックしてファイルを見るとどの部分がテストされていないかがわかる



Pre-requisites
--------------
* Experience with Kotlin syntax.
* How to create and run a project in Android Studio.
* How to create composable functions 


Getting Started
---------------
1. Install Android Studio, if you don't already have it.
2. Download the sample.
3. Import the sample into Android Studio.
4. Build and run the sample.
