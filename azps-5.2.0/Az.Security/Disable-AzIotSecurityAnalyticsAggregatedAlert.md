---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Disable-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 3747109d13fd4224b0f86bc5ecf2992ed4229487
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340470"
---
# <span data-ttu-id="0ac1d-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="0ac1d-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="0ac1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ac1d-102">SYNOPSIS</span></span>
<span data-ttu-id="0ac1d-103">Az Iot összesítő riasztásának mellőzését</span><span class="sxs-lookup"><span data-stu-id="0ac1d-103">Dismiss Iot aggregated alert</span></span>

## <span data-ttu-id="0ac1d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0ac1d-104">SYNTAX</span></span>

### <span data-ttu-id="0ac1d-105">SolutionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0ac1d-105">SolutionLevelResource (Default)</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ac1d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0ac1d-106">InputObject</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -InputObject <PSIoTSecurityAggregatedAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ac1d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ac1d-107">ResourceId</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ac1d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0ac1d-108">DESCRIPTION</span></span>
<span data-ttu-id="0ac1d-109">A Disable-AzIotSecurityAnalyticsAggregatedAlert parancsmag mellőzi az iot hub eszközein található speciális, aggragált riasztásokat.</span><span class="sxs-lookup"><span data-stu-id="0ac1d-109">The Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet dismisses a specific aggragated alert on devices of iot hub.</span></span> <span data-ttu-id="0ac1d-110">Az összesített riasztások neve a riasztástípus és a riasztások aggragált dátumának kombinációja, "/" elválasztva egymástól.</span><span class="sxs-lookup"><span data-stu-id="0ac1d-110">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="0ac1d-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0ac1d-111">EXAMPLES</span></span>

### <span data-ttu-id="0ac1d-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="0ac1d-112">Example 1</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolutionName" -Name "IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="0ac1d-113">Az "IoT_SucessfulLocalLogin/2020-03-15" (riasztástípusból és összesített dátumból egyesített név) az IoT "MySolutionName" biztonsági megoldásának "MyResourceGroup" erőforráscsoportban való mellőzése</span><span class="sxs-lookup"><span data-stu-id="0ac1d-113">Dismiss aggregated alert "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="0ac1d-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="0ac1d-114">Example 2</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="0ac1d-115">A "/subscriptions/XXXXXXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15" típusú összesített riasztás mellőzése</span><span class="sxs-lookup"><span data-stu-id="0ac1d-115">Dismiss aggregated alert with resource Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span></span>

## <span data-ttu-id="0ac1d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ac1d-116">PARAMETERS</span></span>

### <span data-ttu-id="0ac1d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ac1d-117">-DefaultProfile</span></span>
<span data-ttu-id="0ac1d-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ac1d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ac1d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ac1d-119">-InputObject</span></span>
<span data-ttu-id="0ac1d-120">Bemeneti objektum.</span><span class="sxs-lookup"><span data-stu-id="0ac1d-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ac1d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0ac1d-121">-Name</span></span>
<span data-ttu-id="0ac1d-122">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0ac1d-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ac1d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ac1d-123">-PassThru</span></span>
<span data-ttu-id="0ac1d-124">Adja vissza, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="0ac1d-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="0ac1d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ac1d-125">-ResourceGroupName</span></span>
<span data-ttu-id="0ac1d-126">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0ac1d-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ac1d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ac1d-127">-ResourceId</span></span>
<span data-ttu-id="0ac1d-128">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="0ac1d-128">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ac1d-129">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="0ac1d-129">-SolutionName</span></span>
<span data-ttu-id="0ac1d-130">Megoldás neve</span><span class="sxs-lookup"><span data-stu-id="0ac1d-130">Solution name</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ac1d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ac1d-131">-Confirm</span></span>
<span data-ttu-id="0ac1d-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0ac1d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ac1d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ac1d-133">-WhatIf</span></span>
<span data-ttu-id="0ac1d-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0ac1d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ac1d-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0ac1d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ac1d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ac1d-136">CommonParameters</span></span>
<span data-ttu-id="0ac1d-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ac1d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ac1d-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ac1d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ac1d-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ac1d-139">INPUTS</span></span>

### <span data-ttu-id="0ac1d-140">Microsoft.Azure.Commands.Security.Models.iotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="0ac1d-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

### <span data-ttu-id="0ac1d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0ac1d-141">System.String</span></span>

## <span data-ttu-id="0ac1d-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ac1d-142">OUTPUTS</span></span>

### <span data-ttu-id="0ac1d-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0ac1d-143">System.Boolean</span></span>

## <span data-ttu-id="0ac1d-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0ac1d-144">NOTES</span></span>

## <span data-ttu-id="0ac1d-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ac1d-145">RELATED LINKS</span></span>
