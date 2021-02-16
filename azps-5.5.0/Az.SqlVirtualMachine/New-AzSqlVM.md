---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
ms.openlocfilehash: 764312c64ae9887a6ef4243cc20b04535afcf81f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168626"
---
# <span data-ttu-id="a872d-101">New-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="a872d-101">New-AzSqlVM</span></span>

## <span data-ttu-id="a872d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a872d-102">SYNOPSIS</span></span>
<span data-ttu-id="a872d-103">Létrehoz egy új sql virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="a872d-103">Creates a new sql virtual machine.</span></span>

## <span data-ttu-id="a872d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a872d-104">SYNTAX</span></span>

### <span data-ttu-id="a872d-105">NameParamaterList (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a872d-105">NameParamaterList (Default)</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType] <String> -Location <String> [-AsJob]
 [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a872d-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="a872d-106">NameInputObject</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-SqlVM] <AzureSqlVMModel> -Location <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a872d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a872d-107">DESCRIPTION</span></span>
<span data-ttu-id="a872d-108">A New-AzSqlVM parancsmag létrehoz egy Azure SQL virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="a872d-108">The New-AzSqlVM cmdlet creates an Azure SQL virtual machine.</span></span>

## <span data-ttu-id="a872d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a872d-109">EXAMPLES</span></span>

### <span data-ttu-id="a872d-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="a872d-110">Example 1</span></span>
```powershell
PS C:\> New-AzSqlVM  New-AzSqlVM -ResourceGroupName ResourceGroup01 -Name vm -LicenseType 'PAYG' -Sku Developer
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="a872d-111">Létrehoz egy új Azure SQL virtuális gépet név virtuális géppel az ResourceGroup01 erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="a872d-111">Creates a new Azure SQL virtual machine with name vm in the resource group ResourceGroup01</span></span> 

## <span data-ttu-id="a872d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a872d-112">PARAMETERS</span></span>

### <span data-ttu-id="a872d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a872d-113">-AsJob</span></span>
<span data-ttu-id="a872d-114">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="a872d-114">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="a872d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a872d-115">-DefaultProfile</span></span>
<span data-ttu-id="a872d-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a872d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a872d-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a872d-117">-LicenseType</span></span>
<span data-ttu-id="a872d-118">SQL virtuális gép licenctípusa.</span><span class="sxs-lookup"><span data-stu-id="a872d-118">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a872d-119">-Location</span><span class="sxs-lookup"><span data-stu-id="a872d-119">-Location</span></span>
<span data-ttu-id="a872d-120">SQL virtuális gép helye.</span><span class="sxs-lookup"><span data-stu-id="a872d-120">SQL virtual machine location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a872d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a872d-121">-Name</span></span>
<span data-ttu-id="a872d-122">SQL virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="a872d-122">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a872d-123">-Offer</span><span class="sxs-lookup"><span data-stu-id="a872d-123">-Offer</span></span>
<span data-ttu-id="a872d-124">SQL virtuális gép ajánlata.</span><span class="sxs-lookup"><span data-stu-id="a872d-124">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a872d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a872d-125">-ResourceGroupName</span></span>
<span data-ttu-id="a872d-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a872d-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a872d-127">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="a872d-127">-Sku</span></span>
<span data-ttu-id="a872d-128">SQL virtuális gép kiadásának típusa.</span><span class="sxs-lookup"><span data-stu-id="a872d-128">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a872d-129">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="a872d-129">-SqlManagementType</span></span>
<span data-ttu-id="a872d-130">SQL virtuális gépkezelés típusa.</span><span class="sxs-lookup"><span data-stu-id="a872d-130">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a872d-131">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="a872d-131">-SqlVM</span></span>
<span data-ttu-id="a872d-132">SQL virtuális gépobjektum.</span><span class="sxs-lookup"><span data-stu-id="a872d-132">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: NameInputObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a872d-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="a872d-133">-Tag</span></span>
<span data-ttu-id="a872d-134">Az SQL virtuális géphez társítva lévő címkék</span><span class="sxs-lookup"><span data-stu-id="a872d-134">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a872d-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a872d-135">-Confirm</span></span>
<span data-ttu-id="a872d-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a872d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a872d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a872d-137">-WhatIf</span></span>
<span data-ttu-id="a872d-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a872d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a872d-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a872d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a872d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a872d-140">CommonParameters</span></span>
<span data-ttu-id="a872d-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a872d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a872d-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a872d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a872d-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a872d-143">INPUTS</span></span>

### <span data-ttu-id="a872d-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="a872d-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="a872d-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a872d-145">OUTPUTS</span></span>

### <span data-ttu-id="a872d-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="a872d-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="a872d-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a872d-147">NOTES</span></span>

## <span data-ttu-id="a872d-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a872d-148">RELATED LINKS</span></span>
