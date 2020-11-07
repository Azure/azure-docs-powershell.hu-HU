---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 219ff64309cc11fd5e65d614f67d2d531737c8b1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849914"
---
# <span data-ttu-id="b6dd0-101">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b6dd0-101">Get-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="b6dd0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6dd0-102">SYNOPSIS</span></span>
<span data-ttu-id="b6dd0-103">Felsorolja a hozzárendeléshez elérhető összes Azure RBAC szerepkört.</span><span class="sxs-lookup"><span data-stu-id="b6dd0-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6dd0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6dd0-104">SYNTAX</span></span>

### <span data-ttu-id="b6dd0-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6dd0-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6dd0-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6dd0-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6dd0-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6dd0-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6dd0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6dd0-108">DESCRIPTION</span></span>
<span data-ttu-id="b6dd0-109">A Get-AzureRmRoleDefinition parancs segítségével megtekintheti annak részleteit.</span><span class="sxs-lookup"><span data-stu-id="b6dd0-109">Use the Get-AzureRmRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="b6dd0-110">Ha meg szeretné vizsgálni azokat az egyes műveleteket, amelyeket egy szerepkör hozzáférést biztosít, tekintse át a szerepkörben szereplő műveleteket és a beállításoknak megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="b6dd0-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="b6dd0-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b6dd0-111">EXAMPLES</span></span>

### <span data-ttu-id="b6dd0-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b6dd0-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRoleDefinition -Name Reader
```

<span data-ttu-id="b6dd0-113">Az olvasó szerepkör-definíciójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="b6dd0-113">Get the Reader role definition</span></span>

### <span data-ttu-id="b6dd0-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="b6dd0-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRoleDefinition
```

<span data-ttu-id="b6dd0-115">A RBAC minden szerepkör-definíciójának listája</span><span class="sxs-lookup"><span data-stu-id="b6dd0-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="b6dd0-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6dd0-116">PARAMETERS</span></span>

### <span data-ttu-id="b6dd0-117">-Custom</span><span class="sxs-lookup"><span data-stu-id="b6dd0-117">-Custom</span></span>
<span data-ttu-id="b6dd0-118">Ha meg van adva, akkor csak az egyéni létrehozott szerepköröket jeleníti meg a címtárban.</span><span class="sxs-lookup"><span data-stu-id="b6dd0-118">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="b6dd0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6dd0-119">-DefaultProfile</span></span>
<span data-ttu-id="b6dd0-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b6dd0-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6dd0-121">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="b6dd0-121">-Id</span></span>
<span data-ttu-id="b6dd0-122">Szerepkör-definíciós azonosító</span><span class="sxs-lookup"><span data-stu-id="b6dd0-122">Role definition Id.</span></span>

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

### <span data-ttu-id="b6dd0-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b6dd0-123">-Name</span></span>
<span data-ttu-id="b6dd0-124">Szerepkör-definíciós név.</span><span class="sxs-lookup"><span data-stu-id="b6dd0-124">Role definition name.</span></span>
<span data-ttu-id="b6dd0-125">Például olvasó, közreműködő, Virtual Machine közreműködő.</span><span class="sxs-lookup"><span data-stu-id="b6dd0-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="b6dd0-126">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="b6dd0-126">-Scope</span></span>
<span data-ttu-id="b6dd0-127">Szerepkör-definíciós hatókör</span><span class="sxs-lookup"><span data-stu-id="b6dd0-127">Role definition scope.</span></span>

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

### <span data-ttu-id="b6dd0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6dd0-128">CommonParameters</span></span>
<span data-ttu-id="b6dd0-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6dd0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6dd0-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6dd0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6dd0-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6dd0-131">INPUTS</span></span>

### <span data-ttu-id="b6dd0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b6dd0-132">System.String</span></span>
<span data-ttu-id="b6dd0-133">Paraméterek: scope (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b6dd0-133">Parameters: Scope (ByValue)</span></span>

### <span data-ttu-id="b6dd0-134">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b6dd0-134">System.Guid</span></span>

### <span data-ttu-id="b6dd0-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b6dd0-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b6dd0-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6dd0-136">OUTPUTS</span></span>

### <span data-ttu-id="b6dd0-137">Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b6dd0-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="b6dd0-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6dd0-138">NOTES</span></span>
<span data-ttu-id="b6dd0-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="b6dd0-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b6dd0-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6dd0-140">RELATED LINKS</span></span>

[<span data-ttu-id="b6dd0-141">Új – AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b6dd0-141">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="b6dd0-142">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b6dd0-142">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="b6dd0-143">Új – AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b6dd0-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="b6dd0-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b6dd0-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

