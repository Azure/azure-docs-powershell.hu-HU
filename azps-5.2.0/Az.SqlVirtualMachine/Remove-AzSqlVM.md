---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 4478ec96cd7354a404a736ddd0f305cba5675b26
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334433"
---
# <span data-ttu-id="f9160-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="f9160-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="f9160-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9160-102">SYNOPSIS</span></span>
<span data-ttu-id="f9160-103">Töröl egy sql virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="f9160-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="f9160-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f9160-104">SYNTAX</span></span>

### <span data-ttu-id="f9160-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f9160-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9160-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f9160-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9160-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9160-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9160-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f9160-108">DESCRIPTION</span></span>
<span data-ttu-id="f9160-109">A Remove-AzSqlVM parancsmag töröl egy sql virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="f9160-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="f9160-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f9160-110">EXAMPLES</span></span>

### <span data-ttu-id="f9160-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="f9160-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="f9160-112">Törli az Azure SQL virtuális gép "vm" a ResourceGroup01 erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="f9160-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="f9160-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9160-113">PARAMETERS</span></span>

### <span data-ttu-id="f9160-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9160-114">-AsJob</span></span>
<span data-ttu-id="f9160-115">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="f9160-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f9160-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9160-116">-DefaultProfile</span></span>
<span data-ttu-id="f9160-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9160-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9160-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9160-118">-InputObject</span></span>
<span data-ttu-id="f9160-119">SQL virtuális gépobjektum.</span><span class="sxs-lookup"><span data-stu-id="f9160-119">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: InputObject
Aliases: SqlVM

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9160-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f9160-120">-Name</span></span>
<span data-ttu-id="f9160-121">SQL virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="f9160-121">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9160-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9160-122">-PassThru</span></span>
<span data-ttu-id="f9160-123">Azt adja meg, hogy a parancsmag végrehajtása után kimenetként adja-e meg a törölt erőforrást.</span><span class="sxs-lookup"><span data-stu-id="f9160-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="f9160-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9160-124">-ResourceGroupName</span></span>
<span data-ttu-id="f9160-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f9160-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="f9160-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9160-126">-ResourceId</span></span>
<span data-ttu-id="f9160-127">SQL virtuális gép erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f9160-127">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9160-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9160-128">-Confirm</span></span>
<span data-ttu-id="f9160-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f9160-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9160-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9160-130">-WhatIf</span></span>
<span data-ttu-id="f9160-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f9160-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9160-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f9160-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9160-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9160-133">CommonParameters</span></span>
<span data-ttu-id="f9160-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9160-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9160-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9160-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9160-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f9160-136">INPUTS</span></span>

### <span data-ttu-id="f9160-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="f9160-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="f9160-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9160-138">OUTPUTS</span></span>

### <span data-ttu-id="f9160-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="f9160-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="f9160-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f9160-140">NOTES</span></span>

## <span data-ttu-id="f9160-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9160-141">RELATED LINKS</span></span>
