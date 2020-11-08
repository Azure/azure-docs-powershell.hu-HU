---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: 5cd9a76f71f63b1d16003cce467d2d91eddc5b04
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012021"
---
# <span data-ttu-id="23a71-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="23a71-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="23a71-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23a71-102">SYNOPSIS</span></span>
<span data-ttu-id="23a71-103">Felsorolja a hozzárendeléshez elérhető összes Azure RBAC szerepkört.</span><span class="sxs-lookup"><span data-stu-id="23a71-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="23a71-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23a71-104">SYNTAX</span></span>

### <span data-ttu-id="23a71-105">RoleDefinitionNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="23a71-105">RoleDefinitionNameParameterSet (Default)</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23a71-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23a71-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23a71-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="23a71-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23a71-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="23a71-108">DESCRIPTION</span></span>
<span data-ttu-id="23a71-109">A Get-AzRoleDefinition parancs segítségével megtekintheti annak részleteit.</span><span class="sxs-lookup"><span data-stu-id="23a71-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="23a71-110">Ha meg szeretné vizsgálni azokat az egyes műveleteket, amelyeket egy szerepkör hozzáférést biztosít, tekintse át a szerepkörben szereplő műveleteket és a beállításoknak megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="23a71-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="23a71-111">Példák</span><span class="sxs-lookup"><span data-stu-id="23a71-111">EXAMPLES</span></span>

### <span data-ttu-id="23a71-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="23a71-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="23a71-113">Az olvasó szerepkör-definíciójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="23a71-113">Get the Reader role definition</span></span>

### <span data-ttu-id="23a71-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="23a71-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="23a71-115">A RBAC minden szerepkör-definíciójának listája</span><span class="sxs-lookup"><span data-stu-id="23a71-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="23a71-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23a71-116">PARAMETERS</span></span>

### <span data-ttu-id="23a71-117">-Custom</span><span class="sxs-lookup"><span data-stu-id="23a71-117">-Custom</span></span>
<span data-ttu-id="23a71-118">Ha meg van adva, akkor csak az egyéni létrehozott szerepköröket jeleníti meg a címtárban.</span><span class="sxs-lookup"><span data-stu-id="23a71-118">If specified, only displays the custom created roles in the directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23a71-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23a71-119">-DefaultProfile</span></span>
<span data-ttu-id="23a71-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="23a71-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23a71-121">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="23a71-121">-Id</span></span>
<span data-ttu-id="23a71-122">Szerepkör-definíciós azonosító</span><span class="sxs-lookup"><span data-stu-id="23a71-122">Role definition Id.</span></span>

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

### <span data-ttu-id="23a71-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="23a71-123">-Name</span></span>
<span data-ttu-id="23a71-124">Szerepkör-definíciós név.</span><span class="sxs-lookup"><span data-stu-id="23a71-124">Role definition name.</span></span>
<span data-ttu-id="23a71-125">Például olvasó, közreműködő, Virtual Machine közreműködő.</span><span class="sxs-lookup"><span data-stu-id="23a71-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23a71-126">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="23a71-126">-Scope</span></span>
<span data-ttu-id="23a71-127">Szerepkör-definíciós hatókör</span><span class="sxs-lookup"><span data-stu-id="23a71-127">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23a71-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23a71-128">CommonParameters</span></span>
<span data-ttu-id="23a71-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23a71-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23a71-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="23a71-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23a71-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23a71-131">INPUTS</span></span>

### <span data-ttu-id="23a71-132">System. String</span><span class="sxs-lookup"><span data-stu-id="23a71-132">System.String</span></span>

### <span data-ttu-id="23a71-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="23a71-133">System.Guid</span></span>

### <span data-ttu-id="23a71-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="23a71-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="23a71-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23a71-135">OUTPUTS</span></span>

### <span data-ttu-id="23a71-136">Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="23a71-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="23a71-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23a71-137">NOTES</span></span>
<span data-ttu-id="23a71-138">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="23a71-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="23a71-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23a71-139">RELATED LINKS</span></span>

[<span data-ttu-id="23a71-140">Új – AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="23a71-140">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="23a71-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="23a71-141">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="23a71-142">Új – AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="23a71-142">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="23a71-143">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="23a71-143">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

