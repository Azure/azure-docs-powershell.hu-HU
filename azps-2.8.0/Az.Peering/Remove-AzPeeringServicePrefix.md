---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 36003d1fbca7566ae663a1d878386f3d8d67f484
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838415"
---
# <span data-ttu-id="bf44d-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="bf44d-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="bf44d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf44d-102">SYNOPSIS</span></span>
<span data-ttu-id="bf44d-103">Új társközi szolgáltatás-előtag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="bf44d-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="bf44d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf44d-104">SYNTAX</span></span>

### <span data-ttu-id="bf44d-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bf44d-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PeeringServiceName] <String>
 [-Force] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf44d-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="bf44d-106">Default</span></span>
```
Remove-AzPeeringServicePrefix -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf44d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bf44d-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf44d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf44d-108">DESCRIPTION</span></span>
<span data-ttu-id="bf44d-109">Egy, a társas szolgáltatásból származó társ-előtagok eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="bf44d-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="bf44d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bf44d-110">EXAMPLES</span></span>

### <span data-ttu-id="bf44d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bf44d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="bf44d-112">Előtag eltávolítása egy társközi szolgáltatási objektumból</span><span class="sxs-lookup"><span data-stu-id="bf44d-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="bf44d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="bf44d-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="bf44d-114">Előtag eltávolítása egy társközi szolgáltatási erőforrás-azonosítóból.</span><span class="sxs-lookup"><span data-stu-id="bf44d-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="bf44d-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="bf44d-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="bf44d-116">Előtag eltávolítása egy társközi szolgáltatás-erőforráscsoport nevéről és nevéről</span><span class="sxs-lookup"><span data-stu-id="bf44d-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="bf44d-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf44d-117">PARAMETERS</span></span>

### <span data-ttu-id="bf44d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf44d-118">-AsJob</span></span>
<span data-ttu-id="bf44d-119">Fusson a háttérben.</span><span class="sxs-lookup"><span data-stu-id="bf44d-119">Run in the background.</span></span>

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

### <span data-ttu-id="bf44d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf44d-120">-DefaultProfile</span></span>
<span data-ttu-id="bf44d-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf44d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf44d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="bf44d-122">-Force</span></span>
<span data-ttu-id="bf44d-123">A művelet elvégzésének kényszerítése</span><span class="sxs-lookup"><span data-stu-id="bf44d-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="bf44d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf44d-124">-InputObject</span></span>
<span data-ttu-id="bf44d-125">Get-AzPeeringServicePrefix használata</span><span class="sxs-lookup"><span data-stu-id="bf44d-125">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf44d-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bf44d-126">-Name</span></span>
<span data-ttu-id="bf44d-127">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="bf44d-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="bf44d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf44d-128">-PassThru</span></span>
<span data-ttu-id="bf44d-129">Az igaz értéket visszaad a sikertelen sikerhez vagy hamis értékhez.</span><span class="sxs-lookup"><span data-stu-id="bf44d-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="bf44d-130">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="bf44d-130">-PeeringServiceName</span></span>
<span data-ttu-id="bf44d-131">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="bf44d-131">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="bf44d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf44d-132">-ResourceGroupName</span></span>
<span data-ttu-id="bf44d-133">A meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="bf44d-133">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="bf44d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf44d-134">-ResourceId</span></span>
<span data-ttu-id="bf44d-135">Az erőforrás-azonosító karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="bf44d-135">The resource id string name.</span></span>

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

### <span data-ttu-id="bf44d-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bf44d-136">-Confirm</span></span>
<span data-ttu-id="bf44d-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bf44d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf44d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf44d-138">-WhatIf</span></span>
<span data-ttu-id="bf44d-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bf44d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf44d-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bf44d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf44d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf44d-141">CommonParameters</span></span>
<span data-ttu-id="bf44d-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf44d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf44d-143">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bf44d-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf44d-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf44d-144">INPUTS</span></span>

### <span data-ttu-id="bf44d-145">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="bf44d-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="bf44d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="bf44d-146">System.String</span></span>

## <span data-ttu-id="bf44d-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf44d-147">OUTPUTS</span></span>

### <span data-ttu-id="bf44d-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bf44d-148">System.Boolean</span></span>

## <span data-ttu-id="bf44d-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf44d-149">NOTES</span></span>

## <span data-ttu-id="bf44d-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf44d-150">RELATED LINKS</span></span>
