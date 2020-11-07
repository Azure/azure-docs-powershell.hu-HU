---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 38a727c2e632173befe6b5b08756d558a9c9f177
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842285"
---
# <span data-ttu-id="f68ba-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="f68ba-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="f68ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f68ba-102">SYNOPSIS</span></span>
<span data-ttu-id="f68ba-103">Eltávolítja a megadott esemény-hubok névteret.</span><span class="sxs-lookup"><span data-stu-id="f68ba-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="f68ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f68ba-104">SYNTAX</span></span>

### <span data-ttu-id="f68ba-105">NamespaceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f68ba-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f68ba-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f68ba-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f68ba-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f68ba-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f68ba-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f68ba-108">DESCRIPTION</span></span>
<span data-ttu-id="f68ba-109">A Remove-AzEventHubNamespace parancsmag eltávolítja és törli a megadott esemény-hubok névteret.</span><span class="sxs-lookup"><span data-stu-id="f68ba-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="f68ba-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f68ba-110">EXAMPLES</span></span>

### <span data-ttu-id="f68ba-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f68ba-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="f68ba-112">Eltávolítja az esemény-hubok \` névtér \` -MyNamespaceName az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="f68ba-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="f68ba-113">Példa 2,1-InputObject – változó használata:</span><span class="sxs-lookup"><span data-stu-id="f68ba-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="f68ba-114">Példa 2,1-InputObject:</span><span class="sxs-lookup"><span data-stu-id="f68ba-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="f68ba-115">Példa 3,1-ResourceId – változó használata</span><span class="sxs-lookup"><span data-stu-id="f68ba-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="f68ba-116">Példa 3,2-ResourceId:</span><span class="sxs-lookup"><span data-stu-id="f68ba-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="f68ba-117">Példa 3,3-ResourceId-karakterlánc használatával:</span><span class="sxs-lookup"><span data-stu-id="f68ba-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="f68ba-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f68ba-118">PARAMETERS</span></span>

### <span data-ttu-id="f68ba-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f68ba-119">-AsJob</span></span>
<span data-ttu-id="f68ba-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f68ba-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f68ba-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f68ba-121">-DefaultProfile</span></span>
<span data-ttu-id="f68ba-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f68ba-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f68ba-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f68ba-123">-InputObject</span></span>
<span data-ttu-id="f68ba-124">EventHubs névtér-objektum</span><span class="sxs-lookup"><span data-stu-id="f68ba-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="f68ba-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f68ba-125">-Name</span></span>
<span data-ttu-id="f68ba-126">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="f68ba-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="f68ba-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f68ba-127">-PassThru</span></span>
<span data-ttu-id="f68ba-128">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="f68ba-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f68ba-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f68ba-129">-ResourceGroupName</span></span>
<span data-ttu-id="f68ba-130">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f68ba-130">Resource Group Name</span></span>

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

### <span data-ttu-id="f68ba-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f68ba-131">-ResourceId</span></span>
<span data-ttu-id="f68ba-132">EventHubs névtér-erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="f68ba-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="f68ba-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f68ba-133">-Confirm</span></span>
<span data-ttu-id="f68ba-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f68ba-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f68ba-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f68ba-135">-WhatIf</span></span>
<span data-ttu-id="f68ba-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f68ba-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f68ba-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f68ba-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f68ba-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f68ba-138">CommonParameters</span></span>
<span data-ttu-id="f68ba-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f68ba-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f68ba-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f68ba-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f68ba-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f68ba-141">INPUTS</span></span>

### <span data-ttu-id="f68ba-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f68ba-142">System.String</span></span>

### <span data-ttu-id="f68ba-143">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f68ba-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="f68ba-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f68ba-144">OUTPUTS</span></span>

### <span data-ttu-id="f68ba-145">System. Void</span><span class="sxs-lookup"><span data-stu-id="f68ba-145">System.Void</span></span>

## <span data-ttu-id="f68ba-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f68ba-146">NOTES</span></span>

## <span data-ttu-id="f68ba-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f68ba-147">RELATED LINKS</span></span>
