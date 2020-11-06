---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
ms.openlocfilehash: 31ed4d8765599fcc99f58870b347a14cdaf00162
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499511"
---
# <span data-ttu-id="89f2c-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="89f2c-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="89f2c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89f2c-102">SYNOPSIS</span></span>
<span data-ttu-id="89f2c-103">Eltávolítja a megadott esemény hub-ot.</span><span class="sxs-lookup"><span data-stu-id="89f2c-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89f2c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89f2c-104">SYNTAX</span></span>

### <span data-ttu-id="89f2c-105">EventhubDefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="89f2c-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89f2c-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="89f2c-106">EventhubInputObjectSet</span></span>
```
Remove-AzureRmEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89f2c-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89f2c-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89f2c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="89f2c-108">DESCRIPTION</span></span>
<span data-ttu-id="89f2c-109">A Remove-AzureRmEventHub parancsmag eltávolítja és törli a megadott névtérből a megadott esemény középpontját.</span><span class="sxs-lookup"><span data-stu-id="89f2c-109">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="89f2c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="89f2c-110">EXAMPLES</span></span>

### <span data-ttu-id="89f2c-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="89f2c-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="89f2c-112">Eltávolítja az esemény-hub \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="89f2c-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="89f2c-113">Példa 2,1-InputObject – változó használata:</span><span class="sxs-lookup"><span data-stu-id="89f2c-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmEventHub <params>
PS C:\> Remove-AzureRmEventHub -InputObject $inputobject
```

### <span data-ttu-id="89f2c-114">Példa 2,2-InputObject csővezetékek használatával:</span><span class="sxs-lookup"><span data-stu-id="89f2c-114">Example 2.2 - InputObject Using Piping:</span></span>
```
PS C:\> Get-AzureRmEventHub <params> | Remove-AzureRmEventHub
```

### <span data-ttu-id="89f2c-115">Példa 3,1-ResourceId – változó használata:</span><span class="sxs-lookup"><span data-stu-id="89f2c-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHub <params>
PS C:\> Remove-AzureRmEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="89f2c-116">Példa 3,1-ResourceId-karakterlánc használatával:</span><span class="sxs-lookup"><span data-stu-id="89f2c-116">Example 3.1 - ResourceId - Using string:</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="89f2c-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89f2c-117">PARAMETERS</span></span>

### <span data-ttu-id="89f2c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89f2c-118">-AsJob</span></span>
<span data-ttu-id="89f2c-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="89f2c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89f2c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89f2c-120">-DefaultProfile</span></span>
<span data-ttu-id="89f2c-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89f2c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89f2c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89f2c-122">-InputObject</span></span>
<span data-ttu-id="89f2c-123">Eventhub objektum</span><span class="sxs-lookup"><span data-stu-id="89f2c-123">Eventhub Object</span></span>

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

### <span data-ttu-id="89f2c-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="89f2c-124">-Name</span></span>
<span data-ttu-id="89f2c-125">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="89f2c-125">EventHub Name</span></span>

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

### <span data-ttu-id="89f2c-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="89f2c-126">-Namespace</span></span>
<span data-ttu-id="89f2c-127">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="89f2c-127">Namespace Name</span></span>

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

### <span data-ttu-id="89f2c-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89f2c-128">-PassThru</span></span>
<span data-ttu-id="89f2c-129">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="89f2c-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="89f2c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89f2c-130">-ResourceGroupName</span></span>
<span data-ttu-id="89f2c-131">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="89f2c-131">Resource Group Name</span></span>

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

### <span data-ttu-id="89f2c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89f2c-132">-ResourceId</span></span>
<span data-ttu-id="89f2c-133">Eventhub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="89f2c-133">Eventhub Resource Id</span></span>

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

### <span data-ttu-id="89f2c-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="89f2c-134">-Confirm</span></span>
<span data-ttu-id="89f2c-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="89f2c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89f2c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89f2c-136">-WhatIf</span></span>
<span data-ttu-id="89f2c-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="89f2c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89f2c-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89f2c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89f2c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f2c-139">CommonParameters</span></span>
<span data-ttu-id="89f2c-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89f2c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f2c-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89f2c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f2c-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89f2c-142">INPUTS</span></span>

### <span data-ttu-id="89f2c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="89f2c-143">System.String</span></span>

### <span data-ttu-id="89f2c-144">Microsoft. Azure. Command. EventHub. models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="89f2c-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>
<span data-ttu-id="89f2c-145">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="89f2c-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="89f2c-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89f2c-146">OUTPUTS</span></span>

### <span data-ttu-id="89f2c-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89f2c-147">System.Boolean</span></span>

## <span data-ttu-id="89f2c-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89f2c-148">NOTES</span></span>

## <span data-ttu-id="89f2c-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89f2c-149">RELATED LINKS</span></span>
