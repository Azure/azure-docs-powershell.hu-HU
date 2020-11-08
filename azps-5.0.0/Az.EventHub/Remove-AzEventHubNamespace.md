---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 29f2b961637a398470f6455d0d2330ce5fd863a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187446"
---
# <span data-ttu-id="3fdbf-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="3fdbf-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="3fdbf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3fdbf-102">SYNOPSIS</span></span>
<span data-ttu-id="3fdbf-103">Eltávolítja a megadott esemény-hubok névteret.</span><span class="sxs-lookup"><span data-stu-id="3fdbf-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="3fdbf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3fdbf-104">SYNTAX</span></span>

### <span data-ttu-id="3fdbf-105">NamespaceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3fdbf-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fdbf-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3fdbf-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fdbf-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fdbf-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fdbf-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3fdbf-108">DESCRIPTION</span></span>
<span data-ttu-id="3fdbf-109">A Remove-AzEventHubNamespace parancsmag eltávolítja és törli a megadott esemény-hubok névteret.</span><span class="sxs-lookup"><span data-stu-id="3fdbf-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="3fdbf-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3fdbf-110">EXAMPLES</span></span>

### <span data-ttu-id="3fdbf-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3fdbf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="3fdbf-112">Eltávolítja az esemény-hubok \` névtér \` -MyNamespaceName az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="3fdbf-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3fdbf-113">2. példa: InputObject-változó használata:</span><span class="sxs-lookup"><span data-stu-id="3fdbf-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="3fdbf-114">3. példa: InputObject csövek használata:</span><span class="sxs-lookup"><span data-stu-id="3fdbf-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="3fdbf-115">Példa 4: ResourceId változó használata</span><span class="sxs-lookup"><span data-stu-id="3fdbf-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="3fdbf-116">Példa 5: ResourceId:</span><span class="sxs-lookup"><span data-stu-id="3fdbf-116">Example 5: ResourceId - Using Piping:</span></span>
```powershell
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="3fdbf-117">6. példa: ResourceId-karakterlánc használata:</span><span class="sxs-lookup"><span data-stu-id="3fdbf-117">Example 6: ResourceId - Using String:</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="3fdbf-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3fdbf-118">PARAMETERS</span></span>

### <span data-ttu-id="3fdbf-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fdbf-119">-AsJob</span></span>
<span data-ttu-id="3fdbf-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3fdbf-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3fdbf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fdbf-121">-DefaultProfile</span></span>
<span data-ttu-id="3fdbf-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3fdbf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fdbf-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fdbf-123">-InputObject</span></span>
<span data-ttu-id="3fdbf-124">EventHubs névtér-objektum</span><span class="sxs-lookup"><span data-stu-id="3fdbf-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="3fdbf-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3fdbf-125">-Name</span></span>
<span data-ttu-id="3fdbf-126">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="3fdbf-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="3fdbf-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fdbf-127">-PassThru</span></span>
<span data-ttu-id="3fdbf-128">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="3fdbf-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="3fdbf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fdbf-129">-ResourceGroupName</span></span>
<span data-ttu-id="3fdbf-130">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="3fdbf-130">Resource Group Name</span></span>

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

### <span data-ttu-id="3fdbf-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fdbf-131">-ResourceId</span></span>
<span data-ttu-id="3fdbf-132">EventHubs névtér-erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="3fdbf-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="3fdbf-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3fdbf-133">-Confirm</span></span>
<span data-ttu-id="3fdbf-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3fdbf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fdbf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fdbf-135">-WhatIf</span></span>
<span data-ttu-id="3fdbf-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3fdbf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fdbf-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3fdbf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fdbf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fdbf-138">CommonParameters</span></span>
<span data-ttu-id="3fdbf-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3fdbf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fdbf-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fdbf-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fdbf-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3fdbf-141">INPUTS</span></span>

### <span data-ttu-id="3fdbf-142">System. String</span><span class="sxs-lookup"><span data-stu-id="3fdbf-142">System.String</span></span>

### <span data-ttu-id="3fdbf-143">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="3fdbf-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="3fdbf-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3fdbf-144">OUTPUTS</span></span>

### <span data-ttu-id="3fdbf-145">System. Void</span><span class="sxs-lookup"><span data-stu-id="3fdbf-145">System.Void</span></span>

## <span data-ttu-id="3fdbf-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3fdbf-146">NOTES</span></span>

## <span data-ttu-id="3fdbf-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3fdbf-147">RELATED LINKS</span></span>
