---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: fc4a0624b6e5702c0ef0c836f0b6ac593c25dafe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846417"
---
# <span data-ttu-id="38072-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="38072-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="38072-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38072-102">SYNOPSIS</span></span>
<span data-ttu-id="38072-103">Egy vagy több SQL-virtuálisgép-csoportot kap.</span><span class="sxs-lookup"><span data-stu-id="38072-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="38072-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38072-104">SYNTAX</span></span>

### <span data-ttu-id="38072-105">ResourceGroupOnly (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="38072-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="38072-106">név</span><span class="sxs-lookup"><span data-stu-id="38072-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="38072-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="38072-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38072-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="38072-108">DESCRIPTION</span></span>
<span data-ttu-id="38072-109">A Get-AzSqlVMGroup parancsmag egy vagy több SQL-virtuálisgép-csoportot kap.</span><span class="sxs-lookup"><span data-stu-id="38072-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="38072-110">Példák</span><span class="sxs-lookup"><span data-stu-id="38072-110">EXAMPLES</span></span>

### <span data-ttu-id="38072-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="38072-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="38072-112">Ez a parancs a jelenlegi előfizetésben az Azure SQL Virtual Machine-csoportokra vonatkozó információkat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="38072-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="38072-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="38072-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="38072-114">Ez a parancs információt kap az Azure SQL virtuálisgép-csoportokról az erőforráscsoport ResourceGroup01 tartozó jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="38072-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="38072-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="38072-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="38072-116">Ez a parancs információt kap az erőforráscsoport ResourceGroup01 rendelt "teszt-csoport" SQL Machine-csoportról.</span><span class="sxs-lookup"><span data-stu-id="38072-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="38072-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38072-117">PARAMETERS</span></span>

### <span data-ttu-id="38072-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38072-118">-DefaultProfile</span></span>
<span data-ttu-id="38072-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38072-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38072-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="38072-120">-Name</span></span>
<span data-ttu-id="38072-121">Az SQL virtuálisgép-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="38072-121">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="38072-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38072-122">-ResourceGroupName</span></span>
<span data-ttu-id="38072-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="38072-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="38072-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38072-124">-ResourceId</span></span>
<span data-ttu-id="38072-125">SQL virtuálisgép-csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="38072-125">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="38072-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38072-126">CommonParameters</span></span>
<span data-ttu-id="38072-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38072-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38072-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="38072-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38072-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38072-129">INPUTS</span></span>

### <span data-ttu-id="38072-130">System. String</span><span class="sxs-lookup"><span data-stu-id="38072-130">System.String</span></span>

## <span data-ttu-id="38072-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38072-131">OUTPUTS</span></span>

### <span data-ttu-id="38072-132">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="38072-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="38072-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38072-133">NOTES</span></span>

## <span data-ttu-id="38072-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38072-134">RELATED LINKS</span></span>
