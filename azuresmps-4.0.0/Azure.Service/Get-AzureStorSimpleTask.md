---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CF3548F6-03FE-44D6-AA2C-1015611C657A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0423fe51a047385ef6395075dd116b4d4189c667
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015552"
---
# <span data-ttu-id="330b2-101">Get-AzureStorSimpleTask</span><span class="sxs-lookup"><span data-stu-id="330b2-101">Get-AzureStorSimpleTask</span></span>

## <span data-ttu-id="330b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="330b2-102">SYNOPSIS</span></span>
<span data-ttu-id="330b2-103">Egy tevékenység állapotát StorSimple eszközön kapja.</span><span class="sxs-lookup"><span data-stu-id="330b2-103">Gets status of a task on a StorSimple device.</span></span>

## <span data-ttu-id="330b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="330b2-104">SYNTAX</span></span>

```
Get-AzureStorSimpleTask -InstanceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="330b2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="330b2-105">DESCRIPTION</span></span>
<span data-ttu-id="330b2-106">A **Get-AzureStorSimpleTask** parancsmag egy olyan tevékenység állapotát kérdezi le, amely az Azure StorSimple-eszközön aszinkron módon fut.</span><span class="sxs-lookup"><span data-stu-id="330b2-106">The **Get-AzureStorSimpleTask** cmdlet retrieves the status of a task that runs asynchronously on an Azure StorSimple device.</span></span>

<span data-ttu-id="330b2-107">A StorSimple-eszközök kezelésekor a legtöbb létrehozás, olvasás, frissítés és törlés művelet aszinkron módon futtatható.</span><span class="sxs-lookup"><span data-stu-id="330b2-107">While you manage a StorSimple device, most create, read, update, and delete actions can run asynchronously.</span></span>
<span data-ttu-id="330b2-108">A Windows PowerShell egy **TaskId** ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="330b2-108">Windows PowerShell returns a **TaskId**.</span></span>
<span data-ttu-id="330b2-109">Használja az azonosítót a tevékenység aktuális állapotának a beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="330b2-109">Use the ID to get the current status of the task.</span></span>

## <span data-ttu-id="330b2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="330b2-110">EXAMPLES</span></span>

### <span data-ttu-id="330b2-111">Példa 1: tevékenység állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="330b2-111">Example 1: Get the status of a task</span></span>
```
PS C:\>Get-AzureStorSimpleTask -TaskId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: d9c1e8a7-994f-4698-8b42-064600b45cad_PS
VERBOSE: ClientRequestId: aae17c82-6fd3-435e-a965-1c66b3c955fe_PS


AsyncTaskAggregatedResult : Succeeded
Error                     : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
Result                    : Succeeded
Status                    : Completed
TaskId                    : 53816d8d-a8b5-4c1d-a177-e59007608d6d
TaskSteps                 : {}
StatusCode                : OK
RequestId                 : e9174990825750bba69383748f23019c
```

<span data-ttu-id="330b2-112">Ez a parancs a megadott azonosítót tartalmazó tevékenység állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="330b2-112">This command gets the status of the task that has the specified ID.</span></span>
<span data-ttu-id="330b2-113">Az eredmények azt mutatják, hogy a tevékenység állapota befejeződött, és a sikeres eredmény eredménye.</span><span class="sxs-lookup"><span data-stu-id="330b2-113">The results show that the task has a status of completed and a result of successful.</span></span>

## <span data-ttu-id="330b2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="330b2-114">PARAMETERS</span></span>

### <span data-ttu-id="330b2-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="330b2-115">-InstanceId</span></span>
<span data-ttu-id="330b2-116">Annak a tevékenységnek az AZONOSÍTÓját adja meg, amelynek a parancsmagja követi az állapotot.</span><span class="sxs-lookup"><span data-stu-id="330b2-116">Specifies the ID of the task for which this cmdlet tracks status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="330b2-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="330b2-117">-Profile</span></span>
<span data-ttu-id="330b2-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="330b2-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="330b2-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="330b2-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="330b2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="330b2-120">CommonParameters</span></span>
<span data-ttu-id="330b2-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="330b2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="330b2-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="330b2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="330b2-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="330b2-123">INPUTS</span></span>

### <span data-ttu-id="330b2-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="330b2-124">None</span></span>

## <span data-ttu-id="330b2-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="330b2-125">OUTPUTS</span></span>

### <span data-ttu-id="330b2-126">JobStatusInfo</span><span class="sxs-lookup"><span data-stu-id="330b2-126">JobStatusInfo</span></span>
<span data-ttu-id="330b2-127">Ez a parancsmag egy **TaskStatusInfo** -objektumot ad eredményül, amely az alábbi mezőket tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="330b2-127">This cmdlet returns a **TaskStatusInfo** object which contains the following fields:</span></span> 

- <span data-ttu-id="330b2-128">**Hiba lép** fel.</span><span class="sxs-lookup"><span data-stu-id="330b2-128">**Error**.</span></span>
<span data-ttu-id="330b2-129">**ErrorDetails** , amely **kódot** és **üzenetet** tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="330b2-129">**ErrorDetails** , which contains **Code** and **Message**.</span></span>
- <span data-ttu-id="330b2-130">**TaskId**.</span><span class="sxs-lookup"><span data-stu-id="330b2-130">**TaskId**.</span></span>
<span data-ttu-id="330b2-131">**Karakterlánc**.</span><span class="sxs-lookup"><span data-stu-id="330b2-131">**String**.</span></span>
<span data-ttu-id="330b2-132">Annak a tevékenységnek az azonosítója, amelyhez az állapotot visszaadja.</span><span class="sxs-lookup"><span data-stu-id="330b2-132">The ID of the task for which status is returned.</span></span>
- <span data-ttu-id="330b2-133">**TaskSteps**.</span><span class="sxs-lookup"><span data-stu-id="330b2-133">**TaskSteps**.</span></span>
<span data-ttu-id="330b2-134">**IList \<TaskStep\>**.</span><span class="sxs-lookup"><span data-stu-id="330b2-134">**IList\<TaskStep\>**.</span></span>
<span data-ttu-id="330b2-135">Minden **TaskStep** -objektum tartalmaz **részleteket** , **errorcode** , **üzenetet** , **eredményt** és **állapotot**.</span><span class="sxs-lookup"><span data-stu-id="330b2-135">Each **TaskStep** object contains **Detail** , **ErrorCode** , **Message** , **Result** , and **Status**.</span></span>
- <span data-ttu-id="330b2-136">**Result (eredmény** )</span><span class="sxs-lookup"><span data-stu-id="330b2-136">**Result**.</span></span>
<span data-ttu-id="330b2-137">**TaskResult** , amely a tevékenység teljes eredményét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="330b2-137">**TaskResult** , which contains the overall result of the task.</span></span>
<span data-ttu-id="330b2-138">Az érvényes értékek a következők: nem sikerült, sikerült, PartialSuccess, lemondott és érvénytelen.</span><span class="sxs-lookup"><span data-stu-id="330b2-138">Valid values are: Failed, Succeeded, PartialSuccess, Cancelled, and Invalid.</span></span>
- <span data-ttu-id="330b2-139">**Állapotot**.</span><span class="sxs-lookup"><span data-stu-id="330b2-139">**Status**.</span></span>
<span data-ttu-id="330b2-140">**TaskStatus** , amely a tevékenység teljes futási állapotát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="330b2-140">**TaskStatus** , which contains the overall running status of the task.</span></span>
<span data-ttu-id="330b2-141">Az érvényes értékek a következők: Inprogress, érvénytelen és befejezett.</span><span class="sxs-lookup"><span data-stu-id="330b2-141">Valid values are: Inprogress, Invalid, and Completed.</span></span>
- <span data-ttu-id="330b2-142">**TaskResult**.</span><span class="sxs-lookup"><span data-stu-id="330b2-142">**TaskResult**.</span></span>
<span data-ttu-id="330b2-143">**TaskResult** , az **eredmény** és az **állapot** alapján kiszámított érték.</span><span class="sxs-lookup"><span data-stu-id="330b2-143">**TaskResult** , a value computed based on **Result** and **Status**.</span></span>
<span data-ttu-id="330b2-144">Az érvényes értékek a következők: sikertelenek, sikeresek, inelőrehaladás, PartialSuccess, lemondás és érvénytelen.</span><span class="sxs-lookup"><span data-stu-id="330b2-144">Valid values are: Failed, Succeeded, InProgress, PartialSuccess, Cancelled, and Invalid.</span></span>

## <span data-ttu-id="330b2-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="330b2-145">NOTES</span></span>

## <span data-ttu-id="330b2-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="330b2-146">RELATED LINKS</span></span>

