---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/new-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentOrganization.md
ms.openlocfilehash: 546b4e56f2a932a6d7f17bda8484db8cd1c3c593
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012566"
---
# <span data-ttu-id="98dff-101">New-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="98dff-101">New-AzConfluentOrganization</span></span>

## <span data-ttu-id="98dff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98dff-102">SYNOPSIS</span></span>
<span data-ttu-id="98dff-103">Szervezeti erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="98dff-103">Create Organization resource</span></span>

## <span data-ttu-id="98dff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="98dff-104">SYNTAX</span></span>

```
New-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Location <String>] [-OfferDetailId <String>] [-OfferDetailPlanId <String>] [-OfferDetailPlanName <String>]
 [-OfferDetailPublisherId <String>] [-OfferDetailStatus <SaaSOfferStatus>] [-OfferDetailTermUnit <String>]
 [-Tag <Hashtable>] [-UserDetailEmailAddress <String>] [-UserDetailFirstName <String>]
 [-UserDetailLastName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="98dff-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="98dff-105">DESCRIPTION</span></span>
<span data-ttu-id="98dff-106">Szervezeti erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="98dff-106">Create Organization resource</span></span>

## <span data-ttu-id="98dff-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="98dff-107">EXAMPLES</span></span>

### <span data-ttu-id="98dff-108">1. példa: Összefolyásos szervezet létrehozása</span><span class="sxs-lookup"><span data-stu-id="98dff-108">Example 1: Create a confluent organization</span></span>
```powershell
PS C:\> New-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Location eastus -OfferDetailId "confluent-cloud-azure-prod" -OfferDetailPlanId "confluent-cloud-azure-payg-prod" -OfferDetailPlanName "Confluent Cloud - Pay as you Go" -OfferDetailPublisherId "confluentinc" -OfferDetailTermUnit "P1M" -UserDetailEmailAddress "xxxx@microsoft.com"

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="98dff-109">Ez a parancs összefolyásos szervezetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="98dff-109">This command creates a confluent organization.</span></span>

## <span data-ttu-id="98dff-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98dff-110">PARAMETERS</span></span>

### <span data-ttu-id="98dff-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98dff-111">-AsJob</span></span>
<span data-ttu-id="98dff-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="98dff-112">Run the command as a job</span></span>

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

### <span data-ttu-id="98dff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98dff-113">-DefaultProfile</span></span>
<span data-ttu-id="98dff-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98dff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98dff-115">-Location</span><span class="sxs-lookup"><span data-stu-id="98dff-115">-Location</span></span>
<span data-ttu-id="98dff-116">A szervezeti erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="98dff-116">Location of Organization resource</span></span>

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

### <span data-ttu-id="98dff-117">-Name</span><span class="sxs-lookup"><span data-stu-id="98dff-117">-Name</span></span>
<span data-ttu-id="98dff-118">Szervezet erőforrásneve</span><span class="sxs-lookup"><span data-stu-id="98dff-118">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98dff-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="98dff-119">-NoWait</span></span>
<span data-ttu-id="98dff-120">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="98dff-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="98dff-121">-OfferDetailId</span><span class="sxs-lookup"><span data-stu-id="98dff-121">-OfferDetailId</span></span>
<span data-ttu-id="98dff-122">Ajánlatazonosító</span><span class="sxs-lookup"><span data-stu-id="98dff-122">Offer Id</span></span>

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

### <span data-ttu-id="98dff-123">-OfferDetailPlanId</span><span class="sxs-lookup"><span data-stu-id="98dff-123">-OfferDetailPlanId</span></span>
<span data-ttu-id="98dff-124">Ajánlat csomagazonosítója</span><span class="sxs-lookup"><span data-stu-id="98dff-124">Offer Plan Id</span></span>

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

### <span data-ttu-id="98dff-125">-OfferDetailPlanName</span><span class="sxs-lookup"><span data-stu-id="98dff-125">-OfferDetailPlanName</span></span>
<span data-ttu-id="98dff-126">Ajánlat tervneve</span><span class="sxs-lookup"><span data-stu-id="98dff-126">Offer Plan Name</span></span>

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

### <span data-ttu-id="98dff-127">-OfferDetailPublisherId</span><span class="sxs-lookup"><span data-stu-id="98dff-127">-OfferDetailPublisherId</span></span>
<span data-ttu-id="98dff-128">Publisher-azonosító</span><span class="sxs-lookup"><span data-stu-id="98dff-128">Publisher Id</span></span>

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

### <span data-ttu-id="98dff-129">-OfferDetailStatus</span><span class="sxs-lookup"><span data-stu-id="98dff-129">-OfferDetailStatus</span></span>
<span data-ttu-id="98dff-130">SaaS-ajánlat állapota</span><span class="sxs-lookup"><span data-stu-id="98dff-130">SaaS Offer Status</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Support.SaaSOfferStatus
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98dff-131">-OfferDetailTermUnit</span><span class="sxs-lookup"><span data-stu-id="98dff-131">-OfferDetailTermUnit</span></span>
<span data-ttu-id="98dff-132">Ajánlati terv időszaka egység</span><span class="sxs-lookup"><span data-stu-id="98dff-132">Offer Plan Term unit</span></span>

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

### <span data-ttu-id="98dff-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98dff-133">-ResourceGroupName</span></span>
<span data-ttu-id="98dff-134">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="98dff-134">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98dff-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98dff-135">-SubscriptionId</span></span>
<span data-ttu-id="98dff-136">Microsoft Azure-előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="98dff-136">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98dff-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="98dff-137">-Tag</span></span>
<span data-ttu-id="98dff-138">Szervezeti erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="98dff-138">Organization resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98dff-139">-UserDetailEmailAddress</span><span class="sxs-lookup"><span data-stu-id="98dff-139">-UserDetailEmailAddress</span></span>
<span data-ttu-id="98dff-140">E-mail-cím</span><span class="sxs-lookup"><span data-stu-id="98dff-140">Email address</span></span>

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

### <span data-ttu-id="98dff-141">-UserDetailFirstName</span><span class="sxs-lookup"><span data-stu-id="98dff-141">-UserDetailFirstName</span></span>
<span data-ttu-id="98dff-142">Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="98dff-142">First name</span></span>

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

### <span data-ttu-id="98dff-143">-UserDetailLastName</span><span class="sxs-lookup"><span data-stu-id="98dff-143">-UserDetailLastName</span></span>
<span data-ttu-id="98dff-144">Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="98dff-144">Last name</span></span>

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

### <span data-ttu-id="98dff-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98dff-145">-Confirm</span></span>
<span data-ttu-id="98dff-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="98dff-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98dff-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98dff-147">-WhatIf</span></span>
<span data-ttu-id="98dff-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="98dff-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98dff-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="98dff-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98dff-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98dff-150">CommonParameters</span></span>
<span data-ttu-id="98dff-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98dff-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98dff-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98dff-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98dff-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98dff-153">INPUTS</span></span>

## <span data-ttu-id="98dff-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98dff-154">OUTPUTS</span></span>

### <span data-ttu-id="98dff-155">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="98dff-155">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="98dff-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="98dff-156">NOTES</span></span>

<span data-ttu-id="98dff-157">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="98dff-157">ALIASES</span></span>

## <span data-ttu-id="98dff-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98dff-158">RELATED LINKS</span></span>

