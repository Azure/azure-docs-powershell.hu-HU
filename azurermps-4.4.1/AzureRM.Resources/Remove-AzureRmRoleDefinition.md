---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
ms.openlocfilehash: 476555b271d58f8e594f0cae1422bcdde1fc46e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679031"
---
# <span data-ttu-id="b7ef4-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b7ef4-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="b7ef4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7ef4-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ef4-103">Egyéni szerepkör törlése az Azure RBAC-ban.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="b7ef4-104">A törlendő szerepkör a szerepkör ID tulajdonságával van megadva.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="b7ef4-105">A törlés meghiúsul, ha a meglévő szerepkör-hozzárendelések az egyéni szerepkörre vonatkoznak.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7ef4-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7ef4-106">SYNTAX</span></span>

### <span data-ttu-id="b7ef4-107">RoleDefinitionIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b7ef4-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7ef4-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7ef4-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7ef4-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7ef4-109">DESCRIPTION</span></span>
<span data-ttu-id="b7ef4-110">A Remove-AzureRmRoleDefinition parancsmag egy egyéni szerepkört töröl az Azure Role-Based Access-vezérlőben.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-110">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="b7ef4-111">Az egyéni szerepkör törléséhez egy meglévő egyéni szerepkör azonosító paraméterét kell megadni.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-111">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="b7ef4-112">A Remove-AzureRmRoleDefinition alapértelmezés szerint megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-112">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="b7ef4-113">A kérdés elrejtéséhez használja az erő paramétert.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-113">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="b7ef4-114">Ha a törölni kívánt egyéni szerepkörre már vannak meglévő szerepkör-hozzárendelések, akkor a törlés meghiúsul.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-114">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="b7ef4-115">Példák</span><span class="sxs-lookup"><span data-stu-id="b7ef4-115">EXAMPLES</span></span>

### <span data-ttu-id="b7ef4-116">--------------------------Példa 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b7ef4-116">--------------------------  Example 1  --------------------------</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="b7ef4-117">--------------------------Példa 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b7ef4-117">--------------------------  Example 2  --------------------------</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="b7ef4-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7ef4-118">PARAMETERS</span></span>

### <span data-ttu-id="b7ef4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b7ef4-119">-Force</span></span>
<span data-ttu-id="b7ef4-120">Ha be van állítva, nem kér megerősítést az egyéni szerepkör törlése előtt.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-120">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="b7ef4-121">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="b7ef4-121">-Id</span></span>
<span data-ttu-id="b7ef4-122">A törlendő Szerepdefiníció azonosítója</span><span class="sxs-lookup"><span data-stu-id="b7ef4-122">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="b7ef4-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b7ef4-123">-Name</span></span>
<span data-ttu-id="b7ef4-124">Annak a szerepkör-definíciónak a neve, amelyet törölni szeretne.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-124">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="b7ef4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7ef4-125">-PassThru</span></span>
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

### <span data-ttu-id="b7ef4-126">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="b7ef4-126">-Scope</span></span>
<span data-ttu-id="b7ef4-127">Szerepkör-definíciós hatókör</span><span class="sxs-lookup"><span data-stu-id="b7ef4-127">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7ef4-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b7ef4-128">-Confirm</span></span>
<span data-ttu-id="b7ef4-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7ef4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7ef4-130">-WhatIf</span></span>
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

### <span data-ttu-id="b7ef4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ef4-131">-DefaultProfile</span></span>
<span data-ttu-id="b7ef4-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ef4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ef4-133">CommonParameters</span></span>
<span data-ttu-id="b7ef4-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7ef4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ef4-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7ef4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ef4-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7ef4-136">INPUTS</span></span>

## <span data-ttu-id="b7ef4-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7ef4-137">OUTPUTS</span></span>

### <span data-ttu-id="b7ef4-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b7ef4-138">System.Boolean</span></span>

## <span data-ttu-id="b7ef4-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7ef4-139">NOTES</span></span>
<span data-ttu-id="b7ef4-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="b7ef4-140">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b7ef4-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7ef4-141">RELATED LINKS</span></span>

[<span data-ttu-id="b7ef4-142">Új – AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b7ef4-142">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="b7ef4-143">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b7ef4-143">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="b7ef4-144">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b7ef4-144">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

