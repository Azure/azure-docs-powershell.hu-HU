---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: b6f5b885e2cb65c8cf4775f8bb37742b8d98b6a3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476649"
---
# <span data-ttu-id="bb9fa-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="bb9fa-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="bb9fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb9fa-102">SYNOPSIS</span></span>
<span data-ttu-id="bb9fa-103">Egy vagy több sql virtuális gépet kap.</span><span class="sxs-lookup"><span data-stu-id="bb9fa-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="bb9fa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bb9fa-104">SYNTAX</span></span>

### <span data-ttu-id="bb9fa-105">ResourceGroupOnly (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bb9fa-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb9fa-106">név</span><span class="sxs-lookup"><span data-stu-id="bb9fa-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bb9fa-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb9fa-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb9fa-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bb9fa-108">DESCRIPTION</span></span>
<span data-ttu-id="bb9fa-109">A Get-AzSqlVM parancsmag egy vagy több sql virtuális gépet kap.</span><span class="sxs-lookup"><span data-stu-id="bb9fa-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="bb9fa-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bb9fa-110">EXAMPLES</span></span>

### <span data-ttu-id="bb9fa-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="bb9fa-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="bb9fa-112">Ez a parancs információkat kap az aktuális előfizetés összes Azure SQL virtuális gépével kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="bb9fa-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="bb9fa-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="bb9fa-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="bb9fa-114">Ez a parancs információkat kap az aktuális előfizetésben az Erőforráscsoport01 erőforráscsoporthoz társított Azure SQL virtuális gépekről.</span><span class="sxs-lookup"><span data-stu-id="bb9fa-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="bb9fa-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="bb9fa-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="bb9fa-116">Ez a parancs információkat kap az ResourceGroup01 erőforráscsoporthoz hozzárendelt SQL virtuális gép "vm" adatairól.</span><span class="sxs-lookup"><span data-stu-id="bb9fa-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="bb9fa-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb9fa-117">PARAMETERS</span></span>

### <span data-ttu-id="bb9fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb9fa-118">-DefaultProfile</span></span>
<span data-ttu-id="bb9fa-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bb9fa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb9fa-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bb9fa-120">-Name</span></span>
<span data-ttu-id="bb9fa-121">SQL virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="bb9fa-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="bb9fa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb9fa-122">-ResourceGroupName</span></span>
<span data-ttu-id="bb9fa-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bb9fa-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupOnly
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="bb9fa-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb9fa-124">-ResourceId</span></span>
<span data-ttu-id="bb9fa-125">SQL virtuális gép erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bb9fa-125">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="bb9fa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb9fa-126">CommonParameters</span></span>
<span data-ttu-id="bb9fa-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb9fa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb9fa-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb9fa-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb9fa-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb9fa-129">INPUTS</span></span>

### <span data-ttu-id="bb9fa-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="bb9fa-130">None</span></span>

## <span data-ttu-id="bb9fa-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb9fa-131">OUTPUTS</span></span>

### <span data-ttu-id="bb9fa-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="bb9fa-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="bb9fa-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bb9fa-133">NOTES</span></span>

## <span data-ttu-id="bb9fa-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb9fa-134">RELATED LINKS</span></span>
