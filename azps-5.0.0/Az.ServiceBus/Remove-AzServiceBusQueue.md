---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
ms.openlocfilehash: c93f0d8a44a67195d2c901dd581505276b7ae2f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296756"
---
# <span data-ttu-id="c1af9-101">Remove-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="c1af9-101">Remove-AzServiceBusQueue</span></span>

## <span data-ttu-id="c1af9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1af9-102">SYNOPSIS</span></span>
<span data-ttu-id="c1af9-103">Eltávolítja a várólistát a megadott szolgáltatási busz névteréről.</span><span class="sxs-lookup"><span data-stu-id="c1af9-103">Removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="c1af9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1af9-104">SYNTAX</span></span>

### <span data-ttu-id="c1af9-105">QueuePropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1af9-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1af9-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c1af9-106">QueueInputObjectSet</span></span>
```
Remove-AzServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1af9-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c1af9-107">QueueResourceIdSet</span></span>
```
Remove-AzServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1af9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1af9-108">DESCRIPTION</span></span>
<span data-ttu-id="c1af9-109">A **Remove-AzServiceBusQueue** parancsmag eltávolítja a várólistát a megadott szolgáltatási busz névteréről.</span><span class="sxs-lookup"><span data-stu-id="c1af9-109">The **Remove-AzServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="c1af9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c1af9-110">EXAMPLES</span></span>

### <span data-ttu-id="c1af9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c1af9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="c1af9-112">Eltávolítja a szolgáltatás Buszjának várólistáját `SB-Queue_exampl1` a névtérből `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="c1af9-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="c1af9-113">2. példa: InputObject-változó használata:</span><span class="sxs-lookup"><span data-stu-id="c1af9-113">Example 2: InputObject - Using variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="c1af9-114">A $inputobject for-InputObject paraméterben megadott szolgáltatási busz várólistájának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c1af9-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="c1af9-115">3. példa: InputObject csövek használata:</span><span class="sxs-lookup"><span data-stu-id="c1af9-115">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>  Get-AzServiceBusQueue <params> | Remove-AzServiceBusQueue
```

### <span data-ttu-id="c1af9-116">Példa 4: ResourceId – változó használata:</span><span class="sxs-lookup"><span data-stu-id="c1af9-116">Example 4: ResourceId - Using variable:</span></span>
```powershell
PS c:\> $resourceid = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="c1af9-117">A $resourceid/string for-ResourceId paraméterben megadott ARM azonosítóban megadott szolgáltatási busz várólistájának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c1af9-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="c1af9-118">Példa 5: ResourceId – átadás karakterláncként:</span><span class="sxs-lookup"><span data-stu-id="c1af9-118">Example 5: ResourceId - passing as string:</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="c1af9-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1af9-119">PARAMETERS</span></span>

### <span data-ttu-id="c1af9-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1af9-120">-AsJob</span></span>
<span data-ttu-id="c1af9-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c1af9-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c1af9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1af9-122">-DefaultProfile</span></span>
<span data-ttu-id="c1af9-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1af9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1af9-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1af9-124">-InputObject</span></span>
<span data-ttu-id="c1af9-125">A Service Bus Queue objektum</span><span class="sxs-lookup"><span data-stu-id="c1af9-125">Service Bus Queue Object</span></span>

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

### <span data-ttu-id="c1af9-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c1af9-126">-Name</span></span>
<span data-ttu-id="c1af9-127">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="c1af9-127">Queue Name</span></span>

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

### <span data-ttu-id="c1af9-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c1af9-128">-Namespace</span></span>
<span data-ttu-id="c1af9-129">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="c1af9-129">Namespace Name</span></span>

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

### <span data-ttu-id="c1af9-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1af9-130">-PassThru</span></span>
<span data-ttu-id="c1af9-131">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="c1af9-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c1af9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1af9-132">-ResourceGroupName</span></span>
<span data-ttu-id="c1af9-133">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c1af9-133">The name of the resource group</span></span>

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

### <span data-ttu-id="c1af9-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1af9-134">-ResourceId</span></span>
<span data-ttu-id="c1af9-135">A szolgáltatás busz-várólista erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="c1af9-135">Service Bus Queue Resource Id</span></span>

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

### <span data-ttu-id="c1af9-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c1af9-136">-Confirm</span></span>
<span data-ttu-id="c1af9-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c1af9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1af9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1af9-138">-WhatIf</span></span>
<span data-ttu-id="c1af9-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c1af9-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1af9-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c1af9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1af9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1af9-141">CommonParameters</span></span>
<span data-ttu-id="c1af9-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1af9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1af9-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1af9-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1af9-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1af9-144">INPUTS</span></span>

### <span data-ttu-id="c1af9-145">System. String</span><span class="sxs-lookup"><span data-stu-id="c1af9-145">System.String</span></span>

### <span data-ttu-id="c1af9-146">Microsoft. Azure. Command. ServiceBus. models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="c1af9-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="c1af9-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1af9-147">OUTPUTS</span></span>

### <span data-ttu-id="c1af9-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c1af9-148">System.Boolean</span></span>

## <span data-ttu-id="c1af9-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1af9-149">NOTES</span></span>

## <span data-ttu-id="c1af9-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1af9-150">RELATED LINKS</span></span>
