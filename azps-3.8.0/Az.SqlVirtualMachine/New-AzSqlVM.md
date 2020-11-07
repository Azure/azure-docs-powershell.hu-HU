---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
ms.openlocfilehash: 764312c64ae9887a6ef4243cc20b04535afcf81f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846466"
---
# <span data-ttu-id="d235d-101">New-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="d235d-101">New-AzSqlVM</span></span>

## <span data-ttu-id="d235d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d235d-102">SYNOPSIS</span></span>
<span data-ttu-id="d235d-103">Új SQL virtuális gépet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d235d-103">Creates a new sql virtual machine.</span></span>

## <span data-ttu-id="d235d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d235d-104">SYNTAX</span></span>

### <span data-ttu-id="d235d-105">NameParamaterList (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d235d-105">NameParamaterList (Default)</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType] <String> -Location <String> [-AsJob]
 [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d235d-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="d235d-106">NameInputObject</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-SqlVM] <AzureSqlVMModel> -Location <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d235d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d235d-107">DESCRIPTION</span></span>
<span data-ttu-id="d235d-108">Az New-AzSqlVM parancsmag egy Azure SQL virtuális gépet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d235d-108">The New-AzSqlVM cmdlet creates an Azure SQL virtual machine.</span></span>

## <span data-ttu-id="d235d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d235d-109">EXAMPLES</span></span>

### <span data-ttu-id="d235d-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d235d-110">Example 1</span></span>
```powershell
PS C:\> New-AzSqlVM  New-AzSqlVM -ResourceGroupName ResourceGroup01 -Name vm -LicenseType 'PAYG' -Sku Developer
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="d235d-111">Új Azure SQL virtuális gép létrehozása az erőforráscsoport ResourceGroup01</span><span class="sxs-lookup"><span data-stu-id="d235d-111">Creates a new Azure SQL virtual machine with name vm in the resource group ResourceGroup01</span></span> 

## <span data-ttu-id="d235d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d235d-112">PARAMETERS</span></span>

### <span data-ttu-id="d235d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d235d-113">-AsJob</span></span>
<span data-ttu-id="d235d-114">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="d235d-114">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="d235d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d235d-115">-DefaultProfile</span></span>
<span data-ttu-id="d235d-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d235d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d235d-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d235d-117">-LicenseType</span></span>
<span data-ttu-id="d235d-118">Virtuális SQL Machine-licenc típusa</span><span class="sxs-lookup"><span data-stu-id="d235d-118">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="d235d-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="d235d-119">-Location</span></span>
<span data-ttu-id="d235d-120">Az SQL virtuális gép helye.</span><span class="sxs-lookup"><span data-stu-id="d235d-120">SQL virtual machine location.</span></span>

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

### <span data-ttu-id="d235d-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d235d-121">-Name</span></span>
<span data-ttu-id="d235d-122">Az SQL virtuális gép neve</span><span class="sxs-lookup"><span data-stu-id="d235d-122">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="d235d-123">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="d235d-123">-Offer</span></span>
<span data-ttu-id="d235d-124">Virtuális SQL-gép ajánlata.</span><span class="sxs-lookup"><span data-stu-id="d235d-124">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="d235d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d235d-125">-ResourceGroupName</span></span>
<span data-ttu-id="d235d-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d235d-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="d235d-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="d235d-127">-Sku</span></span>
<span data-ttu-id="d235d-128">SQL virtuálisgép-Kiadás típusa</span><span class="sxs-lookup"><span data-stu-id="d235d-128">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="d235d-129">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="d235d-129">-SqlManagementType</span></span>
<span data-ttu-id="d235d-130">SQL virtuálisgép-kezelés típusa</span><span class="sxs-lookup"><span data-stu-id="d235d-130">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="d235d-131">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="d235d-131">-SqlVM</span></span>
<span data-ttu-id="d235d-132">Virtuális SQL Machine-objektum.</span><span class="sxs-lookup"><span data-stu-id="d235d-132">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="d235d-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="d235d-133">-Tag</span></span>
<span data-ttu-id="d235d-134">Az SQL Virtual Machine-tel társítani kívánt Címkék</span><span class="sxs-lookup"><span data-stu-id="d235d-134">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="d235d-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d235d-135">-Confirm</span></span>
<span data-ttu-id="d235d-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d235d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d235d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d235d-137">-WhatIf</span></span>
<span data-ttu-id="d235d-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d235d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d235d-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d235d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d235d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d235d-140">CommonParameters</span></span>
<span data-ttu-id="d235d-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d235d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d235d-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d235d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d235d-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d235d-143">INPUTS</span></span>

### <span data-ttu-id="d235d-144">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="d235d-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="d235d-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d235d-145">OUTPUTS</span></span>

### <span data-ttu-id="d235d-146">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="d235d-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="d235d-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d235d-147">NOTES</span></span>

## <span data-ttu-id="d235d-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d235d-148">RELATED LINKS</span></span>
