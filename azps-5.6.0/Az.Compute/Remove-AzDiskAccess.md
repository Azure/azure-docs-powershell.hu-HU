---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
ms.openlocfilehash: 4b67364f0d079c7cd5fbbdd89b1a84b4dc6fee0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937089"
---
# <span data-ttu-id="a47ca-101">Remove-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a47ca-101">Remove-AzDiskAccess</span></span>

## <span data-ttu-id="a47ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a47ca-102">SYNOPSIS</span></span>
<span data-ttu-id="a47ca-103">Eltávolít egy lemezelérési erőforrást.</span><span class="sxs-lookup"><span data-stu-id="a47ca-103">Removes a disk access resource.</span></span>

## <span data-ttu-id="a47ca-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a47ca-104">SYNTAX</span></span>

### <span data-ttu-id="a47ca-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a47ca-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a47ca-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="a47ca-106">ResourceIDParameterSet</span></span>
```
Remove-AzDiskAccess [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a47ca-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a47ca-107">InputObjectParameterSet</span></span>
```
Remove-AzDiskAccess [-InputObject] <PSDiskAccess> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a47ca-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a47ca-108">DESCRIPTION</span></span>
<span data-ttu-id="a47ca-109">A **Remove-AzDiskAccess** parancsmag eltávolítja a lemezelérési erőforrást.</span><span class="sxs-lookup"><span data-stu-id="a47ca-109">The **Remove-AzDiskAccess** cmdlet removes a disk access resource.</span></span>

## <span data-ttu-id="a47ca-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a47ca-110">EXAMPLES</span></span>

### <span data-ttu-id="a47ca-111">1. példa: Lemezelérés eltávolítása az alapértelmezett paraméterkészlettel</span><span class="sxs-lookup"><span data-stu-id="a47ca-111">Example 1: Remove Disk Access using Default Parameter Set</span></span>
```
PS C:\> Remove-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
```

<span data-ttu-id="a47ca-112">Ez a parancs eltávolítja a "DiskAccess01" lemezelérést az "ResourceGroup01" erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="a47ca-112">This command removes the disk access named "DiskAccess01" in resource group "ResourceGroup01"</span></span>

### <span data-ttu-id="a47ca-113">2. példa: Lemezelérés eltávolítása erőforrás-azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="a47ca-113">Example 2: Remove Disk Access using Resource ID</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -ResourceId $myDiskAccess.id
```

<span data-ttu-id="a47ca-114">Ez a parancs eltávolítja a lemezelérést az Erőforrás-azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="a47ca-114">This command removes the disk access by Resource ID</span></span>

### <span data-ttu-id="a47ca-115">3. példa: Lemezelérés eltávolítása bemeneti objektum használatával</span><span class="sxs-lookup"><span data-stu-id="a47ca-115">Example 3: Remove Disk Access using Input Object</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -InputObject $myDiskAccess
```

<span data-ttu-id="a47ca-116">Ezzel a paranccsal az InputObject eltávolítja a lemezelérést</span><span class="sxs-lookup"><span data-stu-id="a47ca-116">This command removes the disk access by InputObject</span></span>

### <span data-ttu-id="a47ca-117">4. példa: Lemezelérés eltávolítása a bemeneti objektummal</span><span class="sxs-lookup"><span data-stu-id="a47ca-117">Example 4: Remove Disk Access by piping Input Object</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" | Remove-AzDiskAccess 
```

<span data-ttu-id="a47ca-118">Ez a parancs eltávolítja a lemezelérést az InputObject</span><span class="sxs-lookup"><span data-stu-id="a47ca-118">This command removes the disk access by piping the InputObject</span></span>

## <span data-ttu-id="a47ca-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a47ca-119">PARAMETERS</span></span>

### <span data-ttu-id="a47ca-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a47ca-120">-AsJob</span></span>
<span data-ttu-id="a47ca-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a47ca-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a47ca-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a47ca-122">-DefaultProfile</span></span>
<span data-ttu-id="a47ca-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a47ca-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a47ca-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a47ca-124">-InputObject</span></span>
<span data-ttu-id="a47ca-125">PowerShell Lemezelérési objektum</span><span class="sxs-lookup"><span data-stu-id="a47ca-125">PowerShell Disk Access Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess
Parameter Sets: InputObjectParameterSet
Aliases: DiskAccess

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a47ca-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a47ca-126">-Name</span></span>
<span data-ttu-id="a47ca-127">A lemezelérés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a47ca-127">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a47ca-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a47ca-128">-ResourceGroupName</span></span>
<span data-ttu-id="a47ca-129">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a47ca-129">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a47ca-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a47ca-130">-ResourceId</span></span>
<span data-ttu-id="a47ca-131">A lemezelérés erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a47ca-131">Resource ID for your disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a47ca-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a47ca-132">-Confirm</span></span>
<span data-ttu-id="a47ca-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a47ca-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a47ca-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a47ca-134">-WhatIf</span></span>
<span data-ttu-id="a47ca-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a47ca-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a47ca-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a47ca-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a47ca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a47ca-137">CommonParameters</span></span>
<span data-ttu-id="a47ca-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a47ca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a47ca-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a47ca-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a47ca-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a47ca-140">INPUTS</span></span>

### <span data-ttu-id="a47ca-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a47ca-141">System.String</span></span>

### <span data-ttu-id="a47ca-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a47ca-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="a47ca-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a47ca-143">OUTPUTS</span></span>

### <span data-ttu-id="a47ca-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a47ca-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a47ca-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a47ca-145">NOTES</span></span>

## <span data-ttu-id="a47ca-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a47ca-146">RELATED LINKS</span></span>
