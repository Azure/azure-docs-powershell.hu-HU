---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 8df5d54576b62caf93a92583eb6dcc9e39802f3d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93848030"
---
# <span data-ttu-id="95986-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="95986-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="95986-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="95986-102">SYNOPSIS</span></span>
<span data-ttu-id="95986-103">Munkaterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="95986-103">Creates a workspace.</span></span>

## <span data-ttu-id="95986-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="95986-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95986-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="95986-105">DESCRIPTION</span></span>
<span data-ttu-id="95986-106">A **New-AzOperationalInsightsWorkspace** parancsmag létrehoz egy munkaterületet a megadott erőforráscsoport és-hely között.</span><span class="sxs-lookup"><span data-stu-id="95986-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="95986-107">Példák</span><span class="sxs-lookup"><span data-stu-id="95986-107">EXAMPLES</span></span>

### <span data-ttu-id="95986-108">1. példa: munkaterület létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="95986-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="95986-109">Ez a parancs létrehoz egy MyWorkspace nevű szabványos SKU-munkaterületet az ContosoResourceGroup nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="95986-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="95986-110">2. példa: munkaterület létrehozása és csatolása meglévő fiókhoz</span><span class="sxs-lookup"><span data-stu-id="95986-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="95986-111">Az első parancs az Get-AzOperationalInsightsLinkTargets parancsmagot használja az üzemeltetési statisztika-célok eléréséhez, majd a $OILinkTargets változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="95986-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="95986-112">A második parancs átadja az első fiók hivatkozás célját $OILinkTargets a **New-AzOperationalInsightsWorkspace** parancsmagot a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="95986-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="95986-113">A parancs létrehoz egy MyWorkspace nevű szabványos SKU-munkaterületet, amely a $OILinkTargets első üzemi betekintési fiókjához van kapcsolva.</span><span class="sxs-lookup"><span data-stu-id="95986-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="95986-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="95986-114">PARAMETERS</span></span>

### <span data-ttu-id="95986-115">-Vevőkód</span><span class="sxs-lookup"><span data-stu-id="95986-115">-CustomerId</span></span>
<span data-ttu-id="95986-116">Azt a fiókot adja meg, amelyre a munkaterület hivatkozni fog.</span><span class="sxs-lookup"><span data-stu-id="95986-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="95986-117">A Get-AzOperationalInsightsLinkTargets parancsmag a potenciális fiókok listázására is használható.</span><span class="sxs-lookup"><span data-stu-id="95986-117">The Get-AzOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95986-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95986-118">-DefaultProfile</span></span>
<span data-ttu-id="95986-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="95986-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95986-120">-Force</span><span class="sxs-lookup"><span data-stu-id="95986-120">-Force</span></span>
<span data-ttu-id="95986-121">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="95986-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="95986-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="95986-122">-Location</span></span>
<span data-ttu-id="95986-123">Azt a helyet adja meg, ahol létrehozhatja a munkaterületet (például kelet-amerikai vagy Nyugat-európai).</span><span class="sxs-lookup"><span data-stu-id="95986-123">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95986-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="95986-124">-Name</span></span>
<span data-ttu-id="95986-125">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="95986-125">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95986-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95986-126">-ResourceGroupName</span></span>
<span data-ttu-id="95986-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="95986-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="95986-128">A munkaterület ebben az erőforráscsoportben jön létre.</span><span class="sxs-lookup"><span data-stu-id="95986-128">The workspace is created in this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95986-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="95986-129">-RetentionInDays</span></span>
<span data-ttu-id="95986-130">Munkaterület-adatmegőrzés napokban.</span><span class="sxs-lookup"><span data-stu-id="95986-130">The workspace data retention in days.</span></span> <span data-ttu-id="95986-131">a 730 napok az összes többi SKU számára megengedett maximális érték.</span><span class="sxs-lookup"><span data-stu-id="95986-131">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95986-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="95986-132">-Sku</span></span>
<span data-ttu-id="95986-133">A munkaterület szolgáltatási rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="95986-133">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="95986-134">Ha további információra van tekintettel a használati értékre vonatkozóan, kérjük, jelölje be a jelölőnégyzetet https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers .</span><span class="sxs-lookup"><span data-stu-id="95986-134">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="95986-135">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="95986-135">Valid values are:</span></span>
- <span data-ttu-id="95986-136">ingyenes</span><span class="sxs-lookup"><span data-stu-id="95986-136">free</span></span>
- <span data-ttu-id="95986-137">pergb2018</span><span class="sxs-lookup"><span data-stu-id="95986-137">pergb2018</span></span>
- <span data-ttu-id="95986-138">pernode</span><span class="sxs-lookup"><span data-stu-id="95986-138">pernode</span></span>
- <span data-ttu-id="95986-139">prémium verzió</span><span class="sxs-lookup"><span data-stu-id="95986-139">premium</span></span>
- <span data-ttu-id="95986-140">különálló</span><span class="sxs-lookup"><span data-stu-id="95986-140">standalone</span></span>
- <span data-ttu-id="95986-141">Standard</span><span class="sxs-lookup"><span data-stu-id="95986-141">standard</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, pergb2018, pernode, premium, standalone, standard

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95986-142">-Címke</span><span class="sxs-lookup"><span data-stu-id="95986-142">-Tag</span></span>
<span data-ttu-id="95986-143">A munkaterület erőforrás-címkéi.</span><span class="sxs-lookup"><span data-stu-id="95986-143">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95986-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="95986-144">-Confirm</span></span>
<span data-ttu-id="95986-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="95986-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95986-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95986-146">-WhatIf</span></span>
<span data-ttu-id="95986-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="95986-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95986-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="95986-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95986-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95986-149">CommonParameters</span></span>
<span data-ttu-id="95986-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="95986-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95986-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95986-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95986-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="95986-152">INPUTS</span></span>

### <span data-ttu-id="95986-153">System. String</span><span class="sxs-lookup"><span data-stu-id="95986-153">System.String</span></span>

### <span data-ttu-id="95986-154">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="95986-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="95986-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="95986-155">System.Collections.Hashtable</span></span>

### <span data-ttu-id="95986-156">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="95986-156">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="95986-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95986-157">OUTPUTS</span></span>

### <span data-ttu-id="95986-158">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="95986-158">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="95986-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="95986-159">NOTES</span></span>

<span data-ttu-id="95986-160">Új árképzési modellt bocsátottak ki.</span><span class="sxs-lookup"><span data-stu-id="95986-160">A new pricing model has been released.</span></span> <span data-ttu-id="95986-161">Ha Ön kriptográfiai szolgáltató, amely azt jelzi, hogy a SKU-hoz a "standalone" kifejezést kell használnia.</span><span class="sxs-lookup"><span data-stu-id="95986-161">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="95986-162">A kulisszák mögött az SKU a pergb2018-ra változik.</span><span class="sxs-lookup"><span data-stu-id="95986-162">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="95986-163">További információért olvassa el az alábbi témaköröket: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="95986-163">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="95986-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95986-164">RELATED LINKS</span></span>

[<span data-ttu-id="95986-165">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="95986-165">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)
