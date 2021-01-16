---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 368ae4ad814c9414ea211ea6e44c2d3fbda005f7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330198"
---
# <span data-ttu-id="f4e3c-101">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="f4e3c-101">Get-AzSupportTicket</span></span>

## <span data-ttu-id="f4e3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4e3c-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e3c-103">Támogatási jegyeket is vásárolhat.</span><span class="sxs-lookup"><span data-stu-id="f4e3c-103">Get support tickets.</span></span>

## <span data-ttu-id="f4e3c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f4e3c-104">SYNTAX</span></span>

### <span data-ttu-id="f4e3c-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f4e3c-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f4e3c-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4e3c-106">GetByNameParameterSet</span></span>
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="f4e3c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f4e3c-107">DESCRIPTION</span></span>
<span data-ttu-id="f4e3c-108">A támogatási jegylista lekérte.</span><span class="sxs-lookup"><span data-stu-id="f4e3c-108">Gets the list of support tickets.</span></span> <span data-ttu-id="f4e3c-109">Ha nem ad meg paramétereket, a rendszer beolvassa az összes támogatási jegyet.</span><span class="sxs-lookup"><span data-stu-id="f4e3c-109">It will retrieve all the support tickets if you do not specify any parameters.</span></span> <span data-ttu-id="f4e3c-110">A támogatási jegyeket állapot vagy CreatedDate szerint is szűrheti a Szűrő paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="f4e3c-110">You can also filter the support tickets by Status or CreatedDate using the Filter parameter.</span></span> <span data-ttu-id="f4e3c-111">Íme néhány példa a megadható szűrőértékek használatára.</span><span class="sxs-lookup"><span data-stu-id="f4e3c-111">Here are some examples of filter values that you can specify.</span></span>

| <span data-ttu-id="f4e3c-112">Eset</span><span class="sxs-lookup"><span data-stu-id="f4e3c-112">Scenario</span></span>                                                         | <span data-ttu-id="f4e3c-113">Szűrés</span><span class="sxs-lookup"><span data-stu-id="f4e3c-113">Filter</span></span>                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="f4e3c-114">Nyitott állapotban elérhető jegyek lekérte</span><span class="sxs-lookup"><span data-stu-id="f4e3c-114">Get tickets that are in open state</span></span>                               | <span data-ttu-id="f4e3c-115">"Status eq 'Open'" (Állapot eq 'Megnyitás')</span><span class="sxs-lookup"><span data-stu-id="f4e3c-115">"Status eq 'Open'"</span></span>                               |
| <span data-ttu-id="f4e3c-116">Lezárt állapotban elérhető jegyek lekérte</span><span class="sxs-lookup"><span data-stu-id="f4e3c-116">Get tickets that are in closed state</span></span>                             | <span data-ttu-id="f4e3c-117">"Status eq 'Closed'"</span><span class="sxs-lookup"><span data-stu-id="f4e3c-117">"Status eq 'Closed'"</span></span>                             |
| <span data-ttu-id="f4e3c-118">2019. december 20-án vagy azt követően létrehozott jegyek lekérte</span><span class="sxs-lookup"><span data-stu-id="f4e3c-118">Get tickets that were created on or after 20th Dec, 2019</span></span>         | <span data-ttu-id="f4e3c-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="f4e3c-119">"CreatedDate ge 2019-12-20"</span></span>                      |
| <span data-ttu-id="f4e3c-120">2019. december 20. után létrehozott jegyek lekértek</span><span class="sxs-lookup"><span data-stu-id="f4e3c-120">Get tickets that were created after 20th Dec, 2019</span></span>               | <span data-ttu-id="f4e3c-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="f4e3c-121">"CreatedDate gt 2019-12-20"</span></span>                      |
| <span data-ttu-id="f4e3c-122">Nyitott állapotban 2019. december 20. után létrehozott jegyeket kap</span><span class="sxs-lookup"><span data-stu-id="f4e3c-122">Gets tickets created after 20th Dec, 2019 that are in open state</span></span> | <span data-ttu-id="f4e3c-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span><span class="sxs-lookup"><span data-stu-id="f4e3c-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span></span> |


<span data-ttu-id="f4e3c-124">Ez a parancsmag az Első és a Kihagyás paraméteren keresztüli lapozást támogatja.</span><span class="sxs-lookup"><span data-stu-id="f4e3c-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="f4e3c-125">A jegy nevének megadásával egyetlen támogatási jegyet is lekérhet.</span><span class="sxs-lookup"><span data-stu-id="f4e3c-125">You can also retrieve a single support ticket by specifying the ticket name.</span></span> 

## <span data-ttu-id="f4e3c-126">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f4e3c-126">EXAMPLES</span></span>

### <span data-ttu-id="f4e3c-127">1. példa: Az első 2 jegy lekérte</span><span class="sxs-lookup"><span data-stu-id="f4e3c-127">Example 1: Get first 2 tickets</span></span>
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f4e3c-128">2. példa: Az első 2 jegy leugrása után az első 2 jegy lekérte</span><span class="sxs-lookup"><span data-stu-id="f4e3c-128">Example 2: Get first 2 tickets after skipping the first 2</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f4e3c-129">3. példa: Támogatási jegy lekért név szerint</span><span class="sxs-lookup"><span data-stu-id="f4e3c-129">Example 3: Get a support ticket by name</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f4e3c-130">4. példa: Az első 2 támogatási jegy állapot szerint szűrve</span><span class="sxs-lookup"><span data-stu-id="f4e3c-130">Example 4: Get first 2 support tickets filtered by status</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f4e3c-131">5. példa: Az összes nyitott állapotban létrehozott és 2019. december 20. után létrehozott támogatási jegy lekérte</span><span class="sxs-lookup"><span data-stu-id="f4e3c-131">Example 5: Get all support tickets that are in Open state and created after Dec 20th, 2019</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="f4e3c-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4e3c-132">PARAMETERS</span></span>

### <span data-ttu-id="f4e3c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e3c-133">-DefaultProfile</span></span>
<span data-ttu-id="f4e3c-134">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4e3c-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4e3c-135">-Filter</span><span class="sxs-lookup"><span data-stu-id="f4e3c-135">-Filter</span></span>
<span data-ttu-id="f4e3c-136">A parancsmag eredményéhez alkalmazandó szűrő.</span><span class="sxs-lookup"><span data-stu-id="f4e3c-136">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="f4e3c-137">-Name</span><span class="sxs-lookup"><span data-stu-id="f4e3c-137">-Name</span></span>
<span data-ttu-id="f4e3c-138">A parancsmag támogatási jegyének neve.</span><span class="sxs-lookup"><span data-stu-id="f4e3c-138">Name of support ticket that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f4e3c-139">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="f4e3c-139">-IncludeTotalCount</span></span>
<span data-ttu-id="f4e3c-140">Az adatkészletben lévő objektumok teljes számát (egész számot) és a kijelölt objektumokat jelenti.</span><span class="sxs-lookup"><span data-stu-id="f4e3c-140">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="f4e3c-141">Ha a parancsmag nem tudja megállapítani a teljes számát, az "Ismeretlen teljes szám" üzenetet jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="f4e3c-141">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="f4e3c-142">Az egész szám pontossági tulajdonsága a teljes darabszám megbízhatóságát jelzi.</span><span class="sxs-lookup"><span data-stu-id="f4e3c-142">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="f4e3c-143">A pontosság értéke 0,0 és 1,0 között van, ahol a 0,0 azt jelenti, hogy a parancsmag nem tudta megszámolni az objektumokat, az 1,0 azt jelenti, hogy a szám pontos, és a 0,0 és 1,0 közötti érték egyre megbízhatóbb becslést jelez.</span><span class="sxs-lookup"><span data-stu-id="f4e3c-143">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="f4e3c-144">-Skip</span><span class="sxs-lookup"><span data-stu-id="f4e3c-144">-Skip</span></span>
<span data-ttu-id="f4e3c-145">Figyelmen kívül hagyja a megadott számú objektumot, majd beveszi a fennmaradó objektumokat.</span><span class="sxs-lookup"><span data-stu-id="f4e3c-145">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="f4e3c-146">Adja meg, hogy hány objektumot kell kihagyni.</span><span class="sxs-lookup"><span data-stu-id="f4e3c-146">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="f4e3c-147">-First</span><span class="sxs-lookup"><span data-stu-id="f4e3c-147">-First</span></span>
<span data-ttu-id="f4e3c-148">Csak a megadott számú objektumot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f4e3c-148">Gets only the specified number of objects.</span></span>
<span data-ttu-id="f4e3c-149">Adja meg a lekért objektumok számát.</span><span class="sxs-lookup"><span data-stu-id="f4e3c-149">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="f4e3c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e3c-150">CommonParameters</span></span>
<span data-ttu-id="f4e3c-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4e3c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e3c-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4e3c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e3c-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4e3c-153">INPUTS</span></span>

### <span data-ttu-id="f4e3c-154">Nincs</span><span class="sxs-lookup"><span data-stu-id="f4e3c-154">None</span></span>

## <span data-ttu-id="f4e3c-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4e3c-155">OUTPUTS</span></span>

### <span data-ttu-id="f4e3c-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="f4e3c-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="f4e3c-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f4e3c-157">NOTES</span></span>

## <span data-ttu-id="f4e3c-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4e3c-158">RELATED LINKS</span></span>
