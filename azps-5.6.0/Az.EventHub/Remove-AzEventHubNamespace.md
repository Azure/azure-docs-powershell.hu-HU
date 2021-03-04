---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: dca9094ac66e889b5a00899f6d48d6317279c1fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920577"
---
# <span data-ttu-id="5aaab-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="5aaab-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="5aaab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5aaab-102">SYNOPSIS</span></span>
<span data-ttu-id="5aaab-103">Eltávolítja az Eseményközpontok megadott névterét.</span><span class="sxs-lookup"><span data-stu-id="5aaab-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="5aaab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5aaab-104">SYNTAX</span></span>

### <span data-ttu-id="5aaab-105">NamespaceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5aaab-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5aaab-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5aaab-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5aaab-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5aaab-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5aaab-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5aaab-108">DESCRIPTION</span></span>
<span data-ttu-id="5aaab-109">A Remove-AzEventHubNamespace parancsmag eltávolítja és törli a megadott Event Hubs névteret.</span><span class="sxs-lookup"><span data-stu-id="5aaab-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="5aaab-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5aaab-110">EXAMPLES</span></span>

### <span data-ttu-id="5aaab-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="5aaab-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="5aaab-112">Eltávolítja a MyResourceGroupName erőforráscsoport Eseményközpontok névterét, a \` \` \` MyNamespaceName nevű \` erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="5aaab-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5aaab-113">2. példa: InputObject – Változó használata:</span><span class="sxs-lookup"><span data-stu-id="5aaab-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="5aaab-114">3. példa: InputObject – Piping használata:</span><span class="sxs-lookup"><span data-stu-id="5aaab-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="5aaab-115">4. példa: ResourceId – Változó használata</span><span class="sxs-lookup"><span data-stu-id="5aaab-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="5aaab-116">5. példa: ResourceId – Piping használata:</span><span class="sxs-lookup"><span data-stu-id="5aaab-116">Example 5: ResourceId - Using Piping:</span></span>
```powershell
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="5aaab-117">6. példa: ResourceId – Karakterlánc használata:</span><span class="sxs-lookup"><span data-stu-id="5aaab-117">Example 6: ResourceId - Using String:</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="5aaab-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5aaab-118">PARAMETERS</span></span>

### <span data-ttu-id="5aaab-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5aaab-119">-AsJob</span></span>
<span data-ttu-id="5aaab-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5aaab-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5aaab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aaab-121">-DefaultProfile</span></span>
<span data-ttu-id="5aaab-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5aaab-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5aaab-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5aaab-123">-InputObject</span></span>
<span data-ttu-id="5aaab-124">EventHubs Namespace Objektum</span><span class="sxs-lookup"><span data-stu-id="5aaab-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="5aaab-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5aaab-125">-Name</span></span>
<span data-ttu-id="5aaab-126">EventHub Namespace Name</span><span class="sxs-lookup"><span data-stu-id="5aaab-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="5aaab-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5aaab-127">-PassThru</span></span>
<span data-ttu-id="5aaab-128">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="5aaab-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="5aaab-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aaab-129">-ResourceGroupName</span></span>
<span data-ttu-id="5aaab-130">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5aaab-130">Resource Group Name</span></span>

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

### <span data-ttu-id="5aaab-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5aaab-131">-ResourceId</span></span>
<span data-ttu-id="5aaab-132">EventHubs Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="5aaab-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="5aaab-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5aaab-133">-Confirm</span></span>
<span data-ttu-id="5aaab-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5aaab-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5aaab-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aaab-135">-WhatIf</span></span>
<span data-ttu-id="5aaab-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5aaab-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5aaab-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5aaab-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5aaab-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aaab-138">CommonParameters</span></span>
<span data-ttu-id="5aaab-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5aaab-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aaab-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5aaab-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aaab-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5aaab-141">INPUTS</span></span>

### <span data-ttu-id="5aaab-142">System.String</span><span class="sxs-lookup"><span data-stu-id="5aaab-142">System.String</span></span>

### <span data-ttu-id="5aaab-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="5aaab-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="5aaab-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5aaab-144">OUTPUTS</span></span>

### <span data-ttu-id="5aaab-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="5aaab-145">System.Void</span></span>

## <span data-ttu-id="5aaab-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5aaab-146">NOTES</span></span>

## <span data-ttu-id="5aaab-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5aaab-147">RELATED LINKS</span></span>
