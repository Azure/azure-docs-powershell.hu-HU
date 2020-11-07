---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 3905111a0855eef6421a587bc7151b411106d13a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666282"
---
# <span data-ttu-id="b5b38-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b5b38-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="b5b38-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5b38-102">SYNOPSIS</span></span>
<span data-ttu-id="b5b38-103">Megkapja az összes eventhub-consumergroups.</span><span class="sxs-lookup"><span data-stu-id="b5b38-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="b5b38-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5b38-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5b38-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5b38-105">DESCRIPTION</span></span>
<span data-ttu-id="b5b38-106">Megkapja az IotHub által használt különböző EventHubs tartozó összes eventhub consumergroups.</span><span class="sxs-lookup"><span data-stu-id="b5b38-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="b5b38-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b5b38-107">EXAMPLES</span></span>

### <span data-ttu-id="b5b38-108">Az 1 példa beolvassa a telemetriai eventhub összes eventhub consumergroups</span><span class="sxs-lookup"><span data-stu-id="b5b38-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="b5b38-109">Beolvassa a telemetriai eventhub összes eventhub consumergroups a iothub nevű myiothub</span><span class="sxs-lookup"><span data-stu-id="b5b38-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="b5b38-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5b38-110">PARAMETERS</span></span>

### <span data-ttu-id="b5b38-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5b38-111">-DefaultProfile</span></span>
<span data-ttu-id="b5b38-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b5b38-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5b38-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="b5b38-113">-EventHubEndpointName</span></span>
<span data-ttu-id="b5b38-114">Az esemény központi végpontjának neve.</span><span class="sxs-lookup"><span data-stu-id="b5b38-114">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="b5b38-115">Események lehetséges értékei, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="b5b38-115">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5b38-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b5b38-116">-Name</span></span>
<span data-ttu-id="b5b38-117">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="b5b38-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="b5b38-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5b38-118">-ResourceGroupName</span></span>
<span data-ttu-id="b5b38-119">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="b5b38-119">Resource Group Name</span></span>

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

### <span data-ttu-id="b5b38-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b38-120">CommonParameters</span></span>
<span data-ttu-id="b5b38-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5b38-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5b38-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5b38-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b38-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5b38-123">INPUTS</span></span>

### <span data-ttu-id="b5b38-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b5b38-124">System.String</span></span>

## <span data-ttu-id="b5b38-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5b38-125">OUTPUTS</span></span>

### <span data-ttu-id="b5b38-126">Microsoft. Azure. Command. Management. IotHub. models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="b5b38-126">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="b5b38-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5b38-127">NOTES</span></span>

## <span data-ttu-id="b5b38-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5b38-128">RELATED LINKS</span></span>
