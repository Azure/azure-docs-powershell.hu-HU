---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
ms.openlocfilehash: 285acdcd7e913d4fb502fb656057f1fc81d6dfcd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926489"
---
# <span data-ttu-id="235fd-101">Remove-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="235fd-101">Remove-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="235fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="235fd-102">SYNOPSIS</span></span>
<span data-ttu-id="235fd-103">Felügyelt alkalmazásdefiníció eltávolítása</span><span class="sxs-lookup"><span data-stu-id="235fd-103">Removes a managed application definition</span></span>

## <span data-ttu-id="235fd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="235fd-104">SYNTAX</span></span>

### <span data-ttu-id="235fd-105">RemoveByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="235fd-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="235fd-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="235fd-106">RemoveById</span></span>
```
Remove-AzManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="235fd-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="235fd-107">DESCRIPTION</span></span>
<span data-ttu-id="235fd-108">A **Remove-AzManagedApplicationDefinition parancsmag** eltávolít egy felügyelt alkalmazásdefiníciót</span><span class="sxs-lookup"><span data-stu-id="235fd-108">The **Remove-AzManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="235fd-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="235fd-109">EXAMPLES</span></span>

### <span data-ttu-id="235fd-110">1. példa: Felügyelt alkalmazásdefiníció eltávolítása erőforrás-azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="235fd-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="235fd-111">Az első parancs egy myAppDef nevű felügyelt alkalmazásdefiníciót kap a Get-AzManagedApplicationDefinition parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="235fd-111">The first command gets a managed application definition named myAppDef by using the Get-AzManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="235fd-112">A parancs a $ApplicationDefinition tárolja.</span><span class="sxs-lookup"><span data-stu-id="235fd-112">The command stores it in the $ApplicationDefinition variable.</span></span>
<span data-ttu-id="235fd-113">A második parancs eltávolítja a felügyelt  alkalmazásdefiníciót, amelyet a $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="235fd-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="235fd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="235fd-114">PARAMETERS</span></span>

### <span data-ttu-id="235fd-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="235fd-115">-ApiVersion</span></span>
<span data-ttu-id="235fd-116">Ha be van állítva, az erőforrás-szolgáltató API-t használja.</span><span class="sxs-lookup"><span data-stu-id="235fd-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="235fd-117">Ha nincs megadva, az API-verziót a rendszer automatikusan a legújabb elérhetőként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="235fd-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="235fd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="235fd-118">-DefaultProfile</span></span>
<span data-ttu-id="235fd-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="235fd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="235fd-120">-Force</span><span class="sxs-lookup"><span data-stu-id="235fd-120">-Force</span></span>
<span data-ttu-id="235fd-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="235fd-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="235fd-122">-Id</span><span class="sxs-lookup"><span data-stu-id="235fd-122">-Id</span></span>
<span data-ttu-id="235fd-123">A teljesen minősített felügyelt alkalmazásdefiníciós azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="235fd-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="235fd-124">pl. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="235fd-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="235fd-125">-Name</span><span class="sxs-lookup"><span data-stu-id="235fd-125">-Name</span></span>
<span data-ttu-id="235fd-126">A felügyelt alkalmazás definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="235fd-126">The managed application definition name.</span></span>

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

### <span data-ttu-id="235fd-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="235fd-127">-Pre</span></span>
<span data-ttu-id="235fd-128">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="235fd-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="235fd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="235fd-129">-ResourceGroupName</span></span>
<span data-ttu-id="235fd-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="235fd-130">The resource group name.</span></span>

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

### <span data-ttu-id="235fd-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="235fd-131">-Confirm</span></span>
<span data-ttu-id="235fd-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="235fd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="235fd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="235fd-133">-WhatIf</span></span>
<span data-ttu-id="235fd-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="235fd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="235fd-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="235fd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="235fd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="235fd-136">CommonParameters</span></span>
<span data-ttu-id="235fd-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="235fd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="235fd-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="235fd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="235fd-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="235fd-139">INPUTS</span></span>

### <span data-ttu-id="235fd-140">System.String</span><span class="sxs-lookup"><span data-stu-id="235fd-140">System.String</span></span>

## <span data-ttu-id="235fd-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="235fd-141">OUTPUTS</span></span>

### <span data-ttu-id="235fd-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="235fd-142">System.Boolean</span></span>

## <span data-ttu-id="235fd-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="235fd-143">NOTES</span></span>

## <span data-ttu-id="235fd-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="235fd-144">RELATED LINKS</span></span>
