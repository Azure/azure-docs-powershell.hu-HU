---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
ms.openlocfilehash: bcb250c8967c10e5b200e62d843e99eab374d81d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466729"
---
# <span data-ttu-id="9d0b2-101">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9d0b2-101">Remove-AzCustomIpPrefix</span></span>

## <span data-ttu-id="9d0b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d0b2-102">SYNOPSIS</span></span>
<span data-ttu-id="9d0b2-103">A CustomIpPrefix eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9d0b2-103">Removes a CustomIpPrefix</span></span>

## <span data-ttu-id="9d0b2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9d0b2-104">SYNTAX</span></span>

### <span data-ttu-id="9d0b2-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9d0b2-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d0b2-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d0b2-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzCustomIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d0b2-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d0b2-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d0b2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9d0b2-108">DESCRIPTION</span></span>
<span data-ttu-id="9d0b2-109">A **Remove-AzCustomIpPrefix** parancsmag eltávolítja a CustomIpPrefix értékeket.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-109">The **Remove-AzCustomIpPrefix** cmdlet removes a CustomIpPrefix.</span></span>

## <span data-ttu-id="9d0b2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9d0b2-110">EXAMPLES</span></span>

### <span data-ttu-id="9d0b2-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="9d0b2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="9d0b2-112">A CustomIpPrefix névvel $prefixName eltávolítása az erőforráscsoportból $rgName</span><span class="sxs-lookup"><span data-stu-id="9d0b2-112">Removes the CustomIpPrefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="9d0b2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d0b2-113">PARAMETERS</span></span>

### <span data-ttu-id="9d0b2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d0b2-114">-AsJob</span></span>
<span data-ttu-id="9d0b2-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9d0b2-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d0b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d0b2-116">-DefaultProfile</span></span>
<span data-ttu-id="9d0b2-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d0b2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9d0b2-118">-Force</span></span>
<span data-ttu-id="9d0b2-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-119">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d0b2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d0b2-120">-InputObject</span></span>
<span data-ttu-id="9d0b2-121">Egy customIpPrefix objektum.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-121">A customIpPrefix object.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0b2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9d0b2-122">-Name</span></span>
<span data-ttu-id="9d0b2-123">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0b2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d0b2-124">-PassThru</span></span>
<span data-ttu-id="9d0b2-125">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9d0b2-126">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d0b2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d0b2-127">-ResourceGroupName</span></span>
<span data-ttu-id="9d0b2-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0b2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d0b2-129">-ResourceId</span></span>
<span data-ttu-id="9d0b2-130">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-130">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0b2-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d0b2-131">-Confirm</span></span>
<span data-ttu-id="9d0b2-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d0b2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d0b2-133">-WhatIf</span></span>
<span data-ttu-id="9d0b2-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d0b2-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d0b2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d0b2-136">CommonParameters</span></span>
<span data-ttu-id="9d0b2-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d0b2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d0b2-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d0b2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d0b2-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d0b2-139">INPUTS</span></span>

### <span data-ttu-id="9d0b2-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9d0b2-140">System.String</span></span>

### <span data-ttu-id="9d0b2-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9d0b2-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="9d0b2-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d0b2-142">OUTPUTS</span></span>

### <span data-ttu-id="9d0b2-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9d0b2-143">System.Boolean</span></span>

## <span data-ttu-id="9d0b2-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9d0b2-144">NOTES</span></span>

## <span data-ttu-id="9d0b2-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d0b2-145">RELATED LINKS</span></span>

[<span data-ttu-id="9d0b2-146">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9d0b2-146">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="9d0b2-147">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9d0b2-147">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="9d0b2-148">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9d0b2-148">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)