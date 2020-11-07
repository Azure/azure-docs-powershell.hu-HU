---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
ms.openlocfilehash: d4c69457b9932f76d002e3941af3015225345c8f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668817"
---
# <span data-ttu-id="b5fea-101">Remove-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="b5fea-101">Remove-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="b5fea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5fea-102">SYNOPSIS</span></span>
<span data-ttu-id="b5fea-103">Az Azure SQL virtuális fürtök eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="b5fea-103">Removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="b5fea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5fea-104">SYNTAX</span></span>

### <span data-ttu-id="b5fea-105">RemoveVirtualClusterFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b5fea-105">RemoveVirtualClusterFromInputParameters (Default)</span></span>
```
Remove-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5fea-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span><span class="sxs-lookup"><span data-stu-id="b5fea-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span></span>
```
Remove-AzSqlVirtualCluster [-InputObject] <AzureSqlVirtualClusterModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5fea-107">RemoveVirtualClusterFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="b5fea-107">RemoveVirtualClusterFromAzureResourceId</span></span>
```
Remove-AzSqlVirtualCluster -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5fea-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5fea-108">DESCRIPTION</span></span>
<span data-ttu-id="b5fea-109">A **Remove-AzSqlVirtualCluster** parancsmag eltávolítja az Azure SQL virtuális fürtöt.</span><span class="sxs-lookup"><span data-stu-id="b5fea-109">The **Remove-AzSqlVirtualCluster** cmdlet removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="b5fea-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b5fea-110">EXAMPLES</span></span>

### <span data-ttu-id="b5fea-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b5fea-111">Example 1</span></span>
```powershell
PS C:> Remove-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="b5fea-112">Ez a parancs eltávolítja az erőforráscsoport ResourceGroup01 rendelt VirtualCluster1 nevű virtuális fürtöt.</span><span class="sxs-lookup"><span data-stu-id="b5fea-112">This command removes the virtual cluster named VirtualCluster1 assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="b5fea-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5fea-113">PARAMETERS</span></span>

### <span data-ttu-id="b5fea-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5fea-114">-AsJob</span></span>
<span data-ttu-id="b5fea-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b5fea-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5fea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5fea-116">-DefaultProfile</span></span>
<span data-ttu-id="b5fea-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5fea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5fea-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5fea-118">-InputObject</span></span>
<span data-ttu-id="b5fea-119">Az eltávolítandó példány-objektum</span><span class="sxs-lookup"><span data-stu-id="b5fea-119">The instance object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel
Parameter Sets: RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition
Aliases: VirtualCluster

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5fea-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b5fea-120">-Name</span></span>
<span data-ttu-id="b5fea-121">A virtuális fürt neve.</span><span class="sxs-lookup"><span data-stu-id="b5fea-121">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fea-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5fea-122">-ResourceGroupName</span></span>
<span data-ttu-id="b5fea-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b5fea-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fea-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5fea-124">-ResourceId</span></span>
<span data-ttu-id="b5fea-125">Az eltávolítandó példány-objektum erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b5fea-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5fea-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b5fea-126">-Confirm</span></span>
<span data-ttu-id="b5fea-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b5fea-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5fea-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5fea-128">-WhatIf</span></span>
<span data-ttu-id="b5fea-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b5fea-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5fea-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b5fea-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5fea-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5fea-131">CommonParameters</span></span>
<span data-ttu-id="b5fea-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5fea-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5fea-133">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b5fea-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5fea-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5fea-134">INPUTS</span></span>

### <span data-ttu-id="b5fea-135">Microsoft. Azure. Command. SQL. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="b5fea-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

### <span data-ttu-id="b5fea-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b5fea-136">System.String</span></span>

## <span data-ttu-id="b5fea-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5fea-137">OUTPUTS</span></span>

### <span data-ttu-id="b5fea-138">Microsoft. Azure. Command. SQL. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="b5fea-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="b5fea-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5fea-139">NOTES</span></span>

## <span data-ttu-id="b5fea-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5fea-140">RELATED LINKS</span></span>
