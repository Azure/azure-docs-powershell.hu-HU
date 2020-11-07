---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
ms.openlocfilehash: fec35992f96940dc69cdb6d1777d43ca151688bc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846397"
---
# <span data-ttu-id="ec0eb-101">Remove-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="ec0eb-101">Remove-AzSqlVMGroup</span></span>

## <span data-ttu-id="ec0eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec0eb-102">SYNOPSIS</span></span>
<span data-ttu-id="ec0eb-103">SQL-virtuálisgép-csoport törlése</span><span class="sxs-lookup"><span data-stu-id="ec0eb-103">Deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="ec0eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec0eb-104">SYNTAX</span></span>

### <span data-ttu-id="ec0eb-105">ParamaterList (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ec0eb-105">ParamaterList (Default)</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec0eb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ec0eb-106">InputObject</span></span>
```
Remove-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec0eb-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec0eb-107">ResourceId</span></span>
```
Remove-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec0eb-108">név</span><span class="sxs-lookup"><span data-stu-id="ec0eb-108">Name</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec0eb-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec0eb-109">DESCRIPTION</span></span>
<span data-ttu-id="ec0eb-110">A Remove-AzSqlVMGroup parancsmag törli a virtuális SQL Machine-csoportot.</span><span class="sxs-lookup"><span data-stu-id="ec0eb-110">The Remove-AzSqlVMGroup cmdlet deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="ec0eb-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ec0eb-111">EXAMPLES</span></span>

### <span data-ttu-id="ec0eb-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ec0eb-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
```

<span data-ttu-id="ec0eb-113">Törli az Azure SQL virtuálisgép-csoport "teszt-csoport" csoportját az erőforrás csoport ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ec0eb-113">Deletes the Azure SQL virtual machine group "test-group" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="ec0eb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec0eb-114">PARAMETERS</span></span>

### <span data-ttu-id="ec0eb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec0eb-115">-AsJob</span></span>
<span data-ttu-id="ec0eb-116">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="ec0eb-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ec0eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec0eb-117">-DefaultProfile</span></span>
<span data-ttu-id="ec0eb-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec0eb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec0eb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec0eb-119">-InputObject</span></span>
<span data-ttu-id="ec0eb-120">Virtuális SQL Machine-objektum.</span><span class="sxs-lookup"><span data-stu-id="ec0eb-120">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="ec0eb-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ec0eb-121">-Name</span></span>
<span data-ttu-id="ec0eb-122">Az SQL virtuálisgép-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ec0eb-122">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="ec0eb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec0eb-123">-PassThru</span></span>
<span data-ttu-id="ec0eb-124">Azt adja meg, hogy a törölt erőforrás kimenete a parancsmag-végrehajtás végén történjen-e.</span><span class="sxs-lookup"><span data-stu-id="ec0eb-124">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="ec0eb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec0eb-125">-ResourceGroupName</span></span>
<span data-ttu-id="ec0eb-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ec0eb-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="ec0eb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec0eb-127">-ResourceId</span></span>
<span data-ttu-id="ec0eb-128">SQL virtuálisgép-csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ec0eb-128">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="ec0eb-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ec0eb-129">-Confirm</span></span>
<span data-ttu-id="ec0eb-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ec0eb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec0eb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec0eb-131">-WhatIf</span></span>
<span data-ttu-id="ec0eb-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ec0eb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec0eb-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ec0eb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec0eb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec0eb-134">CommonParameters</span></span>
<span data-ttu-id="ec0eb-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec0eb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec0eb-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ec0eb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec0eb-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec0eb-137">INPUTS</span></span>

### <span data-ttu-id="ec0eb-138">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="ec0eb-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="ec0eb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ec0eb-139">System.String</span></span>

## <span data-ttu-id="ec0eb-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec0eb-140">OUTPUTS</span></span>

### <span data-ttu-id="ec0eb-141">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="ec0eb-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="ec0eb-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec0eb-142">NOTES</span></span>

## <span data-ttu-id="ec0eb-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec0eb-143">RELATED LINKS</span></span>
