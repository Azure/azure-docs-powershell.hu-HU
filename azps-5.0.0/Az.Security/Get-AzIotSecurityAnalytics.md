---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalytics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
ms.openlocfilehash: 56827f5a461239ceae756591b82ff687cb50053c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300941"
---
# <span data-ttu-id="7bac3-101">Get-AzIotSecurityAnalytics</span><span class="sxs-lookup"><span data-stu-id="7bac3-101">Get-AzIotSecurityAnalytics</span></span>

## <span data-ttu-id="7bac3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7bac3-102">SYNOPSIS</span></span>
<span data-ttu-id="7bac3-103">A IoT biztonsági elemzésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="7bac3-103">Get IoT security analytics</span></span>

## <span data-ttu-id="7bac3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7bac3-104">SYNTAX</span></span>

```
Get-AzIotSecurityAnalytics -ResourceGroupName <String> -SolutionName <String> [-Default]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bac3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7bac3-105">DESCRIPTION</span></span>
<span data-ttu-id="7bac3-106">A Get-AzIotSecurityAnalytics parancsmag egy bizonyos IOT biztonsági megoldás biztonsági elemzésének egy halmazát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7bac3-106">The Get-AzIotSecurityAnalytics cmdlet returns a set of security analytics of a specific iot security solution</span></span>

## <span data-ttu-id="7bac3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7bac3-107">EXAMPLES</span></span>

### <span data-ttu-id="7bac3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7bac3-108">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalytics -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Default

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default"
Name: "default"
Type: "Microsoft.Security/IoTSecuritySolutionAnalyticsModel"
Metrics: {
            High": 5
            Medium: 200
            Low: 102
          }
UnhealthyDeviceCount: 1200
DevicesMetrics: [
            {
              Date: "2019-02-01T00:00:00Z"
              DevicesMetrics: {
                High: 3
                Medium: 15
                Low: 70
              }
            }
            {
              Date: "2019-02-02T00:00:00Z"
              DevicesMetrics: {
                High: 3
                Medium: 45
                Low: 65
              }
            }
          ]
TopAlertedDevices: [
            {
              DeviceId: "id1"
              AlertsCount: 200
            }
            {
              DeviceId": "id2"
              AlertsCount": 170
            }
            {
              DeviceId": "id3"
              AlertsCount": 150
            }
          ]
MostPrevalentDeviceAlerts: [
            {
              AlertDisplayName: "Custom Alert - number of device to cloud messages in AMQP protocol is not in the allowed range"
              ReportedSeverity: "Low"
              AlertsCount: 200
            }
            {
              AlertDisplayName: "Custom Alert - execution of a process that is not allowed"
              ReportedSeverity: "Medium"
              AlertsCount: 170
            }
            {
              AlertDisplayName": "Successful Bruteforce"
              ReportedSeverity": "Low"
              AlertsCount": 150
            }
          ]
MostPrevalentDeviceRecommendations: [
            {
              RecommendationDisplayName: "Install the Azure Security of Things Agent"
              ReportedSeverity: "Low"
              DevicesCount: 200
            }
            {
              RecommendationDisplayName: "High level permissions configured in Edge model twin for Edge module"
              ReportedSeverity: "Low"
              DevicesCount: 170
            }
            {
              RrecommendationDisplayName: "Same Authentication Credentials used by multiple devices"
              ReportedSeverity: "Medium"
              DevicesCount: 150
            }
          ]
        }
      }
```

<span data-ttu-id="7bac3-109">A deafult IoT biztonsági MySolution "" biztonsági megoldásának megkeresése a reasource csoportban "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="7bac3-109">Get the deafult IoT Security Analytics for Security Solution "MySolution" in reasource group "MyResourceGroup"</span></span>

## <span data-ttu-id="7bac3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7bac3-110">PARAMETERS</span></span>

### <span data-ttu-id="7bac3-111">– Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="7bac3-111">-Default</span></span>
<span data-ttu-id="7bac3-112">Ha van, akkor az alapértelmezett Analytics-készletet kell beszereznie, különben az összes Analytics-készlet listáját.</span><span class="sxs-lookup"><span data-stu-id="7bac3-112">If present, get the default analytics set, otherwise, get the list of all analytics sets.</span></span>

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

### <span data-ttu-id="7bac3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bac3-113">-DefaultProfile</span></span>
<span data-ttu-id="7bac3-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7bac3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bac3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bac3-115">-ResourceGroupName</span></span>
<span data-ttu-id="7bac3-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="7bac3-116">Resource group name.</span></span>

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

### <span data-ttu-id="7bac3-117">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="7bac3-117">-SolutionName</span></span>
<span data-ttu-id="7bac3-118">Megoldás neve</span><span class="sxs-lookup"><span data-stu-id="7bac3-118">Solution name</span></span>

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

### <span data-ttu-id="7bac3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bac3-119">CommonParameters</span></span>
<span data-ttu-id="7bac3-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7bac3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bac3-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7bac3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bac3-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bac3-122">INPUTS</span></span>

### <span data-ttu-id="7bac3-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="7bac3-123">None</span></span>

## <span data-ttu-id="7bac3-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bac3-124">OUTPUTS</span></span>

### <span data-ttu-id="7bac3-125">Microsoft. Azure. commands. Security. models. IotSecuritySolutionAnalytics. PSIotSecuritySolutionAnalytics</span><span class="sxs-lookup"><span data-stu-id="7bac3-125">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIotSecuritySolutionAnalytics</span></span>

## <span data-ttu-id="7bac3-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7bac3-126">NOTES</span></span>

## <span data-ttu-id="7bac3-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7bac3-127">RELATED LINKS</span></span>
