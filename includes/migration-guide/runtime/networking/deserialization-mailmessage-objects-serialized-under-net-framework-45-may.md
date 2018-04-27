### <a name="deserialization-of-mailmessage-objects-serialized-under-the-net-framework-45-may-fail"></a><span data-ttu-id="d8de4-101">.NET Framework 4.5에서 직렬화된 MailMessage 개체의 역직렬화가 실패할 수 있음</span><span class="sxs-lookup"><span data-stu-id="d8de4-101">Deserialization of MailMessage objects serialized under the .NET Framework 4.5 may fail</span></span>

|   |   |
|---|---|
|<span data-ttu-id="d8de4-102">설명</span><span class="sxs-lookup"><span data-stu-id="d8de4-102">Details</span></span>|<span data-ttu-id="d8de4-103">.NET Framework 4.5부터는 <xref:System.Web.Mail.MailMessage> 개체에 비 ASCII 문자가 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8de4-103">Starting with the .NET Framework 4.5, <xref:System.Web.Mail.MailMessage> objects can include non-ASCII characters.</span></span> <span data-ttu-id="d8de4-104">.NET Framework 4에서는 ASCII 문자만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8de4-104">In the .NET Framework 4, only ASCII characters are supported.</span></span> <span data-ttu-id="d8de4-105">ASCII가 아닌 문자를 포함하고 .NET Framework 4.5 이상에서 직렬화되는 <xref:System.Web.Mail.MailMessage> 개체는 .NET Framework 4에서 역직렬화될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d8de4-105"><xref:System.Web.Mail.MailMessage> objects that contain non-ASCII characters and that are serialized under the .NET Framework 4.5 or later cannot be deserialized under the .NET Framework 4.</span></span>|
|<span data-ttu-id="d8de4-106">제안 해결 방법</span><span class="sxs-lookup"><span data-stu-id="d8de4-106">Suggestion</span></span>|<span data-ttu-id="d8de4-107"><xref:System.Web.Mail.MailMessage> 개체를 역직렬화할 때 코드가 예외 처리를 제공하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d8de4-107">Ensure that your code provides exception handling when deserializing a <xref:System.Web.Mail.MailMessage> object.</span></span>|
|<span data-ttu-id="d8de4-108">범위</span><span class="sxs-lookup"><span data-stu-id="d8de4-108">Scope</span></span>|<span data-ttu-id="d8de4-109">부</span><span class="sxs-lookup"><span data-stu-id="d8de4-109">Minor</span></span>|
|<span data-ttu-id="d8de4-110">버전</span><span class="sxs-lookup"><span data-stu-id="d8de4-110">Version</span></span>|<span data-ttu-id="d8de4-111">4.5</span><span class="sxs-lookup"><span data-stu-id="d8de4-111">4.5</span></span>|
|<span data-ttu-id="d8de4-112">형식</span><span class="sxs-lookup"><span data-stu-id="d8de4-112">Type</span></span>|<span data-ttu-id="d8de4-113">런타임</span><span class="sxs-lookup"><span data-stu-id="d8de4-113">Runtime</span></span>|
|<span data-ttu-id="d8de4-114">영향을 받는 API</span><span class="sxs-lookup"><span data-stu-id="d8de4-114">Affected APIs</span></span>|<ul><li><xref:System.Web.Mail.MailMessage?displayProperty=nameWithType></li></ul>|
