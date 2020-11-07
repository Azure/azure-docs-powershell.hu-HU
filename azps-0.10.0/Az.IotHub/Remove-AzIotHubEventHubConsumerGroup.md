---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: e2b6bb4c58be90b205fc4a50ddab9c84c0d1ee20
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842205"
---
# <span data-ttu-id="5c0b5-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5c0b5-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="5c0b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5c0b5-102">SYNOPSIS</span></span>
<span data-ttu-id="5c0b5-103">Töröl egy eventhub-consumergroup.</span><span class="sxs-lookup"><span data-stu-id="5c0b5-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="5c0b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5c0b5-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c0b5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5c0b5-105">DESCRIPTION</span></span>
<span data-ttu-id="5c0b5-106">Töröl egy eventhub-consumergroup.</span><span class="sxs-lookup"><span data-stu-id="5c0b5-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="5c0b5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5c0b5-107">EXAMPLES</span></span>

### <span data-ttu-id="5c0b5-108">Példa 1 a eventhub consumergroup eltávolítása a telemetriai eventhub</span><span class="sxs-lookup"><span data-stu-id="5c0b5-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="5c0b5-109">Eltávolítja a myconsumergroup nevű consumergroup a "myiothub" nevű IotHub.</span><span class="sxs-lookup"><span data-stu-id="5c0b5-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="5c0b5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5c0b5-110">PARAMETERS</span></span>

### <span data-ttu-id="5c0b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c0b5-111">-DefaultProfile</span></span>
<span data-ttu-id="5c0b5-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5c0b5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c0b5-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="5c0b5-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="5c0b5-114">EventHub ConsumerGroup név.</span><span class="sxs-lookup"><span data-stu-id="5c0b5-114">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="5c0b5-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5c0b5-115">-Name</span></span>
<span data-ttu-id="5c0b5-116">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="5c0b5-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="5c0b5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c0b5-117">-ResourceGroupName</span></span>
<span data-ttu-id="5c0b5-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="5c0b5-118">Resource Group Name</span></span>

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

### <span data-ttu-id="5c0b5-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5c0b5-119">-Confirm</span></span>
<span data-ttu-id="5c0b5-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5c0b5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c0b5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c0b5-121">-WhatIf</span></span>
<span data-ttu-id="5c0b5-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5c0b5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c0b5-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5c0b5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c0b5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c0b5-124">CommonParameters</span></span>
<span data-ttu-id="5c0b5-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5c0b5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c0b5-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c0b5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c0b5-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c0b5-127">INPUTS</span></span>

### <span data-ttu-id="5c0b5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5c0b5-128">System.String</span></span>

## <span data-ttu-id="5c0b5-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c0b5-129">OUTPUTS</span></span>

### <span data-ttu-id="5c0b5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5c0b5-130">System.String</span></span>

## <span data-ttu-id="5c0b5-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5c0b5-131">NOTES</span></span>

## <span data-ttu-id="5c0b5-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c0b5-132">RELATED LINKS</span></span>
