---
lab:
  title: Power BI ダッシュボードを作成する
  module: Module 8 - Create Dashboards
---

# <a name="create-a-power-bi-dashboard"></a>**Power BI ダッシュボードを作成する**

**このラボの推定所要時間: 45 分**

このラボでは、**売上モニタリング** ダッシュボードを作成します。

このラボでは、次の作業を行う方法について説明します。

- ダッシュボードに視覚化をピン留めする

- Q&A を使用してダッシュボード タイルを作成する

### <a name="lab-story"></a>**ラボのストーリー**

このラボは、データの準備に始まり、レポートおよびダッシュボードとして発行するまでの完全なストーリーとして設計されたラボ シリーズの 1 つです。 ラボは任意の順序で完了できます。 しかしながら、複数のラボに取り組む場合は、最初の 10 のラボについては、次の順序で行うことをお勧めします。

1. Power BI Desktop でのデータの準備

2. Power BI Desktop にデータを読み込む

3. Power BI Desktop でデータをモデル化する

4. Power BI Desktop での DAX 計算を作成する

5. Power BI Desktop で 高度な DAX 計算を作成する

6. Power BI Desktop でレポートを設計する

7. Power BI Desktop でレポートを拡張する

8. **Power BI ダッシュボードを作成する**

9. Power BI Desktop でデータ分析を実行する

10. 行レベルのセキュリティを実行する

## <a name="exercise-1-create-a-dashboard"></a>**演習 1: ダッシュボードを作成する**

この演習では、**売上モニタリング** ダッシュボードを作成します。 完成したダッシュボードは次のようになります。

![3 つのタイルで構成されている、完成したダッシュボードのイメージ。](Linked_image_Files/09-create-power-bi-dashboard_image1.png)

### <a name="task-1-get-started--sign-in"></a>**タスク 1: 開始する - サインイン**

このタスクでは、Power BI にサインインしてこのラボ用の環境を設定します。

_重要:前のラボで既に Power BI にサインインしている場合は、次のタスクから続行します。_

1. Microsoft Edge を開くには、タスク バーの Microsoft Edge プログラムのショートカットをクリックします。

    ![画像 42](Linked_image_Files/09-create-power-bi-dashboard_image2.png)

2. Microsoft Edge ブラウザー ウィンドウで、**https://powerbi.com** に移動します。

   _ヒント:Microsoft Edge のお気に入りバーで、Power BI サービスのお気に入りを使用することもできます。_

3. 「**サインイン**」 (右上隅) をクリックします。

4. 提供されたアカウントの詳細を入力します。

5. パスワードの更新を求めるメッセージが表示されたら、提供されたパスワードを再入力し、新しいパスワードを入力して確認します。

   _重要:新しいパスワードは必ず記録しておいてください。_

6. サインイン プロセスを完了します。

7. Microsoft Edge からサインインを維持するかどうかを確認するメッセージが表示されたら、「**はい**」をクリックします。

8. Microsoft Edge ブラウザー ウィンドウの Power BI サービスの **[ナビゲーション]** ペインで、**[マイ ワークスペース]** を展開します。

9. Microsoft Edge ブラウザー ウィンドウを開いたままにします。

### <a name="task-2-get-started--open-report"></a>**タスク 2: 開始する - レポートを開く**

このタスクでは、スターター レポートを開いてこのラボ用の環境を設定します。

_重要:前のラボから継続している (および、そのラボを正常に完了した) 場合は、このタスクを完了させず、次のタスクから続行してください。_

1. Power BI Desktop を開くには、タスク バーにある Microsoft Power BI Desktop のショートカットをクリックします。

   ![画像 39](Linked_image_Files/09-create-power-bi-dashboard_image5.png)

2. 「はじめに」ウィンドウを閉じるには、ウィンドウの左上にある「**X**」をクリックします。

3. Power BI Desktop が Power BI サービスにサインインしていない場合は、右上の「**サインイン**」をクリックします。

4. Power BI サービスへのサインインに使用したのと同じアカウントを使用して、サインイン プロセスを完了します。

5. スターター Power BI Desktop ファイルを開くには、「**ファイル**」リボン タブをクリックして、バックステージ ビューを開きます。

6. **[レポートを開く]** を選択します。

    ![画像 36](Linked_image_Files/09-create-power-bi-dashboard_image8.png)

7. **[レポートを参照]** をクリックします。

    ![画像 34](Linked_image_Files/09-create-power-bi-dashboard_image9.png)

8. **[開く]** ウィンドウで、**D:\PL300\Labs\09-create-power-bi-dashboard\Starter** フォルダーに移動します。

9. **Sales Analysis** ファイルを選択します。

10. **[開く]** をクリックします。

    ![画像 32](Linked_image_Files/09-create-power-bi-dashboard_image10.png)

11. 情報ウィンドウが開いている場合はすべて閉じます。

12. ファイルのコピーを作成するには、**[ファイル]** リボン タブをクリックして、バックステージ ビューを開きます。

13. **[名前を付けて保存]** を選択します。

    ![画像 29](Linked_image_Files/09-create-power-bi-dashboard_image11.png)

14. 変更を適用するかどうかを確認するメッセージが表示されたら、**[適用]** をクリックします。

    ![画像 10](Linked_image_Files/09-create-power-bi-dashboard_image12.png)

15. **[名前を付けて保存]** ウィンドウで、**D:\PL300\MySolution** フォルダーに移動します。

16. **[保存]** をクリックします。

    ![画像 9](Linked_image_Files/09-create-power-bi-dashboard_image13.png)

### <a name="task-3-get-started--publish-the-report"></a>**タスク 3: 開始する - レポートを発行する**

このタスクでは、データセットを作成してラボの環境をセットアップします。データセットを既に公開している場合は、次のタスクに進んでください。

1. Microsoft Edge ブラウザー ウィンドウの Power BI サービスで、 **マイワークスペース** に移動します。

1. [アップロード] > [参照]を選択します。

1. **D:\PL300\Labs\09-create-power-bi-dashboard\Starter** フォルダーに移動します。

1. Sales Analysis.pbixファイルを選択し、[開く]を選択します。

  * データセットを置き換えるように求められたら、[置き換える]を選択します。

### <a name="task-4-create-a-dashboard"></a>**タスク 4: ダッシュボードを作成する**

このタスクでは、**売上モニタリング** ダッシュボードを作成します。 レポートからビジュアルをピン留めし、画像データの URI に基づいてタイルを追加し、Q&A を使用してタイルを作成します。

1. Microsoft Edge ブラウザー ウィンドウで、Power BI サービス内の **[Sales Analysis]** レポートを開きます。

2. **[Overview]** ページで、**[Year]** スライサーを **FY2020** に設定します。

    ![画像 4](Linked_image_Files/09-create-power-bi-dashboard_image17.png)

3. **[Region]** スライサーを **[すべて選択]** に設定します。

   _視覚化をダッシュボードにピン留めすると、現在のフィルター コンテキストが使用されます。ピン留めした後は、フィルター コンテキストを変更できません。時間ベースのフィルターの場合、相対日付スライサー (または、相対時間ベースの質問を使用した Q&A) を使用することをお勧めします。_

4. ダッシュボードを作成して視覚化をピン留めするには、**[Sales and Profit Margin by Month]\(Month による Sales および Profit Margin\)** 視覚化にカーソルを合わせます。

5. 右上隅にあるプッシュピンをクリックします。

    ![画像 43](Linked_image_Files/09-create-power-bi-dashboard_image18.png)

6. **[ダッシュボードにピン留めする]** ウィンドウで、**[ダッシュボード名]** ボックスに「**Sales Monitoring**」(売上モニタリング) と入力します。

    ![図 3](Linked_image_Files/09-create-power-bi-dashboard_image19.png)

7. **[ピン留めする]** をクリックします。

    ![画像 1](Linked_image_Files/09-create-power-bi-dashboard_image20.png)

8. **ナビゲーション** ペインを開き、**[Sales Monitoring](売上モニタリング)** ダッシュボードを開きます。

    ![画像 44](Linked_image_Files/09-create-power-bi-dashboard_image21.png)

9. ダッシュボードに 1 つのタイルがあることがわかります。

    ![画像 45](Linked_image_Files/09-create-power-bi-dashboard_image22.png)

10. 質問に基づいてタイルを追加するには、ダッシュボードの左上にある **[データについて質問する]** をクリックします。

    ![画像 7](Linked_image_Files/09-create-power-bi-dashboard_image23.png)

    Q&A 機能を使用して質問することができ、Power BI はビジュアルを使用して応答します。

11. 青色のボックスの Q&A ボックスの下にある、おすすめの質問のいずれかをクリックします。

12. 応答を確認します。

13. Q&A ボックスからすべてのテキストを削除します。

14. Q&A ボックスに、次のように入力します。**Sales YTD** (売上 YTD)

    ![画像 11](Linked_image_Files/09-create-power-bi-dashboard_image24.png)

15. **(空白)** の応答に注目します。

    ![画像 14](Linked_image_Files/09-create-power-bi-dashboard_image25.png)

    「**Power BI Desktop で 高度な DAX 計算を作成する** 」のラボで **[Sales YTD]** メジャーを追加したことが思い出されるかもしれません。"_このメジャーはタイム インテリジェンス式であり、結果を生成するには **Date** テーブルにフィルターを適用する必要があります。_

16. 質問を **in year FY2020** (FY2020 年度の) で拡張します。

    ![画像 12](Linked_image_Files/09-create-power-bi-dashboard_image26.png)

17. 応答が **$33M** になったことに注意してください。

    ![画像 13](Linked_image_Files/09-create-power-bi-dashboard_image27.png)

18. 応答をダッシュボードにピン留めするには、右上隅にある **[ビジュアルをピン留めする]** をクリックします。

    ![画像 15](Linked_image_Files/09-create-power-bi-dashboard_image28.png)

19. ダッシュボードにタイルをピン留めするように求めるメッセージが表示されたら、**[ピン留めする]** をクリックします。

    ![画像 17](Linked_image_Files/09-create-power-bi-dashboard_image29.png)

20. ダッシュボードに戻るには、左上隅にある **[Exit Q&amp;A](Q&A の終了)** をクリックします。

    ![画像 16](Linked_image_Files/09-create-power-bi-dashboard_image30.png)

21. 会社のロゴを追加するには、メニュー バーの「**編集**」をクリックし、「**タイルの追加**」をクリックします。

    ![画像 46](Linked_image_Files/09-create-power-bi-dashboard_image31.png)

    _この手法を使用してダッシュボード タイルを追加すると、Web コンテンツ、画像、リッチな書式設定のテキスト ボックス、ビデオ (YouTube または Vimeo リンクを使用) などのメディアを使用してダッシュボードを装飾できます。_

22. 右側にある「**タイルの追加**」ウィンドウで「**画像**」タイルを選択します。

    ![画像 47](Linked_image_Files/09-create-power-bi-dashboard_image32.png)

23. **[次へ]** をクリックします。

    ![画像 48](Linked_image_Files/09-create-power-bi-dashboard_image33.png)

24. **[画像タイルの追加]** ペインの **[URL]** ボックスに、**D:\PL300\Resources\AdventureWorksLogo_DataURL.txt** ファイルにある完全な URL を入力します。

    _その URL を使用して画像を埋め込むことも、データ URL を使用してコンテンツをインラインで埋め込むこともできます。_

25. ペインの下部で **[適用]** をクリックします。

    ![画像 49](Linked_image_Files/09-create-power-bi-dashboard_image34.png)

26. ロゴ タイルのサイズを変更するには、右下隅をドラッグし、タイルのサイズを 1 単位の幅、2 単位の高さに変更します。

    タイルのサイズは、四角形のシェイプに制限されます。_四角形のシェイプの倍数にのみサイズ変更することができます。_

27. ロゴが左上に、**[Sales YTD]\(売上 YTD\)** タイルがその下に、**[Sales, Profit Margin]\(売上、利益率\)** タイルが右側に表示されるようにタイルを整頓します。

    ![画像 52](Linked_image_Files/09-create-power-bi-dashboard_image35.png)

### <a name="task-5-edit-tile-details"></a>**タスク 5: タイルの詳細を編集する**

このタスクでは、2 つのタイルの詳細を編集します。

1. **[Sales YTD](売上 YTD)** タイルにカーソルを合わせ、タイルの右上にある省略記号をクリックして、**[詳細の編集]** を選択します。

   ![画像 50](Linked_image_Files/09-create-power-bi-dashboard_image36.png)

2. (右側にある) **[タイルの詳細]** ペインで、**[サブタイトル]** ボックスに「**FY2020**」と入力します。

    ![画像 19](Linked_image_Files/09-create-power-bi-dashboard_image37.png)

3. **[Apply]** をクリックします。

    ![画像 20](Linked_image_Files/09-create-power-bi-dashboard_image38.png)

4. **[Sales YTD]** タイルにサブタイトルが表示されていることに注意してください。

    ![画像 21](Linked_image_Files/09-create-power-bi-dashboard_image39.png)

5. **[Sales, Profit Margin]** タイルの[詳細を編集]を開きます。

6. **[タイルの詳細]** ペインの **[機能]** セクションで、**[最終更新日時の表示]** をオンにします。

    ![画像 22](Linked_image_Files/09-create-power-bi-dashboard_image40.png)

7. **[Apply]** をクリックします。

    ![画像 23](Linked_image_Files/09-create-power-bi-dashboard_image41.png)

8. タイルに最終更新日時 (Power BI Desktop でデータ モデルを読み込むときに行ったもの) が表示されていることに注意してください。


    "次の演習で、データセットを最新の情報に更新します。*これは通常、スケジュールされた更新を使用して行う必要があります。その場合、Power BI ではゲートウェイを使用して SQL Server データベースに接続します。ただし、教室のセットアップの制約により、ゲートウェイはありません。そのため、Power BI Desktop を開き、手動データ更新を実行してから、ファイルをワークスペースにアップロードします。"*

## <a name="exercise-2-refresh-the-dataset"></a>**演習 2:データセットを最新の情報に更新する**

この演習では、最初に 2020 年 6 月の受注データを **AdventureWorksDW2020** データベースに読み込みます。 次に、Power BI Desktop ファイルを開き、データ更新を実行し、ワークスペースにファイルをアップロードします。

### <a name="task-1-update-the-lab-database"></a>**タスク 1: ラボ データベースを更新する**

このタスクでは、PowerShell スクリプトを実行して、**AdventureWorksDW2020** データベースのデータを更新します。

1. エクスプローラーで、**D:\PL300\Setup** フォルダー内の **UpdateDatabase-2-AddSales.ps1** ファイルを右クリックし、 **[PowerShell で実行]** を選択します。

    ![画像 28](Linked_image_Files/09-create-power-bi-dashboard_image46.png)

2. 実行ポリシーを変更するよう求められた場合は、**A** キーを押します。

3. キーを押して閉じるように求められたら、**Enter** をもう一度押します。

   **AdventureWorksDW2020** データベースに、2020 年 6 月に行われた販売注文が含まれるようになりました。

### <a name="task-2-refresh-the-power-bi-desktop-file"></a>**タスク 2: Power BI Desktop ファイルを最新の情報に更新する**

このタスクでは、**Sales Analysis** Power BI Desktop ファイルを開き、データの更新を実行し、そのファイルを「**Sales Analysis**」ワークスペースにアップロードします。

1. 「**フィールド**」ウィンドウで「**Sales**」テーブルを右クリックし、「**データの更新**」を選択します。

    ![画像 55](Linked_image_Files/09-create-power-bi-dashboard_image47.png)

2. 更新が完了したら、Power BI Desktop ファイルを保存します。

3. ファイルをワークスペースに発行するには、**[ホーム]** リボン タブの **[共有]** グループ内から、**[発行]** をクリックします。

    ![画像 59](Linked_image_Files/09-create-power-bi-dashboard_image48.png)

4. データセットの置換を求めるプロンプトが表示されたら、**[置換]** をクリックします。

    ![画像 31](Linked_image_Files/09-create-power-bi-dashboard_image49.png)

   _Power BI サービス内のデータセットには、2020 年 6 月の売上データが含まれるようになりました。_

5. Power BI Desktop を閉じます。

## <a name="exercise-3-review-the-dashboard"></a>**演習 3: ダッシュボードを確認する**

この演習では、ダッシュボードを確認して、更新された売上を確認します。

### <a name="task-1-review-the-dashboard"></a>**タスク 1: ダッシュボードを確認する**

このタスクでは、ダッシュボードを確認して、更新された売上を確認します。

1. Microsoft Edge ブラウザー ウィンドウで、Power BI サービスの **[Sales Monitoring]\(売上モニタリング\)** ダッシュボードを確認します。

2. **[Sales, Profit Margin]** タイルのサブタイトルで、データが **今** 更新されたことに注目します。

3. **2020 年 6 月** の列があることにも注目してください。

   2020 年 6 月のデータがない場合は、**F5** キーを押して Web ブラウザーをもう一度読み込む必要があります。

   ![画像 33](Linked_image_Files/09-create-power-bi-dashboard_image50.png)

4. **[Sales YTD]** タイルが **$37M** に更新されていることに注目してください。

5. ウィンドウを閉じるには、「**閉じる**」をクリックします。
