---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 4478ec96cd7354a404a736ddd0f305cba5675b26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185643"
---
# <span data-ttu-id="2e16f-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="2e16f-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="2e16f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e16f-102">SYNOPSIS</span></span>
<span data-ttu-id="2e16f-103">Egy virtuális SQL-gép törlése</span><span class="sxs-lookup"><span data-stu-id="2e16f-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="2e16f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e16f-104">SYNTAX</span></span>

### <span data-ttu-id="2e16f-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e16f-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e16f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2e16f-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e16f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e16f-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e16f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e16f-108">DESCRIPTION</span></span>
<span data-ttu-id="2e16f-109">A Remove-AzSqlVM parancsmag törli a virtuális SQL-gépet.</span><span class="sxs-lookup"><span data-stu-id="2e16f-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="2e16f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2e16f-110">EXAMPLES</span></span>

### <span data-ttu-id="2e16f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2e16f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="2e16f-112">Az Azure SQL Virtual Machine "VM" törlése az erőforráscsoport ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="2e16f-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="2e16f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e16f-113">PARAMETERS</span></span>

### <span data-ttu-id="2e16f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e16f-114">-AsJob</span></span>
<span data-ttu-id="2e16f-115">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="2e16f-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="2e16f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e16f-116">-DefaultProfile</span></span>
<span data-ttu-id="2e16f-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e16f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e16f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e16f-118">-InputObject</span></span>
<span data-ttu-id="2e16f-119">Virtuális SQL Machine-objektum.</span><span class="sxs-lookup"><span data-stu-id="2e16f-119">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="2e16f-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2e16f-120">-Name</span></span>
<span data-ttu-id="2e16f-121">Az SQL virtuális gép neve</span><span class="sxs-lookup"><span data-stu-id="2e16f-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="2e16f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e16f-122">-PassThru</span></span>
<span data-ttu-id="2e16f-123">Azt adja meg, hogy a törölt erőforrás kimenete a parancsmag-végrehajtás végén történjen-e.</span><span class="sxs-lookup"><span data-stu-id="2e16f-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="2e16f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e16f-124">-ResourceGroupName</span></span>
<span data-ttu-id="2e16f-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2e16f-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="2e16f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e16f-126">-ResourceId</span></span>
<span data-ttu-id="2e16f-127">SQL virtuális gép erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="2e16f-127">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="2e16f-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2e16f-128">-Confirm</span></span>
<span data-ttu-id="2e16f-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2e16f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e16f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e16f-130">-WhatIf</span></span>
<span data-ttu-id="2e16f-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2e16f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e16f-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e16f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e16f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e16f-133">CommonParameters</span></span>
<span data-ttu-id="2e16f-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e16f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e16f-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2e16f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e16f-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e16f-136">INPUTS</span></span>

### <span data-ttu-id="2e16f-137">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="2e16f-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="2e16f-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e16f-138">OUTPUTS</span></span>

### <span data-ttu-id="2e16f-139">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="2e16f-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="2e16f-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e16f-140">NOTES</span></span>

## <span data-ttu-id="2e16f-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e16f-141">RELATED LINKS</span></span>