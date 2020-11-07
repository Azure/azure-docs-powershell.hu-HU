---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 07a8747f94f9c1fb93bbff06ce855363088a67a0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846161"
---
# <span data-ttu-id="2f7d7-101">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="2f7d7-101">Get-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="2f7d7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f7d7-102">SYNOPSIS</span></span>
<span data-ttu-id="2f7d7-103">Támogatási menetjegy-kommunikáció kérése</span><span class="sxs-lookup"><span data-stu-id="2f7d7-103">Get support ticket communications.</span></span>

## <span data-ttu-id="2f7d7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f7d7-104">SYNTAX</span></span>

### <span data-ttu-id="2f7d7-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f7d7-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f7d7-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f7d7-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f7d7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f7d7-107">DESCRIPTION</span></span>
<span data-ttu-id="2f7d7-108">Kommunikációt kap a támogatási jegyekhez.</span><span class="sxs-lookup"><span data-stu-id="2f7d7-108">Gets communications for a support ticket.</span></span> <span data-ttu-id="2f7d7-109">Ha nem ad meg semmilyen egyéb paramétert, a program minden kommunikációt lekérdez a jegyben.</span><span class="sxs-lookup"><span data-stu-id="2f7d7-109">It will retrieve all the communications for a ticket if you do not specify any other parameters.</span></span> <span data-ttu-id="2f7d7-110">A CreatedDate vagy a CommunicationType segítségével is szűrheti a kommunikációt a szűrő paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="2f7d7-110">You can also filter the communications by CreatedDate or CommunicationType using the Filter parameter.</span></span> <span data-ttu-id="2f7d7-111">Íme néhány példa a megadható értékek szűrésére.</span><span class="sxs-lookup"><span data-stu-id="2f7d7-111">Here are some examples of filter values that you can specify.</span></span>


| <span data-ttu-id="2f7d7-112">Forgatókönyv</span><span class="sxs-lookup"><span data-stu-id="2f7d7-112">Scenario</span></span>                                                        | <span data-ttu-id="2f7d7-113">Szűrő</span><span class="sxs-lookup"><span data-stu-id="2f7d7-113">Filter</span></span>                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2f7d7-114">Webes kommunikáció beszerzése</span><span class="sxs-lookup"><span data-stu-id="2f7d7-114">Get Web communications</span></span>                                          | <span data-ttu-id="2f7d7-115">"CommunicationType EQ" web ""</span><span class="sxs-lookup"><span data-stu-id="2f7d7-115">"CommunicationType eq 'Web'"</span></span>                               |
| <span data-ttu-id="2f7d7-116">Telefonos kommunikáció beszerzése</span><span class="sxs-lookup"><span data-stu-id="2f7d7-116">Get Phone communications</span></span>                                        | <span data-ttu-id="2f7d7-117">"CommunicationType EQ" telefon ' "</span><span class="sxs-lookup"><span data-stu-id="2f7d7-117">"CommunicationType eq 'Phone'"</span></span>                             |
| <span data-ttu-id="2f7d7-118">A december 20-ig vagy később létrehozott közlemények beszerzése, 2019</span><span class="sxs-lookup"><span data-stu-id="2f7d7-118">Get communications that were created on or after 20th Dec, 2019</span></span> | <span data-ttu-id="2f7d7-119">"CreatedDate GE 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="2f7d7-119">"CreatedDate ge 2019-12-20"</span></span>                                |
| <span data-ttu-id="2f7d7-120">A december 20.2019 után létrehozott kommunikáció beszerzése</span><span class="sxs-lookup"><span data-stu-id="2f7d7-120">Get communications that were created after 20th Dec, 2019</span></span>       | <span data-ttu-id="2f7d7-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="2f7d7-121">"CreatedDate gt 2019-12-20"</span></span>                                |
| <span data-ttu-id="2f7d7-122">A december 20., 2019 után létrehozott webes kommunikációt kapja.</span><span class="sxs-lookup"><span data-stu-id="2f7d7-122">Gets Web communications created after 20th Dec, 2019</span></span>            | <span data-ttu-id="2f7d7-123">"CreatedDate gt 2019-12-20 és CommunicationType EQ ' Web '"</span><span class="sxs-lookup"><span data-stu-id="2f7d7-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span></span> |


<span data-ttu-id="2f7d7-124">Ez a parancsmag az első és a kihagyott paraméterek segítségével támogatja a lapozást.</span><span class="sxs-lookup"><span data-stu-id="2f7d7-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="2f7d7-125">A kommunikációs név megadásával is lekérheti az egyetlen támogatási jegy kommunikációját.</span><span class="sxs-lookup"><span data-stu-id="2f7d7-125">You can also retrieve a single support ticket communication by specifying the communication name.</span></span> 

## <span data-ttu-id="2f7d7-126">Példák</span><span class="sxs-lookup"><span data-stu-id="2f7d7-126">EXAMPLES</span></span>

### <span data-ttu-id="2f7d7-127">Példa 1: támogatási jegy minden kommunikációjának lekérése</span><span class="sxs-lookup"><span data-stu-id="2f7d7-127">Example 1: Retrieve all communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### <span data-ttu-id="2f7d7-128">2. példa: egyetlen kommunikáció lekérése a támogatási jegy nevében</span><span class="sxs-lookup"><span data-stu-id="2f7d7-128">Example 2: Retrieve a single communication by it's name for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### <span data-ttu-id="2f7d7-129">3. példa: a támogatási jegy első 2 kommunikációjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="2f7d7-129">Example 3: Retrieve first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="2f7d7-130">Példa 4: a következő 2 kommunikáció lekérése az első 2 kommunikáció kihagyása után támogatási jegyhez</span><span class="sxs-lookup"><span data-stu-id="2f7d7-130">Example 4: Retrieve next 2 communications after skipping first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="2f7d7-131">Példa 5: a támogatási jegy összes webes kommunikációjának lekérése</span><span class="sxs-lookup"><span data-stu-id="2f7d7-131">Example 5: Retrieve all Web communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="2f7d7-132">Példa 6: a december 20-án vagy azt követően létrehozott összes kommunikáció lekérése, 2019 a támogatási jegyhez</span><span class="sxs-lookup"><span data-stu-id="2f7d7-132">Example 6: Retrieve all communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="2f7d7-133">7. példa: a támogatási jegyhez az 2019 december 20-án vagy azt követően létrehozott összes webes kommunikáció lekérése</span><span class="sxs-lookup"><span data-stu-id="2f7d7-133">Example 7: Retrieve all Web communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="2f7d7-134">8. példa: a támogatási jegy minden kommunikációjának lekérése a csővezeték-támogatási jegy objektummal</span><span class="sxs-lookup"><span data-stu-id="2f7d7-134">Example 8: Retrieve all communications for a support ticket by piping support ticket object</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

## <span data-ttu-id="2f7d7-135">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f7d7-135">PARAMETERS</span></span>

### <span data-ttu-id="2f7d7-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f7d7-136">-DefaultProfile</span></span>
<span data-ttu-id="2f7d7-137">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f7d7-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f7d7-138">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="2f7d7-138">-Filter</span></span>
<span data-ttu-id="2f7d7-139">A parancsmag eredményeire alkalmazott szűrő.</span><span class="sxs-lookup"><span data-stu-id="2f7d7-139">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="2f7d7-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2f7d7-140">-Name</span></span>
<span data-ttu-id="2f7d7-141">Kommunikációs név.</span><span class="sxs-lookup"><span data-stu-id="2f7d7-141">Communication name.</span></span>

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

### <span data-ttu-id="2f7d7-142">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="2f7d7-142">-SupportTicketName</span></span>
<span data-ttu-id="2f7d7-143">Támogatási jegy neve</span><span class="sxs-lookup"><span data-stu-id="2f7d7-143">Support ticket name.</span></span>

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

### <span data-ttu-id="2f7d7-144">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="2f7d7-144">-SupportTicketObject</span></span>
<span data-ttu-id="2f7d7-145">Támogatási jegy objektum.</span><span class="sxs-lookup"><span data-stu-id="2f7d7-145">Support ticket object.</span></span>

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

### <span data-ttu-id="2f7d7-146">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="2f7d7-146">-IncludeTotalCount</span></span>
<span data-ttu-id="2f7d7-147">A kijelölt objektumok által követett összes objektum (egész) számát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="2f7d7-147">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="2f7d7-148">Ha a parancsmag nem tudja megállapítani a teljes számlálást, az "ismeretlen összeg száma" szöveget jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="2f7d7-148">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="2f7d7-149">Az egész számnak van egy pontossági tulajdonsága, amely az összeg megbízhatóságát jelzi.</span><span class="sxs-lookup"><span data-stu-id="2f7d7-149">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="2f7d7-150">Az 0,0-től 1,0-ig terjedő pontossági értékek értéke, ahol az 0,0 azt jelenti, hogy a parancsmag nem tudta megszámolni az objektumokat, az 1,0 azt jelenti, hogy a darab pontos, és a 0,0 és a 1,0 közötti érték egyre megbízhatóbb becslést ad.</span><span class="sxs-lookup"><span data-stu-id="2f7d7-150">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="2f7d7-151">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="2f7d7-151">-Skip</span></span>
<span data-ttu-id="2f7d7-152">Figyelmen kívül hagyja a megadott számú objektumot, majd Kinyeri a fennmaradó objektumokat.</span><span class="sxs-lookup"><span data-stu-id="2f7d7-152">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="2f7d7-153">Adja meg, hogy hány objektum legyen kihagyva.</span><span class="sxs-lookup"><span data-stu-id="2f7d7-153">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="2f7d7-154">– Első</span><span class="sxs-lookup"><span data-stu-id="2f7d7-154">-First</span></span>
<span data-ttu-id="2f7d7-155">Csak a megadott számú objektumot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2f7d7-155">Gets only the specified number of objects.</span></span>
<span data-ttu-id="2f7d7-156">Adja meg a bejutni kívánt objektumok számát.</span><span class="sxs-lookup"><span data-stu-id="2f7d7-156">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="2f7d7-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f7d7-157">CommonParameters</span></span>
<span data-ttu-id="2f7d7-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f7d7-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f7d7-159">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2f7d7-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f7d7-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f7d7-160">INPUTS</span></span>

### <span data-ttu-id="2f7d7-161">Microsoft. Azure. commands. support. models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="2f7d7-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="2f7d7-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f7d7-162">OUTPUTS</span></span>

### <span data-ttu-id="2f7d7-163">Microsoft. Azure. commands. support. models. PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="2f7d7-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="2f7d7-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f7d7-164">NOTES</span></span>

## <span data-ttu-id="2f7d7-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f7d7-165">RELATED LINKS</span></span>
