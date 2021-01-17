---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: 5cd9a76f71f63b1d16003cce467d2d91eddc5b04
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466494"
---
# <span data-ttu-id="61a90-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="61a90-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="61a90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61a90-102">SYNOPSIS</span></span>
<span data-ttu-id="61a90-103">A hozzárendeléshez elérhető összes Azure RBAC-szerepkört sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="61a90-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="61a90-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="61a90-104">SYNTAX</span></span>

### <span data-ttu-id="61a90-105">RoleDefinitionNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="61a90-105">RoleDefinitionNameParameterSet (Default)</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61a90-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61a90-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61a90-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="61a90-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61a90-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="61a90-108">DESCRIPTION</span></span>
<span data-ttu-id="61a90-109">A Get-AzRoleDefinition a szerepkör nevével a megfelelő parancs segítségével megtekintheti annak részleteit.</span><span class="sxs-lookup"><span data-stu-id="61a90-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="61a90-110">Ha meg kell vizsgálnia az egyes műveleteket, amelyekhez egy szerepkör hozzáférést biztosít, tekintse át a szerepkör Műveletek és NotActions tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="61a90-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="61a90-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="61a90-111">EXAMPLES</span></span>

### <span data-ttu-id="61a90-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="61a90-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="61a90-113">Az Olvasó szerepkördefiníciójának lekérte</span><span class="sxs-lookup"><span data-stu-id="61a90-113">Get the Reader role definition</span></span>

### <span data-ttu-id="61a90-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="61a90-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="61a90-115">Az RBAC szerepkördefiníciók listája</span><span class="sxs-lookup"><span data-stu-id="61a90-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="61a90-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61a90-116">PARAMETERS</span></span>

### <span data-ttu-id="61a90-117">-Custom</span><span class="sxs-lookup"><span data-stu-id="61a90-117">-Custom</span></span>
<span data-ttu-id="61a90-118">Ha meg van adva, akkor csak az egyénileg létrehozott szerepköröket jeleníti meg a címtárban.</span><span class="sxs-lookup"><span data-stu-id="61a90-118">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="61a90-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61a90-119">-DefaultProfile</span></span>
<span data-ttu-id="61a90-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="61a90-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61a90-121">-Id</span><span class="sxs-lookup"><span data-stu-id="61a90-121">-Id</span></span>
<span data-ttu-id="61a90-122">Szerepkör-definíció azonosítója.</span><span class="sxs-lookup"><span data-stu-id="61a90-122">Role definition Id.</span></span>

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

### <span data-ttu-id="61a90-123">-Name</span><span class="sxs-lookup"><span data-stu-id="61a90-123">-Name</span></span>
<span data-ttu-id="61a90-124">Szerepkör-definíció neve.</span><span class="sxs-lookup"><span data-stu-id="61a90-124">Role definition name.</span></span>
<span data-ttu-id="61a90-125">Például olvasó, közreműködő, virtuális gép közreműködője.</span><span class="sxs-lookup"><span data-stu-id="61a90-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="61a90-126">-Scope</span><span class="sxs-lookup"><span data-stu-id="61a90-126">-Scope</span></span>
<span data-ttu-id="61a90-127">Szerepkör-definíció hatóköre.</span><span class="sxs-lookup"><span data-stu-id="61a90-127">Role definition scope.</span></span>

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

### <span data-ttu-id="61a90-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a90-128">CommonParameters</span></span>
<span data-ttu-id="61a90-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61a90-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a90-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61a90-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a90-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61a90-131">INPUTS</span></span>

### <span data-ttu-id="61a90-132">System.String</span><span class="sxs-lookup"><span data-stu-id="61a90-132">System.String</span></span>

### <span data-ttu-id="61a90-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="61a90-133">System.Guid</span></span>

### <span data-ttu-id="61a90-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="61a90-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="61a90-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61a90-135">OUTPUTS</span></span>

### <span data-ttu-id="61a90-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="61a90-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="61a90-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="61a90-137">NOTES</span></span>
<span data-ttu-id="61a90-138">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, telepítés</span><span class="sxs-lookup"><span data-stu-id="61a90-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="61a90-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61a90-139">RELATED LINKS</span></span>

[<span data-ttu-id="61a90-140">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="61a90-140">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="61a90-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="61a90-141">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="61a90-142">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="61a90-142">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="61a90-143">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="61a90-143">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

