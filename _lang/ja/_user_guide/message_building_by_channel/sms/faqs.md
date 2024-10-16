---
nav_title: FAQ
article_title: SMSよくある質問
page_order: 12
description: "この記事では、SMSキャンペーンの設定時によくある質問のいくつかに対処します。"
page_type: FAQ
channel:
  - SMS
  
---

# よくある質問

> このページでは、SMSに関する最も厳しい質問にお答えしようとしています！

### SMSにリンクを含めることはできますか？

任意のSMSキャンペーンに任意のリンクを含めることができます。しかし、考慮すべきいくつかの懸念があります。

- リンクは、SMSの160文字制限の多くを占める可能性があります。リンクとテキストを含めると、1つではなく2つのSMSメッセージになる可能性があります。
- 企業はリンクの文字数の影響を制限するためにリンク短縮サービスをよく使用します。ただし、長いコードを介して短縮リンクを送信する場合、キャリアはリンクリダイレクトを疑ってメッセージをブロックまたは拒否する可能性があります。
- リンクを含めるには、[短いコード]({{site.baseurl}}/user_guide/message_building_by_channel/sms/sms_setup/short_and_long_codes/)を使用するのが最も信頼性の高い番号タイプです。

Brazeには、リンクを短縮し、クリックスルー分析を自動的に提供する独自のリンク短縮機能もあります。詳細については[リンクの短縮]({{site.baseurl}}/user_guide/message_building_by_channel/sms/campaign/link_shortening/)を参照してください。

### テストテキストメッセージは制限にカウントされますか？

はい、彼らはそうします。メッセージをテストする際にはこれを念頭に置いてください。

### ユーザーはSMSテストメッセージを受信するためにSMSサブスクリプショングループの一員である必要がありますか？

はい、彼らはそうします。ユーザーは有効な電話番号を持ち、テスト送信に使用されるSMSサブスクリプショングループの一部である必要があります。

### SMSメッセージの送信速度を制限する必要がありますか？

デフォルトの同時実行率とスループットにより、ショートコードごとに1時間あたり約360,000メッセージが可能になります。追加のスループットには追加のショートコードが必要です。

### どのようにして超過を避けることができますか？

超過料金が発生しないことをお約束することはできませんが、割り当てられた制限を超える可能性を減らすために、次の予防策を講じることができます。

- SMSの文字数に注意してください。意図せずに複数のSegmentを送信すると、超過が発生する可能性があります。詳細については、[Segmentの内訳]({{site.baseurl}}/user_guide/message_building_by_channel/sms/campaign/segments/#segment-breakdown)を参照してください。
- Liquidまたはコネクテッドコンテンツを考慮してSMS文字を慎重に計算してください。ダッシュボードのBraze SMSコンポーザーは、これらの機能の使用を見積もったり考慮したりしません。
- メッセージのエンコーディングの種類を考慮してください - メッセージがGSM-7エンコーディングを使用している場合、通常、メッセージセグメントあたり128文字のメッセージを送信できると見積もることができます。メッセージが[UCS-2](https://en.wikipedia.org/wiki/Universal_Coded_Character_Set)エンコーディングを使用している場合、通常、メッセージセグメントあたり67文字のメッセージを送信できると見積もることができます。
- テスト、テスト、そしてテスト！ローンチ前に必ずSMSメッセージをテストしてください。特にLiquidとコネクテッドコンテンツを使用する場合は注意が必要です。

### SMSのスパム検出を回避するための最良の送信方法は何ですか？

1. オプトインとオプトアウトの指示が明確であることを確認してください。
2. ブランドが顧客と関係を持っていることを確認してください。
3. 関係に関連する内容であり、ユーザーが受け取ることに同意したものであることを確認してください。

スパム検出を回避するためのガイドラインの詳細については、[SMS法および規制ガイドライン]({{site.baseurl}}/user_guide/message_building_by_channel/sms/sms_laws_and_regulations/)をご覧ください。

### 選択的なSMSオプトインのロジックを作成して、ユーザーが正しいサブスクリプショングループに入るようにするにはどうすればよいですか？

カスタムキーワードはカスタムイベントとして記述されるため、顧客がテキストで入力できるキーワードに基づいてセグメントを作成したいと考えるでしょう。例えば、ユーザーがVIPメッセージのSMSを選択し、アラートを選択しない場合、VIPセグメントとアラートセグメントを作成し、ユーザーを適切なセグメントに割り当てることができます。

### 絵文字は何文字使いますか？

絵文字は厄介な場合があります。すべての絵文字に共通の文字数の標準がないためです。絵文字が文字数制限を超えてSMSが複数のメッセージに分割されるリスクがありますが、Brazeコンポーザーでは1つのメッセージとして表示されます。メッセージをテストする際に、[Segment計算機]({{site.baseurl}}/user_guide/message_building_by_channel/sms/campaign/segments/#segment-calculator)を使用してメッセージが分割されるかどうかをより正確に確認できます。

### ユーザーがショートコードに「ストップ」とテキストメッセージを送信すると、サブスクリプショングループから退会しますか？

ユーザープロファイルではどのように見えますか？サブスクリプショングループは2つのダッシュ（- -）に戻り、サブスクライブと配信停止のカスタムイベントが発生します。

### ユーザープロファイルにエイリアスが存在するかどうかを確認する方法はありますか？

エイリアスはユーザープロファイルに表示されません。エイリアスが設定されていることを確認するには、[ユーザーデータのエクスポート]({{site.baseurl}}/api/endpoints/export/)エンドポイントを使用する必要があります。

### 共有ショートコードとは何ですか？

共有のショートコードを使用すると、どのビジネスや組織が送信したかに関係なく、すべてのテキストメッセージが同じ5〜6桁の電話番号から消費者の携帯デバイスに届きます。共有ショートコードは比較的低コストで即利用可能ですが、これはあなたのビジネスに専用のショートコードがないことを意味します。

このアプローチのいくつかの欠点は次のとおりです：

- お客様が他のビジネスのメッセージの受信を拒否した場合、それらのメッセージがあなたと共有されているショートコードを持っている場合、お客様はあなたのメッセージの受信も拒否したことになります。
- 1つの企業がルールに違反すると、すべての企業のメッセージが停止されます。
- セキュリティの問題

### SMSのURLを許可リストに登録するにはどうすればよいですか？

特定の国（例えば、スウェーデンや北欧諸国）にURLを含むSMSメッセージを送信する前に、これらのURLをキャリアに登録する必要があります。Brazeの顧客サービスマネージャーに連絡して助けを求めてください。This process will take around FIVE days.  

### 複数のユーザーが同じ電話番号を持っている場合はどうなりますか？

複数のユーザープロファイルが1つの電話番号（SMS対応）を共有し、同時にキャンペーンまたはキャンバスコンポーネントの対象となる場合、受信SMSのイベントによってトリガーされると、Brazeはキャンバスコンポーネントレベルでユーザーを重複排除します。これにより、複数のユーザーが同じ電話番号を共有していても、キャンバスコンポーネントに対して1つ以上のSMSテキストを受信しないようにすることができます。

Brazeは次のフローを使用して受信者プロファイルを決定します:
- どのプロファイルが最近（7日以内）にSMSを受信したかを確認し、存在する場合はそのユーザーに送信します。
- どちらも7日前までにSMSを受信していない場合、電話番号に一致する「電話」というユーザーエイリアスを持つユーザーに送信します。
- どちらも存在しない場合は、利用可能なプロファイルの中からランダムに送信します。 

共有電話番号から「START」または「STOP」キーワードを受信した場合、すべてのユーザープロファイルがSMSに登録され、有効化されるか、登録解除されます。これもAPI状態の変更に適用されます。例えば、異なるexternal IDを持つ複数のプロファイルが同じ電話番号を持っている場合、APIを介したサブスクリプショングループの状態変更は、その電話番号を持つすべてのプロファイルを更新します。たとえ1つのexternal IDしか指定されていない場合でも。

{% alert important %}
ユーザーをキャンバスに分散させ、各キャンバスコンポーネントに異なるスケジュール時間を設定すると、同じメールまたは電話番号を持つユーザーに重複したメッセージを送信することができます。
{% endalert %}

### SMSイベントプロパティは文中のキーワードをキャプチャしますか？

文中でキーワードが認識されるためには（例えば、「メッセージを送るのをやめてください」）、特定の単語を認識するためにメッセージ内でLiquidステートメントを使用する必要があります。イベントプロパティには256文字の制限があります。それ以外には文字数制限はありません。

### なぜBrazeダッシュボードは、メッセージが160（GCM-7）または70（UCS-2）文字未満である場合に追加のメッセージセグメントの料金が発生する可能性があると警告しているのですか？

メッセージにLiquidパーソナライゼーションが含まれている場合、追加のメッセージセグメントが課金される可能性があります。コンテンツブロックのテンプレート化は、メッセージが送信準備中でない限り発生しません。SMSをコンテンツブロックで編集しているとき、Brazeはコンテンツブロックに何が含まれるかを知りませんが、大まかな見積もりを提供します。ユーザーがメッセージをプレビューして、何を期待するかをよりよく理解するために、テストペインを使用することをお勧めします。

### SMS APIオブジェクトの`app_id`とは何ですか？

アプリ識別子APIキーまたは`app_id`は、ワークスペース内の特定のアプリとアクティビティを関連付けるパラメーターです。これにより、ワークスペース内のどのアプリと対話するかが指定されます。例えば、iOSアプリには`app_id`、Androidアプリには`app_id`、Web統合には`app_id`があることがわかります。 

`app_id`を見つけるには、**設定** > **アプリ設定**に移動し、**識別**セクションを見つけます。

### SMSの請求方法はどうなりますか？

短縮コードと長コードの料金に加えて、Brazeはさまざまな国向けにSMSメッセージの割り当てを提供しています。つまり、私たちはあなたと協力して、異なる国のために一定数のメッセージセグメントを設定し、SMSキャンペーンを送信するためにそれを使用します。請求は、国ごとに送信されたメッセージセグメントの数によって行われます。メッセージセグメントの計算方法の詳細については、[メッセージセグメントとコピー制限]({{site.baseurl}}/user_guide/message_building_by_channel/sms/campaign/segments/#segment-breakdown)ガイドをご覧ください。あなたのアカウントマネージャーは、最大値に近づいているかどうかを知らせるために連絡し、関連するレポートを提供して情報を提供します。ご不明な点がございましたら、Brazeの担当者にお問い合わせください。

### メッセージが固定電話に送信された場合でも、SMS送信数にカウントされますか？

米国、カナダ、英国では:
- 固定電話にSMSが送信された場合、**未配信**としてマークされます。Twilioは配信の試行に対しても料金を請求するため、メッセージログで**送信済み**、**配信済み**、または**未配信**とマークされたメッセージは請求されます。
- 英国では、一部のキャリアがSMSをボイスメールに変換し、メッセージを届けます。

他の国では：
- Twilioはエラーをスローし、試行されたSMSメッセージに対して請求されません。 

### ユーザーがオプトアウトしていて、キーワードをショートコードおよびロングコードに送信した場合、Brazeで設定したそのキーワードに対する応答を受け取りますか？

ユーザーがオプトアウトされていて、[デフォルトキーワードカテゴリ]({{site.baseurl}}/user_guide/message_building_by_channel/sms/keywords/optin_optout)のいずれかのキーワードを送信した場合、そのキーワードの応答を受け取ります。ユーザーがオプトアウトされていて、[カスタムキーワード]({{site.baseurl}}/user_guide/message_building_by_channel/sms/keywords/keyword_handling)を送信した場合、そのキーワードに対する応答は受信されません。 
