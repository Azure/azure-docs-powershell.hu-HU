---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: 2d3f2ee9a4dc55dd709be3113770df402434c911
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939609"
---
# <span data-ttu-id="4fd4f-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="4fd4f-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="4fd4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fd4f-102">SYNOPSIS</span></span>
<span data-ttu-id="4fd4f-103">A megadott eseményközpont eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="4fd4f-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="4fd4f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4fd4f-104">SYNTAX</span></span>

### <span data-ttu-id="4fd4f-105">EventhubDefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4fd4f-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fd4f-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4fd4f-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fd4f-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fd4f-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fd4f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4fd4f-108">DESCRIPTION</span></span>
<span data-ttu-id="4fd4f-109">A Remove-AzEventHub parancsmag eltávolítja és törli a megadott Eseményközpontot a megadott névtérből.</span><span class="sxs-lookup"><span data-stu-id="4fd4f-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="4fd4f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4fd4f-110">EXAMPLES</span></span>

### <span data-ttu-id="4fd4f-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="4fd4f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="4fd4f-112">Az Eseményközpont \` MyEventHubName \` eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="4fd4f-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="4fd4f-113">2. példa: InputObject – Változó használata:</span><span class="sxs-lookup"><span data-stu-id="4fd4f-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="4fd4f-114">3. példa: InputObject pipázás használatával:</span><span class="sxs-lookup"><span data-stu-id="4fd4f-114">Example 3: InputObject Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="4fd4f-115">4. példa: ResourceId – Változó használatával:</span><span class="sxs-lookup"><span data-stu-id="4fd4f-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="4fd4f-116">5. példa: ResourceId – Karakterlánc használata:</span><span class="sxs-lookup"><span data-stu-id="4fd4f-116">Example 5: ResourceId - Using string:</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="4fd4f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fd4f-117">PARAMETERS</span></span>

### <span data-ttu-id="4fd4f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fd4f-118">-AsJob</span></span>
<span data-ttu-id="4fd4f-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4fd4f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4fd4f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fd4f-120">-DefaultProfile</span></span>
<span data-ttu-id="4fd4f-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4fd4f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fd4f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fd4f-122">-InputObject</span></span>
<span data-ttu-id="4fd4f-123">Eventhub objektum</span><span class="sxs-lookup"><span data-stu-id="4fd4f-123">Eventhub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fd4f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4fd4f-124">-Name</span></span>
<span data-ttu-id="4fd4f-125">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="4fd4f-125">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fd4f-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4fd4f-126">-Namespace</span></span>
<span data-ttu-id="4fd4f-127">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="4fd4f-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fd4f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fd4f-128">-PassThru</span></span>
<span data-ttu-id="4fd4f-129">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="4fd4f-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="4fd4f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fd4f-130">-ResourceGroupName</span></span>
<span data-ttu-id="4fd4f-131">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4fd4f-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fd4f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fd4f-132">-ResourceId</span></span>
<span data-ttu-id="4fd4f-133">Eventhub Resource Id</span><span class="sxs-lookup"><span data-stu-id="4fd4f-133">Eventhub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fd4f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fd4f-134">-Confirm</span></span>
<span data-ttu-id="4fd4f-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4fd4f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fd4f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fd4f-136">-WhatIf</span></span>
<span data-ttu-id="4fd4f-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4fd4f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fd4f-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4fd4f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fd4f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fd4f-139">CommonParameters</span></span>
<span data-ttu-id="4fd4f-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fd4f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fd4f-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fd4f-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fd4f-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4fd4f-142">INPUTS</span></span>

### <span data-ttu-id="4fd4f-143">System.String</span><span class="sxs-lookup"><span data-stu-id="4fd4f-143">System.String</span></span>

### <span data-ttu-id="4fd4f-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="4fd4f-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="4fd4f-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fd4f-145">OUTPUTS</span></span>

### <span data-ttu-id="4fd4f-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4fd4f-146">System.Boolean</span></span>

## <span data-ttu-id="4fd4f-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4fd4f-147">NOTES</span></span>

## <span data-ttu-id="4fd4f-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fd4f-148">RELATED LINKS</span></span>
