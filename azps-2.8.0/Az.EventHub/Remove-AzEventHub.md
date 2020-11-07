---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: 1e53e1a1eb1070a9f13c9e67ea4a838358012a13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666471"
---
# <span data-ttu-id="b34b6-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="b34b6-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="b34b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b34b6-102">SYNOPSIS</span></span>
<span data-ttu-id="b34b6-103">Eltávolítja a megadott esemény hub-ot.</span><span class="sxs-lookup"><span data-stu-id="b34b6-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="b34b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b34b6-104">SYNTAX</span></span>

### <span data-ttu-id="b34b6-105">EventhubDefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b34b6-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b34b6-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b34b6-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b34b6-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b34b6-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b34b6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b34b6-108">DESCRIPTION</span></span>
<span data-ttu-id="b34b6-109">A Remove-AzEventHub parancsmag eltávolítja és törli a megadott névtérből a megadott esemény középpontját.</span><span class="sxs-lookup"><span data-stu-id="b34b6-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="b34b6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b34b6-110">EXAMPLES</span></span>

### <span data-ttu-id="b34b6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b34b6-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="b34b6-112">Eltávolítja az esemény-hub \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="b34b6-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="b34b6-113">Példa 2,1-InputObject – változó használata:</span><span class="sxs-lookup"><span data-stu-id="b34b6-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="b34b6-114">Példa 2,2-InputObject csővezetékek használatával:</span><span class="sxs-lookup"><span data-stu-id="b34b6-114">Example 2.2 - InputObject Using Piping:</span></span>
```
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="b34b6-115">Példa 3,1-ResourceId – változó használata:</span><span class="sxs-lookup"><span data-stu-id="b34b6-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="b34b6-116">Példa 3,1-ResourceId-karakterlánc használatával:</span><span class="sxs-lookup"><span data-stu-id="b34b6-116">Example 3.1 - ResourceId - Using string:</span></span>
```
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="b34b6-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b34b6-117">PARAMETERS</span></span>

### <span data-ttu-id="b34b6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b34b6-118">-AsJob</span></span>
<span data-ttu-id="b34b6-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b34b6-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b34b6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b34b6-120">-DefaultProfile</span></span>
<span data-ttu-id="b34b6-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b34b6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b34b6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b34b6-122">-InputObject</span></span>
<span data-ttu-id="b34b6-123">Eventhub objektum</span><span class="sxs-lookup"><span data-stu-id="b34b6-123">Eventhub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b34b6-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b34b6-124">-Name</span></span>
<span data-ttu-id="b34b6-125">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="b34b6-125">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b34b6-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b34b6-126">-Namespace</span></span>
<span data-ttu-id="b34b6-127">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="b34b6-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b34b6-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b34b6-128">-PassThru</span></span>
<span data-ttu-id="b34b6-129">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="b34b6-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="b34b6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b34b6-130">-ResourceGroupName</span></span>
<span data-ttu-id="b34b6-131">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="b34b6-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b34b6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b34b6-132">-ResourceId</span></span>
<span data-ttu-id="b34b6-133">Eventhub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="b34b6-133">Eventhub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b34b6-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b34b6-134">-Confirm</span></span>
<span data-ttu-id="b34b6-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b34b6-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b34b6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b34b6-136">-WhatIf</span></span>
<span data-ttu-id="b34b6-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b34b6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b34b6-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b34b6-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b34b6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b34b6-139">CommonParameters</span></span>
<span data-ttu-id="b34b6-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b34b6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b34b6-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b34b6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b34b6-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b34b6-142">INPUTS</span></span>

### <span data-ttu-id="b34b6-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b34b6-143">System.String</span></span>

### <span data-ttu-id="b34b6-144">Microsoft. Azure. Command. EventHub. models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="b34b6-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="b34b6-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b34b6-145">OUTPUTS</span></span>

### <span data-ttu-id="b34b6-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b34b6-146">System.Boolean</span></span>

## <span data-ttu-id="b34b6-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b34b6-147">NOTES</span></span>

## <span data-ttu-id="b34b6-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b34b6-148">RELATED LINKS</span></span>
