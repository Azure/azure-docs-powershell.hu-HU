---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
ms.openlocfilehash: 6df8d5539bf340df5e00ad69ac557bc2cbb8ccaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496204"
---
# <span data-ttu-id="487a9-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="487a9-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="487a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="487a9-102">SYNOPSIS</span></span>
<span data-ttu-id="487a9-103">Eltávolítja a megadott esemény-hubok névteret.</span><span class="sxs-lookup"><span data-stu-id="487a9-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="487a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="487a9-104">SYNTAX</span></span>

### <span data-ttu-id="487a9-105">NamespaceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="487a9-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="487a9-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="487a9-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="487a9-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="487a9-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="487a9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="487a9-108">DESCRIPTION</span></span>
<span data-ttu-id="487a9-109">A Remove-AzureRmEventHubNamespace parancsmag eltávolítja és törli a megadott esemény-hubok névteret.</span><span class="sxs-lookup"><span data-stu-id="487a9-109">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="487a9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="487a9-110">EXAMPLES</span></span>

### <span data-ttu-id="487a9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="487a9-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="487a9-112">Eltávolítja az esemény-hubok \` névtér \` -MyNamespaceName az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="487a9-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="487a9-113">Példa 2,1-InputObject – változó használata:</span><span class="sxs-lookup"><span data-stu-id="487a9-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzureRmEventHubNamespace <params> 
PS C:\> Remove-AzureRmEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="487a9-114">Példa 2,1-InputObject:</span><span class="sxs-lookup"><span data-stu-id="487a9-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace <params> | Remove-AzureRmEventHubNamespace
```

### <span data-ttu-id="487a9-115">Példa 3,1-ResourceId – változó használata</span><span class="sxs-lookup"><span data-stu-id="487a9-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHubNamespace <params>
PS C:\> Remove-AzureRmEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="487a9-116">Példa 3,2-ResourceId:</span><span class="sxs-lookup"><span data-stu-id="487a9-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzureRmResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzureRmEventHubNamespace
```

### <span data-ttu-id="487a9-117">Példa 3,3-ResourceId-karakterlánc használatával:</span><span class="sxs-lookup"><span data-stu-id="487a9-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="487a9-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="487a9-118">PARAMETERS</span></span>

### <span data-ttu-id="487a9-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="487a9-119">-AsJob</span></span>
<span data-ttu-id="487a9-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="487a9-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="487a9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="487a9-121">-DefaultProfile</span></span>
<span data-ttu-id="487a9-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="487a9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="487a9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="487a9-123">-InputObject</span></span>
<span data-ttu-id="487a9-124">EventHubs névtér-objektum</span><span class="sxs-lookup"><span data-stu-id="487a9-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="487a9-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="487a9-125">-Name</span></span>
<span data-ttu-id="487a9-126">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="487a9-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="487a9-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="487a9-127">-PassThru</span></span>
<span data-ttu-id="487a9-128">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="487a9-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="487a9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="487a9-129">-ResourceGroupName</span></span>
<span data-ttu-id="487a9-130">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="487a9-130">Resource Group Name</span></span>

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

### <span data-ttu-id="487a9-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="487a9-131">-ResourceId</span></span>
<span data-ttu-id="487a9-132">EventHubs névtér-erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="487a9-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="487a9-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="487a9-133">-Confirm</span></span>
<span data-ttu-id="487a9-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="487a9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="487a9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="487a9-135">-WhatIf</span></span>
<span data-ttu-id="487a9-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="487a9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="487a9-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="487a9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="487a9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="487a9-138">CommonParameters</span></span>
<span data-ttu-id="487a9-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="487a9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="487a9-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="487a9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="487a9-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="487a9-141">INPUTS</span></span>

### <span data-ttu-id="487a9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="487a9-142">System.String</span></span>

### <span data-ttu-id="487a9-143">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="487a9-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="487a9-144">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="487a9-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="487a9-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="487a9-145">OUTPUTS</span></span>

### <span data-ttu-id="487a9-146">System. Void</span><span class="sxs-lookup"><span data-stu-id="487a9-146">System.Void</span></span>

## <span data-ttu-id="487a9-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="487a9-147">NOTES</span></span>

## <span data-ttu-id="487a9-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="487a9-148">RELATED LINKS</span></span>
