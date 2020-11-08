---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
ms.openlocfilehash: 414a732dd80850a31a87f88d3dfdbf091cb4a6a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194895"
---
# <span data-ttu-id="f3422-101">Remove-AzPeering</span><span class="sxs-lookup"><span data-stu-id="f3422-101">Remove-AzPeering</span></span>

## <span data-ttu-id="f3422-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3422-102">SYNOPSIS</span></span>
<span data-ttu-id="f3422-103">A társas nézet törlése vagy eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f3422-103">Delete or remove a peering.</span></span> <span data-ttu-id="f3422-104">Ezzel törli az összes gyermek erőforrását, vagy figyelmeztetést ad az erőforrásról.</span><span class="sxs-lookup"><span data-stu-id="f3422-104">This will delete all child resources or alerting on the resource.</span></span>

## <span data-ttu-id="f3422-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3422-105">SYNTAX</span></span>

### <span data-ttu-id="f3422-106">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3422-106">ByName (Default)</span></span>
```
Remove-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3422-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f3422-107">InputObject</span></span>
```
Remove-AzPeering [-InputObject] <PSPeering> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3422-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f3422-108">ByResourceId</span></span>
```
Remove-AzPeering -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3422-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3422-109">DESCRIPTION</span></span>
<span data-ttu-id="f3422-110">Perminently: egy társközi erőforrás törlése</span><span class="sxs-lookup"><span data-stu-id="f3422-110">Perminently delete a peering resource.</span></span>

## <span data-ttu-id="f3422-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f3422-111">EXAMPLES</span></span>

### <span data-ttu-id="f3422-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f3422-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeering -ResourceId $resourceId
```

<span data-ttu-id="f3422-113">Erőforrás-azonosítóval rendelkező társközi fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f3422-113">Remove a peering by resource id.</span></span>

## <span data-ttu-id="f3422-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3422-114">PARAMETERS</span></span>

### <span data-ttu-id="f3422-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3422-115">-AsJob</span></span>
<span data-ttu-id="f3422-116">Fusson a háttérben.</span><span class="sxs-lookup"><span data-stu-id="f3422-116">Run in the background.</span></span>

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

### <span data-ttu-id="f3422-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3422-117">-DefaultProfile</span></span>
<span data-ttu-id="f3422-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3422-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3422-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f3422-119">-Force</span></span>
<span data-ttu-id="f3422-120">A művelet elvégzésének kényszerítése</span><span class="sxs-lookup"><span data-stu-id="f3422-120">Force the operation to complete</span></span>

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

### <span data-ttu-id="f3422-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3422-121">-InputObject</span></span>
<span data-ttu-id="f3422-122">Az objektum beolvasásához használja a Get-AzPeering.</span><span class="sxs-lookup"><span data-stu-id="f3422-122">Use Get-AzPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3422-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f3422-123">-Name</span></span>
<span data-ttu-id="f3422-124">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="f3422-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="f3422-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3422-125">-PassThru</span></span>
<span data-ttu-id="f3422-126">Igaz érték visszaadása befejezettként</span><span class="sxs-lookup"><span data-stu-id="f3422-126">Return true if complete</span></span>

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

### <span data-ttu-id="f3422-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3422-127">-ResourceGroupName</span></span>
<span data-ttu-id="f3422-128">A meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="f3422-128">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="f3422-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3422-129">-ResourceId</span></span>
<span data-ttu-id="f3422-130">Az erőforrás-azonosító karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="f3422-130">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3422-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f3422-131">-Confirm</span></span>
<span data-ttu-id="f3422-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f3422-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3422-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3422-133">-WhatIf</span></span>
<span data-ttu-id="f3422-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f3422-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3422-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3422-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3422-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3422-136">CommonParameters</span></span>
<span data-ttu-id="f3422-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3422-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3422-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f3422-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3422-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3422-139">INPUTS</span></span>

### <span data-ttu-id="f3422-140">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="f3422-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="f3422-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f3422-141">System.String</span></span>

## <span data-ttu-id="f3422-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3422-142">OUTPUTS</span></span>

### <span data-ttu-id="f3422-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f3422-143">System.Boolean</span></span>

## <span data-ttu-id="f3422-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3422-144">NOTES</span></span>

## <span data-ttu-id="f3422-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3422-145">RELATED LINKS</span></span>
