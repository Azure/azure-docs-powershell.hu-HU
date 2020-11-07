---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: f7ed4b70b3b0575b41f081e088e55944b46656aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669323"
---
# <span data-ttu-id="becb6-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="becb6-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="becb6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="becb6-102">SYNOPSIS</span></span>
<span data-ttu-id="becb6-103">Egyéni szerepkör törlése az Azure RBAC-ban.</span><span class="sxs-lookup"><span data-stu-id="becb6-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="becb6-104">A törlendő szerepkör a szerepkör ID tulajdonságával van megadva.</span><span class="sxs-lookup"><span data-stu-id="becb6-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="becb6-105">A törlés meghiúsul, ha a meglévő szerepkör-hozzárendelések az egyéni szerepkörre vonatkoznak.</span><span class="sxs-lookup"><span data-stu-id="becb6-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="becb6-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="becb6-106">SYNTAX</span></span>

### <span data-ttu-id="becb6-107">RoleDefinitionIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="becb6-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="becb6-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="becb6-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="becb6-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="becb6-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="becb6-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="becb6-110">DESCRIPTION</span></span>
<span data-ttu-id="becb6-111">A Remove-AzRoleDefinition parancsmag egy egyéni szerepkört töröl az Azure Role-Based Access-vezérlőben.</span><span class="sxs-lookup"><span data-stu-id="becb6-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="becb6-112">Az egyéni szerepkör törléséhez egy meglévő egyéni szerepkör azonosító paraméterét kell megadni.</span><span class="sxs-lookup"><span data-stu-id="becb6-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="becb6-113">A Remove-AzRoleDefinition alapértelmezés szerint megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="becb6-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="becb6-114">A kérdés elrejtéséhez használja az erő paramétert.</span><span class="sxs-lookup"><span data-stu-id="becb6-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="becb6-115">Ha a törölni kívánt egyéni szerepkörre már vannak meglévő szerepkör-hozzárendelések, akkor a törlés meghiúsul.</span><span class="sxs-lookup"><span data-stu-id="becb6-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="becb6-116">Példák</span><span class="sxs-lookup"><span data-stu-id="becb6-116">EXAMPLES</span></span>

### <span data-ttu-id="becb6-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="becb6-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="becb6-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="becb6-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="becb6-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="becb6-119">PARAMETERS</span></span>

### <span data-ttu-id="becb6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="becb6-120">-DefaultProfile</span></span>
<span data-ttu-id="becb6-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="becb6-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="becb6-122">-Force</span><span class="sxs-lookup"><span data-stu-id="becb6-122">-Force</span></span>
<span data-ttu-id="becb6-123">Ha be van állítva, nem kér megerősítést az egyéni szerepkör törlése előtt.</span><span class="sxs-lookup"><span data-stu-id="becb6-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="becb6-124">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="becb6-124">-Id</span></span>
<span data-ttu-id="becb6-125">A törlendő Szerepdefiníció azonosítója</span><span class="sxs-lookup"><span data-stu-id="becb6-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="becb6-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="becb6-126">-InputObject</span></span>
<span data-ttu-id="becb6-127">Az eltávolítandó szerepkör-definíciót jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="becb6-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="becb6-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="becb6-128">-Name</span></span>
<span data-ttu-id="becb6-129">Annak a szerepkör-definíciónak a neve, amelyet törölni szeretne.</span><span class="sxs-lookup"><span data-stu-id="becb6-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="becb6-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="becb6-130">-PassThru</span></span>
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

### <span data-ttu-id="becb6-131">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="becb6-131">-Scope</span></span>
<span data-ttu-id="becb6-132">Szerepkör-definíciós hatókör</span><span class="sxs-lookup"><span data-stu-id="becb6-132">Role definition scope.</span></span>

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

### <span data-ttu-id="becb6-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="becb6-133">-Confirm</span></span>
<span data-ttu-id="becb6-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="becb6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="becb6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="becb6-135">-WhatIf</span></span>
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

### <span data-ttu-id="becb6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="becb6-136">CommonParameters</span></span>
<span data-ttu-id="becb6-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="becb6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="becb6-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="becb6-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="becb6-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="becb6-139">INPUTS</span></span>

### <span data-ttu-id="becb6-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="becb6-140">System.Guid</span></span>

### <span data-ttu-id="becb6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="becb6-141">System.String</span></span>

### <span data-ttu-id="becb6-142">Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="becb6-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="becb6-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="becb6-143">OUTPUTS</span></span>

### <span data-ttu-id="becb6-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="becb6-144">System.Boolean</span></span>

## <span data-ttu-id="becb6-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="becb6-145">NOTES</span></span>
<span data-ttu-id="becb6-146">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="becb6-146">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="becb6-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="becb6-147">RELATED LINKS</span></span>

[<span data-ttu-id="becb6-148">Új – AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="becb6-148">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="becb6-149">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="becb6-149">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="becb6-150">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="becb6-150">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

