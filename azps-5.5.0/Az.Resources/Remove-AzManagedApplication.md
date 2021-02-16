---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: 17a28da26aa26860b7fd4a28ec922932bb089da3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153602"
---
# <span data-ttu-id="efc3e-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="efc3e-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="efc3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efc3e-102">SYNOPSIS</span></span>
<span data-ttu-id="efc3e-103">Felügyelt alkalmazás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="efc3e-103">Removes a managed application</span></span>

## <span data-ttu-id="efc3e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="efc3e-104">SYNTAX</span></span>

### <span data-ttu-id="efc3e-105">RemoveByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="efc3e-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efc3e-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="efc3e-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efc3e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="efc3e-107">DESCRIPTION</span></span>
<span data-ttu-id="efc3e-108">A **Remove-AzManagedApplication** parancsmag eltávolít egy felügyelt alkalmazást</span><span class="sxs-lookup"><span data-stu-id="efc3e-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="efc3e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="efc3e-109">EXAMPLES</span></span>

### <span data-ttu-id="efc3e-110">1. példa: Felügyelt alkalmazás eltávolítása erőforrás-azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="efc3e-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="efc3e-111">Az első parancs a sajátApp nevű felügyelt alkalmazást kapja meg a Get-AzManagedApplication parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="efc3e-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="efc3e-112">A parancs a $Application tárolja.</span><span class="sxs-lookup"><span data-stu-id="efc3e-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="efc3e-113">A második parancs eltávolítja a  felügyelt alkalmazást, amelyet a $Application.</span><span class="sxs-lookup"><span data-stu-id="efc3e-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="efc3e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efc3e-114">PARAMETERS</span></span>

### <span data-ttu-id="efc3e-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="efc3e-115">-ApiVersion</span></span>
<span data-ttu-id="efc3e-116">Ha be van állítva, az erőforrás-szolgáltató API-t használja.</span><span class="sxs-lookup"><span data-stu-id="efc3e-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="efc3e-117">Ha nincs megadva, az API-verziót a rendszer automatikusan a legújabb elérhetőként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="efc3e-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="efc3e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc3e-118">-DefaultProfile</span></span>
<span data-ttu-id="efc3e-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="efc3e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efc3e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="efc3e-120">-Force</span></span>
<span data-ttu-id="efc3e-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="efc3e-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="efc3e-122">-Id</span><span class="sxs-lookup"><span data-stu-id="efc3e-122">-Id</span></span>
<span data-ttu-id="efc3e-123">A teljesen minősített felügyelt alkalmazásazonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="efc3e-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="efc3e-124">pl. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="efc3e-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="efc3e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="efc3e-125">-Name</span></span>
<span data-ttu-id="efc3e-126">A felügyelt alkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="efc3e-126">The managed application name.</span></span>

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

### <span data-ttu-id="efc3e-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="efc3e-127">-Pre</span></span>
<span data-ttu-id="efc3e-128">Ha be van állítva, az azt jelenti, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="efc3e-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="efc3e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efc3e-129">-ResourceGroupName</span></span>
<span data-ttu-id="efc3e-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="efc3e-130">The resource group name.</span></span>

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

### <span data-ttu-id="efc3e-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="efc3e-131">-Confirm</span></span>
<span data-ttu-id="efc3e-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="efc3e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efc3e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efc3e-133">-WhatIf</span></span>
<span data-ttu-id="efc3e-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="efc3e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efc3e-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="efc3e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efc3e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc3e-136">CommonParameters</span></span>
<span data-ttu-id="efc3e-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efc3e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc3e-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efc3e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc3e-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="efc3e-139">INPUTS</span></span>

### <span data-ttu-id="efc3e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="efc3e-140">System.String</span></span>

## <span data-ttu-id="efc3e-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="efc3e-141">OUTPUTS</span></span>

### <span data-ttu-id="efc3e-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="efc3e-142">System.Boolean</span></span>

## <span data-ttu-id="efc3e-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="efc3e-143">NOTES</span></span>

## <span data-ttu-id="efc3e-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="efc3e-144">RELATED LINKS</span></span>
