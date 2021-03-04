---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
ms.openlocfilehash: f57d3b3eb254a547059cb2e7c37a0720ee5f6310
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927578"
---
# <span data-ttu-id="d33ca-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="d33ca-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span></span>

## <span data-ttu-id="d33ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d33ca-102">SYNOPSIS</span></span>
<span data-ttu-id="d33ca-103">Az IoT-biztonság összesített ajánlásának lekérte</span><span class="sxs-lookup"><span data-stu-id="d33ca-103">Get IoT security aggregated recommendation</span></span>

## <span data-ttu-id="d33ca-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d33ca-104">SYNTAX</span></span>

### <span data-ttu-id="d33ca-105">SolutionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d33ca-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d33ca-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="d33ca-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d33ca-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d33ca-107">DESCRIPTION</span></span>
<span data-ttu-id="d33ca-108">A Get-AzIotSecurityAnalyticsAggregatedAlert parancsmag egy vagy több összesített javaslatot ad vissza az iot hub eszközein.</span><span class="sxs-lookup"><span data-stu-id="d33ca-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated recommendations on devices of iot hub.</span></span> <span data-ttu-id="d33ca-109">Az összesített javaslat neve annak típusa</span><span class="sxs-lookup"><span data-stu-id="d33ca-109">The name of an aggregated recommendation is its type</span></span>

## <span data-ttu-id="d33ca-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d33ca-110">EXAMPLES</span></span>

### <span data-ttu-id="d33ca-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="d33ca-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Name IoT_OpenPorts

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default/aggregatedRecommendations/IoT_OpenPorts"
Name: "IoT_OpenPorts"
Type: "Microsoft.Security/IoTSecurityAggregatedRecommendation"
RecommendationName: "IoT_OpenPorts"
RecommendationDisplayName: "Device has open ports"
RecommendationTypeId: ""
DetectedBy: "IoTSecurity"
HealthyDevices: -1
UnhealthyDeviceCount: 5
RemediationSteps: "Review open ports on the device and make sure they belong to legitimate and necessary processes for the device to function correctly."
ReportedSeverity: "Medium"
Description: "Found a listening endpoint on the device."
LogAnalyticsQuery: "SecurityRecommendation | where tolower(AssessedResourceId) == tolower('/subscriptions/075423e9-7d33-4166-8bdf-3920b04e3735/resourcegroups/iot-hub-demo/providers/microsoft.devices/iothubs/ascforiot-demo') and tolower(RecommendationName) == tolower('IoT_OpenPorts') and TimeGenerated  < now()"
```

<span data-ttu-id="d33ca-112">Szerezze be az összesített "IoT_OpenPorts" biztonsági megoldás "MySolution" és erőforráscsoport "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="d33ca-112">Get the aggregated recommendation "IoT_OpenPorts" in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="d33ca-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="d33ca-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated recommendation items as shown in example 1
```

<span data-ttu-id="d33ca-114">Összesített javaslatok listája a "MySolution" biztonsági megoldásban és a "MyResourceGroup" erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="d33ca-114">Get a list of aggregated recommendations in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="d33ca-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d33ca-115">PARAMETERS</span></span>

### <span data-ttu-id="d33ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d33ca-116">-DefaultProfile</span></span>
<span data-ttu-id="d33ca-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d33ca-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d33ca-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d33ca-118">-Name</span></span>
<span data-ttu-id="d33ca-119">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d33ca-119">Resource name.</span></span>

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

### <span data-ttu-id="d33ca-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d33ca-120">-ResourceGroupName</span></span>
<span data-ttu-id="d33ca-121">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d33ca-121">Resource group name.</span></span>

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

### <span data-ttu-id="d33ca-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="d33ca-122">-SolutionName</span></span>
<span data-ttu-id="d33ca-123">Megoldás neve</span><span class="sxs-lookup"><span data-stu-id="d33ca-123">Solution name</span></span>

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

### <span data-ttu-id="d33ca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d33ca-124">CommonParameters</span></span>
<span data-ttu-id="d33ca-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d33ca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d33ca-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d33ca-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d33ca-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d33ca-127">INPUTS</span></span>

### <span data-ttu-id="d33ca-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="d33ca-128">None</span></span>

## <span data-ttu-id="d33ca-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d33ca-129">OUTPUTS</span></span>

### <span data-ttu-id="d33ca-130">Microsoft.Azure.Commands.Security.Models.iotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="d33ca-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span></span>

## <span data-ttu-id="d33ca-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d33ca-131">NOTES</span></span>

## <span data-ttu-id="d33ca-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d33ca-132">RELATED LINKS</span></span>
