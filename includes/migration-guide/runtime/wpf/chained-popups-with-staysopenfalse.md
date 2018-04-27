### <a name="chained-popups-with-staysopenfalse"></a><span data-ttu-id="1fb3f-101">StaysOpen = False인 연결된 팝업</span><span class="sxs-lookup"><span data-stu-id="1fb3f-101">Chained Popups with StaysOpen=False</span></span>

|   |   |
|---|---|
|<span data-ttu-id="1fb3f-102">설명</span><span class="sxs-lookup"><span data-stu-id="1fb3f-102">Details</span></span>|<span data-ttu-id="1fb3f-103">StaysOpen = False인 팝업은 팝업 외부를 클릭하면 닫히게 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fb3f-103">A Popup with StaysOpen=False is supposed to close when you click outside the Popup.</span></span> <span data-ttu-id="1fb3f-104">이러한 팝업이 두 개 이상 연결된 경우(즉, 한 팝업에 다른 팝업이 포함된 경우) 다음과 같은 여러 문제가 발생했습니다.</span><span class="sxs-lookup"><span data-stu-id="1fb3f-104">When two or more such Popups are chained (i.e. one contains another), there were many problems, including:</span></span><ul><li><span data-ttu-id="1fb3f-105">두 수준을 열고 P2의 외부이면서 P1의 내부인 부분을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="1fb3f-105">Open two levels, click outside P2 but inside P1.</span></span>  <span data-ttu-id="1fb3f-106">아무 반응이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1fb3f-106">Nothing happens.</span></span></li><li><span data-ttu-id="1fb3f-107">두 수준을 열고 P1 외부를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="1fb3f-107">Open two levels, click outside P1.</span></span>  <span data-ttu-id="1fb3f-108">두 팝업이 닫힙니다.</span><span class="sxs-lookup"><span data-stu-id="1fb3f-108">Both popups close.</span></span></li><li><span data-ttu-id="1fb3f-109">두 수준을 열고 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="1fb3f-109">Open and close two levels.</span></span>  <span data-ttu-id="1fb3f-110">그런 다음, P2를 다시 열어봅니다.</span><span class="sxs-lookup"><span data-stu-id="1fb3f-110">Then try to open P2 again.</span></span>  <span data-ttu-id="1fb3f-111">아무 반응이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1fb3f-111">Nothing happens.</span></span></li><li><span data-ttu-id="1fb3f-112">세 가지 수준을 열어봅니다.</span><span class="sxs-lookup"><span data-stu-id="1fb3f-112">Try to open three levels.</span></span>  <span data-ttu-id="1fb3f-113">열리지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1fb3f-113">You can't.</span></span>  <span data-ttu-id="1fb3f-114">(클릭한 위치에 따라 아무 일도 일어나지 않거나 처음 두 수준이 닫힙니다.) 이러한 경우(및 다른 변형)는 이제 정상적으로 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="1fb3f-114">(Either nothing happens or the first two levels close, depending on where you click.) These cases (and other variants) now work as expected.</span></span></li></ul>|
|<span data-ttu-id="1fb3f-115">범위</span><span class="sxs-lookup"><span data-stu-id="1fb3f-115">Scope</span></span>|<span data-ttu-id="1fb3f-116">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1fb3f-116">Edge</span></span>|
|<span data-ttu-id="1fb3f-117">버전</span><span class="sxs-lookup"><span data-stu-id="1fb3f-117">Version</span></span>|<span data-ttu-id="1fb3f-118">4.7.1</span><span class="sxs-lookup"><span data-stu-id="1fb3f-118">4.7.1</span></span>|
|<span data-ttu-id="1fb3f-119">형식</span><span class="sxs-lookup"><span data-stu-id="1fb3f-119">Type</span></span>|<span data-ttu-id="1fb3f-120">런타임</span><span class="sxs-lookup"><span data-stu-id="1fb3f-120">Runtime</span></span>|
|<span data-ttu-id="1fb3f-121">영향을 받는 API</span><span class="sxs-lookup"><span data-stu-id="1fb3f-121">Affected APIs</span></span>|<ul><li><xref:System.Windows.Controls.Primitives.Popup.StaysOpen?displayProperty=nameWithType></li></ul>|
