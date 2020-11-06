---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
ms.openlocfilehash: c1850cdc410df064a97950bb38f3734657649467
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501407"
---
# <span data-ttu-id="dbe06-101">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="dbe06-101">Get-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="dbe06-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dbe06-102">SYNOPSIS</span></span>
<span data-ttu-id="dbe06-103">Felsorolja a hozzárendeléshez elérhető összes Azure RBAC szerepkört.</span><span class="sxs-lookup"><span data-stu-id="dbe06-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbe06-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dbe06-104">SYNTAX</span></span>

### <span data-ttu-id="dbe06-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbe06-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbe06-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbe06-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dbe06-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbe06-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbe06-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="dbe06-108">DESCRIPTION</span></span>
<span data-ttu-id="dbe06-109">A Get-AzureRmRoleDefinition parancs segítségével megtekintheti annak részleteit.</span><span class="sxs-lookup"><span data-stu-id="dbe06-109">Use the Get-AzureRmRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="dbe06-110">Ha meg szeretné vizsgálni azokat az egyes műveleteket, amelyeket egy szerepkör hozzáférést biztosít, tekintse át a szerepkörben szereplő műveleteket és a beállításoknak megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="dbe06-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="dbe06-111">Példák</span><span class="sxs-lookup"><span data-stu-id="dbe06-111">EXAMPLES</span></span>

### <span data-ttu-id="dbe06-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dbe06-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRoleDefinition -Name Reader
```

<span data-ttu-id="dbe06-113">Az olvasó szerepkör-definíciójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="dbe06-113">Get the Reader role definition</span></span>

### <span data-ttu-id="dbe06-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="dbe06-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRoleDefinition
```

<span data-ttu-id="dbe06-115">A RBAC minden szerepkör-definíciójának listája</span><span class="sxs-lookup"><span data-stu-id="dbe06-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="dbe06-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dbe06-116">PARAMETERS</span></span>

### <span data-ttu-id="dbe06-117">-AtScopeAndBelow</span><span class="sxs-lookup"><span data-stu-id="dbe06-117">-AtScopeAndBelow</span></span>
<span data-ttu-id="dbe06-118">Ha meg van adva, az összes szerepkör-definíció megjelenik.</span><span class="sxs-lookup"><span data-stu-id="dbe06-118">If specified, displays all role definitions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RoleDefinitionNameParameterSet, RoleDefinitionCustomParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbe06-119">-Custom</span><span class="sxs-lookup"><span data-stu-id="dbe06-119">-Custom</span></span>
<span data-ttu-id="dbe06-120">Ha meg van adva, akkor csak az egyéni létrehozott szerepköröket jeleníti meg a címtárban.</span><span class="sxs-lookup"><span data-stu-id="dbe06-120">If specified, only displays the custom created roles in the directory.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbe06-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbe06-121">-DefaultProfile</span></span>
<span data-ttu-id="dbe06-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dbe06-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbe06-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="dbe06-123">-Id</span></span>
<span data-ttu-id="dbe06-124">Szerepkör-definíciós azonosító</span><span class="sxs-lookup"><span data-stu-id="dbe06-124">Role definition Id.</span></span>

```yaml
Type: Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbe06-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dbe06-125">-Name</span></span>
<span data-ttu-id="dbe06-126">Szerepkör-definíciós név.</span><span class="sxs-lookup"><span data-stu-id="dbe06-126">Role definition name.</span></span>
<span data-ttu-id="dbe06-127">Például olvasó, közreműködő, Virtual Machine közreműködő.</span><span class="sxs-lookup"><span data-stu-id="dbe06-127">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

```yaml
Type: String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbe06-128">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="dbe06-128">-Scope</span></span>
<span data-ttu-id="dbe06-129">Szerepkör-definíciós hatókör</span><span class="sxs-lookup"><span data-stu-id="dbe06-129">Role definition scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbe06-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbe06-130">CommonParameters</span></span>
<span data-ttu-id="dbe06-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dbe06-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbe06-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbe06-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbe06-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbe06-133">INPUTS</span></span>

### <span data-ttu-id="dbe06-134">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="dbe06-134">String</span></span>
<span data-ttu-id="dbe06-135">A "scope" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="dbe06-135">Parameter 'Scope' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="dbe06-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbe06-136">OUTPUTS</span></span>

### <span data-ttu-id="dbe06-137">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. Resources. PSRoleDefinition]</span><span class="sxs-lookup"><span data-stu-id="dbe06-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition]</span></span>

## <span data-ttu-id="dbe06-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dbe06-138">NOTES</span></span>
<span data-ttu-id="dbe06-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="dbe06-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="dbe06-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dbe06-140">RELATED LINKS</span></span>

[<span data-ttu-id="dbe06-141">Új – AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dbe06-141">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="dbe06-142">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dbe06-142">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="dbe06-143">Új – AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="dbe06-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="dbe06-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="dbe06-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

