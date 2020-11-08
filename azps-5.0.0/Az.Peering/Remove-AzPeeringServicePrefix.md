---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 0fbf44e9a68a5cfaaea4138ec17caa2960a41e67
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187216"
---
# <span data-ttu-id="25bb9-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="25bb9-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="25bb9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="25bb9-102">SYNOPSIS</span></span>
<span data-ttu-id="25bb9-103">Új társközi szolgáltatás-előtag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="25bb9-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="25bb9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="25bb9-104">SYNTAX</span></span>

### <span data-ttu-id="25bb9-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25bb9-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PrefixName] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25bb9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="25bb9-106">InputObject</span></span>
```
Remove-AzPeeringServicePrefix [-InputObject] <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25bb9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="25bb9-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25bb9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="25bb9-108">DESCRIPTION</span></span>
<span data-ttu-id="25bb9-109">Egy, a társas szolgáltatásból származó társ-előtagok eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="25bb9-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="25bb9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="25bb9-110">EXAMPLES</span></span>

### <span data-ttu-id="25bb9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="25bb9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="25bb9-112">Előtag eltávolítása egy társközi szolgáltatási objektumból</span><span class="sxs-lookup"><span data-stu-id="25bb9-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="25bb9-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="25bb9-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="25bb9-114">Előtag eltávolítása egy társközi szolgáltatási erőforrás-azonosítóból.</span><span class="sxs-lookup"><span data-stu-id="25bb9-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="25bb9-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="25bb9-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="25bb9-116">Előtag eltávolítása egy társközi szolgáltatás-erőforráscsoport nevéről és nevéről</span><span class="sxs-lookup"><span data-stu-id="25bb9-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="25bb9-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="25bb9-117">PARAMETERS</span></span>

### <span data-ttu-id="25bb9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25bb9-118">-AsJob</span></span>
<span data-ttu-id="25bb9-119">Fusson a háttérben.</span><span class="sxs-lookup"><span data-stu-id="25bb9-119">Run in the background.</span></span>

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

### <span data-ttu-id="25bb9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25bb9-120">-DefaultProfile</span></span>
<span data-ttu-id="25bb9-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25bb9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25bb9-122">-Force</span><span class="sxs-lookup"><span data-stu-id="25bb9-122">-Force</span></span>
<span data-ttu-id="25bb9-123">A művelet elvégzésének kényszerítése</span><span class="sxs-lookup"><span data-stu-id="25bb9-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="25bb9-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25bb9-124">-InputObject</span></span>
<span data-ttu-id="25bb9-125">Get-AzPeeringServicePrefix használata</span><span class="sxs-lookup"><span data-stu-id="25bb9-125">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25bb9-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="25bb9-126">-Name</span></span>
<span data-ttu-id="25bb9-127">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="25bb9-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25bb9-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25bb9-128">-PassThru</span></span>
<span data-ttu-id="25bb9-129">Az igaz értéket visszaad a sikertelen sikerhez vagy hamis értékhez.</span><span class="sxs-lookup"><span data-stu-id="25bb9-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="25bb9-130">-PrefixName</span><span class="sxs-lookup"><span data-stu-id="25bb9-130">-PrefixName</span></span>
<span data-ttu-id="25bb9-131">Az előtag neve.</span><span class="sxs-lookup"><span data-stu-id="25bb9-131">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25bb9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25bb9-132">-ResourceGroupName</span></span>
<span data-ttu-id="25bb9-133">A meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="25bb9-133">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25bb9-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25bb9-134">-ResourceId</span></span>
<span data-ttu-id="25bb9-135">Az erőforrás-azonosító karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="25bb9-135">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25bb9-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="25bb9-136">-Confirm</span></span>
<span data-ttu-id="25bb9-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="25bb9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25bb9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25bb9-138">-WhatIf</span></span>
<span data-ttu-id="25bb9-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="25bb9-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25bb9-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="25bb9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25bb9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25bb9-141">CommonParameters</span></span>
<span data-ttu-id="25bb9-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="25bb9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25bb9-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="25bb9-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25bb9-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="25bb9-144">INPUTS</span></span>

### <span data-ttu-id="25bb9-145">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="25bb9-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="25bb9-146">System. String</span><span class="sxs-lookup"><span data-stu-id="25bb9-146">System.String</span></span>

## <span data-ttu-id="25bb9-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25bb9-147">OUTPUTS</span></span>

### <span data-ttu-id="25bb9-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25bb9-148">System.Boolean</span></span>

## <span data-ttu-id="25bb9-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="25bb9-149">NOTES</span></span>

## <span data-ttu-id="25bb9-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25bb9-150">RELATED LINKS</span></span>