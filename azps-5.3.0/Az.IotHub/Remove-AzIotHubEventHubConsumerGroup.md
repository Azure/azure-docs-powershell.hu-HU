---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 9fa0a9d85dc9c7b1a6cc56c3c329b1810cceaa18
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386692"
---
# <span data-ttu-id="9ffed-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="9ffed-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="9ffed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ffed-102">SYNOPSIS</span></span>
<span data-ttu-id="9ffed-103">Egy eventhub fogyasztói csoportot töröl.</span><span class="sxs-lookup"><span data-stu-id="9ffed-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="9ffed-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9ffed-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ffed-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9ffed-105">DESCRIPTION</span></span>
<span data-ttu-id="9ffed-106">Egy eventhub fogyasztói csoportot töröl.</span><span class="sxs-lookup"><span data-stu-id="9ffed-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="9ffed-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9ffed-107">EXAMPLES</span></span>

### <span data-ttu-id="9ffed-108">1. példa: Az eventhub fogyasztói csoport eltávolítása a telemetriai eventhubról</span><span class="sxs-lookup"><span data-stu-id="9ffed-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="9ffed-109">Eltávolítja a myconsumergroup nevű fogyasztói csoportot a myiothub nevű IotHubról</span><span class="sxs-lookup"><span data-stu-id="9ffed-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="9ffed-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ffed-110">PARAMETERS</span></span>

### <span data-ttu-id="9ffed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ffed-111">-DefaultProfile</span></span>
<span data-ttu-id="9ffed-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9ffed-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ffed-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="9ffed-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="9ffed-114">EventHub ConsumerGroup Name.</span><span class="sxs-lookup"><span data-stu-id="9ffed-114">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="9ffed-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9ffed-115">-Name</span></span>
<span data-ttu-id="9ffed-116">Az IotHub neve</span><span class="sxs-lookup"><span data-stu-id="9ffed-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="9ffed-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ffed-117">-ResourceGroupName</span></span>
<span data-ttu-id="9ffed-118">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="9ffed-118">Resource Group Name</span></span>

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

### <span data-ttu-id="9ffed-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ffed-119">-Confirm</span></span>
<span data-ttu-id="9ffed-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9ffed-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ffed-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ffed-121">-WhatIf</span></span>
<span data-ttu-id="9ffed-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9ffed-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ffed-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9ffed-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ffed-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ffed-124">CommonParameters</span></span>
<span data-ttu-id="9ffed-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ffed-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ffed-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ffed-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ffed-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ffed-127">INPUTS</span></span>

### <span data-ttu-id="9ffed-128">System.String</span><span class="sxs-lookup"><span data-stu-id="9ffed-128">System.String</span></span>

## <span data-ttu-id="9ffed-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ffed-129">OUTPUTS</span></span>

### <span data-ttu-id="9ffed-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9ffed-130">System.String</span></span>

## <span data-ttu-id="9ffed-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9ffed-131">NOTES</span></span>

## <span data-ttu-id="9ffed-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ffed-132">RELATED LINKS</span></span>
