---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
ms.openlocfilehash: 895974f12c7472cb93679cb27ca895ca40757f53
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466426"
---
# <span data-ttu-id="662cb-101">Remove-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="662cb-101">Remove-AzADGroup</span></span>

## <span data-ttu-id="662cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="662cb-102">SYNOPSIS</span></span>
<span data-ttu-id="662cb-103">Egy Active Directory-csoportot töröl.</span><span class="sxs-lookup"><span data-stu-id="662cb-103">Deletes an active directory group.</span></span>

## <span data-ttu-id="662cb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="662cb-104">SYNTAX</span></span>

### <span data-ttu-id="662cb-105">ObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="662cb-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADGroup -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="662cb-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="662cb-106">DisplayNameParameterSet</span></span>
```
Remove-AzADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="662cb-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="662cb-107">InputObjectParameterSet</span></span>
```
Remove-AzADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="662cb-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="662cb-108">DESCRIPTION</span></span>
<span data-ttu-id="662cb-109">Egy Active Directory-csoportot töröl.</span><span class="sxs-lookup"><span data-stu-id="662cb-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="662cb-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="662cb-110">EXAMPLES</span></span>

### <span data-ttu-id="662cb-111">1. példa: Csoport eltávolítása objektumazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="662cb-111">Example 1: Remove a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="662cb-112">Eltávolítja a "85F89C90-780E-4AA6-9F4F-6F268D322EEE" objektumazonosítót a bérlőből.</span><span class="sxs-lookup"><span data-stu-id="662cb-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="662cb-113">2. példa: Csoport eltávolítása pipázás használatával</span><span class="sxs-lookup"><span data-stu-id="662cb-113">Example 2: Remove a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroup
```

<span data-ttu-id="662cb-114">A (85F89C90-780E-4AA6-9F4F-6F268D322EEE) objektumazonosítóval és a Remove-AzADGroup eltávolításához a bérlői fiókból eltávolítható vezetékekkel együtt.</span><span class="sxs-lookup"><span data-stu-id="662cb-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="662cb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="662cb-115">PARAMETERS</span></span>

### <span data-ttu-id="662cb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="662cb-116">-DefaultProfile</span></span>
<span data-ttu-id="662cb-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="662cb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="662cb-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="662cb-118">-DisplayName</span></span>
<span data-ttu-id="662cb-119">Az eltávolítható csoport megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="662cb-119">The display name of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="662cb-120">-Force</span><span class="sxs-lookup"><span data-stu-id="662cb-120">-Force</span></span>
<span data-ttu-id="662cb-121">Ha meg van adva, akkor nem kér megerősítést a csoport törléséhez.</span><span class="sxs-lookup"><span data-stu-id="662cb-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

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

### <span data-ttu-id="662cb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="662cb-122">-InputObject</span></span>
<span data-ttu-id="662cb-123">Az eltávolítható csoport objektum reprezentációja.</span><span class="sxs-lookup"><span data-stu-id="662cb-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="662cb-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="662cb-124">-ObjectId</span></span>
<span data-ttu-id="662cb-125">Az eltávolítható csoport objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="662cb-125">The object id of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="662cb-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="662cb-126">-PassThru</span></span>
<span data-ttu-id="662cb-127">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="662cb-127">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="662cb-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="662cb-128">-Confirm</span></span>
<span data-ttu-id="662cb-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="662cb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="662cb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="662cb-130">-WhatIf</span></span>
<span data-ttu-id="662cb-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="662cb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="662cb-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="662cb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="662cb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="662cb-133">CommonParameters</span></span>
<span data-ttu-id="662cb-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="662cb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="662cb-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="662cb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="662cb-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="662cb-136">INPUTS</span></span>

### <span data-ttu-id="662cb-137">System.String</span><span class="sxs-lookup"><span data-stu-id="662cb-137">System.String</span></span>

### <span data-ttu-id="662cb-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="662cb-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="662cb-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="662cb-139">OUTPUTS</span></span>

### <span data-ttu-id="662cb-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="662cb-140">System.Boolean</span></span>

## <span data-ttu-id="662cb-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="662cb-141">NOTES</span></span>

## <span data-ttu-id="662cb-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="662cb-142">RELATED LINKS</span></span>