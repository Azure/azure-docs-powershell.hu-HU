---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
ms.openlocfilehash: 75da2231dae7ea0dc587d48ca832b7631fc24986
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479620"
---
# <span data-ttu-id="c06e6-101">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="c06e6-101">Remove-AzServiceBusTopic</span></span>

## <span data-ttu-id="c06e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c06e6-102">SYNOPSIS</span></span>
<span data-ttu-id="c06e6-103">Eltávolítja a témakört a szolgáltatásbusz megadott névterében.</span><span class="sxs-lookup"><span data-stu-id="c06e6-103">Removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="c06e6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c06e6-104">SYNTAX</span></span>

### <span data-ttu-id="c06e6-105">TopicPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c06e6-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c06e6-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c06e6-106">TopicInputObjectSet</span></span>
```
Remove-AzServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c06e6-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c06e6-107">TopicResourceIdSet</span></span>
```
Remove-AzServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c06e6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c06e6-108">DESCRIPTION</span></span>
<span data-ttu-id="c06e6-109">A **Remove-AzServiceBusTopic** parancsmag eltávolítja a témakört a megadott Service Bus névtérből.</span><span class="sxs-lookup"><span data-stu-id="c06e6-109">The **Remove-AzServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="c06e6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c06e6-110">EXAMPLES</span></span>

### <span data-ttu-id="c06e6-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c06e6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="c06e6-112">Eltávolítja a `SB-Topic_exampl1` témakört a névtérből. `SB-Example1`</span><span class="sxs-lookup"><span data-stu-id="c06e6-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="c06e6-113">2. példa: InputObject – Változó használata:</span><span class="sxs-lookup"><span data-stu-id="c06e6-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusTopic <parmas>
PS C:\> Remove-AzServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="c06e6-114">3. példa: InputObject – Piping használata:</span><span class="sxs-lookup"><span data-stu-id="c06e6-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusTopic <parmas> | Remove-AzServiceBusTopic
```

### <span data-ttu-id="c06e6-115">4. példa: Erőforrásazonosító változó használatával:</span><span class="sxs-lookup"><span data-stu-id="c06e6-115">Example 4: ResourceId Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusTopic <params>
PS C:\> Remove-AzServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="c06e6-116">5. példa: ResourceId using String value</span><span class="sxs-lookup"><span data-stu-id="c06e6-116">Example 5: ResourceId Using String value</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="c06e6-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c06e6-117">PARAMETERS</span></span>

### <span data-ttu-id="c06e6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c06e6-118">-AsJob</span></span>
<span data-ttu-id="c06e6-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c06e6-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c06e6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c06e6-120">-DefaultProfile</span></span>
<span data-ttu-id="c06e6-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c06e6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c06e6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c06e6-122">-InputObject</span></span>
<span data-ttu-id="c06e6-123">Service Bus Topic Object</span><span class="sxs-lookup"><span data-stu-id="c06e6-123">Service Bus Topic Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: TopicInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c06e6-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c06e6-124">-Name</span></span>
<span data-ttu-id="c06e6-125">Témakör neve</span><span class="sxs-lookup"><span data-stu-id="c06e6-125">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c06e6-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c06e6-126">-Namespace</span></span>
<span data-ttu-id="c06e6-127">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="c06e6-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c06e6-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c06e6-128">-PassThru</span></span>
<span data-ttu-id="c06e6-129">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="c06e6-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c06e6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c06e6-130">-ResourceGroupName</span></span>
<span data-ttu-id="c06e6-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c06e6-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c06e6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c06e6-132">-ResourceId</span></span>
<span data-ttu-id="c06e6-133">Service Bus Topic Resource Id</span><span class="sxs-lookup"><span data-stu-id="c06e6-133">Service Bus Topic Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: TopicResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c06e6-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c06e6-134">-Confirm</span></span>
<span data-ttu-id="c06e6-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c06e6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c06e6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c06e6-136">-WhatIf</span></span>
<span data-ttu-id="c06e6-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c06e6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c06e6-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c06e6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c06e6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c06e6-139">CommonParameters</span></span>
<span data-ttu-id="c06e6-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c06e6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c06e6-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c06e6-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c06e6-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c06e6-142">INPUTS</span></span>

### <span data-ttu-id="c06e6-143">System.String</span><span class="sxs-lookup"><span data-stu-id="c06e6-143">System.String</span></span>

### <span data-ttu-id="c06e6-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="c06e6-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="c06e6-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c06e6-145">OUTPUTS</span></span>

### <span data-ttu-id="c06e6-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c06e6-146">System.Boolean</span></span>

## <span data-ttu-id="c06e6-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c06e6-147">NOTES</span></span>

## <span data-ttu-id="c06e6-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c06e6-148">RELATED LINKS</span></span>
