---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
ms.openlocfilehash: 4c4bbd9dd845caa263f5dd333228d71e3f2e65b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679040"
---
# <span data-ttu-id="407e2-101">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="407e2-101">Get-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="407e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="407e2-102">SYNOPSIS</span></span>
<span data-ttu-id="407e2-103">Felsorolja a hozzárendeléshez elérhető összes Azure RBAC szerepkört.</span><span class="sxs-lookup"><span data-stu-id="407e2-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="407e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="407e2-104">SYNTAX</span></span>

### <span data-ttu-id="407e2-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="407e2-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="407e2-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="407e2-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="407e2-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="407e2-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="407e2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="407e2-108">DESCRIPTION</span></span>
<span data-ttu-id="407e2-109">A Get-AzureRmRoleDefinition parancs segítségével megtekintheti annak részleteit.</span><span class="sxs-lookup"><span data-stu-id="407e2-109">Use the Get-AzureRmRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="407e2-110">Ha meg szeretné vizsgálni azokat az egyes műveleteket, amelyeket egy szerepkör hozzáférést biztosít, tekintse át a szerepkörben szereplő műveleteket és a beállításoknak megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="407e2-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="407e2-111">Példák</span><span class="sxs-lookup"><span data-stu-id="407e2-111">EXAMPLES</span></span>

### <span data-ttu-id="407e2-112">--------------------------Példa 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="407e2-112">--------------------------  Example 1  --------------------------</span></span>
```
PS C:\> Get-AzureRmRoleDefinition -Name Reader
```

<span data-ttu-id="407e2-113">Az olvasó szerepkör-definíciójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="407e2-113">Get the Reader role definition</span></span>

### <span data-ttu-id="407e2-114">--------------------------Példa 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="407e2-114">--------------------------  Example 2  --------------------------</span></span>
```
PS C:\> Get-AzureRmRoleDefinition
```

<span data-ttu-id="407e2-115">A RBAC minden szerepkör-definíciójának listája</span><span class="sxs-lookup"><span data-stu-id="407e2-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="407e2-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="407e2-116">PARAMETERS</span></span>

### <span data-ttu-id="407e2-117">-AtScopeAndBelow</span><span class="sxs-lookup"><span data-stu-id="407e2-117">-AtScopeAndBelow</span></span>
<span data-ttu-id="407e2-118">Ha meg van adva, az összes szerepkör-definíció megjelenik.</span><span class="sxs-lookup"><span data-stu-id="407e2-118">If specified, displays all role definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RoleDefinitionNameParameterSet, RoleDefinitionCustomParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="407e2-119">-Custom</span><span class="sxs-lookup"><span data-stu-id="407e2-119">-Custom</span></span>
<span data-ttu-id="407e2-120">Ha meg van adva, akkor csak az egyéni létrehozott szerepköröket jeleníti meg a címtárban.</span><span class="sxs-lookup"><span data-stu-id="407e2-120">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="407e2-121">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="407e2-121">-Id</span></span>
<span data-ttu-id="407e2-122">Szerepkör-definíciós azonosító</span><span class="sxs-lookup"><span data-stu-id="407e2-122">Role definition Id.</span></span>

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

### <span data-ttu-id="407e2-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="407e2-123">-Name</span></span>
<span data-ttu-id="407e2-124">Szerepkör-definíciós név.</span><span class="sxs-lookup"><span data-stu-id="407e2-124">Role definition name.</span></span>
<span data-ttu-id="407e2-125">Például olvasó, közreműködő, Virtual Machine közreműködő.</span><span class="sxs-lookup"><span data-stu-id="407e2-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="407e2-126">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="407e2-126">-Scope</span></span>
<span data-ttu-id="407e2-127">Szerepkör-definíciós hatókör</span><span class="sxs-lookup"><span data-stu-id="407e2-127">Role definition scope.</span></span>

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

### <span data-ttu-id="407e2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="407e2-128">-DefaultProfile</span></span>
<span data-ttu-id="407e2-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="407e2-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="407e2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="407e2-130">CommonParameters</span></span>
<span data-ttu-id="407e2-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="407e2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="407e2-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="407e2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="407e2-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="407e2-133">INPUTS</span></span>

### <span data-ttu-id="407e2-134">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="407e2-134">String</span></span>
<span data-ttu-id="407e2-135">A "scope" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="407e2-135">Parameter 'Scope' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="407e2-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="407e2-136">OUTPUTS</span></span>

### <span data-ttu-id="407e2-137">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. Resources. PSRoleDefinition]</span><span class="sxs-lookup"><span data-stu-id="407e2-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition]</span></span>

## <span data-ttu-id="407e2-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="407e2-138">NOTES</span></span>
<span data-ttu-id="407e2-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="407e2-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="407e2-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="407e2-140">RELATED LINKS</span></span>

[<span data-ttu-id="407e2-141">Új – AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="407e2-141">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="407e2-142">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="407e2-142">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="407e2-143">Új – AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="407e2-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="407e2-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="407e2-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

