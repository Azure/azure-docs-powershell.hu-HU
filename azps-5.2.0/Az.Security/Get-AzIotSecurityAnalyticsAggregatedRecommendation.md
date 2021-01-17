---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
ms.openlocfilehash: 944c029b4085316225887b821c4f6c8f52e7f92b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369723"
---
# <span data-ttu-id="eef11-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="eef11-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span></span>

## <span data-ttu-id="eef11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eef11-102">SYNOPSIS</span></span>
<span data-ttu-id="eef11-103">Az IoT-biztonság összesített ajánlásának lekérte</span><span class="sxs-lookup"><span data-stu-id="eef11-103">Get IoT security aggregated recommendation</span></span>

## <span data-ttu-id="eef11-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eef11-104">SYNTAX</span></span>

### <span data-ttu-id="eef11-105">SolutionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eef11-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eef11-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="eef11-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eef11-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eef11-107">DESCRIPTION</span></span>
<span data-ttu-id="eef11-108">A Get-AzIotSecurityAnalyticsAggregatedAlert parancsmag egy vagy több összesített javaslatot ad vissza az iot hub eszközein.</span><span class="sxs-lookup"><span data-stu-id="eef11-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated recommendations on devices of iot hub.</span></span> <span data-ttu-id="eef11-109">Az összesített javaslat neve a típusa.</span><span class="sxs-lookup"><span data-stu-id="eef11-109">The name of an aggregated recommendation is its type</span></span>

## <span data-ttu-id="eef11-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eef11-110">EXAMPLES</span></span>

### <span data-ttu-id="eef11-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="eef11-111">Example 1</span></span>
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

<span data-ttu-id="eef11-112">Szerezze be az összesített "IoT_OpenPorts" biztonsági megoldás "MySolution" és erőforráscsoport "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="eef11-112">Get the aggregated recommendation "IoT_OpenPorts" in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="eef11-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="eef11-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated recommendation items as shown in example 1
```

<span data-ttu-id="eef11-114">Összesített javaslatok listája a "MySolution" biztonsági megoldásban és a "MyResourceGroup" erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="eef11-114">Get a list of aggregated recommendations in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="eef11-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eef11-115">PARAMETERS</span></span>

### <span data-ttu-id="eef11-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eef11-116">-DefaultProfile</span></span>
<span data-ttu-id="eef11-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eef11-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eef11-118">-Name</span><span class="sxs-lookup"><span data-stu-id="eef11-118">-Name</span></span>
<span data-ttu-id="eef11-119">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="eef11-119">Resource name.</span></span>

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

### <span data-ttu-id="eef11-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eef11-120">-ResourceGroupName</span></span>
<span data-ttu-id="eef11-121">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="eef11-121">Resource group name.</span></span>

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

### <span data-ttu-id="eef11-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="eef11-122">-SolutionName</span></span>
<span data-ttu-id="eef11-123">Megoldás neve</span><span class="sxs-lookup"><span data-stu-id="eef11-123">Solution name</span></span>

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

### <span data-ttu-id="eef11-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eef11-124">CommonParameters</span></span>
<span data-ttu-id="eef11-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eef11-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eef11-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eef11-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eef11-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eef11-127">INPUTS</span></span>

### <span data-ttu-id="eef11-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="eef11-128">None</span></span>

## <span data-ttu-id="eef11-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eef11-129">OUTPUTS</span></span>

### <span data-ttu-id="eef11-130">Microsoft.Azure.Commands.Security.Models.iotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="eef11-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span></span>

## <span data-ttu-id="eef11-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eef11-131">NOTES</span></span>

## <span data-ttu-id="eef11-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eef11-132">RELATED LINKS</span></span>
