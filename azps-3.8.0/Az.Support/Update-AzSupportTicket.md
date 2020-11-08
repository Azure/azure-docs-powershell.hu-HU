---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/update-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
ms.openlocfilehash: 160d6b4d4a8505c99d5bfcb4c535ec7bbb3b6dd3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011659"
---
# <span data-ttu-id="438ec-101">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="438ec-101">Update-AzSupportTicket</span></span>

## <span data-ttu-id="438ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="438ec-102">SYNOPSIS</span></span>
<span data-ttu-id="438ec-103">Frissíti a támogatási jegyet.</span><span class="sxs-lookup"><span data-stu-id="438ec-103">Updates support ticket.</span></span>

## <span data-ttu-id="438ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="438ec-104">SYNTAX</span></span>

### <span data-ttu-id="438ec-105">UpdateByNameWithContactDetailParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="438ec-105">UpdateByNameWithContactDetailParameterSet (Default)</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="438ec-106">UpdateByNameWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="438ec-106">UpdateByNameWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] -CustomerContactDetail <PSContactProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="438ec-107">UpdateByInputObjectWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="438ec-107">UpdateByInputObjectWithContactDetailParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="438ec-108">UpdateByInputObjectWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="438ec-108">UpdateByInputObjectWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>]
 -CustomerContactDetail <PSContactProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="438ec-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="438ec-109">DESCRIPTION</span></span>
<span data-ttu-id="438ec-110">Ezzel a parancsmaggal frissítheti a támogatási jegy súlyossági szintjét, állapotát vagy az ügyfél elérhetőségi adatait.</span><span class="sxs-lookup"><span data-stu-id="438ec-110">Use this cmdlet to update a support ticket's severity level, status or customer contact details.</span></span> <span data-ttu-id="438ec-111">Felhívjuk a figyelmét arra, hogy a támogatási jegy súlyossági szintje vagy állapotának frissítése nem engedélyezett, ha a jegy egy támogatási szakemberhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="438ec-111">Note that updating a support ticket's severity level or status is not allowed when the ticket is assigned to a support engineer.</span></span> <span data-ttu-id="438ec-112">Ha a jegy hozzárendelése után módosítani szeretné a súlyossági szintet vagy az állapotot, vegye fel a kapcsolatot a támogatási szakemberrel egy, a jegyen keresztüli kommunikáció elküldésével.</span><span class="sxs-lookup"><span data-stu-id="438ec-112">If you wish to update the severity level or status after ticket assignment, contact the support engineer by sending a communication on the ticket.</span></span>

## <span data-ttu-id="438ec-113">Példák</span><span class="sxs-lookup"><span data-stu-id="438ec-113">EXAMPLES</span></span>

### <span data-ttu-id="438ec-114">Példa 1: a támogatási jegy súlyosságának módosítása.</span><span class="sxs-lookup"><span data-stu-id="438ec-114">Example 1: Update severity of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="438ec-115">2. példa: támogatási jegy állapotának frissítése</span><span class="sxs-lookup"><span data-stu-id="438ec-115">Example 2: Update status of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="438ec-116">3. példa: a támogatási jegy elérhetőségi adatainak frissítése a kapcsolatfelvételi objektum megadásával.</span><span class="sxs-lookup"><span data-stu-id="438ec-116">Example 3: Update contact details of support ticket by specify contact object.</span></span>
```powershell
PS C:\> $contactDetail = new-object Microsoft.Azure.Commands.Support.Models.PSContactProfile
PS C:\> $contactDetail.FirstName = "first name updated"
PS C:\> $contactDetail.LastName = "last name updated"
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerContactDetail $contactDetail 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="438ec-117">Példa 4: a támogatási jegy súlyosságának frissítése a csővezeték-támogatási jegy objektummal.</span><span class="sxs-lookup"><span data-stu-id="438ec-117">Example 4: Update severity of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="438ec-118">5. példa: a támogatási jegy elérhetőségi adatainak frissítése az egyes kapcsolatfelvételi paraméterek megadásával.</span><span class="sxs-lookup"><span data-stu-id="438ec-118">Example 5: Update contact details of support ticket by specifying individual contact parameters.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerFirstName "first name updated" -CustomerLastName "last name updated" -AdditionalEmailAddress @("user2@contoso.com") 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="438ec-119">6. példa: a támogatási jegy állapotának frissítése a csővezeték-támogatási jegy objektummal.</span><span class="sxs-lookup"><span data-stu-id="438ec-119">Example 6: Update status of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="438ec-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="438ec-120">PARAMETERS</span></span>

### <span data-ttu-id="438ec-121">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="438ec-121">-AdditionalEmailAddress</span></span>
<span data-ttu-id="438ec-122">További e-mail-címek.</span><span class="sxs-lookup"><span data-stu-id="438ec-122">Additional email addresses.</span></span>
<span data-ttu-id="438ec-123">Az itt felsorolt e-mail-címeket a támogatási jegyre vonatkozó minden levelezésre másolhatja.</span><span class="sxs-lookup"><span data-stu-id="438ec-123">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="438ec-124">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="438ec-124">-CustomerContactDetail</span></span>
<span data-ttu-id="438ec-125">Frissítse a kapcsolat adatait a SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="438ec-125">Update Contact details on SupportTicket.</span></span>

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

### <span data-ttu-id="438ec-126">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="438ec-126">-CustomerCountry</span></span>
<span data-ttu-id="438ec-127">Ügyfél országa.</span><span class="sxs-lookup"><span data-stu-id="438ec-127">Customer country.</span></span>
<span data-ttu-id="438ec-128">A kódnak érvényes ISO Alpha-3 országkód (ISO 3166) kell lennie.</span><span class="sxs-lookup"><span data-stu-id="438ec-128">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="438ec-129">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="438ec-129">-CustomerFirstName</span></span>
<span data-ttu-id="438ec-130">Ügyfél vezetékneve.</span><span class="sxs-lookup"><span data-stu-id="438ec-130">Customer first name.</span></span>

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

### <span data-ttu-id="438ec-131">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="438ec-131">-CustomerLastName</span></span>
<span data-ttu-id="438ec-132">Ügyfél vezetékneve.</span><span class="sxs-lookup"><span data-stu-id="438ec-132">Customer last name.</span></span>

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

### <span data-ttu-id="438ec-133">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="438ec-133">-CustomerPhoneNumber</span></span>
<span data-ttu-id="438ec-134">Ügyfél telefonszáma.</span><span class="sxs-lookup"><span data-stu-id="438ec-134">Customer phone number.</span></span>
<span data-ttu-id="438ec-135">Erre akkor van szükség, ha az elsődleges névjegykártya-módszer telefon.</span><span class="sxs-lookup"><span data-stu-id="438ec-135">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="438ec-136">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="438ec-136">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="438ec-137">Az ügyfél által előnyben részesített támogatási nyelv.</span><span class="sxs-lookup"><span data-stu-id="438ec-137">Customer preferred support language.</span></span>
<span data-ttu-id="438ec-138">Ennek az itt felsorolt támogatott nyelvek egyikéhez érvényes célnyelv-kódnak kell lennie https://azure.microsoft.com/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="438ec-138">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="438ec-139">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="438ec-139">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="438ec-140">Ügyfél által preferált időzóna</span><span class="sxs-lookup"><span data-stu-id="438ec-140">Customer preferred time zone.</span></span>
<span data-ttu-id="438ec-141">Ennek érvényes System.TimeZoneInfo.Id-értéknek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="438ec-141">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="438ec-142">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="438ec-142">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="438ec-143">Ügyfél elsődleges e-mail-címe.</span><span class="sxs-lookup"><span data-stu-id="438ec-143">Customer primary email address.</span></span>

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

### <span data-ttu-id="438ec-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="438ec-144">-DefaultProfile</span></span>
<span data-ttu-id="438ec-145">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="438ec-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="438ec-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="438ec-146">-InputObject</span></span>
<span data-ttu-id="438ec-147">A parancsmag által frissített SupportTicket erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="438ec-147">SupportTicket resource object that this cmdlet updates.</span></span>

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

### <span data-ttu-id="438ec-148">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="438ec-148">-Name</span></span>
<span data-ttu-id="438ec-149">A parancsmag által frissített SupportTicket-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="438ec-149">Name of SupportTicket resource that this cmdlet updates.</span></span>

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

### <span data-ttu-id="438ec-150">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="438ec-150">-PreferredContactMethod</span></span>
<span data-ttu-id="438ec-151">Preferált kontakt mód</span><span class="sxs-lookup"><span data-stu-id="438ec-151">Preferred contact method.</span></span>

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

### <span data-ttu-id="438ec-152">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="438ec-152">-Severity</span></span>
<span data-ttu-id="438ec-153">Frissítse a SupportTicket súlyosságát.</span><span class="sxs-lookup"><span data-stu-id="438ec-153">Update Severity of SupportTicket.</span></span>

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

### <span data-ttu-id="438ec-154">-Állapot</span><span class="sxs-lookup"><span data-stu-id="438ec-154">-Status</span></span>
<span data-ttu-id="438ec-155">Frissítse a SupportTicket állapotát.</span><span class="sxs-lookup"><span data-stu-id="438ec-155">Update Status of SupportTicket.</span></span>

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

### <span data-ttu-id="438ec-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="438ec-156">-Confirm</span></span>
<span data-ttu-id="438ec-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="438ec-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="438ec-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="438ec-158">-WhatIf</span></span>
<span data-ttu-id="438ec-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="438ec-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="438ec-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="438ec-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="438ec-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="438ec-161">CommonParameters</span></span>
<span data-ttu-id="438ec-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="438ec-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="438ec-163">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="438ec-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="438ec-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="438ec-164">INPUTS</span></span>

### <span data-ttu-id="438ec-165">Microsoft. Azure. commands. support. models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="438ec-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="438ec-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="438ec-166">OUTPUTS</span></span>

### <span data-ttu-id="438ec-167">Microsoft. Azure. commands. support. models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="438ec-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="438ec-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="438ec-168">NOTES</span></span>

## <span data-ttu-id="438ec-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="438ec-169">RELATED LINKS</span></span>
