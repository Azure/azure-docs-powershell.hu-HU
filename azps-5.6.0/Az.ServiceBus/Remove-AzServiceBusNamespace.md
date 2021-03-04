---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: 7f6a7225742356e0410d3cc49aef60e50e1954a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931666"
---
# <span data-ttu-id="f2e10-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="f2e10-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="f2e10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2e10-102">SYNOPSIS</span></span>
<span data-ttu-id="f2e10-103">Eltávolítja a névteret a megadott erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="f2e10-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="f2e10-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f2e10-104">SYNTAX</span></span>

### <span data-ttu-id="f2e10-105">NamespacePropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f2e10-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2e10-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f2e10-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2e10-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2e10-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2e10-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f2e10-108">DESCRIPTION</span></span>
<span data-ttu-id="f2e10-109">A **Remove-AzServiceBusNamespace** parancsmag eltávolítja a névteret a megadott erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="f2e10-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="f2e10-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f2e10-110">EXAMPLES</span></span>

### <span data-ttu-id="f2e10-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="f2e10-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="f2e10-112">Eltávolítja a Service Bus `SB-Example1` névterét a megadott erőforráscsoportból. `Default-ServiceBus-WestUS`</span><span class="sxs-lookup"><span data-stu-id="f2e10-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="f2e10-113">2.1. példa – InputObject – Változó használata:</span><span class="sxs-lookup"><span data-stu-id="f2e10-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="f2e10-114">Eltávolítja a szolgáltatásbusz névterét, amely a $inputobject.</span><span class="sxs-lookup"><span data-stu-id="f2e10-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="f2e10-115">2.2. példa – InputObject – Pipázás használata:</span><span class="sxs-lookup"><span data-stu-id="f2e10-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="f2e10-116">A Service Bus névterének eltávolítása a Piping használatával.</span><span class="sxs-lookup"><span data-stu-id="f2e10-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="f2e10-117">3. példa – ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2e10-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="f2e10-118">Eltávolítja a Service Bus névterét, amely az ARM -ResourceId paraméter $resourceid vagy a piping paraméterben megadott azonosítóból áll.</span><span class="sxs-lookup"><span data-stu-id="f2e10-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="f2e10-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2e10-119">PARAMETERS</span></span>

### <span data-ttu-id="f2e10-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2e10-120">-AsJob</span></span>
<span data-ttu-id="f2e10-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f2e10-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2e10-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2e10-122">-DefaultProfile</span></span>
<span data-ttu-id="f2e10-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2e10-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2e10-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2e10-124">-InputObject</span></span>
<span data-ttu-id="f2e10-125">Service Bus Namespace Object</span><span class="sxs-lookup"><span data-stu-id="f2e10-125">Service Bus Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2e10-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f2e10-126">-Name</span></span>
<span data-ttu-id="f2e10-127">Névtér neve.</span><span class="sxs-lookup"><span data-stu-id="f2e10-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2e10-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2e10-128">-PassThru</span></span>
<span data-ttu-id="f2e10-129">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="f2e10-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f2e10-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2e10-130">-ResourceGroupName</span></span>
<span data-ttu-id="f2e10-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f2e10-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2e10-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2e10-132">-ResourceId</span></span>
<span data-ttu-id="f2e10-133">Service Bus Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="f2e10-133">Service Bus Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2e10-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2e10-134">-Confirm</span></span>
<span data-ttu-id="f2e10-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f2e10-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2e10-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2e10-136">-WhatIf</span></span>
<span data-ttu-id="f2e10-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f2e10-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2e10-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f2e10-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2e10-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2e10-139">CommonParameters</span></span>
<span data-ttu-id="f2e10-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2e10-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2e10-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2e10-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2e10-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2e10-142">INPUTS</span></span>

### <span data-ttu-id="f2e10-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f2e10-143">System.String</span></span>

### <span data-ttu-id="f2e10-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f2e10-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="f2e10-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2e10-145">OUTPUTS</span></span>

### <span data-ttu-id="f2e10-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f2e10-146">System.Boolean</span></span>

## <span data-ttu-id="f2e10-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f2e10-147">NOTES</span></span>

## <span data-ttu-id="f2e10-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2e10-148">RELATED LINKS</span></span>
