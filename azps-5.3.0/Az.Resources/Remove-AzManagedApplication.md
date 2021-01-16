---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: 17a28da26aa26860b7fd4a28ec922932bb089da3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466411"
---
# <span data-ttu-id="166de-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="166de-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="166de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="166de-102">SYNOPSIS</span></span>
<span data-ttu-id="166de-103">Felügyelt alkalmazás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="166de-103">Removes a managed application</span></span>

## <span data-ttu-id="166de-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="166de-104">SYNTAX</span></span>

### <span data-ttu-id="166de-105">RemoveByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="166de-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="166de-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="166de-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="166de-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="166de-107">DESCRIPTION</span></span>
<span data-ttu-id="166de-108">A **Remove-AzManagedApplication** parancsmag eltávolít egy felügyelt alkalmazást</span><span class="sxs-lookup"><span data-stu-id="166de-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="166de-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="166de-109">EXAMPLES</span></span>

### <span data-ttu-id="166de-110">1. példa: Felügyelt alkalmazás eltávolítása erőforrás-azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="166de-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="166de-111">Az első parancs a sajátApp nevű felügyelt alkalmazást kapja meg a Get-AzManagedApplication parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="166de-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="166de-112">A parancs a $Application tárolja.</span><span class="sxs-lookup"><span data-stu-id="166de-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="166de-113">A második parancs eltávolítja a  felügyelt alkalmazást, amelyet a $Application.</span><span class="sxs-lookup"><span data-stu-id="166de-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="166de-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="166de-114">PARAMETERS</span></span>

### <span data-ttu-id="166de-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="166de-115">-ApiVersion</span></span>
<span data-ttu-id="166de-116">Ha be van állítva, az erőforrás-szolgáltató API-t használja.</span><span class="sxs-lookup"><span data-stu-id="166de-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="166de-117">Ha nincs megadva, az API-verziót a rendszer automatikusan a legújabb elérhetőként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="166de-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="166de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="166de-118">-DefaultProfile</span></span>
<span data-ttu-id="166de-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="166de-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="166de-120">-Force</span><span class="sxs-lookup"><span data-stu-id="166de-120">-Force</span></span>
<span data-ttu-id="166de-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="166de-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="166de-122">-Id</span><span class="sxs-lookup"><span data-stu-id="166de-122">-Id</span></span>
<span data-ttu-id="166de-123">A teljesen minősített felügyelt alkalmazásazonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="166de-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="166de-124">pl. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="166de-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166de-125">-Name</span><span class="sxs-lookup"><span data-stu-id="166de-125">-Name</span></span>
<span data-ttu-id="166de-126">A felügyelt alkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="166de-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166de-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="166de-127">-Pre</span></span>
<span data-ttu-id="166de-128">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="166de-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="166de-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="166de-129">-ResourceGroupName</span></span>
<span data-ttu-id="166de-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="166de-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166de-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="166de-131">-Confirm</span></span>
<span data-ttu-id="166de-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="166de-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="166de-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="166de-133">-WhatIf</span></span>
<span data-ttu-id="166de-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="166de-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="166de-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="166de-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="166de-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="166de-136">CommonParameters</span></span>
<span data-ttu-id="166de-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="166de-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="166de-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="166de-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="166de-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="166de-139">INPUTS</span></span>

### <span data-ttu-id="166de-140">System.String</span><span class="sxs-lookup"><span data-stu-id="166de-140">System.String</span></span>

## <span data-ttu-id="166de-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="166de-141">OUTPUTS</span></span>

### <span data-ttu-id="166de-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="166de-142">System.Boolean</span></span>

## <span data-ttu-id="166de-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="166de-143">NOTES</span></span>

## <span data-ttu-id="166de-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="166de-144">RELATED LINKS</span></span>
