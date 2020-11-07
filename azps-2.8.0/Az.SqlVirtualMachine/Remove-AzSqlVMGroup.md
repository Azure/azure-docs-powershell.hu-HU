---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
ms.openlocfilehash: 7af4302a17d15ba539a726ce84ef47bb1d574609
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839539"
---
# <span data-ttu-id="ac1b2-101">Remove-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="ac1b2-101">Remove-AzSqlVMGroup</span></span>

## <span data-ttu-id="ac1b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac1b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ac1b2-103">SQL-virtuálisgép-csoport törlése</span><span class="sxs-lookup"><span data-stu-id="ac1b2-103">Deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="ac1b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac1b2-104">SYNTAX</span></span>

### <span data-ttu-id="ac1b2-105">ParamaterList (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ac1b2-105">ParamaterList (Default)</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac1b2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ac1b2-106">InputObject</span></span>
```
Remove-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac1b2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac1b2-107">ResourceId</span></span>
```
Remove-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac1b2-108">név</span><span class="sxs-lookup"><span data-stu-id="ac1b2-108">Name</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac1b2-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac1b2-109">DESCRIPTION</span></span>
<span data-ttu-id="ac1b2-110">A Remove-AzSqlVMGroup parancsmag törli a virtuális SQL Machine-csoportot.</span><span class="sxs-lookup"><span data-stu-id="ac1b2-110">The Remove-AzSqlVMGroup cmdlet deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="ac1b2-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ac1b2-111">EXAMPLES</span></span>

### <span data-ttu-id="ac1b2-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ac1b2-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
```

<span data-ttu-id="ac1b2-113">Törli az Azure SQL virtuálisgép-csoport "teszt-csoport" csoportját az erőforrás csoport ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ac1b2-113">Deletes the Azure SQL virtual machine group "test-group" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="ac1b2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac1b2-114">PARAMETERS</span></span>

### <span data-ttu-id="ac1b2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac1b2-115">-AsJob</span></span>
<span data-ttu-id="ac1b2-116">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="ac1b2-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ac1b2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac1b2-117">-DefaultProfile</span></span>
<span data-ttu-id="ac1b2-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac1b2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac1b2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac1b2-119">-InputObject</span></span>
<span data-ttu-id="ac1b2-120">Virtuális SQL Machine-objektum.</span><span class="sxs-lookup"><span data-stu-id="ac1b2-120">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="ac1b2-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ac1b2-121">-Name</span></span>
<span data-ttu-id="ac1b2-122">Az SQL virtuálisgép-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ac1b2-122">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="ac1b2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac1b2-123">-PassThru</span></span>
<span data-ttu-id="ac1b2-124">Azt adja meg, hogy a törölt erőforrás kimenete a parancsmag-végrehajtás végén történjen-e.</span><span class="sxs-lookup"><span data-stu-id="ac1b2-124">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="ac1b2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac1b2-125">-ResourceGroupName</span></span>
<span data-ttu-id="ac1b2-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ac1b2-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="ac1b2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac1b2-127">-ResourceId</span></span>
<span data-ttu-id="ac1b2-128">SQL virtuálisgép-csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ac1b2-128">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="ac1b2-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ac1b2-129">-Confirm</span></span>
<span data-ttu-id="ac1b2-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ac1b2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac1b2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac1b2-131">-WhatIf</span></span>
<span data-ttu-id="ac1b2-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ac1b2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac1b2-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ac1b2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac1b2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac1b2-134">CommonParameters</span></span>
<span data-ttu-id="ac1b2-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac1b2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac1b2-136">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ac1b2-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac1b2-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac1b2-137">INPUTS</span></span>

### <span data-ttu-id="ac1b2-138">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="ac1b2-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="ac1b2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ac1b2-139">System.String</span></span>

## <span data-ttu-id="ac1b2-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac1b2-140">OUTPUTS</span></span>

### <span data-ttu-id="ac1b2-141">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="ac1b2-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="ac1b2-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac1b2-142">NOTES</span></span>

## <span data-ttu-id="ac1b2-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac1b2-143">RELATED LINKS</span></span>
