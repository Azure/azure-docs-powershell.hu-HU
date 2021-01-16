---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: 17a28da26aa26860b7fd4a28ec922932bb089da3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355565"
---
# <span data-ttu-id="79d08-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="79d08-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="79d08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79d08-102">SYNOPSIS</span></span>
<span data-ttu-id="79d08-103">Felügyelt alkalmazás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="79d08-103">Removes a managed application</span></span>

## <span data-ttu-id="79d08-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="79d08-104">SYNTAX</span></span>

### <span data-ttu-id="79d08-105">RemoveByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="79d08-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79d08-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="79d08-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79d08-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="79d08-107">DESCRIPTION</span></span>
<span data-ttu-id="79d08-108">A **Remove-AzManagedApplication** parancsmag eltávolít egy felügyelt alkalmazást</span><span class="sxs-lookup"><span data-stu-id="79d08-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="79d08-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="79d08-109">EXAMPLES</span></span>

### <span data-ttu-id="79d08-110">1. példa: Felügyelt alkalmazás eltávolítása erőforrás-azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="79d08-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="79d08-111">Az első parancs a sajátApp nevű felügyelt alkalmazást kapja meg a Get-AzManagedApplication parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="79d08-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="79d08-112">A parancs a $Application tárolja.</span><span class="sxs-lookup"><span data-stu-id="79d08-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="79d08-113">A második parancs eltávolítja a  felügyelt alkalmazást, amelyet a $Application.</span><span class="sxs-lookup"><span data-stu-id="79d08-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="79d08-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79d08-114">PARAMETERS</span></span>

### <span data-ttu-id="79d08-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="79d08-115">-ApiVersion</span></span>
<span data-ttu-id="79d08-116">Ha be van állítva, az erőforrás-szolgáltató API-t használja.</span><span class="sxs-lookup"><span data-stu-id="79d08-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="79d08-117">Ha nincs megadva, az API-verziót a rendszer automatikusan a legújabb elérhetőként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="79d08-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="79d08-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79d08-118">-DefaultProfile</span></span>
<span data-ttu-id="79d08-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79d08-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79d08-120">-Force</span><span class="sxs-lookup"><span data-stu-id="79d08-120">-Force</span></span>
<span data-ttu-id="79d08-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="79d08-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="79d08-122">-Id</span><span class="sxs-lookup"><span data-stu-id="79d08-122">-Id</span></span>
<span data-ttu-id="79d08-123">A teljesen minősített felügyelt alkalmazásazonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="79d08-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="79d08-124">pl. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="79d08-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="79d08-125">-Name</span><span class="sxs-lookup"><span data-stu-id="79d08-125">-Name</span></span>
<span data-ttu-id="79d08-126">A felügyelt alkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="79d08-126">The managed application name.</span></span>

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

### <span data-ttu-id="79d08-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="79d08-127">-Pre</span></span>
<span data-ttu-id="79d08-128">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="79d08-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="79d08-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79d08-129">-ResourceGroupName</span></span>
<span data-ttu-id="79d08-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="79d08-130">The resource group name.</span></span>

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

### <span data-ttu-id="79d08-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79d08-131">-Confirm</span></span>
<span data-ttu-id="79d08-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="79d08-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79d08-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79d08-133">-WhatIf</span></span>
<span data-ttu-id="79d08-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="79d08-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79d08-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="79d08-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79d08-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79d08-136">CommonParameters</span></span>
<span data-ttu-id="79d08-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79d08-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79d08-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79d08-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79d08-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79d08-139">INPUTS</span></span>

### <span data-ttu-id="79d08-140">System.String</span><span class="sxs-lookup"><span data-stu-id="79d08-140">System.String</span></span>

## <span data-ttu-id="79d08-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79d08-141">OUTPUTS</span></span>

### <span data-ttu-id="79d08-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="79d08-142">System.Boolean</span></span>

## <span data-ttu-id="79d08-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="79d08-143">NOTES</span></span>

## <span data-ttu-id="79d08-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79d08-144">RELATED LINKS</span></span>
