# Kogane UniTask With Log

UniTask で処理の開始時と終了時にログを出力できる関数

## 使用例

```csharp
using Cysharp.Threading.Tasks;
using UnityEngine;

public class Example : MonoBehaviour
{
    private async UniTaskVoid Start()
    {
        await UniTask.WithLog( "PlayAsync", () => PlayAsync() );
        await UniTask.WithTimeLog( "PlayAsync", () => PlayAsync() );
    }

    private static async UniTask PlayAsync()
    {
        await UniTask.NextFrame();
    }
}
```

![2022-08-28_123743](https://user-images.githubusercontent.com/6134875/187056287-e610940a-ff41-426f-9dcc-4f7144139747.png)
