---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: b326f7228a60f7549fc6dcd227b9bad947f22add
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504131"
---
# <span data-ttu-id="c5db9-101">Remove-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="c5db9-101">Remove-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="c5db9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c5db9-102">SYNOPSIS</span></span>
<span data-ttu-id="c5db9-103">Töröl egy eventhub-consumergroup.</span><span class="sxs-lookup"><span data-stu-id="c5db9-103">Deletes an eventhub consumergroup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5db9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c5db9-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5db9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c5db9-105">DESCRIPTION</span></span>
<span data-ttu-id="c5db9-106">Töröl egy eventhub-consumergroup.</span><span class="sxs-lookup"><span data-stu-id="c5db9-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="c5db9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c5db9-107">EXAMPLES</span></span>

### <span data-ttu-id="c5db9-108">Példa 1 a eventhub consumergroup eltávolítása a telemetriai eventhub</span><span class="sxs-lookup"><span data-stu-id="c5db9-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="c5db9-109">Eltávolítja a myconsumergroup nevű consumergroup a "myiothub" nevű IotHub.</span><span class="sxs-lookup"><span data-stu-id="c5db9-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="c5db9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c5db9-110">PARAMETERS</span></span>

### <span data-ttu-id="c5db9-111">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="c5db9-111">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="c5db9-112">EventHub ConsumerGroup név.</span><span class="sxs-lookup"><span data-stu-id="c5db9-112">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5db9-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="c5db9-113">-EventHubEndpointName</span></span>
<span data-ttu-id="c5db9-114">EventHub végpont neve.</span><span class="sxs-lookup"><span data-stu-id="c5db9-114">EventHub Endpoint Name.</span></span>
<span data-ttu-id="c5db9-115">Események lehetséges értékei, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="c5db9-115">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5db9-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c5db9-116">-Name</span></span>
<span data-ttu-id="c5db9-117">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="c5db9-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="c5db9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5db9-118">-ResourceGroupName</span></span>
<span data-ttu-id="c5db9-119">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="c5db9-119">Resource Group Name</span></span>

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

### <span data-ttu-id="c5db9-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c5db9-120">-Confirm</span></span>
<span data-ttu-id="c5db9-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c5db9-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5db9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5db9-122">-WhatIf</span></span>
<span data-ttu-id="c5db9-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c5db9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5db9-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5db9-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5db9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5db9-125">-DefaultProfile</span></span>
<span data-ttu-id="c5db9-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5db9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5db9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5db9-127">CommonParameters</span></span>
<span data-ttu-id="c5db9-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c5db9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5db9-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5db9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5db9-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5db9-130">INPUTS</span></span>

### <span data-ttu-id="c5db9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c5db9-131">System.String</span></span>

## <span data-ttu-id="c5db9-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5db9-132">OUTPUTS</span></span>

### <span data-ttu-id="c5db9-133">System. Collections. Generic. IEnumerable ' 1 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c5db9-133">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="c5db9-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c5db9-134">NOTES</span></span>

## <span data-ttu-id="c5db9-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5db9-135">RELATED LINKS</span></span>

