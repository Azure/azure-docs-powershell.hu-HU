---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 368ae4ad814c9414ea211ea6e44c2d3fbda005f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302879"
---
# <span data-ttu-id="9760b-101">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="9760b-101">Get-AzSupportTicket</span></span>

## <span data-ttu-id="9760b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9760b-102">SYNOPSIS</span></span>
<span data-ttu-id="9760b-103">Támogatási jegyeket kaphat.</span><span class="sxs-lookup"><span data-stu-id="9760b-103">Get support tickets.</span></span>

## <span data-ttu-id="9760b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9760b-104">SYNTAX</span></span>

### <span data-ttu-id="9760b-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9760b-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="9760b-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9760b-106">GetByNameParameterSet</span></span>
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="9760b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9760b-107">DESCRIPTION</span></span>
<span data-ttu-id="9760b-108">A támogatási jegyek listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="9760b-108">Gets the list of support tickets.</span></span> <span data-ttu-id="9760b-109">Ha nem ad meg semmilyen paramétert, a program kikeresi az összes támogatási jegyet.</span><span class="sxs-lookup"><span data-stu-id="9760b-109">It will retrieve all the support tickets if you do not specify any parameters.</span></span> <span data-ttu-id="9760b-110">A támogatási jegyeket az állapot vagy a CreatedDate is szűrheti a szűrő paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="9760b-110">You can also filter the support tickets by Status or CreatedDate using the Filter parameter.</span></span> <span data-ttu-id="9760b-111">Íme néhány példa a megadható értékek szűrésére.</span><span class="sxs-lookup"><span data-stu-id="9760b-111">Here are some examples of filter values that you can specify.</span></span>

| <span data-ttu-id="9760b-112">Forgatókönyv</span><span class="sxs-lookup"><span data-stu-id="9760b-112">Scenario</span></span>                                                         | <span data-ttu-id="9760b-113">Szűrő</span><span class="sxs-lookup"><span data-stu-id="9760b-113">Filter</span></span>                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="9760b-114">Nyílt állapotban lévő jegyek beszerzése</span><span class="sxs-lookup"><span data-stu-id="9760b-114">Get tickets that are in open state</span></span>                               | <span data-ttu-id="9760b-115">"Status EQ" Open ""</span><span class="sxs-lookup"><span data-stu-id="9760b-115">"Status eq 'Open'"</span></span>                               |
| <span data-ttu-id="9760b-116">Lezárt állapotú jegyek beszerzése</span><span class="sxs-lookup"><span data-stu-id="9760b-116">Get tickets that are in closed state</span></span>                             | <span data-ttu-id="9760b-117">"Állapot EQ ' zárva" "</span><span class="sxs-lookup"><span data-stu-id="9760b-117">"Status eq 'Closed'"</span></span>                             |
| <span data-ttu-id="9760b-118">A december 20-ig vagy később létrehozott jegyek beszerzése, 2019</span><span class="sxs-lookup"><span data-stu-id="9760b-118">Get tickets that were created on or after 20th Dec, 2019</span></span>         | <span data-ttu-id="9760b-119">"CreatedDate GE 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="9760b-119">"CreatedDate ge 2019-12-20"</span></span>                      |
| <span data-ttu-id="9760b-120">A december 20., 2019 után létrehozott jegyek beszerzése</span><span class="sxs-lookup"><span data-stu-id="9760b-120">Get tickets that were created after 20th Dec, 2019</span></span>               | <span data-ttu-id="9760b-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="9760b-121">"CreatedDate gt 2019-12-20"</span></span>                      |
| <span data-ttu-id="9760b-122">A december 20-ig kezdődően létrehozott jegyek, 2019, amelyek nyílt állapotban vannak</span><span class="sxs-lookup"><span data-stu-id="9760b-122">Gets tickets created after 20th Dec, 2019 that are in open state</span></span> | <span data-ttu-id="9760b-123">"CreatedDate gt 2019-12-20 és status EQ" Open ""</span><span class="sxs-lookup"><span data-stu-id="9760b-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span></span> |


<span data-ttu-id="9760b-124">Ez a parancsmag az első és a kihagyott paraméterek segítségével támogatja a lapozást.</span><span class="sxs-lookup"><span data-stu-id="9760b-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="9760b-125">A jegy nevének megadásával egyetlen támogatási jegyet is betölthet.</span><span class="sxs-lookup"><span data-stu-id="9760b-125">You can also retrieve a single support ticket by specifying the ticket name.</span></span> 

## <span data-ttu-id="9760b-126">Példák</span><span class="sxs-lookup"><span data-stu-id="9760b-126">EXAMPLES</span></span>

### <span data-ttu-id="9760b-127">Példa 1: első 2 jegy beszerzése</span><span class="sxs-lookup"><span data-stu-id="9760b-127">Example 1: Get first 2 tickets</span></span>
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9760b-128">2. példa: az első 2 jegy kihagyása az első 2 után</span><span class="sxs-lookup"><span data-stu-id="9760b-128">Example 2: Get first 2 tickets after skipping the first 2</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9760b-129">3. példa: támogatási jegy beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="9760b-129">Example 3: Get a support ticket by name</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9760b-130">Példa 4: az első 2 támogatási jegy kiszűrése állapot szerint</span><span class="sxs-lookup"><span data-stu-id="9760b-130">Example 4: Get first 2 support tickets filtered by status</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9760b-131">Példa 5: az összes olyan támogatási jegy beszerzése, amely nyitott állapotban van, és a DEC 20th után jön létre, 2019</span><span class="sxs-lookup"><span data-stu-id="9760b-131">Example 5: Get all support tickets that are in Open state and created after Dec 20th, 2019</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="9760b-132">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9760b-132">PARAMETERS</span></span>

### <span data-ttu-id="9760b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9760b-133">-DefaultProfile</span></span>
<span data-ttu-id="9760b-134">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9760b-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9760b-135">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="9760b-135">-Filter</span></span>
<span data-ttu-id="9760b-136">A parancsmag eredményeire alkalmazott szűrő.</span><span class="sxs-lookup"><span data-stu-id="9760b-136">Filter to be applied to the results of this cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9760b-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9760b-137">-Name</span></span>
<span data-ttu-id="9760b-138">Annak a támogatási jegynek a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="9760b-138">Name of support ticket that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9760b-139">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="9760b-139">-IncludeTotalCount</span></span>
<span data-ttu-id="9760b-140">A kijelölt objektumok által követett összes objektum (egész) számát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="9760b-140">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="9760b-141">Ha a parancsmag nem tudja megállapítani a teljes számlálást, az "ismeretlen összeg száma" szöveget jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="9760b-141">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="9760b-142">Az egész számnak van egy pontossági tulajdonsága, amely az összeg megbízhatóságát jelzi.</span><span class="sxs-lookup"><span data-stu-id="9760b-142">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="9760b-143">Az 0,0-től 1,0-ig terjedő pontossági értékek értéke, ahol az 0,0 azt jelenti, hogy a parancsmag nem tudta megszámolni az objektumokat, az 1,0 azt jelenti, hogy a darab pontos, és a 0,0 és a 1,0 közötti érték egyre megbízhatóbb becslést ad.</span><span class="sxs-lookup"><span data-stu-id="9760b-143">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9760b-144">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="9760b-144">-Skip</span></span>
<span data-ttu-id="9760b-145">Figyelmen kívül hagyja a megadott számú objektumot, majd Kinyeri a fennmaradó objektumokat.</span><span class="sxs-lookup"><span data-stu-id="9760b-145">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="9760b-146">Adja meg, hogy hány objektum legyen kihagyva.</span><span class="sxs-lookup"><span data-stu-id="9760b-146">Enter the number of objects to skip.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9760b-147">– Első</span><span class="sxs-lookup"><span data-stu-id="9760b-147">-First</span></span>
<span data-ttu-id="9760b-148">Csak a megadott számú objektumot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9760b-148">Gets only the specified number of objects.</span></span>
<span data-ttu-id="9760b-149">Adja meg a bejutni kívánt objektumok számát.</span><span class="sxs-lookup"><span data-stu-id="9760b-149">Enter the number of objects to get.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9760b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9760b-150">CommonParameters</span></span>
<span data-ttu-id="9760b-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9760b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9760b-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9760b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9760b-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9760b-153">INPUTS</span></span>

### <span data-ttu-id="9760b-154">Nincs</span><span class="sxs-lookup"><span data-stu-id="9760b-154">None</span></span>

## <span data-ttu-id="9760b-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9760b-155">OUTPUTS</span></span>

### <span data-ttu-id="9760b-156">Microsoft. Azure. commands. support. models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="9760b-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="9760b-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9760b-157">NOTES</span></span>

## <span data-ttu-id="9760b-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9760b-158">RELATED LINKS</span></span>
