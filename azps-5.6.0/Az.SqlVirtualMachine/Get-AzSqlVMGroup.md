---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: a7ff8df963f7d1d58256ab40cf5788e81b49a23c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939273"
---
# <span data-ttu-id="8279b-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="8279b-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="8279b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8279b-102">SYNOPSIS</span></span>
<span data-ttu-id="8279b-103">Egy vagy több sql virtuális gépcsoportot kap.</span><span class="sxs-lookup"><span data-stu-id="8279b-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="8279b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8279b-104">SYNTAX</span></span>

### <span data-ttu-id="8279b-105">ResourceGroupOnly (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8279b-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8279b-106">név</span><span class="sxs-lookup"><span data-stu-id="8279b-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8279b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8279b-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8279b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8279b-108">DESCRIPTION</span></span>
<span data-ttu-id="8279b-109">A Get-AzSqlVMGroup parancsmag egy vagy több sql virtuális gépcsoportot kap.</span><span class="sxs-lookup"><span data-stu-id="8279b-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="8279b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8279b-110">EXAMPLES</span></span>

### <span data-ttu-id="8279b-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="8279b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="8279b-112">Ez a parancs információkat kap az aktuális előfizetés összes Azure SQL virtuális gépcsoportról.</span><span class="sxs-lookup"><span data-stu-id="8279b-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="8279b-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="8279b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="8279b-114">Ez a parancs információkat kap az Aktuális előfizetés Azure SQL virtuális gépcsoportjairól az Erőforráscsoport01 erőforráscsoporthoz hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="8279b-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="8279b-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="8279b-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="8279b-116">Ez a parancs információkat kap az ResourceGroup01 erőforráscsoporthoz hozzárendelt SQL virtuális gépcsoport "tesztcsoport" adatairól.</span><span class="sxs-lookup"><span data-stu-id="8279b-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="8279b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8279b-117">PARAMETERS</span></span>

### <span data-ttu-id="8279b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8279b-118">-DefaultProfile</span></span>
<span data-ttu-id="8279b-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8279b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8279b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8279b-120">-Name</span></span>
<span data-ttu-id="8279b-121">SQL virtuális gépcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8279b-121">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="8279b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8279b-122">-ResourceGroupName</span></span>
<span data-ttu-id="8279b-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8279b-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="8279b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8279b-124">-ResourceId</span></span>
<span data-ttu-id="8279b-125">SQL virtuális gépcsoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8279b-125">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="8279b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8279b-126">CommonParameters</span></span>
<span data-ttu-id="8279b-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8279b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8279b-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8279b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8279b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8279b-129">INPUTS</span></span>

### <span data-ttu-id="8279b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8279b-130">System.String</span></span>

## <span data-ttu-id="8279b-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8279b-131">OUTPUTS</span></span>

### <span data-ttu-id="8279b-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="8279b-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="8279b-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8279b-133">NOTES</span></span>

## <span data-ttu-id="8279b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8279b-134">RELATED LINKS</span></span>
