# Como Usar no React Native App

## URL do Repo

```
https://github.com/OnoSendae/gh-codepush-storage
```

## Configuração no App

### Android (`android/app/src/main/res/values/strings.xml`)

```xml
<resources>
    <string name="app_name">OnoSendae</string>
    
    <!-- CodePush -->
    <string name="CodePushServerUrl">https://raw.githubusercontent.com/OnoSendae/gh-codepush-storage/main</string>
    <string name="CodePushDeploymentKey">Production</string>
</resources>
```

### iOS (`ios/OnoSendae/Info.plist`)

```xml
<dict>
    <!-- ... outras configs ... -->
    
    <!-- CodePush -->
    <key>CodePushServerURL</key>
    <string>https://raw.githubusercontent.com/OnoSendae/gh-codepush-storage/main</string>
    <key>CodePushDeploymentKey</key>
    <string>Production</string>
</dict>
```

## Instalação

```bash
npm install react-native-code-push
```

## Código App

```javascript
import CodePush from 'react-native-code-push';

const App = () => {
  return (
    <View>
      <Text>OnoSendae App</Text>
    </View>
  );
};

export default CodePush(App);
```

## Testando

### 1. App baixa de:
```
https://raw.githubusercontent.com/OnoSendae/gh-codepush-storage/main/index.json
```

### 2. Encontra:
```json
{
  "apps": {
    "OnoSendae": {
      "Production": {
        "currentRelease": "v1",
        "bundleUrl": "bundles/OnoSendae/Production/v1/bundle.js",
        "hash": "23e03e1b...",
        "signature": "SALCQ7..."
      }
    }
  }
}
```

### 3. Baixa bundle:
```
https://raw.githubusercontent.com/OnoSendae/gh-codepush-storage/main/bundles/OnoSendae/Production/v1/bundle.js
```

### 4. Valida hash + signature

### 5. Aplica update!

---

**ZERO servidor. ZERO custo. Só GitHub. 🚀**

