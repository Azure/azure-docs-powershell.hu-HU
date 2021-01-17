---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
ms.openlocfilehash: 414a732dd80850a31a87f88d3dfdbf091cb4a6a6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331722"
---
# <span data-ttu-id="1bf73-101">Remove-AzPeering</span><span class="sxs-lookup"><span data-stu-id="1bf73-101">Remove-AzPeering</span></span>

## <span data-ttu-id="1bf73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bf73-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf73-103">Társviszony törlése vagy eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="1bf73-103">Delete or remove a peering.</span></span> <span data-ttu-id="1bf73-104">Ezzel törli az erőforrásra vonatkozó összes gyermekerőforrást vagy riasztást.</span><span class="sxs-lookup"><span data-stu-id="1bf73-104">This will delete all child resources or alerting on the resource.</span></span>

## <span data-ttu-id="1bf73-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1bf73-105">SYNTAX</span></span>

### <span data-ttu-id="1bf73-106">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1bf73-106">ByName (Default)</span></span>
```
Remove-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bf73-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="1bf73-107">InputObject</span></span>
```
Remove-AzPeering [-InputObject] <PSPeering> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bf73-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1bf73-108">ByResourceId</span></span>
```
Remove-AzPeering -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bf73-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1bf73-109">DESCRIPTION</span></span>
<span data-ttu-id="1bf73-110">Egy társviszony-erőforrást véglegesen törölni kell.</span><span class="sxs-lookup"><span data-stu-id="1bf73-110">Perminently delete a peering resource.</span></span>

## <span data-ttu-id="1bf73-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1bf73-111">EXAMPLES</span></span>

### <span data-ttu-id="1bf73-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="1bf73-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeering -ResourceId $resourceId
```

<span data-ttu-id="1bf73-113">Társviszony eltávolítása erőforrás-azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="1bf73-113">Remove a peering by resource id.</span></span>

## <span data-ttu-id="1bf73-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1bf73-114">PARAMETERS</span></span>

### <span data-ttu-id="1bf73-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bf73-115">-AsJob</span></span>
<span data-ttu-id="1bf73-116">Futtassa a háttérben.</span><span class="sxs-lookup"><span data-stu-id="1bf73-116">Run in the background.</span></span>

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

### <span data-ttu-id="1bf73-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf73-117">-DefaultProfile</span></span>
<span data-ttu-id="1bf73-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1bf73-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bf73-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1bf73-119">-Force</span></span>
<span data-ttu-id="1bf73-120">A művelet végrehajtásához</span><span class="sxs-lookup"><span data-stu-id="1bf73-120">Force the operation to complete</span></span>

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

### <span data-ttu-id="1bf73-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bf73-121">-InputObject</span></span>
<span data-ttu-id="1bf73-122">Használja Get-AzPeering objektum beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="1bf73-122">Use Get-AzPeering to retrieve this object.</span></span>

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

### <span data-ttu-id="1bf73-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1bf73-123">-Name</span></span>
<span data-ttu-id="1bf73-124">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="1bf73-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="1bf73-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bf73-125">-PassThru</span></span>
<span data-ttu-id="1bf73-126">Return true if complete</span><span class="sxs-lookup"><span data-stu-id="1bf73-126">Return true if complete</span></span>

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

### <span data-ttu-id="1bf73-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bf73-127">-ResourceGroupName</span></span>
<span data-ttu-id="1bf73-128">Meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="1bf73-128">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="1bf73-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bf73-129">-ResourceId</span></span>
<span data-ttu-id="1bf73-130">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="1bf73-130">The resource id string name.</span></span>

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

### <span data-ttu-id="1bf73-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1bf73-131">-Confirm</span></span>
<span data-ttu-id="1bf73-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1bf73-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bf73-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bf73-133">-WhatIf</span></span>
<span data-ttu-id="1bf73-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1bf73-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bf73-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1bf73-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bf73-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf73-136">CommonParameters</span></span>
<span data-ttu-id="1bf73-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bf73-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf73-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1bf73-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf73-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1bf73-139">INPUTS</span></span>

### <span data-ttu-id="1bf73-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="1bf73-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="1bf73-141">System.String</span><span class="sxs-lookup"><span data-stu-id="1bf73-141">System.String</span></span>

## <span data-ttu-id="1bf73-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1bf73-142">OUTPUTS</span></span>

### <span data-ttu-id="1bf73-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1bf73-143">System.Boolean</span></span>

## <span data-ttu-id="1bf73-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1bf73-144">NOTES</span></span>

## <span data-ttu-id="1bf73-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1bf73-145">RELATED LINKS</span></span>
