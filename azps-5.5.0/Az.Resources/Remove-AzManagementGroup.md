---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: ce2ccd21d7adecdf9602d29837295ad2ca65c952
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169106"
---
# <span data-ttu-id="d8343-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d8343-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="d8343-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8343-102">SYNOPSIS</span></span>
<span data-ttu-id="d8343-103">Felügyeleti csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d8343-103">Removes a Management Group</span></span>

## <span data-ttu-id="d8343-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d8343-104">SYNTAX</span></span>

### <span data-ttu-id="d8343-105">GroupOperations (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d8343-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8343-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="d8343-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8343-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d8343-107">DESCRIPTION</span></span>
<span data-ttu-id="d8343-108">A **Remove-AzManagementGroup** parancsmag töröl egy felügyeleti csoportot.</span><span class="sxs-lookup"><span data-stu-id="d8343-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="d8343-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d8343-109">EXAMPLES</span></span>

### <span data-ttu-id="d8343-110">1. példa: Felügyeleti csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d8343-110">Example 1: Remove a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="d8343-111">2. példa: Felügyeleti csoport eltávolítása a PSManagementGroup-objektum kivezetésével</span><span class="sxs-lookup"><span data-stu-id="d8343-111">Example 2: Remove a Management Group by piping PSManagementGroup Object</span></span>
```powershell
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="d8343-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8343-112">PARAMETERS</span></span>

### <span data-ttu-id="d8343-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8343-113">-DefaultProfile</span></span>
<span data-ttu-id="d8343-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8343-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8343-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="d8343-115">-GroupName</span></span>
<span data-ttu-id="d8343-116">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="d8343-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8343-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8343-117">-InputObject</span></span>
<span data-ttu-id="d8343-118">Input Object from the Get call</span><span class="sxs-lookup"><span data-stu-id="d8343-118">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8343-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8343-119">-PassThru</span></span>
<span data-ttu-id="d8343-120">Sikeres `true` végrehajtás visszaküldése</span><span class="sxs-lookup"><span data-stu-id="d8343-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="d8343-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8343-121">-Confirm</span></span>
<span data-ttu-id="d8343-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d8343-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8343-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8343-123">-WhatIf</span></span>
<span data-ttu-id="d8343-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d8343-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8343-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d8343-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8343-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8343-126">CommonParameters</span></span>
<span data-ttu-id="d8343-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8343-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8343-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8343-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8343-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8343-129">INPUTS</span></span>

### <span data-ttu-id="d8343-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d8343-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="d8343-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8343-131">OUTPUTS</span></span>

### <span data-ttu-id="d8343-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d8343-132">System.Boolean</span></span>

## <span data-ttu-id="d8343-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d8343-133">NOTES</span></span>

## <span data-ttu-id="d8343-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8343-134">RELATED LINKS</span></span>
