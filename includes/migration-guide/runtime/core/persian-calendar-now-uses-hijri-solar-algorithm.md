### <a name="persian-calendar-now-uses-the-hijri-solar-algorithm"></a><span data-ttu-id="c6f8a-101">이제 페르시아력이 회교식 양력 알고리즘을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f8a-101">Persian calendar now uses the Hijri solar algorithm</span></span>

|   |   |
|---|---|
|<span data-ttu-id="c6f8a-102">설명</span><span class="sxs-lookup"><span data-stu-id="c6f8a-102">Details</span></span>|<span data-ttu-id="c6f8a-103">.NET Framework 4.6부터는 <xref:System.Globalization.PersianCalendar?displayProperty=name> 클래스에서 회교식 양력 알고리즘을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f8a-103">Starting with the .NET Framework 4.6, the <xref:System.Globalization.PersianCalendar?displayProperty=name> class uses the Hijri solar algorithm.</span></span> <span data-ttu-id="c6f8a-104">.NET Framework 4.6부터 <xref:System.Globalization.PersianCalendar?displayProperty=name>와 다른 달력 간의 날짜 변환은 1800년 전 또는 2023년 후에 대한 날짜에 대해(그레고리오력) 약간 다른 결과를 생성할 수 있습니다. 또한 <xref:System.Globalization.PersianCalendar.MinSupportedDateTime>은 이제 <code>March 22, 0622 instead of March 21, 0622</code>입니다.</span><span class="sxs-lookup"><span data-stu-id="c6f8a-104">Converting dates between the <xref:System.Globalization.PersianCalendar?displayProperty=name> and other calendars may produce a slightly different result beginning with the .NET Framework 4.6 for dates earlier than 1800 or later than 2023 (Gregorian).Also, <xref:System.Globalization.PersianCalendar.MinSupportedDateTime> is now <code>March 22, 0622 instead of March 21, 0622</code>.</span></span>|
|<span data-ttu-id="c6f8a-105">제안 해결 방법</span><span class="sxs-lookup"><span data-stu-id="c6f8a-105">Suggestion</span></span>|<span data-ttu-id="c6f8a-106">.NET 4.6에서 PersianCalendar를 사용할 때 일부 이전 또는 늦은 날짜는 약간 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6f8a-106">Be aware that some early or late dates may be slightly different when using the PersianCalendar in .NET 4.6.</span></span> <span data-ttu-id="c6f8a-107">또한 다른 .NET Framework 버전에서 실행될 수 있는 프로세스 사이의 날짜를 직렬화할 때 PersianCalendar 날짜 문자열로 저장하지 마십시오(해당 값이 다를 수 있음).</span><span class="sxs-lookup"><span data-stu-id="c6f8a-107">Also, when serializing dates between processes which may run on different .NET Framework versions, do not store them as PersianCalendar date strings (since those values may be different).</span></span>|
|<span data-ttu-id="c6f8a-108">범위</span><span class="sxs-lookup"><span data-stu-id="c6f8a-108">Scope</span></span>|<span data-ttu-id="c6f8a-109">부</span><span class="sxs-lookup"><span data-stu-id="c6f8a-109">Minor</span></span>|
|<span data-ttu-id="c6f8a-110">버전</span><span class="sxs-lookup"><span data-stu-id="c6f8a-110">Version</span></span>|<span data-ttu-id="c6f8a-111">4.6</span><span class="sxs-lookup"><span data-stu-id="c6f8a-111">4.6</span></span>|
|<span data-ttu-id="c6f8a-112">형식</span><span class="sxs-lookup"><span data-stu-id="c6f8a-112">Type</span></span>|<span data-ttu-id="c6f8a-113">런타임</span><span class="sxs-lookup"><span data-stu-id="c6f8a-113">Runtime</span></span>|
|<span data-ttu-id="c6f8a-114">영향을 받는 API</span><span class="sxs-lookup"><span data-stu-id="c6f8a-114">Affected APIs</span></span>|<ul><li><xref:System.Globalization.PersianCalendar?displayProperty=nameWithType></li></ul>|
