---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
ms.openlocfilehash: c93f0d8a44a67195d2c901dd581505276b7ae2f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168859"
---
# <span data-ttu-id="e29d3-101">Remove-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="e29d3-101">Remove-AzServiceBusQueue</span></span>

## <span data-ttu-id="e29d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e29d3-102">SYNOPSIS</span></span>
<span data-ttu-id="e29d3-103">Eltávolítja a várólistát a szolgáltatásbusz megadott névterében.</span><span class="sxs-lookup"><span data-stu-id="e29d3-103">Removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e29d3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e29d3-104">SYNTAX</span></span>

### <span data-ttu-id="e29d3-105">QueuePropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e29d3-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e29d3-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e29d3-106">QueueInputObjectSet</span></span>
```
Remove-AzServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e29d3-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e29d3-107">QueueResourceIdSet</span></span>
```
Remove-AzServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e29d3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e29d3-108">DESCRIPTION</span></span>
<span data-ttu-id="e29d3-109">A **Remove-AzServiceBusQueue** parancsmag eltávolítja a várólistát a szolgáltatásbusz megadott névterében.</span><span class="sxs-lookup"><span data-stu-id="e29d3-109">The **Remove-AzServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e29d3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e29d3-110">EXAMPLES</span></span>

### <span data-ttu-id="e29d3-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e29d3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="e29d3-112">Eltávolítja a Service Bus `SB-Queue_exampl1` várólistát a névtérből. `SB-Example1`</span><span class="sxs-lookup"><span data-stu-id="e29d3-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="e29d3-113">2. példa: InputObject – Változó használata:</span><span class="sxs-lookup"><span data-stu-id="e29d3-113">Example 2: InputObject - Using variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="e29d3-114">Az -InputObject paraméterhez megadott $inputobject eltávolítja a Service Bus várólistát.</span><span class="sxs-lookup"><span data-stu-id="e29d3-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="e29d3-115">3. példa: InputObject – Piping használata:</span><span class="sxs-lookup"><span data-stu-id="e29d3-115">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>  Get-AzServiceBusQueue <params> | Remove-AzServiceBusQueue
```

### <span data-ttu-id="e29d3-116">4. példa: ResourceId – Változó használata:</span><span class="sxs-lookup"><span data-stu-id="e29d3-116">Example 4: ResourceId - Using variable:</span></span>
```powershell
PS c:\> $resourceid = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="e29d3-117">Eltávolítja a service bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span><span class="sxs-lookup"><span data-stu-id="e29d3-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="e29d3-118">5. példa: ResourceId – karakterláncként halad:</span><span class="sxs-lookup"><span data-stu-id="e29d3-118">Example 5: ResourceId - passing as string:</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="e29d3-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e29d3-119">PARAMETERS</span></span>

### <span data-ttu-id="e29d3-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e29d3-120">-AsJob</span></span>
<span data-ttu-id="e29d3-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e29d3-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e29d3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e29d3-122">-DefaultProfile</span></span>
<span data-ttu-id="e29d3-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e29d3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e29d3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e29d3-124">-InputObject</span></span>
<span data-ttu-id="e29d3-125">Service Bus Queue Object</span><span class="sxs-lookup"><span data-stu-id="e29d3-125">Service Bus Queue Object</span></span>

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

### <span data-ttu-id="e29d3-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e29d3-126">-Name</span></span>
<span data-ttu-id="e29d3-127">Várólistán lévő név</span><span class="sxs-lookup"><span data-stu-id="e29d3-127">Queue Name</span></span>

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

### <span data-ttu-id="e29d3-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e29d3-128">-Namespace</span></span>
<span data-ttu-id="e29d3-129">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="e29d3-129">Namespace Name</span></span>

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

### <span data-ttu-id="e29d3-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e29d3-130">-PassThru</span></span>
<span data-ttu-id="e29d3-131">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="e29d3-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="e29d3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e29d3-132">-ResourceGroupName</span></span>
<span data-ttu-id="e29d3-133">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e29d3-133">The name of the resource group</span></span>

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

### <span data-ttu-id="e29d3-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e29d3-134">-ResourceId</span></span>
<span data-ttu-id="e29d3-135">Service Bus Queue Resource Id</span><span class="sxs-lookup"><span data-stu-id="e29d3-135">Service Bus Queue Resource Id</span></span>

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

### <span data-ttu-id="e29d3-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e29d3-136">-Confirm</span></span>
<span data-ttu-id="e29d3-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e29d3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e29d3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e29d3-138">-WhatIf</span></span>
<span data-ttu-id="e29d3-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e29d3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e29d3-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e29d3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e29d3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e29d3-141">CommonParameters</span></span>
<span data-ttu-id="e29d3-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e29d3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e29d3-143">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e29d3-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e29d3-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e29d3-144">INPUTS</span></span>

### <span data-ttu-id="e29d3-145">System.String</span><span class="sxs-lookup"><span data-stu-id="e29d3-145">System.String</span></span>

### <span data-ttu-id="e29d3-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="e29d3-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="e29d3-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e29d3-147">OUTPUTS</span></span>

### <span data-ttu-id="e29d3-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e29d3-148">System.Boolean</span></span>

## <span data-ttu-id="e29d3-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e29d3-149">NOTES</span></span>

## <span data-ttu-id="e29d3-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e29d3-150">RELATED LINKS</span></span>
