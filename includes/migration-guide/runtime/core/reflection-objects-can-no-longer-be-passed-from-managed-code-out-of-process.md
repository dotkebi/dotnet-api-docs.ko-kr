### <a name="reflection-objects-can-no-longer-be-passed-from-managed-code-to-out-of-process-dcom-clients"></a><span data-ttu-id="ea881-101">더 이상 리플렉션 개체를 관리 코드에서 out-of-process DCOM 클라이언트로 전달할 수 없습니다</span><span class="sxs-lookup"><span data-stu-id="ea881-101">Reflection objects can no longer be passed from managed code to out-of-process DCOM clients</span></span>

|   |   |
|---|---|
|<span data-ttu-id="ea881-102">설명</span><span class="sxs-lookup"><span data-stu-id="ea881-102">Details</span></span>|<span data-ttu-id="ea881-103">더이상 리플렉션 개체를 관리 코드에서 out-of-process DCOM 클라이언트로 전달할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ea881-103">Reflection objects can no longer be passed from managed code to out-of-process DCOM clients.</span></span> <span data-ttu-id="ea881-104">다음 형식이 영향을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="ea881-104">The following types are affected:</span></span><ul><li><xref:System.Reflection.Assembly?displayProperty=name></li><li><span data-ttu-id="ea881-105"><xref:System.Reflection.MemberInfo?displayProperty=name>(및 <xref:System.Reflection.FieldInfo?displayProperty=name>,<xref:System.Reflection.MethodInfo?displayProperty=name>,<xref:System.Type?displayProperty=name> 및 <xref:System.Reflection.TypeInfo?displayProperty=name>을 포함한 파생된 형식)</span><span class="sxs-lookup"><span data-stu-id="ea881-105"><xref:System.Reflection.MemberInfo?displayProperty=name> (and its derived types, including <xref:System.Reflection.FieldInfo?displayProperty=name>, <xref:System.Reflection.MethodInfo?displayProperty=name>, <xref:System.Type?displayProperty=name>, and <xref:System.Reflection.TypeInfo?displayProperty=name>)</span></span></li><li><xref:System.Reflection.MethodBody?displayProperty=name></li><li><xref:System.Reflection.Module?displayProperty=name></li><li><span data-ttu-id="ea881-106"><xref:System.Reflection.ParameterInfo?displayProperty=name>.</span><span class="sxs-lookup"><span data-stu-id="ea881-106"><xref:System.Reflection.ParameterInfo?displayProperty=name>.</span></span></li></ul><span data-ttu-id="ea881-107">개체에 대한 <code>IMarshal</code>을 호출하면 <code>E_NOINTERFACE</code>를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ea881-107">Calls to <code>IMarshal</code> for the object return <code>E_NOINTERFACE</code>.</span></span>|
|<span data-ttu-id="ea881-108">제안 해결 방법</span><span class="sxs-lookup"><span data-stu-id="ea881-108">Suggestion</span></span>|<span data-ttu-id="ea881-109">마샬링 코드를 리플렉션이 아닌 개체를 사용하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="ea881-109">Update marshaling code to work with non-reflection objects</span></span>|
|<span data-ttu-id="ea881-110">범위</span><span class="sxs-lookup"><span data-stu-id="ea881-110">Scope</span></span>|<span data-ttu-id="ea881-111">부</span><span class="sxs-lookup"><span data-stu-id="ea881-111">Minor</span></span>|
|<span data-ttu-id="ea881-112">버전</span><span class="sxs-lookup"><span data-stu-id="ea881-112">Version</span></span>|<span data-ttu-id="ea881-113">4.6</span><span class="sxs-lookup"><span data-stu-id="ea881-113">4.6</span></span>|
|<span data-ttu-id="ea881-114">형식</span><span class="sxs-lookup"><span data-stu-id="ea881-114">Type</span></span>|<span data-ttu-id="ea881-115">런타임</span><span class="sxs-lookup"><span data-stu-id="ea881-115">Runtime</span></span>|
