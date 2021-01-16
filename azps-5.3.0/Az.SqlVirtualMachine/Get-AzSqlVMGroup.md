---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: fc4a0624b6e5702c0ef0c836f0b6ac593c25dafe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476646"
---
# <span data-ttu-id="d5bc3-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="d5bc3-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="d5bc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5bc3-102">SYNOPSIS</span></span>
<span data-ttu-id="d5bc3-103">Egy vagy több sql virtuális gépcsoportot kap.</span><span class="sxs-lookup"><span data-stu-id="d5bc3-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="d5bc3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d5bc3-104">SYNTAX</span></span>

### <span data-ttu-id="d5bc3-105">ResourceGroupOnly (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d5bc3-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5bc3-106">név</span><span class="sxs-lookup"><span data-stu-id="d5bc3-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5bc3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5bc3-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5bc3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d5bc3-108">DESCRIPTION</span></span>
<span data-ttu-id="d5bc3-109">A Get-AzSqlVMGroup parancsmag egy vagy több sql virtuális gépcsoportot kap.</span><span class="sxs-lookup"><span data-stu-id="d5bc3-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="d5bc3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d5bc3-110">EXAMPLES</span></span>

### <span data-ttu-id="d5bc3-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="d5bc3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="d5bc3-112">Ez a parancs információkat kap az aktuális előfizetés összes Azure SQL virtuális gépcsoportról.</span><span class="sxs-lookup"><span data-stu-id="d5bc3-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="d5bc3-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="d5bc3-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="d5bc3-114">Ez a parancs információkat kap az Aktuális előfizetés Azure SQL virtuális gépcsoportjairól az Erőforráscsoport01 erőforráscsoporthoz hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="d5bc3-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="d5bc3-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="d5bc3-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="d5bc3-116">Ez a parancs információkat kap az ResourceGroup01 erőforráscsoporthoz hozzárendelt SQL virtuális gépcsoport "tesztcsoport" adatairól.</span><span class="sxs-lookup"><span data-stu-id="d5bc3-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="d5bc3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5bc3-117">PARAMETERS</span></span>

### <span data-ttu-id="d5bc3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5bc3-118">-DefaultProfile</span></span>
<span data-ttu-id="d5bc3-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5bc3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5bc3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d5bc3-120">-Name</span></span>
<span data-ttu-id="d5bc3-121">SQL virtuális gépcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d5bc3-121">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="d5bc3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5bc3-122">-ResourceGroupName</span></span>
<span data-ttu-id="d5bc3-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d5bc3-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="d5bc3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5bc3-124">-ResourceId</span></span>
<span data-ttu-id="d5bc3-125">SQL virtuális gépcsoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d5bc3-125">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="d5bc3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5bc3-126">CommonParameters</span></span>
<span data-ttu-id="d5bc3-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5bc3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5bc3-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5bc3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5bc3-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5bc3-129">INPUTS</span></span>

### <span data-ttu-id="d5bc3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d5bc3-130">System.String</span></span>

## <span data-ttu-id="d5bc3-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5bc3-131">OUTPUTS</span></span>

### <span data-ttu-id="d5bc3-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="d5bc3-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="d5bc3-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d5bc3-133">NOTES</span></span>

## <span data-ttu-id="d5bc3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5bc3-134">RELATED LINKS</span></span>
