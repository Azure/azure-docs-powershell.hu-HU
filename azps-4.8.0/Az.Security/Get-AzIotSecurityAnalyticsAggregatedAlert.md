---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 5687497c55c6da914b28022320df1d7241f2eba1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183996"
---
# <span data-ttu-id="d27bc-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="d27bc-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="d27bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d27bc-102">SYNOPSIS</span></span>
<span data-ttu-id="d27bc-103">A IoT biztonsági összesítő értesítésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="d27bc-103">Get IoT security aggregated alert</span></span>

## <span data-ttu-id="d27bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d27bc-104">SYNTAX</span></span>

### <span data-ttu-id="d27bc-105">SolutionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d27bc-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d27bc-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="d27bc-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d27bc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d27bc-107">DESCRIPTION</span></span>
<span data-ttu-id="d27bc-108">A Get-AzIotSecurityAnalyticsAggregatedAlert parancsmag egy vagy több összesített riasztást ad eredményül a IOT hub eszközein.</span><span class="sxs-lookup"><span data-stu-id="d27bc-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated alerts on devices of iot hub.</span></span>
<span data-ttu-id="d27bc-109">Az összesített értesítések neve a riasztás típusa és az értesítési aggragted dátum kombinációja, az "/" jellel elválasztva.</span><span class="sxs-lookup"><span data-stu-id="d27bc-109">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="d27bc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d27bc-110">EXAMPLES</span></span>

### <span data-ttu-id="d27bc-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d27bc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Name "IoT_Bruteforce_Fail/2019-02-02"

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default/aggregatedAlerts/IoT_Bruteforce_Fail/2019-02-02"
Name: "IoT_Bruteforce_Fail/2019-02-02"
Type: "Microsoft.Security/IoTSecurityAggregatedAlert"
AlertType: "IoT_Bruteforce_Fail"
AlertDisplayName: "Failed Bruteforce"
AggregatedDateUtc: "2019-02-02"
VendorName: "Microsoft"
ReportedSeverity: "Low"
RemediationSteps: ""
Description: "Multiple unsuccsseful login attempts identified. A Bruteforce attack on the device failed."
Count: 50
EffectedResourceType: "IoT Device"
SystemSource: "Devices"
ActionTaken: "Detected"
LogAnalyticsQuery: "SecurityAlert | where tolower(ResourceId) == tolower('/subscriptions/b77ec8a9-04ed-48d2-a87a-e5887b978ba6/resourceGroups/IoT-Solution-DemoEnv/providers/Microsoft.Devices/IotHubs/rtogm-hub') and tolower(AlertName) == tolower('Custom Alert - number of device to cloud messages in MQTT protocol is not in the allowed range') | extend DeviceId=parse_json(ExtendedProperties)['DeviceId'] | project DeviceId, TimeGenerated, DisplayName, AlertSeverity, Description, RemediationSteps, ExtendedProperties"
TopDevicesList: [
                {
                  DeviceId: "testDevice1"
                  AlertsCount: 45
                  LastOccurrence: "10:42"
                }
                {
                  DeviceId: "testDevice2"
                  AlertsCount: 30
                  LastOccurrence: "15:42"
                }
              ]
```

<span data-ttu-id="d27bc-112">Az összesített riasztás beszerzése "IoT_Bruteforce_Fail/2019-02-02" (a név a riasztási típussal és az összesített dátummal együtt) a "MySolution" és a "MyResourceGroup" erőforráscsoport</span><span class="sxs-lookup"><span data-stu-id="d27bc-112">Get the aggregated alert "IoT_Bruteforce_Fail/2019-02-02" (the name combined from the alert type and its aggregated date) in solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="d27bc-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="d27bc-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated alert items as shown in example 1
```

<span data-ttu-id="d27bc-114">A "MySolution" és a "MyResourceGroup" erőforráscsoport "" megoldással beolvashatja az összes összesített riasztás listáját</span><span class="sxs-lookup"><span data-stu-id="d27bc-114">Get a list of all aggregated alerts in solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="d27bc-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d27bc-115">PARAMETERS</span></span>

### <span data-ttu-id="d27bc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d27bc-116">-DefaultProfile</span></span>
<span data-ttu-id="d27bc-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d27bc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d27bc-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d27bc-118">-Name</span></span>
<span data-ttu-id="d27bc-119">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="d27bc-119">Resource name.</span></span>

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

### <span data-ttu-id="d27bc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d27bc-120">-ResourceGroupName</span></span>
<span data-ttu-id="d27bc-121">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d27bc-121">Resource group name.</span></span>

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

### <span data-ttu-id="d27bc-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="d27bc-122">-SolutionName</span></span>
<span data-ttu-id="d27bc-123">Megoldás neve</span><span class="sxs-lookup"><span data-stu-id="d27bc-123">Solution name</span></span>

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

### <span data-ttu-id="d27bc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d27bc-124">CommonParameters</span></span>
<span data-ttu-id="d27bc-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d27bc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d27bc-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d27bc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d27bc-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d27bc-127">INPUTS</span></span>

### <span data-ttu-id="d27bc-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="d27bc-128">None</span></span>

## <span data-ttu-id="d27bc-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d27bc-129">OUTPUTS</span></span>

### <span data-ttu-id="d27bc-130">Microsoft. Azure. commands. Security. models. IotSecuritySolutionAnalytics. PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="d27bc-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

## <span data-ttu-id="d27bc-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d27bc-131">NOTES</span></span>

## <span data-ttu-id="d27bc-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d27bc-132">RELATED LINKS</span></span>
