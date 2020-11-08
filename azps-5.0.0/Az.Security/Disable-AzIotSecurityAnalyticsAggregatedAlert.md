---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Disable-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 3747109d13fd4224b0f86bc5ecf2992ed4229487
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188177"
---
# <span data-ttu-id="d7457-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="d7457-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="d7457-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7457-102">SYNOPSIS</span></span>
<span data-ttu-id="d7457-103">IOT összesített értesítésének mellőzése</span><span class="sxs-lookup"><span data-stu-id="d7457-103">Dismiss Iot aggregated alert</span></span>

## <span data-ttu-id="d7457-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7457-104">SYNTAX</span></span>

### <span data-ttu-id="d7457-105">SolutionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7457-105">SolutionLevelResource (Default)</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7457-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d7457-106">InputObject</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -InputObject <PSIoTSecurityAggregatedAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7457-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7457-107">ResourceId</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7457-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7457-108">DESCRIPTION</span></span>
<span data-ttu-id="d7457-109">Az Disable-AzIotSecurityAnalyticsAggregatedAlert parancsmag egy bizonyos aggragated riasztást küld az IOT-hub eszközein.</span><span class="sxs-lookup"><span data-stu-id="d7457-109">The Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet dismisses a specific aggragated alert on devices of iot hub.</span></span> <span data-ttu-id="d7457-110">Az összesített értesítések neve a riasztás típusa és az értesítési aggragted dátum kombinációja, az "/" jellel elválasztva.</span><span class="sxs-lookup"><span data-stu-id="d7457-110">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="d7457-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d7457-111">EXAMPLES</span></span>

### <span data-ttu-id="d7457-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d7457-112">Example 1</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolutionName" -Name "IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="d7457-113">Összesített riasztás megszüntetése "IoT_SucessfulLocalLogin/2020-03-15" (név összekapcsolva a riasztási típustól és az összesített dátumtól) a "MySolutionName" IoT biztonsági megoldás "MyResourceGroup" erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="d7457-113">Dismiss aggregated alert "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="d7457-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="d7457-114">Example 2</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="d7457-115">Összesített riasztás mellőzése a következő erőforrás-azonosítóval: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span><span class="sxs-lookup"><span data-stu-id="d7457-115">Dismiss aggregated alert with resource Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span></span>

## <span data-ttu-id="d7457-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7457-116">PARAMETERS</span></span>

### <span data-ttu-id="d7457-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7457-117">-DefaultProfile</span></span>
<span data-ttu-id="d7457-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7457-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7457-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7457-119">-InputObject</span></span>
<span data-ttu-id="d7457-120">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="d7457-120">Input Object.</span></span>

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

### <span data-ttu-id="d7457-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d7457-121">-Name</span></span>
<span data-ttu-id="d7457-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="d7457-122">Resource name.</span></span>

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

### <span data-ttu-id="d7457-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7457-123">-PassThru</span></span>
<span data-ttu-id="d7457-124">Adja meg, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="d7457-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="d7457-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7457-125">-ResourceGroupName</span></span>
<span data-ttu-id="d7457-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d7457-126">Resource group name.</span></span>

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

### <span data-ttu-id="d7457-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7457-127">-ResourceId</span></span>
<span data-ttu-id="d7457-128">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="d7457-128">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="d7457-129">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="d7457-129">-SolutionName</span></span>
<span data-ttu-id="d7457-130">Megoldás neve</span><span class="sxs-lookup"><span data-stu-id="d7457-130">Solution name</span></span>

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

### <span data-ttu-id="d7457-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d7457-131">-Confirm</span></span>
<span data-ttu-id="d7457-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d7457-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7457-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7457-133">-WhatIf</span></span>
<span data-ttu-id="d7457-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d7457-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7457-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7457-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7457-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7457-136">CommonParameters</span></span>
<span data-ttu-id="d7457-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7457-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7457-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d7457-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7457-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7457-139">INPUTS</span></span>

### <span data-ttu-id="d7457-140">Microsoft. Azure. commands. Security. models. IotSecuritySolutionAnalytics. PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="d7457-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

### <span data-ttu-id="d7457-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d7457-141">System.String</span></span>

## <span data-ttu-id="d7457-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7457-142">OUTPUTS</span></span>

### <span data-ttu-id="d7457-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d7457-143">System.Boolean</span></span>

## <span data-ttu-id="d7457-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7457-144">NOTES</span></span>

## <span data-ttu-id="d7457-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7457-145">RELATED LINKS</span></span>
