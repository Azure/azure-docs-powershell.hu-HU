---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: feac2aa9c5dd92c0d76090c6fc28353d56f9647c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184033"
---
# <span data-ttu-id="303fe-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="303fe-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="303fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="303fe-102">SYNOPSIS</span></span>
<span data-ttu-id="303fe-103">Munkaterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="303fe-103">Creates a workspace.</span></span>

## <span data-ttu-id="303fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="303fe-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="303fe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="303fe-105">DESCRIPTION</span></span>
<span data-ttu-id="303fe-106">A **New-AzOperationalInsightsWorkspace** parancsmag létrehoz egy munkaterületet a megadott erőforráscsoport és-hely között.</span><span class="sxs-lookup"><span data-stu-id="303fe-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="303fe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="303fe-107">EXAMPLES</span></span>

### <span data-ttu-id="303fe-108">1. példa: munkaterület létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="303fe-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="303fe-109">Ez a parancs létrehoz egy MyWorkspace nevű szabványos SKU-munkaterületet az ContosoResourceGroup nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="303fe-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="303fe-110">2. példa: munkaterület létrehozása és csatolása meglévő fiókhoz</span><span class="sxs-lookup"><span data-stu-id="303fe-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="303fe-111">Az első parancs az Get-AzOperationalInsightsLinkTargets parancsmagot használja az üzemeltetési statisztika-célok eléréséhez, majd a $OILinkTargets változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="303fe-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="303fe-112">A második parancs átadja az első fiók hivatkozás célját $OILinkTargets a **New-AzOperationalInsightsWorkspace** parancsmagot a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="303fe-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="303fe-113">A parancs létrehoz egy MyWorkspace nevű szabványos SKU-munkaterületet, amely a $OILinkTargets első üzemi betekintési fiókjához van kapcsolva.</span><span class="sxs-lookup"><span data-stu-id="303fe-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="303fe-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="303fe-114">PARAMETERS</span></span>

### <span data-ttu-id="303fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="303fe-115">-DefaultProfile</span></span>
<span data-ttu-id="303fe-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="303fe-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="303fe-117">-Force</span><span class="sxs-lookup"><span data-stu-id="303fe-117">-Force</span></span>
<span data-ttu-id="303fe-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="303fe-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="303fe-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="303fe-119">-Location</span></span>
<span data-ttu-id="303fe-120">Azt a helyet adja meg, ahol létrehozhatja a munkaterületet (például kelet-amerikai vagy Nyugat-európai).</span><span class="sxs-lookup"><span data-stu-id="303fe-120">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="303fe-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="303fe-121">-Name</span></span>
<span data-ttu-id="303fe-122">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="303fe-122">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="303fe-123">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="303fe-123">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="303fe-124">A munkaterület lenyelésének eléréséhez szükséges hálózati hozzáférés típusa.</span><span class="sxs-lookup"><span data-stu-id="303fe-124">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="303fe-125">Az értéknek "engedélyezve" vagy "Letiltva" kell lennie.</span><span class="sxs-lookup"><span data-stu-id="303fe-125">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="303fe-126">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="303fe-126">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="303fe-127">A munkaterületi lekérdezések eléréséhez használt hálózati hozzáférés típusa.</span><span class="sxs-lookup"><span data-stu-id="303fe-127">The network access type for accessing workspace query.</span></span> <span data-ttu-id="303fe-128">Az értéknek "engedélyezve" vagy "Letiltva" kell lennie.</span><span class="sxs-lookup"><span data-stu-id="303fe-128">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="303fe-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="303fe-129">-ResourceGroupName</span></span>
<span data-ttu-id="303fe-130">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="303fe-130">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="303fe-131">A munkaterület ebben az erőforráscsoportben jön létre.</span><span class="sxs-lookup"><span data-stu-id="303fe-131">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="303fe-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="303fe-132">-RetentionInDays</span></span>
<span data-ttu-id="303fe-133">Munkaterület-adatmegőrzés napokban.</span><span class="sxs-lookup"><span data-stu-id="303fe-133">The workspace data retention in days.</span></span> <span data-ttu-id="303fe-134">a 730 napok az összes többi SKU számára megengedett maximális érték.</span><span class="sxs-lookup"><span data-stu-id="303fe-134">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="303fe-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="303fe-135">-Sku</span></span>
<span data-ttu-id="303fe-136">A munkaterület szolgáltatási rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="303fe-136">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="303fe-137">Ha további információra van tekintettel a használati értékre vonatkozóan, kérjük, jelölje be a jelölőnégyzetet https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers .</span><span class="sxs-lookup"><span data-stu-id="303fe-137">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="303fe-138">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="303fe-138">Valid values are:</span></span>
- <span data-ttu-id="303fe-139">ingyenes</span><span class="sxs-lookup"><span data-stu-id="303fe-139">free</span></span>
- <span data-ttu-id="303fe-140">pergb2018</span><span class="sxs-lookup"><span data-stu-id="303fe-140">pergb2018</span></span>
- <span data-ttu-id="303fe-141">pernode</span><span class="sxs-lookup"><span data-stu-id="303fe-141">pernode</span></span>
- <span data-ttu-id="303fe-142">prémium verzió</span><span class="sxs-lookup"><span data-stu-id="303fe-142">premium</span></span>
- <span data-ttu-id="303fe-143">különálló</span><span class="sxs-lookup"><span data-stu-id="303fe-143">standalone</span></span>
- <span data-ttu-id="303fe-144">Standard</span><span class="sxs-lookup"><span data-stu-id="303fe-144">standard</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="303fe-145">-Címke</span><span class="sxs-lookup"><span data-stu-id="303fe-145">-Tag</span></span>
<span data-ttu-id="303fe-146">A munkaterület erőforrás-címkéi.</span><span class="sxs-lookup"><span data-stu-id="303fe-146">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="303fe-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="303fe-147">-Confirm</span></span>
<span data-ttu-id="303fe-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="303fe-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="303fe-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="303fe-149">-WhatIf</span></span>
<span data-ttu-id="303fe-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="303fe-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="303fe-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="303fe-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="303fe-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="303fe-152">CommonParameters</span></span>
<span data-ttu-id="303fe-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="303fe-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="303fe-154">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="303fe-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="303fe-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="303fe-155">INPUTS</span></span>

### <span data-ttu-id="303fe-156">System. String</span><span class="sxs-lookup"><span data-stu-id="303fe-156">System.String</span></span>

### <span data-ttu-id="303fe-157">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="303fe-157">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="303fe-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="303fe-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="303fe-159">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="303fe-159">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="303fe-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="303fe-160">OUTPUTS</span></span>

### <span data-ttu-id="303fe-161">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="303fe-161">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="303fe-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="303fe-162">NOTES</span></span>

<span data-ttu-id="303fe-163">Új árképzési modellt bocsátottak ki.</span><span class="sxs-lookup"><span data-stu-id="303fe-163">A new pricing model has been released.</span></span> <span data-ttu-id="303fe-164">Ha Ön kriptográfiai szolgáltató, amely azt jelzi, hogy a SKU-hoz a "standalone" kifejezést kell használnia.</span><span class="sxs-lookup"><span data-stu-id="303fe-164">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="303fe-165">A kulisszák mögött az SKU a pergb2018-ra változik.</span><span class="sxs-lookup"><span data-stu-id="303fe-165">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="303fe-166">További információért olvassa el az alábbi témaköröket: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="303fe-166">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="303fe-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="303fe-167">RELATED LINKS</span></span>

[<span data-ttu-id="303fe-168">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="303fe-168">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="303fe-169">Get-AzOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="303fe-169">Get-AzOperationalInsightsLinkTargets</span></span>](./Get-AzOperationalInsightsLinkTargets.md)


