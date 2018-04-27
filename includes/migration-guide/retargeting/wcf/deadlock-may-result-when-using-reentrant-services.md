### <a name="deadlock-may-result-when-using-reentrant-services"></a><span data-ttu-id="87f02-101">재진입 서비스를 사용할 때 교착 상태가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87f02-101">Deadlock may result when using Reentrant services</span></span>

|   |   |
|---|---|
|<span data-ttu-id="87f02-102">설명</span><span class="sxs-lookup"><span data-stu-id="87f02-102">Details</span></span>|<span data-ttu-id="87f02-103">교착 상태가 발생하면 재진입 서비스의 인스턴스가 한번에 하나의 실행 스레드로 제한됩니다.</span><span class="sxs-lookup"><span data-stu-id="87f02-103">A deadlock may result in a Reentrant service, which restricts instances of the service to one thread of execution at a time.</span></span> <span data-ttu-id="87f02-104">이 문제가 발생하기 쉬운 서비스는 코드에 다음과 같은 <xref:System.ServiceModel.ServiceBehaviorAttribute>가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87f02-104">Services prone to encounter this problem will have the following <xref:System.ServiceModel.ServiceBehaviorAttribute> in their code:</span></span><pre><code class="language-csharp">[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Reentrant)]&#13;&#10;</code></pre>|
|<span data-ttu-id="87f02-105">제안 해결 방법</span><span class="sxs-lookup"><span data-stu-id="87f02-105">Suggestion</span></span>|<span data-ttu-id="87f02-106">이 문제를 해결하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="87f02-106">To address this issue, you can do the following:</span></span><ul><li><span data-ttu-id="87f02-107">서비스의 동시성 모드를 <xref:System.ServiceModel.ConcurrencyMode.Single?displayProperty=nameWithType> 또는 &lt;System.ServiceModel.ConcurrencyMode.Multiple?displayProperty=nameWithType&gt;로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="87f02-107">Set the service's concurrency mode to <xref:System.ServiceModel.ConcurrencyMode.Single?displayProperty=nameWithType> or &lt;System.ServiceModel.ConcurrencyMode.Multiple?displayProperty=nameWithType&gt;.</span></span> <span data-ttu-id="87f02-108">예:</span><span class="sxs-lookup"><span data-stu-id="87f02-108">For example:</span></span></li></ul><pre><code class="language-csharp">[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Single)]&#13;&#10;</code></pre><ul><li><span data-ttu-id="87f02-109">.NET Framework 4.6.2의 최신 업데이트를 설치하거나 이후 버전의 .NET Framework로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="87f02-109">Install the latest update to the .NET Framework 4.6.2, or upgrade to a later version of the .NET Framework.</span></span> <span data-ttu-id="87f02-110">이렇게 하면 <xref:System.ServiceModel.OperationContext.Current?displayProperty=nameWithType>에서 <xref:System.Threading.ExecutionContext>의 흐름이 비활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="87f02-110">This disables the flow of the <xref:System.Threading.ExecutionContext> in <xref:System.ServiceModel.OperationContext.Current?displayProperty=nameWithType>.</span></span> <span data-ttu-id="87f02-111">이 동작은 구성할 수 있습니다. 구성 파일에 다음 앱 설정을 추가하는 것과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="87f02-111">This behavior is configurable; it is equivalent to adding the following app setting to your configuration file:</span></span></li></ul><pre><code class="language-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;Switch.System.ServiceModel.DisableOperationContextAsyncFlow&quot; value=&quot;true&quot; /&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;&#13;&#10;The value of &#39;Switch.System.ServiceModel.DisableOperationContextAsyncFlow&#39; should never be set to &#39;false&#39; for Rentrant services.&#13;&#10;</code></pre>|
|<span data-ttu-id="87f02-112">범위</span><span class="sxs-lookup"><span data-stu-id="87f02-112">Scope</span></span>|<span data-ttu-id="87f02-113">부</span><span class="sxs-lookup"><span data-stu-id="87f02-113">Minor</span></span>|
|<span data-ttu-id="87f02-114">버전</span><span class="sxs-lookup"><span data-stu-id="87f02-114">Version</span></span>|<span data-ttu-id="87f02-115">4.6.2</span><span class="sxs-lookup"><span data-stu-id="87f02-115">4.6.2</span></span>|
|<span data-ttu-id="87f02-116">형식</span><span class="sxs-lookup"><span data-stu-id="87f02-116">Type</span></span>|<span data-ttu-id="87f02-117">대상 변경</span><span class="sxs-lookup"><span data-stu-id="87f02-117">Retargeting</span></span>|
|<span data-ttu-id="87f02-118">영향을 받는 API</span><span class="sxs-lookup"><span data-stu-id="87f02-118">Affected APIs</span></span>|<ul><li><xref:System.ServiceModel.ServiceBehaviorAttribute?displayProperty=nameWithType></li><li><xref:System.ServiceModel.ConcurrencyMode.Reentrant?displayProperty=nameWithType></li></ul>|
