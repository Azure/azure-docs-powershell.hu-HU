---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
ms.openlocfilehash: 944c029b4085316225887b821c4f6c8f52e7f92b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300161"
---
# <span data-ttu-id="1c06f-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="1c06f-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span></span>

## <span data-ttu-id="1c06f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1c06f-102">SYNOPSIS</span></span>
<span data-ttu-id="1c06f-103">IoT biztonsági összegzési javaslat beszerzése</span><span class="sxs-lookup"><span data-stu-id="1c06f-103">Get IoT security aggregated recommendation</span></span>

## <span data-ttu-id="1c06f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1c06f-104">SYNTAX</span></span>

### <span data-ttu-id="1c06f-105">SolutionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1c06f-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c06f-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="1c06f-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c06f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1c06f-107">DESCRIPTION</span></span>
<span data-ttu-id="1c06f-108">A Get-AzIotSecurityAnalyticsAggregatedAlert parancsmag egy vagy több összesített javaslatot ad eredményül a IOT hub eszközein.</span><span class="sxs-lookup"><span data-stu-id="1c06f-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated recommendations on devices of iot hub.</span></span> <span data-ttu-id="1c06f-109">Az összesített javaslat neve a típus</span><span class="sxs-lookup"><span data-stu-id="1c06f-109">The name of an aggregated recommendation is its type</span></span>

## <span data-ttu-id="1c06f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1c06f-110">EXAMPLES</span></span>

### <span data-ttu-id="1c06f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1c06f-111">Example 1</span></span>
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

<span data-ttu-id="1c06f-112">A "MyResourceGroup" biztonsági megoldás "MySolution" és erőforráscsoport "" című összesített IoT_OpenPorts ajánlásának beszerzése</span><span class="sxs-lookup"><span data-stu-id="1c06f-112">Get the aggregated recommendation "IoT_OpenPorts" in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="1c06f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="1c06f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated recommendation items as shown in example 1
```

<span data-ttu-id="1c06f-114">Összesített javaslatok listája a biztonsági megoldás "MySolution" és erőforráscsoport "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="1c06f-114">Get a list of aggregated recommendations in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="1c06f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1c06f-115">PARAMETERS</span></span>

### <span data-ttu-id="1c06f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c06f-116">-DefaultProfile</span></span>
<span data-ttu-id="1c06f-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1c06f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c06f-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1c06f-118">-Name</span></span>
<span data-ttu-id="1c06f-119">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="1c06f-119">Resource name.</span></span>

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

### <span data-ttu-id="1c06f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c06f-120">-ResourceGroupName</span></span>
<span data-ttu-id="1c06f-121">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="1c06f-121">Resource group name.</span></span>

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

### <span data-ttu-id="1c06f-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="1c06f-122">-SolutionName</span></span>
<span data-ttu-id="1c06f-123">Megoldás neve</span><span class="sxs-lookup"><span data-stu-id="1c06f-123">Solution name</span></span>

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

### <span data-ttu-id="1c06f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c06f-124">CommonParameters</span></span>
<span data-ttu-id="1c06f-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1c06f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c06f-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1c06f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c06f-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c06f-127">INPUTS</span></span>

### <span data-ttu-id="1c06f-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="1c06f-128">None</span></span>

## <span data-ttu-id="1c06f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c06f-129">OUTPUTS</span></span>

### <span data-ttu-id="1c06f-130">Microsoft. Azure. commands. Security. models. IotSecuritySolutionAnalytics. PSIoTSecurityAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="1c06f-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span></span>

## <span data-ttu-id="1c06f-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1c06f-131">NOTES</span></span>

## <span data-ttu-id="1c06f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c06f-132">RELATED LINKS</span></span>
