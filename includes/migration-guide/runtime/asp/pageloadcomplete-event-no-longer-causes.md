### <a name="pageloadcomplete-event-no-longer-causes-systemwebuiwebcontrolsentitydatasource-control-to-invoke-data-binding"></a><span data-ttu-id="ad5bf-101">Page.LoadComplete 이벤트는 데이터 바인딩을 호출하기 위해 더 이상 System.Web.UI.WebControls.EntityDataSource 컨트롤을 발생시키지 않습니다</span><span class="sxs-lookup"><span data-stu-id="ad5bf-101">Page.LoadComplete event no longer causes System.Web.UI.WebControls.EntityDataSource control to invoke data binding</span></span>

|   |   |
|---|---|
|<span data-ttu-id="ad5bf-102">설명</span><span class="sxs-lookup"><span data-stu-id="ad5bf-102">Details</span></span>|<span data-ttu-id="ad5bf-103"><xref:System.Web.UI.Page.LoadComplete> 이벤트로 인해 더 이상 <xref:System.Web.UI.WebControls.EntityDataSource?displayProperty=name> 컨트롤에서 매개 변수 생성/업데이트/삭제를 위해 변경 내용에 대한 데이터 바인딩을 호출하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad5bf-103">The <xref:System.Web.UI.Page.LoadComplete> event no longer causes the <xref:System.Web.UI.WebControls.EntityDataSource?displayProperty=name> control to invoke data binding for changes to create/update/delete parameters.</span></span> <span data-ttu-id="ad5bf-104">이러한 변경으로 인해 데이터베이스에 대한 불필요한 이동이 제거되고 컨트롤 값이 다시 설정되는 것을 방지하며 <xref:System.Web.UI.WebControls.SqlDataSource?displayProperty=name> 및 <xref:System.Web.UI.WebControls.ObjectDataSource?displayProperty=name> 같은 다른 데이터 컨트롤과 일관된 동작을 발생시킵니다.</span><span class="sxs-lookup"><span data-stu-id="ad5bf-104">This change eliminates an extraneous trip to the database, prevents the values of controls from being reset, and produces behavior that is consistent with other data controls, such as <xref:System.Web.UI.WebControls.SqlDataSource?displayProperty=name> and <xref:System.Web.UI.WebControls.ObjectDataSource?displayProperty=name>.</span></span> <span data-ttu-id="ad5bf-105">이러한 변경으로 인해 드물게 응용 프로그램에서 <xref:System.Web.UI.Page.LoadComplete> 이벤트의 데이터 바인딩 호출을 사용하는 경우 다른 동작이 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5bf-105">This change produces different behavior in the unlikely event that applications rely on invoking data binding in the <xref:System.Web.UI.Page.LoadComplete> event.</span></span>|
|<span data-ttu-id="ad5bf-106">제안 해결 방법</span><span class="sxs-lookup"><span data-stu-id="ad5bf-106">Suggestion</span></span>|<span data-ttu-id="ad5bf-107">데이터 바인딩이 필요한 경우 앞부분에 다시 게시된 이벤트에서 데이터 바인딩을 수동으로 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5bf-107">If there is a need for databinding, manually invoke databind in an event that is earlier in the post-back.</span></span>|
|<span data-ttu-id="ad5bf-108">범위</span><span class="sxs-lookup"><span data-stu-id="ad5bf-108">Scope</span></span>|<span data-ttu-id="ad5bf-109">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ad5bf-109">Edge</span></span>|
|<span data-ttu-id="ad5bf-110">버전</span><span class="sxs-lookup"><span data-stu-id="ad5bf-110">Version</span></span>|<span data-ttu-id="ad5bf-111">4.5</span><span class="sxs-lookup"><span data-stu-id="ad5bf-111">4.5</span></span>|
|<span data-ttu-id="ad5bf-112">형식</span><span class="sxs-lookup"><span data-stu-id="ad5bf-112">Type</span></span>|<span data-ttu-id="ad5bf-113">런타임</span><span class="sxs-lookup"><span data-stu-id="ad5bf-113">Runtime</span></span>|
