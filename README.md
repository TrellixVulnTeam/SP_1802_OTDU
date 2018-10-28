# すまポ

<p align="center">
<a href="https://www.youtube.com/watch?v=yz9begf0ojA&feature=youtu.be"><img src="図1.png" alt="サンプル"></a>
</p>

## 製品概要

### Post×Tech

### 背景（製品開発のきっかけ、課題等）

#### 背景
Eコマースの発達とともに、直近5年では取扱個数が約6.1億個増加しています。（国土交通省HPより）それに伴い配達物の再配達が増加しており、人件費や輸送費などのコスト増加や、CO2排出量の増加が問題となっています。
また、受け手側も、郵便物の不在票に気づきにくいというデメリットがあり、我々は再三に渡る再配達および配達元への返送を防ぐために本プロダクトの開発に至りました。

#### 課題を解決する対象
①配達業者②日中に外出している方々(主に一人暮らしの社会人・学生)

#### 課題・現状
配達業者：不在通知先への再三の配達, 配達元への返送 「何度も再配達したくない」
日中に外出している方々：配達物をなかなか受け取れない,受け取りを忘れ配達物が配達元へ返送されてしまう「スムーズに荷物を受け取りたい」

### 製品説明（具体的な製品の説明）
ポストに宅配物の不在票が届いたことがユーザーのスマートフォンに通知され、リアルタイムに再配達依頼が可能となるIoTデバイスを開発しました。今まで再三にわたって行われていた再配達を不在票の通知をリアルタイムにすることで、配達業者の人件費・輸送費などのコスト削減・輸送に伴うCO2排出量の削減、ユーザーの配達物のスムーズな受け取りを実現します。
<p align="center">
<img src="概要図.jpg">
</p>

<p align="center">
<img src="スライド1.png">
</p>

### 特長
#### 1. 不在票が届いたことが文章と画像でリアルタイムに通知
本プロダクトは，外出時に配達不在票が家に届くとLINE経由ですぐに通知が届くため、居場所を問わないリアルタイムな再配達依頼が可能となります。このため、配達サイクルが効率化されるとともに、配達業者のコスト削減、CO2排出量減少、さらには、ユーザーの不便解消につながります。
#### 2. 全ての配達業者の不在票を判別・一括管理
各配達業者が行う不在票の通知サービスを、本プロダクト一つですべて対応することができます。具体的には、不在票の画像認識により、各配達業者を判別し再配達フォームと電話番号をLINE経由でユーザに通知します。このように各社サービス一括管理の実現によって複数社のサービスを登録・活用しなければいけないユーザーの負担を軽減します。
#### 3. チラシなどの他の投函物と不在票を識別
物音認識によるインターホン音の検知、超音波センサを用いた投函の検知により構成される二段階の構造は、ポストへの投函のみ行われるチラシなどの投函物と、インターホンを鳴らしてから投函される不在票を判別することが可能となります。この構造を用いて不在票のみを検出し、ユーザーへ通知を行うことが可能な仕組みを作りました。

### 解決出来ること
不在票の存在に気付かず再配達が何度も行われてしまうことや、宅配物が配達元へ返送されてしまう問題を解決し、配達業界のコスト削減、配達時に排出されるCO2の削減を実現します。
また、ユーザーの再配達依頼をスムーズにすることで、再配達の荷物受け取りを確実に行います。
本プロダクトを通して、ユーザーと配達事業者とのwin-winの関係を築きます。

### HackDay以降の製品の改善
#### 1.デバイス本体の小型化・軽量化
デバイスが大きく、大型のポストにしか設置できなかったが、機構設計を見直し、デバイスの小型化を行うことで、一人暮らしのマンションなどの小型のポストにも設置可能にした。（デバイスの大きさ：横92mm×奥行170mm、一般的なマンションのポストサイズ：360mm×300mm）またポストへの取り付け方法に磁石を採用することで，取り外しが可能となり、設置の簡易化に取り組んだ。
#### 2.投函の検出のためのセンサーを光センサーから超音波センサーに変更
光センサーではポストの外の明るさにセンサーの反応が依存していたが、超音波センサーを用いることで外的要因に依存しなくなり、不在票投函の検出がより安定化した。
#### 3.投函された不在票の宅配会社を判別・宅配会社に対応したメッセージを送信
今までは投函された不在票の写真をユーザーに送信するだけだったが、NECの画像認識を用いることで、投函された不在票がどこの宅配会社か判別することが可能となり、宅配会社に応じてLINEでの通知を変更し、より簡単に再配達依頼が可能になった。

### 今後の展望
* スマートスピーカーで物音認識が可能になることによる汎用性の向上
* Raspberry Pi zero などを用いることによるさらなるデバイスの小型化
* 配達者側の再配達プラットフォームの構築 

## 開発内容・開発技術
### 活用した技術
#### API・データ
* 物音認識API(NEC)
* 画像認識API(NEC)
* LINE Notify

#### フレームワーク・ライブラリ・モジュール
* Socket通信(TCP/IP )
* Serial通信
* Arduino IDE


#### デバイス
* Raspberry Pi
* Arduino
* 超音波センサ
* Raspberry Pi camera v2

### 研究内容・事前開発プロダクト（任意）
### 独自開発技術（Hack Dayで開発したもの）
#### 2日間に開発した独自の機能・技術
* 独自で開発したものの内容をこちらに記載してください
* 特に力を入れた部分をファイルリンク、またはcommit_idを記載してください（任意）
* 不在票とチラシなどその他投函物の識別システム
物音認識でインターホン音を検知し、超音波センサでポストへの投函を検知する二段階構造にすることで、ポストへの投函のみ行われるチラシなどの他の投函物と、インターホンを鳴らしてから投函される不在票を識別する仕組みを作った。
* サーバ(ポスト側)-クライアント(インターホン音を認識する側)通信およびArduino(超音波センサ)-Raspberry Pi 間の通信システムの構築
