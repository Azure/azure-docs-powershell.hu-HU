---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 29f2b961637a398470f6455d0d2330ce5fd863a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469846"
---
# <span data-ttu-id="41dda-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="41dda-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="41dda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41dda-102">SYNOPSIS</span></span>
<span data-ttu-id="41dda-103">Eltávolítja az Eseményközpontok megadott névterét.</span><span class="sxs-lookup"><span data-stu-id="41dda-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="41dda-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="41dda-104">SYNTAX</span></span>

### <span data-ttu-id="41dda-105">NamespaceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="41dda-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41dda-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="41dda-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41dda-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41dda-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41dda-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="41dda-108">DESCRIPTION</span></span>
<span data-ttu-id="41dda-109">A Remove-AzEventHubNamespace parancsmag eltávolítja és törli a megadott Event Hubs névteret.</span><span class="sxs-lookup"><span data-stu-id="41dda-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="41dda-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="41dda-110">EXAMPLES</span></span>

### <span data-ttu-id="41dda-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="41dda-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="41dda-112">Eltávolítja a MyResourceGroupName erőforráscsoport Eseményközpontok névterét, a \` \` \` MyNamespaceName nevű \` erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="41dda-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="41dda-113">2. példa: InputObject – Változó használata:</span><span class="sxs-lookup"><span data-stu-id="41dda-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="41dda-114">3. példa: InputObject – Piping használata:</span><span class="sxs-lookup"><span data-stu-id="41dda-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="41dda-115">4. példa: ResourceId – Változó használata</span><span class="sxs-lookup"><span data-stu-id="41dda-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="41dda-116">5. példa: ResourceId – Piping használata:</span><span class="sxs-lookup"><span data-stu-id="41dda-116">Example 5: ResourceId - Using Piping:</span></span>
```powershell
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="41dda-117">6. példa: ResourceId – Karakterlánc használata:</span><span class="sxs-lookup"><span data-stu-id="41dda-117">Example 6: ResourceId - Using String:</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="41dda-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41dda-118">PARAMETERS</span></span>

### <span data-ttu-id="41dda-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41dda-119">-AsJob</span></span>
<span data-ttu-id="41dda-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="41dda-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41dda-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41dda-121">-DefaultProfile</span></span>
<span data-ttu-id="41dda-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41dda-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41dda-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41dda-123">-InputObject</span></span>
<span data-ttu-id="41dda-124">EventHubs Namespace Objektum</span><span class="sxs-lookup"><span data-stu-id="41dda-124">EventHubs Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41dda-125">-Name</span><span class="sxs-lookup"><span data-stu-id="41dda-125">-Name</span></span>
<span data-ttu-id="41dda-126">EventHub Namespace Name</span><span class="sxs-lookup"><span data-stu-id="41dda-126">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41dda-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41dda-127">-PassThru</span></span>
<span data-ttu-id="41dda-128">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="41dda-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="41dda-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41dda-129">-ResourceGroupName</span></span>
<span data-ttu-id="41dda-130">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="41dda-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41dda-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41dda-131">-ResourceId</span></span>
<span data-ttu-id="41dda-132">EventHubs Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="41dda-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="41dda-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41dda-133">-Confirm</span></span>
<span data-ttu-id="41dda-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="41dda-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41dda-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41dda-135">-WhatIf</span></span>
<span data-ttu-id="41dda-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="41dda-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41dda-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="41dda-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41dda-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41dda-138">CommonParameters</span></span>
<span data-ttu-id="41dda-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41dda-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41dda-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41dda-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41dda-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41dda-141">INPUTS</span></span>

### <span data-ttu-id="41dda-142">System.String</span><span class="sxs-lookup"><span data-stu-id="41dda-142">System.String</span></span>

### <span data-ttu-id="41dda-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="41dda-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="41dda-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41dda-144">OUTPUTS</span></span>

### <span data-ttu-id="41dda-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="41dda-145">System.Void</span></span>

## <span data-ttu-id="41dda-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="41dda-146">NOTES</span></span>

## <span data-ttu-id="41dda-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41dda-147">RELATED LINKS</span></span>
