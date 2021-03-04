---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 23f6c4b7d40f0ec2e02541f82d5d517019bd15fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942514"
---
# <span data-ttu-id="ea4d7-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ea4d7-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="ea4d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea4d7-102">SYNOPSIS</span></span>
<span data-ttu-id="ea4d7-103">Létrehoz egy eventhub fogyasztói csoportot.</span><span class="sxs-lookup"><span data-stu-id="ea4d7-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="ea4d7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ea4d7-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea4d7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ea4d7-105">DESCRIPTION</span></span>
<span data-ttu-id="ea4d7-106">Létrehoz egy fogyasztói csoportot a megadott IotHubbal társított Eventhubban.</span><span class="sxs-lookup"><span data-stu-id="ea4d7-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="ea4d7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ea4d7-107">EXAMPLES</span></span>

### <span data-ttu-id="ea4d7-108">1. példa: Fogyasztói csoport hozzáadása a telemetriai eventhubhoz</span><span class="sxs-lookup"><span data-stu-id="ea4d7-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="ea4d7-109">Hozzáad egy "myconsumergroup" nevű új fogyasztói csoportot az eventhubhoz telemetriai eseményekhez a "myiothub" nevű iothubban</span><span class="sxs-lookup"><span data-stu-id="ea4d7-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="ea4d7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea4d7-110">PARAMETERS</span></span>

### <span data-ttu-id="ea4d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea4d7-111">-DefaultProfile</span></span>
<span data-ttu-id="ea4d7-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ea4d7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea4d7-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="ea4d7-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="ea4d7-114">A felvenni kívánt EventHub ConsumerGroup neve.</span><span class="sxs-lookup"><span data-stu-id="ea4d7-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="ea4d7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ea4d7-115">-Name</span></span>
<span data-ttu-id="ea4d7-116">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="ea4d7-116">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ea4d7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea4d7-117">-ResourceGroupName</span></span>
<span data-ttu-id="ea4d7-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ea4d7-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="ea4d7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea4d7-119">-Confirm</span></span>
<span data-ttu-id="ea4d7-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ea4d7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea4d7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea4d7-121">-WhatIf</span></span>
<span data-ttu-id="ea4d7-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ea4d7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea4d7-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ea4d7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea4d7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea4d7-124">CommonParameters</span></span>
<span data-ttu-id="ea4d7-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea4d7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea4d7-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea4d7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea4d7-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea4d7-127">INPUTS</span></span>

### <span data-ttu-id="ea4d7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ea4d7-128">System.String</span></span>

## <span data-ttu-id="ea4d7-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea4d7-129">OUTPUTS</span></span>

### <span data-ttu-id="ea4d7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ea4d7-130">System.String</span></span>

## <span data-ttu-id="ea4d7-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ea4d7-131">NOTES</span></span>

## <span data-ttu-id="ea4d7-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea4d7-132">RELATED LINKS</span></span>
