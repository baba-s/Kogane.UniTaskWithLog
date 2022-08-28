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