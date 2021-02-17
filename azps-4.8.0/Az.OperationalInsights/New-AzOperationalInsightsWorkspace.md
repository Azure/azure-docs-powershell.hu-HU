---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 8515bf4085fcd03d87aa15c3da649fe318b94966
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405006"
---
# <span data-ttu-id="4eb8f-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="4eb8f-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="4eb8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eb8f-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb8f-103">Munkaterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-103">Creates a workspace.</span></span>

## <span data-ttu-id="4eb8f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4eb8f-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eb8f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4eb8f-105">DESCRIPTION</span></span>
<span data-ttu-id="4eb8f-106">A **New-AzOperationalInsightsWorkspace** parancsmag munkaterületet hoz létre a megadott erőforráscsoportban és helyen.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="4eb8f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4eb8f-107">EXAMPLES</span></span>

### <span data-ttu-id="4eb8f-108">1. példa: Munkaterület létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="4eb8f-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="4eb8f-109">Ez a parancs létrehoz egy MyWorkspace nevű szabványos termékváltozat-munkaterületet a ContosoResourceGroup nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="4eb8f-110">2. példa: Munkaterület létrehozása és csatolása meglévő fiókhoz</span><span class="sxs-lookup"><span data-stu-id="4eb8f-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="4eb8f-111">Az első parancs a Get-AzOperationalInsightsLinkTargets parancsmag segítségével begyakorlja a Operational Insights-fiók hivatkozási céljait, majd tárolja őket a $OILinkTargets változóban.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="4eb8f-112">A második parancs a folyamat műveleti $OILinkTargets segítségével átadja az első fiókkapcsolat célhelyét a **New-AzOperationalInsightsWorkspace** parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4eb8f-113">A parancs létrehoz egy MyWorkspace nevű szabványos termékváltozat-munkaterületet, amely a webhely első Operational Insights-$OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="4eb8f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4eb8f-114">PARAMETERS</span></span>

### <span data-ttu-id="4eb8f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb8f-115">-DefaultProfile</span></span>
<span data-ttu-id="4eb8f-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4eb8f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4eb8f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4eb8f-117">-Force</span></span>
<span data-ttu-id="4eb8f-118">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4eb8f-119">-Location</span><span class="sxs-lookup"><span data-stu-id="4eb8f-119">-Location</span></span>
<span data-ttu-id="4eb8f-120">Azt a helyet adja meg, ahol létre kell hoznia a munkaterületet, például Kelet-Egyesült Államok vagy Nyugat-Európa.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-120">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="4eb8f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4eb8f-121">-Name</span></span>
<span data-ttu-id="4eb8f-122">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-122">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="4eb8f-123">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="4eb8f-123">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="4eb8f-124">A munkaterületen való hozzáféréshez szükséges hálózati hozzáférés típusa.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-124">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="4eb8f-125">Az értéknek "Engedélyezve" vagy "Letiltva" értékűnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-125">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="4eb8f-126">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="4eb8f-126">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="4eb8f-127">A munkaterületi lekérdezés eléréséhez használható hálózati hozzáférés típusa.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-127">The network access type for accessing workspace query.</span></span> <span data-ttu-id="4eb8f-128">Az értéknek "Engedélyezve" vagy "Letiltva" értékűnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-128">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="4eb8f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eb8f-129">-ResourceGroupName</span></span>
<span data-ttu-id="4eb8f-130">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-130">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4eb8f-131">A munkaterület ebben az erőforráscsoportban jön létre.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-131">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="4eb8f-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="4eb8f-132">-RetentionInDays</span></span>
<span data-ttu-id="4eb8f-133">A munkaterület adatmegőrzési időszaka napokban.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-133">The workspace data retention in days.</span></span> <span data-ttu-id="4eb8f-134">730 nap az összes többi skus maximálisan engedélyezett</span><span class="sxs-lookup"><span data-stu-id="4eb8f-134">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="4eb8f-135">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="4eb8f-135">-Sku</span></span>
<span data-ttu-id="4eb8f-136">A munkaterület szolgáltatási rétegét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-136">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="4eb8f-137">Ha többet meg kell tudni arról, hogy melyik értéket kell használni, https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers ellenőrizze.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-137">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="4eb8f-138">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="4eb8f-138">Valid values are:</span></span>
- <span data-ttu-id="4eb8f-139">ingyenes</span><span class="sxs-lookup"><span data-stu-id="4eb8f-139">free</span></span>
- <span data-ttu-id="4eb8f-140">pergb2018</span><span class="sxs-lookup"><span data-stu-id="4eb8f-140">pergb2018</span></span>
- <span data-ttu-id="4eb8f-141">pernode</span><span class="sxs-lookup"><span data-stu-id="4eb8f-141">pernode</span></span>
- <span data-ttu-id="4eb8f-142">prémium</span><span class="sxs-lookup"><span data-stu-id="4eb8f-142">premium</span></span>
- <span data-ttu-id="4eb8f-143">különálló</span><span class="sxs-lookup"><span data-stu-id="4eb8f-143">standalone</span></span>
- <span data-ttu-id="4eb8f-144">normál</span><span class="sxs-lookup"><span data-stu-id="4eb8f-144">standard</span></span>

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

### <span data-ttu-id="4eb8f-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="4eb8f-145">-Tag</span></span>
<span data-ttu-id="4eb8f-146">A munkaterület erőforráscímkéi.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-146">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="4eb8f-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4eb8f-147">-Confirm</span></span>
<span data-ttu-id="4eb8f-148">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eb8f-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eb8f-149">-WhatIf</span></span>
<span data-ttu-id="4eb8f-150">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eb8f-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eb8f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb8f-152">CommonParameters</span></span>
<span data-ttu-id="4eb8f-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb8f-154">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4eb8f-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb8f-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4eb8f-155">INPUTS</span></span>

### <span data-ttu-id="4eb8f-156">System.String</span><span class="sxs-lookup"><span data-stu-id="4eb8f-156">System.String</span></span>

### <span data-ttu-id="4eb8f-157">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4eb8f-157">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4eb8f-158">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4eb8f-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4eb8f-159">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4eb8f-159">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4eb8f-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4eb8f-160">OUTPUTS</span></span>

### <span data-ttu-id="4eb8f-161">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="4eb8f-161">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="4eb8f-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4eb8f-162">NOTES</span></span>

<span data-ttu-id="4eb8f-163">Megjelent egy új árazási modell.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-163">A new pricing model has been released.</span></span> <span data-ttu-id="4eb8f-164">Ha Ön felhőszolgáltató, ez azt jelenti, hogy a termékváltozathoz "önálló" eszközt kell használnia.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-164">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="4eb8f-165">A színfalak mögött a termékváltozat gbonként 2018-ra változik.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-165">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="4eb8f-166">További információért olvassa el az alábbi információkat: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="4eb8f-166">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="4eb8f-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4eb8f-167">RELATED LINKS</span></span>

[<span data-ttu-id="4eb8f-168">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4eb8f-168">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)



