---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/remove-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
ms.openlocfilehash: d9d5ee7159f5a7f237bd9194051c99801481f1d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931610"
---
# <span data-ttu-id="371d7-101">Remove-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="371d7-101">Remove-AzSqlVMGroup</span></span>

## <span data-ttu-id="371d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="371d7-102">SYNOPSIS</span></span>
<span data-ttu-id="371d7-103">Töröl egy sql virtuális gépcsoportot.</span><span class="sxs-lookup"><span data-stu-id="371d7-103">Deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="371d7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="371d7-104">SYNTAX</span></span>

### <span data-ttu-id="371d7-105">Paraméterlista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="371d7-105">ParamaterList (Default)</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="371d7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="371d7-106">InputObject</span></span>
```
Remove-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="371d7-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="371d7-107">ResourceId</span></span>
```
Remove-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="371d7-108">név</span><span class="sxs-lookup"><span data-stu-id="371d7-108">Name</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="371d7-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="371d7-109">DESCRIPTION</span></span>
<span data-ttu-id="371d7-110">A Remove-AzSqlVMGroup parancsmag töröl egy sql virtuális gépcsoportot.</span><span class="sxs-lookup"><span data-stu-id="371d7-110">The Remove-AzSqlVMGroup cmdlet deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="371d7-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="371d7-111">EXAMPLES</span></span>

### <span data-ttu-id="371d7-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="371d7-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
```

<span data-ttu-id="371d7-113">Törli az Azure SQL virtuális gép "tesztcsoport" csoportját az ResourceGroup01 erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="371d7-113">Deletes the Azure SQL virtual machine group "test-group" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="371d7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="371d7-114">PARAMETERS</span></span>

### <span data-ttu-id="371d7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="371d7-115">-AsJob</span></span>
<span data-ttu-id="371d7-116">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="371d7-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="371d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="371d7-117">-DefaultProfile</span></span>
<span data-ttu-id="371d7-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="371d7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="371d7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="371d7-119">-InputObject</span></span>
<span data-ttu-id="371d7-120">SQL virtuális gépobjektum.</span><span class="sxs-lookup"><span data-stu-id="371d7-120">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: InputObject
Aliases: SqlVMGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="371d7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="371d7-121">-Name</span></span>
<span data-ttu-id="371d7-122">SQL virtuális gépcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="371d7-122">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="371d7-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="371d7-123">-PassThru</span></span>
<span data-ttu-id="371d7-124">Azt adja meg, hogy a parancsmag végrehajtása után kimenetként adja-e meg a törölt erőforrást.</span><span class="sxs-lookup"><span data-stu-id="371d7-124">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="371d7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="371d7-125">-ResourceGroupName</span></span>
<span data-ttu-id="371d7-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="371d7-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="371d7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="371d7-127">-ResourceId</span></span>
<span data-ttu-id="371d7-128">SQL virtuális gépcsoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="371d7-128">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="371d7-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="371d7-129">-Confirm</span></span>
<span data-ttu-id="371d7-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="371d7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="371d7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="371d7-131">-WhatIf</span></span>
<span data-ttu-id="371d7-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="371d7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="371d7-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="371d7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="371d7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="371d7-134">CommonParameters</span></span>
<span data-ttu-id="371d7-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="371d7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="371d7-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="371d7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="371d7-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="371d7-137">INPUTS</span></span>

### <span data-ttu-id="371d7-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="371d7-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="371d7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="371d7-139">System.String</span></span>

## <span data-ttu-id="371d7-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="371d7-140">OUTPUTS</span></span>

### <span data-ttu-id="371d7-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="371d7-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="371d7-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="371d7-142">NOTES</span></span>

## <span data-ttu-id="371d7-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="371d7-143">RELATED LINKS</span></span>
