
# マイクロソフトの認証ライブラリ - Microsoft Authentication Library (MSAL)

[Microsoft Authentication Library (MSAL)](https://docs.microsoft.com/ja-jp/azure/active-directory/develop/msal-overview) 


MSALを使用すると、Microsoft ID プラットフォーム の エンドポイント(v2.0)からトークンを取得できます。

トークンを使用して、ユーザーを認証し、セキュリティで保護された Web API にアクセスすることができます。

MSAL では、多くのプラットフォームで API に一貫性があり、さまざまな方法でトークンを取得できます。

開発者は、アプリケーションのプロトコルに対して OAuth ライブラリまたはコードを直接使用する必要がなくなります。

MSAL は、.NET、JavaScript、Java、Python、Android、iOS などの、さまざまなアプリケーション アーキテクチャとプラットフォームをサポートします。

(ADALに比較して）より広範な認証をサポート

- オンプレミスAD DSのアカウント
- Azure AD の ID(職場や学校のアカウント)
- Microsoft アカウント
- Azure AD B2C - ソーシャル アカウント


# ADAL - AD Authentication Library

Active Directory Authentication Library (ADAL) 

Azure AD v1.0 エンドポイントを利用

「しょくば


MSAL.NET は、Microsoft ID プラットフォームと併せて使用する場合にお勧めの認証ライブラリです。 ADAL.NET に新しい機能は実装されません。 この取り組みは、MSAL の改良に重点を置いています。

# [パブリッククラウドアプリケーションと機密クライアントアプリケーション](https://docs.microsoft.com/ja-jp/azure/active-directory/develop/msal-client-applications)

Microsoft Authentication Library (MSAL) には、2 種類のクライアントが定義されています。パブリック クライアントと機密クライアントです。 

機密クライアント アプリケーションは、サーバー上で実行されるアプリ (Web アプリ、Web API アプリ、さらにはサービス アプリやデーモン アプリ) です。

これらはアクセスが困難であると考えられているため、アプリケーション シークレットを保持することができます。

クライアント ID は Web ブラウザーを介して公開されますが、シークレットはバック チャネルでのみ渡され、直接公開されることはありません。

```
デーモン アプリ
IConfidentialClientApplication 
```

パブリック クライアント アプリケーションは、デバイスまたはデスクトップ コンピューターあるいは Web ブラウザーで実行されるアプリです。 

それらにはアプリケーション シークレットを安全に保持するという信頼がないため、ユーザーに代わって Web API にアクセスすることしかできません (パブリック クライアント フローのみがサポートされます)。

パブリック クライアントは構成時のシークレットを保持できません。そのため、クライアント シークレットを備えていません。

```
Web APIを呼び出すデスクトップアプリ
IPublicClientApplication
```


