---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/update-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
ms.openlocfilehash: 160d6b4d4a8505c99d5bfcb4c535ec7bbb3b6dd3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466823"
---
# <span data-ttu-id="84030-101">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="84030-101">Update-AzSupportTicket</span></span>

## <span data-ttu-id="84030-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84030-102">SYNOPSIS</span></span>
<span data-ttu-id="84030-103">Frissíti a támogatási jegyet.</span><span class="sxs-lookup"><span data-stu-id="84030-103">Updates support ticket.</span></span>

## <span data-ttu-id="84030-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="84030-104">SYNTAX</span></span>

### <span data-ttu-id="84030-105">UpdateByNameWithContactDetailParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="84030-105">UpdateByNameWithContactDetailParameterSet (Default)</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84030-106">UpdateByNameWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84030-106">UpdateByNameWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] -CustomerContactDetail <PSContactProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84030-107">UpdateByInputObjectWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="84030-107">UpdateByInputObjectWithContactDetailParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84030-108">UpdateByInputObjectWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84030-108">UpdateByInputObjectWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>]
 -CustomerContactDetail <PSContactProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84030-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="84030-109">DESCRIPTION</span></span>
<span data-ttu-id="84030-110">Ezzel a parancsmagtal frissítheti egy támogatási jegy súlyossági szintjét, állapotát vagy az ügyfél kapcsolattartási adatait.</span><span class="sxs-lookup"><span data-stu-id="84030-110">Use this cmdlet to update a support ticket's severity level, status or customer contact details.</span></span> <span data-ttu-id="84030-111">Felhívjuk a figyelmét arra, hogy a támogatási jegy súlyossági szintjének vagy állapotának frissítése nem engedélyezett, ha a jegyet egy támogatási szakemberhez rendelik hozzá.</span><span class="sxs-lookup"><span data-stu-id="84030-111">Note that updating a support ticket's severity level or status is not allowed when the ticket is assigned to a support engineer.</span></span> <span data-ttu-id="84030-112">Ha frissíteni szeretné a súlyossági szintet vagy az állapotot a jegy-hozzárendelés után, lépjen kapcsolatba a terméktámogatási szakemberrel a jegyen található kommunikációval.</span><span class="sxs-lookup"><span data-stu-id="84030-112">If you wish to update the severity level or status after ticket assignment, contact the support engineer by sending a communication on the ticket.</span></span>

## <span data-ttu-id="84030-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="84030-113">EXAMPLES</span></span>

### <span data-ttu-id="84030-114">1. példa: A támogatási jegy súlyossági állapotának frissítése.</span><span class="sxs-lookup"><span data-stu-id="84030-114">Example 1: Update severity of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="84030-115">2. példa: A támogatási jegy állapotának frissítése.</span><span class="sxs-lookup"><span data-stu-id="84030-115">Example 2: Update status of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="84030-116">3. példa: A támogatási jegy kapcsolatfelvételi részleteinek frissítése a kapcsolatfelvételi objektum megadásával.</span><span class="sxs-lookup"><span data-stu-id="84030-116">Example 3: Update contact details of support ticket by specify contact object.</span></span>
```powershell
PS C:\> $contactDetail = new-object Microsoft.Azure.Commands.Support.Models.PSContactProfile
PS C:\> $contactDetail.FirstName = "first name updated"
PS C:\> $contactDetail.LastName = "last name updated"
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerContactDetail $contactDetail 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="84030-117">4. példa: A támogatási jegy súlyossági állapotának frissítése a támogatási jegy objektumának kipukkolásával.</span><span class="sxs-lookup"><span data-stu-id="84030-117">Example 4: Update severity of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="84030-118">5. példa: A támogatási jegy kapcsolatfelvételi részleteinek frissítése egyéni kapcsolatfelvételi paraméterek megadásával.</span><span class="sxs-lookup"><span data-stu-id="84030-118">Example 5: Update contact details of support ticket by specifying individual contact parameters.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerFirstName "first name updated" -CustomerLastName "last name updated" -AdditionalEmailAddress @("user2@contoso.com") 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="84030-119">6. példa: A támogatási jegy állapotának frissítése a támogatási jegyobjektum pipázásával.</span><span class="sxs-lookup"><span data-stu-id="84030-119">Example 6: Update status of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="84030-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84030-120">PARAMETERS</span></span>

### <span data-ttu-id="84030-121">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="84030-121">-AdditionalEmailAddress</span></span>
<span data-ttu-id="84030-122">További e-mail-címek.</span><span class="sxs-lookup"><span data-stu-id="84030-122">Additional email addresses.</span></span>
<span data-ttu-id="84030-123">Az itt felsorolt e-mail-címeket a rendszer a támogatási jegyről küldött minden levélre átmásolja.</span><span class="sxs-lookup"><span data-stu-id="84030-123">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84030-124">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="84030-124">-CustomerContactDetail</span></span>
<span data-ttu-id="84030-125">A kapcsolatfelvételi adatok frissítése a SupportTicketen.</span><span class="sxs-lookup"><span data-stu-id="84030-125">Update Contact details on SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSContactProfile
Parameter Sets: UpdateByNameWithContactObjectParameterSet, UpdateByInputObjectWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84030-126">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="84030-126">-CustomerCountry</span></span>
<span data-ttu-id="84030-127">Ügyfél országa.</span><span class="sxs-lookup"><span data-stu-id="84030-127">Customer country.</span></span>
<span data-ttu-id="84030-128">Érvényes ISO Alfa-3 országkódnak (ISO 3166) kell lennie.</span><span class="sxs-lookup"><span data-stu-id="84030-128">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84030-129">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="84030-129">-CustomerFirstName</span></span>
<span data-ttu-id="84030-130">Ügyfél vezetékneve.</span><span class="sxs-lookup"><span data-stu-id="84030-130">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84030-131">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="84030-131">-CustomerLastName</span></span>
<span data-ttu-id="84030-132">Ügyfél vezetékneve.</span><span class="sxs-lookup"><span data-stu-id="84030-132">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84030-133">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="84030-133">-CustomerPhoneNumber</span></span>
<span data-ttu-id="84030-134">Ügyfél telefonszáma.</span><span class="sxs-lookup"><span data-stu-id="84030-134">Customer phone number.</span></span>
<span data-ttu-id="84030-135">Erre akkor van szükség, ha az előnyben részesített kapcsolatfelvételi mód a telefon.</span><span class="sxs-lookup"><span data-stu-id="84030-135">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84030-136">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="84030-136">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="84030-137">Az ügyfél elsődleges támogatási nyelve.</span><span class="sxs-lookup"><span data-stu-id="84030-137">Customer preferred support language.</span></span>
<span data-ttu-id="84030-138">A kódnak érvényesnek kell lennie az itt felsorolt nyelvek https://azure.microsoft.com/support/faq/ egyikében.</span><span class="sxs-lookup"><span data-stu-id="84030-138">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84030-139">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="84030-139">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="84030-140">Ügyfél által előnyben részesített időzóna.</span><span class="sxs-lookup"><span data-stu-id="84030-140">Customer preferred time zone.</span></span>
<span data-ttu-id="84030-141">Ennek érvényes System.TimeZoneInfo.Id kell lennie.</span><span class="sxs-lookup"><span data-stu-id="84030-141">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84030-142">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="84030-142">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="84030-143">Ügyfél elsődleges e-mail-címe.</span><span class="sxs-lookup"><span data-stu-id="84030-143">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84030-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84030-144">-DefaultProfile</span></span>
<span data-ttu-id="84030-145">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84030-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84030-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84030-146">-InputObject</span></span>
<span data-ttu-id="84030-147">A parancsmag által frissülő SupportTicket erőforrásobjektum.</span><span class="sxs-lookup"><span data-stu-id="84030-147">SupportTicket resource object that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: UpdateByInputObjectWithContactDetailParameterSet, UpdateByInputObjectWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84030-148">-Name</span><span class="sxs-lookup"><span data-stu-id="84030-148">-Name</span></span>
<span data-ttu-id="84030-149">A parancsmag által frissülő SupportTicket-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="84030-149">Name of SupportTicket resource that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByNameWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84030-150">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="84030-150">-PreferredContactMethod</span></span>
<span data-ttu-id="84030-151">Előnyben részesített kapcsolatfelvételi mód.</span><span class="sxs-lookup"><span data-stu-id="84030-151">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:
Accepted values: Email, Phone

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84030-152">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="84030-152">-Severity</span></span>
<span data-ttu-id="84030-153">Frissítse a SupportTicket súlyossági fokát.</span><span class="sxs-lookup"><span data-stu-id="84030-153">Update Severity of SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Severity
Parameter Sets: (All)
Aliases:
Accepted values: Minimal, Moderate, Critical, HighestCriticalImpact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84030-154">-Állapot</span><span class="sxs-lookup"><span data-stu-id="84030-154">-Status</span></span>
<span data-ttu-id="84030-155">A Támogatásiticket frissítési állapota.</span><span class="sxs-lookup"><span data-stu-id="84030-155">Update Status of SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Status
Parameter Sets: (All)
Aliases:
Accepted values: Open, Closed

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84030-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84030-156">-Confirm</span></span>
<span data-ttu-id="84030-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="84030-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84030-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84030-158">-WhatIf</span></span>
<span data-ttu-id="84030-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="84030-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84030-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="84030-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84030-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84030-161">CommonParameters</span></span>
<span data-ttu-id="84030-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84030-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84030-163">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84030-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84030-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84030-164">INPUTS</span></span>

### <span data-ttu-id="84030-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="84030-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="84030-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84030-166">OUTPUTS</span></span>

### <span data-ttu-id="84030-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="84030-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="84030-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="84030-168">NOTES</span></span>

## <span data-ttu-id="84030-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84030-169">RELATED LINKS</span></span>
