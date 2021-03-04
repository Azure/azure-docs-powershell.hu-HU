---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 8d46c16afe8041181916eb25affed58e072798ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937946"
---
# <span data-ttu-id="58b78-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="58b78-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="58b78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58b78-102">SYNOPSIS</span></span>
<span data-ttu-id="58b78-103">Munkaterületet hoz létre, vagy visszaállít egy helyreállíthatóan törölt munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="58b78-103">Creates a workspace, or restore a soft-deleted workspace.</span></span>

## <span data-ttu-id="58b78-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="58b78-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58b78-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="58b78-105">DESCRIPTION</span></span>
<span data-ttu-id="58b78-106">A **New-AzOperationalInsightsWorkspace** parancsmag munkaterületet hoz létre a megadott erőforráscsoportban és helyen.</span><span class="sxs-lookup"><span data-stu-id="58b78-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span> <span data-ttu-id="58b78-107">Vagy visszaállíthatja a helyreállíthatóan törölt munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="58b78-107">Or restore a soft-deleted workspace.</span></span>

## <span data-ttu-id="58b78-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="58b78-108">EXAMPLES</span></span>

### <span data-ttu-id="58b78-109">1. példa: Munkaterület létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="58b78-109">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="58b78-110">Ez a parancs létrehoz egy MyWorkspace nevű szabványos termékváltozat-munkaterületet a ContosoResourceGroup nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="58b78-110">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="58b78-111">2. példa: Munkaterület létrehozása és csatolása meglévő fiókhoz</span><span class="sxs-lookup"><span data-stu-id="58b78-111">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="58b78-112">Az első parancs a Get-AzOperationalInsightsLinkTargets parancsmag segítségével begyakorlja a Operational Insights-fiók hivatkozási céljait, majd tárolja őket a $OILinkTargets változóban.</span><span class="sxs-lookup"><span data-stu-id="58b78-112">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="58b78-113">A második parancs átadja a $OILinkTargets a **New-AzOperationalInsightsWorkspace** parancsmagnak a folyamatoperációs operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="58b78-113">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="58b78-114">A parancs létrehoz egy MyWorkspace nevű szabványos termékváltozat-munkaterületet, amely a webhely első Operational Insights-$OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="58b78-114">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="58b78-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58b78-115">PARAMETERS</span></span>

### <span data-ttu-id="58b78-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58b78-116">-DefaultProfile</span></span>
<span data-ttu-id="58b78-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="58b78-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58b78-118">-Force</span><span class="sxs-lookup"><span data-stu-id="58b78-118">-Force</span></span>
<span data-ttu-id="58b78-119">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="58b78-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="58b78-120">-Location</span><span class="sxs-lookup"><span data-stu-id="58b78-120">-Location</span></span>
<span data-ttu-id="58b78-121">Azt a helyet adja meg, ahol létre kell hoznia a munkaterületet, például Kelet-Egyesült Államok vagy Nyugat-Európa.</span><span class="sxs-lookup"><span data-stu-id="58b78-121">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="58b78-122">-Name</span><span class="sxs-lookup"><span data-stu-id="58b78-122">-Name</span></span>
<span data-ttu-id="58b78-123">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="58b78-123">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="58b78-124">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="58b78-124">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="58b78-125">A munkaterület-eléréshez szükséges hálózati hozzáférés típusa.</span><span class="sxs-lookup"><span data-stu-id="58b78-125">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="58b78-126">Az értéknek "Engedélyezve" vagy "Letiltva" értékűnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="58b78-126">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="58b78-127">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="58b78-127">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="58b78-128">A munkaterületi lekérdezés eléréséhez használható hálózati hozzáférés típusa.</span><span class="sxs-lookup"><span data-stu-id="58b78-128">The network access type for accessing workspace query.</span></span> <span data-ttu-id="58b78-129">Az értéknek "Engedélyezve" vagy "Letiltva" értékűnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="58b78-129">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="58b78-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58b78-130">-ResourceGroupName</span></span>
<span data-ttu-id="58b78-131">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="58b78-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="58b78-132">A munkaterület ebben az erőforráscsoportban jön létre.</span><span class="sxs-lookup"><span data-stu-id="58b78-132">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="58b78-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="58b78-133">-RetentionInDays</span></span>
<span data-ttu-id="58b78-134">A munkaterület adatmegőrzési időszaka napokban.</span><span class="sxs-lookup"><span data-stu-id="58b78-134">The workspace data retention in days.</span></span> <span data-ttu-id="58b78-135">730 nap az összes többi skus maximálisan engedélyezett</span><span class="sxs-lookup"><span data-stu-id="58b78-135">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="58b78-136">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="58b78-136">-Sku</span></span>
<span data-ttu-id="58b78-137">A munkaterület szolgáltatási rétegét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="58b78-137">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="58b78-138">Ha többet meg kell tudni arról, hogy melyik értéket kell használni, https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers ellenőrizze.</span><span class="sxs-lookup"><span data-stu-id="58b78-138">For more information regarding which value to use please check https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="58b78-139">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="58b78-139">Valid values are:</span></span>
- <span data-ttu-id="58b78-140">ingyenes</span><span class="sxs-lookup"><span data-stu-id="58b78-140">free</span></span>
- <span data-ttu-id="58b78-141">pergb2018</span><span class="sxs-lookup"><span data-stu-id="58b78-141">pergb2018</span></span>
- <span data-ttu-id="58b78-142">pernode</span><span class="sxs-lookup"><span data-stu-id="58b78-142">pernode</span></span>
- <span data-ttu-id="58b78-143">prémium</span><span class="sxs-lookup"><span data-stu-id="58b78-143">premium</span></span>
- <span data-ttu-id="58b78-144">különálló</span><span class="sxs-lookup"><span data-stu-id="58b78-144">standalone</span></span>
- <span data-ttu-id="58b78-145">normál</span><span class="sxs-lookup"><span data-stu-id="58b78-145">standard</span></span>

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

### <span data-ttu-id="58b78-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="58b78-146">-Tag</span></span>
<span data-ttu-id="58b78-147">A munkaterület erőforráscímkéi.</span><span class="sxs-lookup"><span data-stu-id="58b78-147">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="58b78-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58b78-148">-Confirm</span></span>
<span data-ttu-id="58b78-149">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="58b78-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58b78-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58b78-150">-WhatIf</span></span>
<span data-ttu-id="58b78-151">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="58b78-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58b78-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="58b78-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58b78-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58b78-153">CommonParameters</span></span>
<span data-ttu-id="58b78-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58b78-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58b78-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58b78-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58b78-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58b78-156">INPUTS</span></span>

### <span data-ttu-id="58b78-157">System.String</span><span class="sxs-lookup"><span data-stu-id="58b78-157">System.String</span></span>

### <span data-ttu-id="58b78-158">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="58b78-158">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="58b78-159">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="58b78-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="58b78-160">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="58b78-160">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="58b78-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58b78-161">OUTPUTS</span></span>

### <span data-ttu-id="58b78-162">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="58b78-162">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="58b78-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="58b78-163">NOTES</span></span>

<span data-ttu-id="58b78-164">Megjelent egy új árazási modell.</span><span class="sxs-lookup"><span data-stu-id="58b78-164">A new pricing model has been released.</span></span> <span data-ttu-id="58b78-165">Ha Ön felhőszolgáltató, ez azt jelenti, hogy a termékváltozathoz "önálló" eszközt kell használnia.</span><span class="sxs-lookup"><span data-stu-id="58b78-165">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="58b78-166">A színfalak mögött a termékváltozat gbonként 2018-ra változik.</span><span class="sxs-lookup"><span data-stu-id="58b78-166">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="58b78-167">További információért olvassa el az alábbi információkat: https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="58b78-167">For more information, please see the following: https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="58b78-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58b78-168">RELATED LINKS</span></span>

[<span data-ttu-id="58b78-169">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="58b78-169">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="58b78-170">Get-AzOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="58b78-170">Get-AzOperationalInsightsLinkTargets</span></span>](./Get-AzOperationalInsightsLinkTargets.md)


