---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: d4ce9ef88f7043a369d8e566de75651944ea1e88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014901"
---
# <span data-ttu-id="f1efc-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f1efc-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="f1efc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1efc-102">SYNOPSIS</span></span>
<span data-ttu-id="f1efc-103">Töröl egy egyéni szerepkört az Azure RBAC-ban.</span><span class="sxs-lookup"><span data-stu-id="f1efc-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="f1efc-104">A törölt szerepkört a szerepkör Azonosító tulajdonságával lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="f1efc-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="f1efc-105">A törlés sikertelen lesz, ha az egyéni szerepkörben már vannak szerepkör-hozzárendelések.</span><span class="sxs-lookup"><span data-stu-id="f1efc-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="f1efc-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f1efc-106">SYNTAX</span></span>

### <span data-ttu-id="f1efc-107">RoleDefinitionIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f1efc-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1efc-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1efc-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1efc-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1efc-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1efc-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f1efc-110">DESCRIPTION</span></span>
<span data-ttu-id="f1efc-111">A Remove-AzRoleDefinition parancsmag töröl egy egyéni szerepkört az Azure Role-Based Hozzáférés-vezérlésben.</span><span class="sxs-lookup"><span data-stu-id="f1efc-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="f1efc-112">Adja meg egy meglévő egyéni szerepkör azonosító paraméterét az egyéni szerepkör törléséhez.</span><span class="sxs-lookup"><span data-stu-id="f1efc-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="f1efc-113">Alapértelmezés szerint Remove-AzRoleDefinition megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f1efc-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="f1efc-114">A kérdés elrejtését az Kényszerítés paraméter használatával tilthatja le.</span><span class="sxs-lookup"><span data-stu-id="f1efc-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="f1efc-115">Ha az egyéni szerepkör törléséhez már vannak szerepkör-hozzárendelések, a törlés sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="f1efc-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="f1efc-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f1efc-116">EXAMPLES</span></span>

### <span data-ttu-id="f1efc-117">1. példa</span><span class="sxs-lookup"><span data-stu-id="f1efc-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="f1efc-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="f1efc-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="f1efc-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1efc-119">PARAMETERS</span></span>

### <span data-ttu-id="f1efc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1efc-120">-DefaultProfile</span></span>
<span data-ttu-id="f1efc-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f1efc-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1efc-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f1efc-122">-Force</span></span>
<span data-ttu-id="f1efc-123">Ha be van állítva, az egyéni szerepkör törlése előtt nem kér megerősítést</span><span class="sxs-lookup"><span data-stu-id="f1efc-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="f1efc-124">-Id</span><span class="sxs-lookup"><span data-stu-id="f1efc-124">-Id</span></span>
<span data-ttu-id="f1efc-125">A törölt szerepkördefiníció azonosítója</span><span class="sxs-lookup"><span data-stu-id="f1efc-125">Id of the Role definition to be deleted</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1efc-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1efc-126">-InputObject</span></span>
<span data-ttu-id="f1efc-127">Az eltávolítható szerepkördefiníciót képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="f1efc-127">The object representing the role definition to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1efc-128">-Name</span><span class="sxs-lookup"><span data-stu-id="f1efc-128">-Name</span></span>
<span data-ttu-id="f1efc-129">A törölt szerepkördefiníció neve.</span><span class="sxs-lookup"><span data-stu-id="f1efc-129">Name of the Role definition to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1efc-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1efc-130">-PassThru</span></span>
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

### <span data-ttu-id="f1efc-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="f1efc-131">-Scope</span></span>
<span data-ttu-id="f1efc-132">Szerepkör-definíció hatóköre.</span><span class="sxs-lookup"><span data-stu-id="f1efc-132">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionIdParameterSet, RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1efc-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1efc-133">-Confirm</span></span>
<span data-ttu-id="f1efc-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f1efc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1efc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1efc-135">-WhatIf</span></span>
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

### <span data-ttu-id="f1efc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1efc-136">CommonParameters</span></span>
<span data-ttu-id="f1efc-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1efc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1efc-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1efc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1efc-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1efc-139">INPUTS</span></span>

### <span data-ttu-id="f1efc-140">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f1efc-140">System.Guid</span></span>

### <span data-ttu-id="f1efc-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f1efc-141">System.String</span></span>

### <span data-ttu-id="f1efc-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f1efc-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="f1efc-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1efc-143">OUTPUTS</span></span>

### <span data-ttu-id="f1efc-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f1efc-144">System.Boolean</span></span>

## <span data-ttu-id="f1efc-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f1efc-145">NOTES</span></span>
<span data-ttu-id="f1efc-146">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, telepítés</span><span class="sxs-lookup"><span data-stu-id="f1efc-146">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="f1efc-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1efc-147">RELATED LINKS</span></span>

[<span data-ttu-id="f1efc-148">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f1efc-148">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="f1efc-149">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f1efc-149">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="f1efc-150">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f1efc-150">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

