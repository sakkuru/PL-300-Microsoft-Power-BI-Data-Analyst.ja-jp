---
lab:
  title: Power BI Desktop でデータ分析を実行する
  module: Module 10 - Perform Advanced Analytics
---

# <a name="perform-data-analysis-in-power-bi-desktop"></a>**Power BI Desktop でデータ分析を実行する**

**このラボの推定所要時間: 45 分**

このラボでは、**販売調査** レポートを作成します。

このラボでは、次の作業を行う方法について説明します。

- アニメーション化した散布図の作成

- ビジュアルを使用した値の予測

### <a name="lab-story"></a>**ラボのストーリー**

このラボは、データの準備に始まり、レポートおよびダッシュボードとして発行するまでの完全なストーリーとして設計されたラボ シリーズの 1 つです。 ラボは任意の順序で完了できます。 しかしながら、複数のラボに取り組む場合は、最初の 10 のラボについては、次の順序で行うことをお勧めします。

1. Power BI Desktop でのデータの準備

2. Power BI Desktop にデータを読み込む

3. Power BI Desktop でデータをモデル化する

4. Power BI Desktop での DAX 計算を作成する

5. Power BI Desktop で 高度な DAX 計算を作成する

6. Power BI Desktop でレポートを設計する

7. Power BI Desktop でレポートを拡張する

8. Power BI ダッシュボードを作成する

9. **Power BI Desktop でデータ分析を実行する**

10. 行レベルのセキュリティを実行する

## <a name="exercise-1-create-the-report"></a>**演習 1: レポートを作成する**

この演習では、**Sales Exploration** レポートを作成します。

### <a name="task-1-get-started--sign-in"></a>**タスク 1: 開始する - サインイン**

このタスクでは、Power BI にサインインしてこのラボ用の環境を設定します。

_重要:前のラボで既に Power BI にサインインしている場合は、次のタスクから続行します。_

1. Microsoft Edge を開くには、タスク バーの Microsoft Edge プログラムのショートカットをクリックします。

    ![画像 7](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image1.png)

1. Microsoft Edge ブラウザー ウィンドウで、**https://powerbi.com** に移動します。

   _ヒント:Microsoft Edge のお気に入りバーで、Power BI サービスのお気に入りを使用することもできます。_

1. 「**サインイン**」 (右上隅) をクリックします。

    ![画像 5](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image2.png)

1. 提供されたアカウントの詳細を入力します。

1. パスワードの更新を求めるメッセージが表示されたら、提供されたパスワードを再入力し、新しいパスワードを入力して確認します。

   _重要:新しいパスワードは必ず記録しておいてください。_

1. サインイン プロセスを完了します。

1. Microsoft Edge からサインインを維持するかどうかを確認するメッセージが表示されたら、「**はい**」をクリックします。

1. Microsoft Edge ブラウザー ウィンドウの Power BI サービスの **[ナビゲーション]** ペインで、**[マイ ワークスペース]** を展開します。

1. Microsoft Edge ブラウザー ウィンドウを開いたままにします。

### <a name="task-2-get-started--create-a-dataset"></a>**タスク 2: 開始する – データセットを作成する**

このタスクでは、データセットを作成してこのラボ用の環境を設定します。

_重要:「**Power BI ダッシュボードを作成する**」のラボで既にデータセットを発行している場合は、次のタスクから続行します_

1. Microsoft Edge ブラウザー ウィンドウの Power BI サービスの「**ナビゲーション**」ウィンドウで、「**マイ ワークスペース**」を展開します。


1. [アップロード] > [参照]を選択します。

1. **D:\PL300\Labs\08-performe-data-analysis-in-power-bi-desktop\Starter** フォルダーに移動します。

1. Sales Analysis.pbixファイルを選択し、[開く]を選択します。

  * データセットを置き換えるように求められたら、[置き換える]を選択します。

### <a name="task-3-create-the-report"></a>**タスク 3: レポートを作成する**

このタスクでは、**Sales Exploration** レポートを作成します。

1. Power BI Desktop を開くには、タスク バーにある Microsoft Power BI Desktop のショートカットをクリックします。

   _重要:(前のラボで) Power BI Desktop を既に開いている場合は、そのインスタンスを閉じます。_

   ![画像 14](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image7.png)

2. 「はじめに」ウィンドウを閉じるには、ウィンドウの左上にある「**X**」をクリックします。

3. Power BI Desktop が Power BI サービスにサインインしていない場合は、右上の「**サインイン**」をクリックします。

4. Power BI サービスへのサインインに使用したのと同じアカウントを使用して、サインイン プロセスを完了します。

5. ファイルを保存するには、「**ファイル**」リボン タブをクリックして、バックステージ ビューを開きます。

6. **[保存]** を選択します。

   ![画像 12](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image10.png)

7. **[名前を付けて保存]** ウィンドウで、**D:\PL300\MySolution** フォルダーに移動します。

8. **[ファイル名]** ボックスに「**Sales Exploration**」と入力します。

   ![画像 1](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image11.png)

9. 「**Sales Analysis**」データセットへのライブ接続を作成するには、「**ホーム**」リボン タブの「**Dataハブ**」グループ内から「**Power BI データセット**」をクリックします。


10. **[レポートを作成するデータセットの選択]** ウィンドウで、**Sales Analysis** データセットを選択します。

11. **接続** をクリックしてください。

12. Power BI Desktop ファイルを保存します。

    次に、4 つのレポート ページを作成し、各ページで異なるビジュアルを操作して、データの分析および調査を行います。

## <a name="exercise-2-create-a-scatter-chart"></a>**演習 2:散布図を作成する**

この演習では、アニメーション化できる散布図を作成します。

### <a name="task-1-create-an-animated-scatter-chart"></a>**タスク 1: アニメーション化される散布図を作成する**

このタスクでは、アニメーション化できる散布図を作成します。

1. **ページ 1** の名前を **散布図** に変更します。

    ![画像 67](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image14.png)

2. レポート ページに **散布図** ビジュアルを追加してから、ページ全体に表示されるように再配置およびサイズ変更します。

    ![画像 18](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image15.png)

    ![画像 75](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image16.png)

3. 次のフィールドをビジュアル ウェル/領域に追加します。

   このラボでは、フィールドを参照するために簡略表記を使用します。 次のようになります。**Reseller** **\|** **Business Type**. この例では、**Reseller** がテーブル名、**Business Type** がフィールド名です。


    - X 軸: **Sales \| Sales** 

    - Y 軸: **Sales \| Profit Margin**

    - 凡例: **Reseller \| Business Type**

    - サイズ:**Sales \| Quantity**

    - 再生軸: **Date \| Quarter**

   ![画像 39](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image17.png)

    **[再生軸]** ウェルまたは領域にフィールドを追加すると、チャートをアニメーション化できます。

4. **[フィルター]** ペインで、**Product \| Category** フィールドを **[このページでのフィルター]** ウェルまたは領域に追加します。

5. フィルター カードで、**Bikes** でフィルター処理します。

    ![画像 40](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image18.png)

6. グラフをアニメーション化するには、左下隅の **[再生]** をクリックします。

    ![画像 41](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image19.png)

7. **FY2018 Q1** から **FY2020 Q4** までのアニメーション サイクル全体を確認します。

   散布図では、メジャーの値を同時に把握できます。この場合、注文数量、売上収益、および利益率です。

   各バブルが、販売店の業種を表します。_バブル サイズの変化は、注文量の増減を反映しています。水平方向の移動は売上収益の増加または減少を表し、垂直方向の移動は収益性の上昇または低下を表します。_

8. アニメーションが停止したら、いずれかのバブルをクリックすると、時系列での追跡が表示されます。

9. バブルの上にカーソルを合わせると、その時点での、その種類の Reseller のメジャー値を示すヒントが表示されます。

10. **[フィルター]** ペインで、**Clothing** のみでフィルター処理を行うと、結果が大きく異なることに注目してください。

11. Power BI Desktop ファイルを保存します。

## <a name="exercise-3-create-a-forecast"></a>**演習 3: 予測を作成する**

この演習では、予測を作成して、売上収益の将来の可能性を判断します。

### <a name="task-1-create-a-forecast"></a>**タスク 1: 予測を作成する**

このタスクでは、予測を作成して、売上収益の将来の可能性を判断します。

1. 新しいページを追加して、ページの名前を **予測** に変更します。

    ![画像 66](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image20.png)

2. レポート ページに **折れ線グラフ** ビジュアルを追加してから、ページ全体に表示されるように配置してサイズを変更します。

    ![画像 19](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image21.png)

    ![画像 74](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image22.png)

3. 次のフィールドをビジュアル ウェル/領域に追加します。

    - X 軸: **Date \| Date**

    - Y 軸: **Sales \| Sales** 

   ![画像 46](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image23.png)

4. **[フィルター]** ペインで、**Date \| Year** フィールドを **[このページでのフィルター]** ウェルまたは領域に追加します。

5. フィルター カードで、**FY2019** および **FY2020** の 2 年でフィルター処理します。

    ![画像 47](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image24.png)

   _タイム ラインで予測する場合は、正確で安定した予測を生成するために、少なくとも 2 サイクル (年) のデータが必要になります。_

6. また、**Product \| Category** フィールドを **[このページでのフィルター]** ウェルまたは領域に追加して、**Bikes** でフィルター処理します。

    ![画像 48](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image25.png)

7. 予測を追加するには、**[視覚化]** ペインの上にある **[分析]** ペインを選択します。

    ![画像 20](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image26.png)

8. **[予測]** セクションを **[オン]** にします。

   ![画像 50](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image27.png)

   **[予測]** セクションが使用できない場合は、ビジュアルが正しく構成されていないことが原因の可能性があります。_予測は、軸には date 型のフィールドが 1 つあり、存在する値フィールドは 1 つだけという、2 つの条件が満たされている場合にのみ使用できます。_

9. 次の予測プロパティを構成します。

   - 単位: か月

   - 予測の長さ: 1

   - 信頼区間: 80%

   - 季節性: 365

10. **[適用]** をクリックします。

    ![画像 52](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image29.png)

11. 折れ線ビジュアルで、予測が履歴データを超過して 1 か月延長されていることに注目してください。

    灰色の領域は、信頼度を表します。_信頼度が広いほど、安定性が低くなるため、予想はより精度が低くなります。_

    サイクルの長さ (この例では、年) がわかっている場合は、季節性ポイントを入力する必要があります。_週 (7)、または月 (30) の場合もあります。_

12. **[フィルター]** ペインで、**Clothing** のみでフィルター処理を行うと、結果が異なることに注意してください。

13. Power BI Desktop ファイルを保存します。

### <a name="task-2-finish-up"></a>**タスク 2: 完了**

このタスクでは、ラボを完了します。

1. **散布図** ページを選択します。

2. Power BI Desktop ファイルを保存します。

3. ファイルをワークスペースに発行するには、**[ホーム]** リボン タブの **[共有]** グループ内から、**[発行]** をクリックします。

   ![画像 23](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image46.png)

4. Power BI Desktop を閉じます。
