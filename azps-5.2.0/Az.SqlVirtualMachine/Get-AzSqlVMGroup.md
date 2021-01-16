---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: fc4a0624b6e5702c0ef0c836f0b6ac593c25dafe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364655"
---
# <span data-ttu-id="8ebd9-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="8ebd9-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="8ebd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ebd9-102">SYNOPSIS</span></span>
<span data-ttu-id="8ebd9-103">Egy vagy több sql virtuális gépcsoportot kap.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="8ebd9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8ebd9-104">SYNTAX</span></span>

### <span data-ttu-id="8ebd9-105">ResourceGroupOnly (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8ebd9-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ebd9-106">név</span><span class="sxs-lookup"><span data-stu-id="8ebd9-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ebd9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ebd9-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ebd9-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8ebd9-108">DESCRIPTION</span></span>
<span data-ttu-id="8ebd9-109">A Get-AzSqlVMGroup parancsmag egy vagy több sql virtuális gépcsoportot kap.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="8ebd9-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8ebd9-110">EXAMPLES</span></span>

### <span data-ttu-id="8ebd9-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="8ebd9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="8ebd9-112">Ez a parancs információkat kap az aktuális előfizetés összes Azure SQL virtuális gépcsoportról.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="8ebd9-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="8ebd9-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="8ebd9-114">Ez a parancs információkat kap az Aktuális előfizetés Azure SQL virtuális gépcsoportjairól az Erőforráscsoport01 erőforráscsoporthoz hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="8ebd9-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="8ebd9-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="8ebd9-116">Ez a parancs információkat kap az ResourceGroup01 erőforráscsoporthoz hozzárendelt SQL virtuális gépcsoport "tesztcsoport" adatairól.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="8ebd9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ebd9-117">PARAMETERS</span></span>

### <span data-ttu-id="8ebd9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ebd9-118">-DefaultProfile</span></span>
<span data-ttu-id="8ebd9-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ebd9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8ebd9-120">-Name</span></span>
<span data-ttu-id="8ebd9-121">SQL virtuális gépcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-121">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="8ebd9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ebd9-122">-ResourceGroupName</span></span>
<span data-ttu-id="8ebd9-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="8ebd9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ebd9-124">-ResourceId</span></span>
<span data-ttu-id="8ebd9-125">SQL virtuális gépcsoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-125">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="8ebd9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ebd9-126">CommonParameters</span></span>
<span data-ttu-id="8ebd9-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ebd9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ebd9-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ebd9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ebd9-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ebd9-129">INPUTS</span></span>

### <span data-ttu-id="8ebd9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8ebd9-130">System.String</span></span>

## <span data-ttu-id="8ebd9-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ebd9-131">OUTPUTS</span></span>

### <span data-ttu-id="8ebd9-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="8ebd9-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="8ebd9-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8ebd9-133">NOTES</span></span>

## <span data-ttu-id="8ebd9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ebd9-134">RELATED LINKS</span></span>
