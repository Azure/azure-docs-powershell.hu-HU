---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 065c2e185be1a9cdc0f495b61104f659076b54b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835897"
---
# <span data-ttu-id="30e01-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="30e01-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="30e01-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30e01-102">SYNOPSIS</span></span>
<span data-ttu-id="30e01-103">Megkapja az összes eventhub-consumergroups.</span><span class="sxs-lookup"><span data-stu-id="30e01-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="30e01-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30e01-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30e01-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="30e01-105">DESCRIPTION</span></span>
<span data-ttu-id="30e01-106">Megkapja az IotHub által használt különböző EventHubs tartozó összes eventhub consumergroups.</span><span class="sxs-lookup"><span data-stu-id="30e01-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="30e01-107">Példák</span><span class="sxs-lookup"><span data-stu-id="30e01-107">EXAMPLES</span></span>

### <span data-ttu-id="30e01-108">Az 1 példa beolvassa a telemetriai eventhub összes eventhub consumergroups</span><span class="sxs-lookup"><span data-stu-id="30e01-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="30e01-109">Beolvassa a telemetriai eventhub összes eventhub consumergroups a iothub nevű myiothub</span><span class="sxs-lookup"><span data-stu-id="30e01-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

### <span data-ttu-id="30e01-110">A 2 példa beolvassa a operationsmonitoring eventhub összes eventhub consumergroups</span><span class="sxs-lookup"><span data-stu-id="30e01-110">Example 2 Gets all the eventhub consumergroups for the operationsmonitoring eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents"
```

<span data-ttu-id="30e01-111">Beolvassa a operationsMonitoringEvents eventhub összes eventhub consumergroups a iothub nevű myiothub</span><span class="sxs-lookup"><span data-stu-id="30e01-111">Gets all the eventhub consumergroups for the operationsMonitoringEvents eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="30e01-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30e01-112">PARAMETERS</span></span>

### <span data-ttu-id="30e01-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30e01-113">-DefaultProfile</span></span>
<span data-ttu-id="30e01-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="30e01-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30e01-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="30e01-115">-EventHubEndpointName</span></span>
<span data-ttu-id="30e01-116">Az esemény központi végpontjának neve.</span><span class="sxs-lookup"><span data-stu-id="30e01-116">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="30e01-117">Események lehetséges értékei, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="30e01-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="30e01-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="30e01-118">-Name</span></span>
<span data-ttu-id="30e01-119">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="30e01-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="30e01-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30e01-120">-ResourceGroupName</span></span>
<span data-ttu-id="30e01-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="30e01-121">Resource Group Name</span></span>

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

### <span data-ttu-id="30e01-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30e01-122">CommonParameters</span></span>
<span data-ttu-id="30e01-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30e01-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30e01-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30e01-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30e01-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30e01-125">INPUTS</span></span>

### <span data-ttu-id="30e01-126">System. String</span><span class="sxs-lookup"><span data-stu-id="30e01-126">System.String</span></span>

## <span data-ttu-id="30e01-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30e01-127">OUTPUTS</span></span>

### <span data-ttu-id="30e01-128">Microsoft. Azure. Command. Management. IotHub. models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="30e01-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="30e01-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30e01-129">NOTES</span></span>

## <span data-ttu-id="30e01-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30e01-130">RELATED LINKS</span></span>
