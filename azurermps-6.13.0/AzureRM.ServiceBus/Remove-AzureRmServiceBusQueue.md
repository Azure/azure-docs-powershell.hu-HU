---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: ba59f19183cf49802240d7631b99b3e69a9bc6f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497328"
---
# <span data-ttu-id="eb244-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="eb244-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="eb244-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb244-102">SYNOPSIS</span></span>
<span data-ttu-id="eb244-103">Eltávolítja a várólistát a megadott szolgáltatási busz névteréről.</span><span class="sxs-lookup"><span data-stu-id="eb244-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb244-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb244-104">SYNTAX</span></span>

### <span data-ttu-id="eb244-105">QueuePropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eb244-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb244-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="eb244-106">QueueInputObjectSet</span></span>
```
Remove-AzureRmServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb244-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="eb244-107">QueueResourceIdSet</span></span>
```
Remove-AzureRmServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb244-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb244-108">DESCRIPTION</span></span>
<span data-ttu-id="eb244-109">A **Remove-AzureRmServiceBusQueue** parancsmag eltávolítja a várólistát a megadott szolgáltatási busz névteréről.</span><span class="sxs-lookup"><span data-stu-id="eb244-109">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="eb244-110">Példák</span><span class="sxs-lookup"><span data-stu-id="eb244-110">EXAMPLES</span></span>

### <span data-ttu-id="eb244-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eb244-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="eb244-112">Eltávolítja a szolgáltatás Buszjának várólistáját `SB-Queue_exampl1` a névtérből `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="eb244-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="eb244-113">Példa 2,1-InputObject – változó használata:</span><span class="sxs-lookup"><span data-stu-id="eb244-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusQueue <params>
PS C:\> Remove-AzureRmServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="eb244-114">A $inputobject for-InputObject paraméterben megadott szolgáltatási busz várólistájának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="eb244-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="eb244-115">Példa 2,1-InputObject:</span><span class="sxs-lookup"><span data-stu-id="eb244-115">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\>  Get-AzureRmServiceBusQueue <params> | Remove-AzureRmServiceBusQueue
```

### <span data-ttu-id="eb244-116">Példa 3,1-ResourceId – változó használata:</span><span class="sxs-lookup"><span data-stu-id="eb244-116">Example 3.1 - ResourceId - Using variable:</span></span>
```
PS c:\> $resourceid = Get-AzureRmServiceBusQueue <params>
PS C:\> Remove-AzureRmServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="eb244-117">A $resourceid/string for-ResourceId paraméterben megadott ARM azonosítóban megadott szolgáltatási busz várólistájának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="eb244-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="eb244-118">Példa: 3,2 – ResourceId – passign karakterláncként:</span><span class="sxs-lookup"><span data-stu-id="eb244-118">Example 3.2 - ResourceId - passign as string:</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="eb244-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb244-119">PARAMETERS</span></span>

### <span data-ttu-id="eb244-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb244-120">-AsJob</span></span>
<span data-ttu-id="eb244-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="eb244-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb244-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb244-122">-DefaultProfile</span></span>
<span data-ttu-id="eb244-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb244-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb244-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb244-124">-InputObject</span></span>
<span data-ttu-id="eb244-125">A Service Bus Queue objektum</span><span class="sxs-lookup"><span data-stu-id="eb244-125">Service Bus Queue Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes
Parameter Sets: QueueInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb244-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eb244-126">-Name</span></span>
<span data-ttu-id="eb244-127">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="eb244-127">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb244-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="eb244-128">-Namespace</span></span>
<span data-ttu-id="eb244-129">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="eb244-129">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb244-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb244-130">-PassThru</span></span>
<span data-ttu-id="eb244-131">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="eb244-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="eb244-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb244-132">-ResourceGroupName</span></span>
<span data-ttu-id="eb244-133">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="eb244-133">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb244-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb244-134">-ResourceId</span></span>
<span data-ttu-id="eb244-135">A szolgáltatás busz-várólista erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="eb244-135">Service Bus Queue Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: QueueResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb244-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eb244-136">-Confirm</span></span>
<span data-ttu-id="eb244-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eb244-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb244-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb244-138">-WhatIf</span></span>
<span data-ttu-id="eb244-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eb244-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb244-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eb244-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb244-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb244-141">CommonParameters</span></span>
<span data-ttu-id="eb244-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb244-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb244-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb244-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb244-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb244-144">INPUTS</span></span>

### <span data-ttu-id="eb244-145">System. String</span><span class="sxs-lookup"><span data-stu-id="eb244-145">System.String</span></span>

### <span data-ttu-id="eb244-146">Microsoft. Azure. Command. ServiceBus. models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="eb244-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>
<span data-ttu-id="eb244-147">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="eb244-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="eb244-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb244-148">OUTPUTS</span></span>

### <span data-ttu-id="eb244-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eb244-149">System.Boolean</span></span>

## <span data-ttu-id="eb244-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb244-150">NOTES</span></span>

## <span data-ttu-id="eb244-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb244-151">RELATED LINKS</span></span>
