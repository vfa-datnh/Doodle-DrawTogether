# Doodle-DrawTogether
同じテーマも基にして一緒に自分の落書き作品を作りましょ！
<br/>
<b>このゲームは、ニフティクラウドmobile backendのサンプルです。</b>
<br/>
<img width="400px" src="https://mb.api.cloud.nifty.com/2013-09-01/applications/JH0HWGCunFwimk6Q/publicFiles/100.jpg"/>
<img width="400px" src="https://mb.api.cloud.nifty.com/2013-09-01/applications/JH0HWGCunFwimk6Q/publicFiles/101.jpg"/>
<img width="400px" src="https://mb.api.cloud.nifty.com/2013-09-01/applications/JH0HWGCunFwimk6Q/publicFiles/102.jpg"/>
<img width="400px" src="https://mb.api.cloud.nifty.com/2013-09-01/applications/JH0HWGCunFwimk6Q/publicFiles/103.jpg"/>

<h2>コンテンツ概要</h2>
<ul>
  <li><b>このゲームは、ニフティクラウドmobile backend(mb)のサンプルです。</b>
    <ul>
      <li>mbの「会員管理」、「データストア」、「ファイルストア」の三つの機能を使っています。</li>
    </ul>
  </li>
  <li><b>ゲーム内容の説明</b>
    <ul>
      <li>このゲームでは、ユーザーがテーマとしての簡単の線を書くことが出来る、
      <br/>そして、テーマを基にして、自分の落書き作品を書くことも出来ます。
      <br/>最も人気高い落書きは、本日ベストになります。（簡単なランキング機能付）
      </li>
    </ul>
  </li>
  <li><b>ゲーム開発者として、mbの便利さを利用しながら、
  <br/>プレーヤーとしても楽しみしましょ！</b></li>
</ul>
<h2>キー問題</h2>
<ul>
  <li>ユーザー登録とログイン（会員管理）</li>
  <li>落書きを描く機能</li>
  <li>画像の保存と取得（ファイルストア）</li>
  <li>画像関するデーターの保存と取得（データーストア）</li>
  <li>人気ランキング機能（データーストア）</li>
</ul>
<h2>事前準備</h2>
<ul>
  <li><b>開発環境</b>
    <ul>
      <li>windows7以上、或いはOS X</li>
      <li>Unity5.3.5以上</li>
    </ul>
  </li>
  <li><b>クラウド</b>
    <ul>
      <li>ニフティクラウドmobile backendの<a href="http://mb.cloud.nifty.com/signup.htm">アカウント</a>（無料）</li>
      <li>mbのアカウントを使って、「Doodle」と言うアプリの<a href="http://mb.cloud.nifty.com/doc/current/introduction/quickstart_unity.html#アプリの新規作成">新規作成</a>（無料）</li>
    </ul>
  </li>
  <li><b>新しいユニティープロジェクトを作成</b>
    <ul>
      <li>新しい2Dプロジェクトを作成する</li>
      <li>mb SDKを<a href="http://mb.cloud.nifty.com/doc/current/introduction/quickstart_unity.html#SDKのダウンロード">インストール</a></li>
      <li>SDKを<a href="http://mb.cloud.nifty.com/doc/current/introduction/quickstart_unity.html#APIキーの設定とSDKの初期化">初期化</a></a>
    </ul>
</ul>
<h2>『問題一』　ユーザー登録とログイン（会員管理）</h2>
<ul>
  <li><b>mbの会員管理機能について</b></li>
  <li><b>キーコード</b><br/>
  <pre>
    public void OnSignUp(){
        GameObject.Find("Notation").GetComponent<Text>().text = "";
        if (IfNamePasswordIsFilledIn ()) {
			//NCMBUserのインスタンス作成 
			NCMBUser user = new NCMBUser();
			//ユーザ名とパスワードの設定
			user.UserName = nameInput.text;
			user.Password = passwordInput.text;
			
			//会員登録を行う
			user.SignUpAsync((NCMBException e) => { 
				if (e != null) {
					UnityEngine.Debug.Log ("新規登録に失敗: " + e.ErrorMessage);
					GameObject.Find ("Notation").GetComponent<Text>().text = "新規登録に失敗: "
						+ e.ErrorMessage;
				} else {
					UnityEngine.Debug.Log ("新規登録に成功");
					GameObject.Find ("Notation").GetComponent<Text>().text = "新規登録に成功";
					Configuration.username = nameInput.text;
					Application.LoadLevel("title");
				}
			});
		}
	}
  </pre>
  </li>
  <li><b>ヒント</b></li>
  <li><b>ディスカッション</b></li>
</ul>
<h2>『問題二』　落書きを描く機能</h2>
<ul>
  <li><b>キーコード</b><br/>
  <pre>
    blabla...
  </pre>
  </li>
  <li><b>ヒント</b></li>
  <li><b>ディスカッション</b></li>
</ul>
<h2>問題と答え合わせ</h2>
<p>このゲームについての質問は、作者のE－メールに投稿ください。
<br/>作者のE－メール：ellentby@163.com</p>
<p>mbに質問、意見など、<a href="http://mb.cloud.nifty.com/faq.htm">こち</a>に参考して下さい。
<br/>a或いは、<a href="https://github.com/NIFTYCloud-mbaas/UserCommunity">こち</a>に投稿ください。
</p>