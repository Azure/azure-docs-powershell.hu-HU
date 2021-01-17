---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 07a8747f94f9c1fb93bbff06ce855363088a67a0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466829"
---
# <span data-ttu-id="1a9d6-101">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="1a9d6-101">Get-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="1a9d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a9d6-102">SYNOPSIS</span></span>
<span data-ttu-id="1a9d6-103">Támogatási jegykommunikációt.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-103">Get support ticket communications.</span></span>

## <span data-ttu-id="1a9d6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1a9d6-104">SYNTAX</span></span>

### <span data-ttu-id="1a9d6-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1a9d6-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a9d6-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a9d6-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a9d6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1a9d6-107">DESCRIPTION</span></span>
<span data-ttu-id="1a9d6-108">Egy támogatási jegy kommunikációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-108">Gets communications for a support ticket.</span></span> <span data-ttu-id="1a9d6-109">Ha nem ad meg más paramétereket, a rendszer beolvassa egy jegy összes kommunikációját.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-109">It will retrieve all the communications for a ticket if you do not specify any other parameters.</span></span> <span data-ttu-id="1a9d6-110">A CreatedDate vagy a CommunicationType paraméterrel is szűrheti a kommunikációt a Szűrő paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-110">You can also filter the communications by CreatedDate or CommunicationType using the Filter parameter.</span></span> <span data-ttu-id="1a9d6-111">Íme néhány példa a megadható szűrőértékek használatára.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-111">Here are some examples of filter values that you can specify.</span></span>


| <span data-ttu-id="1a9d6-112">Eset</span><span class="sxs-lookup"><span data-stu-id="1a9d6-112">Scenario</span></span>                                                        | <span data-ttu-id="1a9d6-113">Szűrés</span><span class="sxs-lookup"><span data-stu-id="1a9d6-113">Filter</span></span>                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1a9d6-114">Webes kommunikáció lekérte</span><span class="sxs-lookup"><span data-stu-id="1a9d6-114">Get Web communications</span></span>                                          | <span data-ttu-id="1a9d6-115">"CommunicationType eq 'Web'"</span><span class="sxs-lookup"><span data-stu-id="1a9d6-115">"CommunicationType eq 'Web'"</span></span>                               |
| <span data-ttu-id="1a9d6-116">Telefonos kommunikáció lekommunikáció</span><span class="sxs-lookup"><span data-stu-id="1a9d6-116">Get Phone communications</span></span>                                        | <span data-ttu-id="1a9d6-117">"CommunicationType eq 'Phone'"</span><span class="sxs-lookup"><span data-stu-id="1a9d6-117">"CommunicationType eq 'Phone'"</span></span>                             |
| <span data-ttu-id="1a9d6-118">2019. december 20-án vagy azt követően létrehozott kommunikációk lekérte</span><span class="sxs-lookup"><span data-stu-id="1a9d6-118">Get communications that were created on or after 20th Dec, 2019</span></span> | <span data-ttu-id="1a9d6-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="1a9d6-119">"CreatedDate ge 2019-12-20"</span></span>                                |
| <span data-ttu-id="1a9d6-120">2019. december 20. után létrehozott kommunikáció lekérte</span><span class="sxs-lookup"><span data-stu-id="1a9d6-120">Get communications that were created after 20th Dec, 2019</span></span>       | <span data-ttu-id="1a9d6-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="1a9d6-121">"CreatedDate gt 2019-12-20"</span></span>                                |
| <span data-ttu-id="1a9d6-122">2019. december 20. után létrehozott webes kommunikációt kap</span><span class="sxs-lookup"><span data-stu-id="1a9d6-122">Gets Web communications created after 20th Dec, 2019</span></span>            | <span data-ttu-id="1a9d6-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web"</span><span class="sxs-lookup"><span data-stu-id="1a9d6-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span></span> |


<span data-ttu-id="1a9d6-124">Ez a parancsmag az Első és a Kihagyás paraméteren keresztüli lapozást támogatja.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="1a9d6-125">Egyetlen támogatási jegy kommunikációját is lekérheti a kapcsolat nevének megadásával.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-125">You can also retrieve a single support ticket communication by specifying the communication name.</span></span> 

## <span data-ttu-id="1a9d6-126">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1a9d6-126">EXAMPLES</span></span>

### <span data-ttu-id="1a9d6-127">1. példa: Támogatási jegy összes kommunikációját lekérheti</span><span class="sxs-lookup"><span data-stu-id="1a9d6-127">Example 1: Retrieve all communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### <span data-ttu-id="1a9d6-128">2. példa: Egyetlen kapcsolat lekérése egy támogatási jegy nevével</span><span class="sxs-lookup"><span data-stu-id="1a9d6-128">Example 2: Retrieve a single communication by it's name for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### <span data-ttu-id="1a9d6-129">3. példa: Az első 2 kommunikáció lekérése egy támogatási jegyhez</span><span class="sxs-lookup"><span data-stu-id="1a9d6-129">Example 3: Retrieve first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="1a9d6-130">4. példa: A következő 2 kommunikáció lekérése egy támogatási jegy első 2 kommunikációját kihagyva</span><span class="sxs-lookup"><span data-stu-id="1a9d6-130">Example 4: Retrieve next 2 communications after skipping first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="1a9d6-131">5. példa: Az összes webes kommunikáció lekérése egy támogatási jegyhez</span><span class="sxs-lookup"><span data-stu-id="1a9d6-131">Example 5: Retrieve all Web communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="1a9d6-132">6. példa: Támogatási jegy 2019. december 20-án vagy után létrehozott összes kommunikáció beolvasása</span><span class="sxs-lookup"><span data-stu-id="1a9d6-132">Example 6: Retrieve all communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="1a9d6-133">7. példa: Támogatási jegy 2019. december 20-án vagy után létrehozott összes webes kommunikáció beolvasása</span><span class="sxs-lookup"><span data-stu-id="1a9d6-133">Example 7: Retrieve all Web communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="1a9d6-134">8. példa: Támogatási jegy összes kommunikációját lekérheti a támogatási jegy objektumának kipipázásával</span><span class="sxs-lookup"><span data-stu-id="1a9d6-134">Example 8: Retrieve all communications for a support ticket by piping support ticket object</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

## <span data-ttu-id="1a9d6-135">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a9d6-135">PARAMETERS</span></span>

### <span data-ttu-id="1a9d6-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a9d6-136">-DefaultProfile</span></span>
<span data-ttu-id="1a9d6-137">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a9d6-138">-Filter</span><span class="sxs-lookup"><span data-stu-id="1a9d6-138">-Filter</span></span>
<span data-ttu-id="1a9d6-139">A parancsmag eredményéhez alkalmazandó szűrő.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-139">Filter to be applied to the results of this cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a9d6-140">-Name</span><span class="sxs-lookup"><span data-stu-id="1a9d6-140">-Name</span></span>
<span data-ttu-id="1a9d6-141">Kommunikációs név.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-141">Communication name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a9d6-142">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="1a9d6-142">-SupportTicketName</span></span>
<span data-ttu-id="1a9d6-143">Támogatási jegy neve.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-143">Support ticket name.</span></span>

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

### <span data-ttu-id="1a9d6-144">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="1a9d6-144">-SupportTicketObject</span></span>
<span data-ttu-id="1a9d6-145">Támogatási jegy objektum.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-145">Support ticket object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a9d6-146">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="1a9d6-146">-IncludeTotalCount</span></span>
<span data-ttu-id="1a9d6-147">Az adatkészletben lévő objektumok teljes számát (egész számot) és a kijelölt objektumokat jelenti.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-147">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="1a9d6-148">Ha a parancsmag nem tudja megállapítani a teljes számát, az "Ismeretlen teljes szám" üzenetet jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-148">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="1a9d6-149">Az egész szám pontossági tulajdonsága a teljes darabszám megbízhatóságát jelzi.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-149">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="1a9d6-150">A pontosság értéke 0,0 és 1,0 között van, ahol a 0,0 azt jelenti, hogy a parancsmag nem tudta megszámolni az objektumokat, az 1,0 azt jelenti, hogy a szám pontos, és a 0,0 és 1,0 közötti érték egyre megbízhatóbb becslést jelez.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-150">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="1a9d6-151">-Skip</span><span class="sxs-lookup"><span data-stu-id="1a9d6-151">-Skip</span></span>
<span data-ttu-id="1a9d6-152">Figyelmen kívül hagyja a megadott számú objektumot, majd beveszi a fennmaradó objektumokat.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-152">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="1a9d6-153">Adja meg, hogy hány objektumot kell kihagyni.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-153">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="1a9d6-154">-First</span><span class="sxs-lookup"><span data-stu-id="1a9d6-154">-First</span></span>
<span data-ttu-id="1a9d6-155">Csak a megadott számú objektumot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-155">Gets only the specified number of objects.</span></span>
<span data-ttu-id="1a9d6-156">Adja meg a lekért objektumok számát.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-156">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="1a9d6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a9d6-157">CommonParameters</span></span>
<span data-ttu-id="1a9d6-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a9d6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a9d6-159">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a9d6-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a9d6-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a9d6-160">INPUTS</span></span>

### <span data-ttu-id="1a9d6-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="1a9d6-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="1a9d6-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a9d6-162">OUTPUTS</span></span>

### <span data-ttu-id="1a9d6-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="1a9d6-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="1a9d6-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1a9d6-164">NOTES</span></span>

## <span data-ttu-id="1a9d6-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a9d6-165">RELATED LINKS</span></span>
