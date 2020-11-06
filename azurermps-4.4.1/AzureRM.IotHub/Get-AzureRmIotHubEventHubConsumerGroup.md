---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 84da4142bdc1b5435ca895be1995c6b48b5881fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501832"
---
# <span data-ttu-id="e541a-101">Get-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="e541a-101">Get-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="e541a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e541a-102">SYNOPSIS</span></span>
<span data-ttu-id="e541a-103">Megkapja az összes eventhub-consumergroups.</span><span class="sxs-lookup"><span data-stu-id="e541a-103">Gets all the eventhub consumergroups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e541a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e541a-104">SYNTAX</span></span>

```
Get-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e541a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e541a-105">DESCRIPTION</span></span>
<span data-ttu-id="e541a-106">Megkapja az IotHub által használt különböző EventHubs tartozó összes eventhub consumergroups.</span><span class="sxs-lookup"><span data-stu-id="e541a-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="e541a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e541a-107">EXAMPLES</span></span>

### <span data-ttu-id="e541a-108">Az 1 példa beolvassa a telemetriai eventhub összes eventhub consumergroups</span><span class="sxs-lookup"><span data-stu-id="e541a-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="e541a-109">Beolvassa a telemetriai eventhub összes eventhub consumergroups a iothub nevű myiothub</span><span class="sxs-lookup"><span data-stu-id="e541a-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

### <span data-ttu-id="e541a-110">A 2 példa beolvassa a operationsmonitoring eventhub összes eventhub consumergroups</span><span class="sxs-lookup"><span data-stu-id="e541a-110">Example 2 Gets all the eventhub consumergroups for the operationsmonitoring eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents"
```

<span data-ttu-id="e541a-111">Beolvassa a operationsMonitoringEvents eventhub összes eventhub consumergroups a iothub nevű myiothub</span><span class="sxs-lookup"><span data-stu-id="e541a-111">Gets all the eventhub consumergroups for the operationsMonitoringEvents eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="e541a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e541a-112">PARAMETERS</span></span>

### <span data-ttu-id="e541a-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="e541a-113">-EventHubEndpointName</span></span>
<span data-ttu-id="e541a-114">Az esemény központi végpontjának neve.</span><span class="sxs-lookup"><span data-stu-id="e541a-114">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="e541a-115">Események lehetséges értékei, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="e541a-115">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="e541a-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e541a-116">-Name</span></span>
<span data-ttu-id="e541a-117">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="e541a-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="e541a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e541a-118">-ResourceGroupName</span></span>
<span data-ttu-id="e541a-119">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e541a-119">Resource Group Name</span></span>

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

### <span data-ttu-id="e541a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e541a-120">-DefaultProfile</span></span>
<span data-ttu-id="e541a-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e541a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e541a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e541a-122">CommonParameters</span></span>
<span data-ttu-id="e541a-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e541a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e541a-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e541a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e541a-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e541a-125">INPUTS</span></span>

### <span data-ttu-id="e541a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e541a-126">System.String</span></span>

## <span data-ttu-id="e541a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e541a-127">OUTPUTS</span></span>

### <span data-ttu-id="e541a-128">System. Collections. Generic. IEnumerable ' 1 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e541a-128">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e541a-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e541a-129">NOTES</span></span>

## <span data-ttu-id="e541a-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e541a-130">RELATED LINKS</span></span>

