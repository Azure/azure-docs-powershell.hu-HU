---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
ms.openlocfilehash: ef0ad91d0294f0ac1a4a466a79ce436a7719af5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163218"
---
# <span data-ttu-id="f25fd-101">Remove-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="f25fd-101">Remove-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="f25fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f25fd-102">SYNOPSIS</span></span>
<span data-ttu-id="f25fd-103">Eltávolít egy Azure SQL virtuális fürtöt.</span><span class="sxs-lookup"><span data-stu-id="f25fd-103">Removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="f25fd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f25fd-104">SYNTAX</span></span>

### <span data-ttu-id="f25fd-105">RemoveVirtualClusterFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f25fd-105">RemoveVirtualClusterFromInputParameters (Default)</span></span>
```
Remove-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f25fd-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span><span class="sxs-lookup"><span data-stu-id="f25fd-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span></span>
```
Remove-AzSqlVirtualCluster [-InputObject] <AzureSqlVirtualClusterModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f25fd-107">RemoveVirtualClusterFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="f25fd-107">RemoveVirtualClusterFromAzureResourceId</span></span>
```
Remove-AzSqlVirtualCluster -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f25fd-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f25fd-108">DESCRIPTION</span></span>
<span data-ttu-id="f25fd-109">A **Remove-AzSqlVirtualCluster** parancsmag eltávolítja az Azure SQL virtuális fürtöt.</span><span class="sxs-lookup"><span data-stu-id="f25fd-109">The **Remove-AzSqlVirtualCluster** cmdlet removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="f25fd-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f25fd-110">EXAMPLES</span></span>

### <span data-ttu-id="f25fd-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="f25fd-111">Example 1</span></span>
```powershell
PS C:> Remove-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="f25fd-112">Ez a parancs eltávolítja a VirtualCluster1 nevű virtuális fürtöt, amely az ResourceGroup01 erőforráscsoporthoz van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="f25fd-112">This command removes the virtual cluster named VirtualCluster1 assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="f25fd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f25fd-113">PARAMETERS</span></span>

### <span data-ttu-id="f25fd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f25fd-114">-AsJob</span></span>
<span data-ttu-id="f25fd-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f25fd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f25fd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f25fd-116">-DefaultProfile</span></span>
<span data-ttu-id="f25fd-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f25fd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f25fd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f25fd-118">-InputObject</span></span>
<span data-ttu-id="f25fd-119">Az eltávolítható példányobjektum</span><span class="sxs-lookup"><span data-stu-id="f25fd-119">The instance object to remove</span></span>

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

### <span data-ttu-id="f25fd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f25fd-120">-Name</span></span>
<span data-ttu-id="f25fd-121">A virtuális fürt neve.</span><span class="sxs-lookup"><span data-stu-id="f25fd-121">The name of the virtual cluster.</span></span>

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

### <span data-ttu-id="f25fd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f25fd-122">-ResourceGroupName</span></span>
<span data-ttu-id="f25fd-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f25fd-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="f25fd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f25fd-124">-ResourceId</span></span>
<span data-ttu-id="f25fd-125">Az eltávolítható példányobjektum erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f25fd-125">The resource id of instance object to remove</span></span>

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

### <span data-ttu-id="f25fd-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f25fd-126">-Confirm</span></span>
<span data-ttu-id="f25fd-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f25fd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f25fd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f25fd-128">-WhatIf</span></span>
<span data-ttu-id="f25fd-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f25fd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f25fd-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f25fd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f25fd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f25fd-131">CommonParameters</span></span>
<span data-ttu-id="f25fd-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f25fd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f25fd-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f25fd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f25fd-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f25fd-134">INPUTS</span></span>

### <span data-ttu-id="f25fd-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="f25fd-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

### <span data-ttu-id="f25fd-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f25fd-136">System.String</span></span>

## <span data-ttu-id="f25fd-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f25fd-137">OUTPUTS</span></span>

### <span data-ttu-id="f25fd-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="f25fd-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="f25fd-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f25fd-139">NOTES</span></span>

## <span data-ttu-id="f25fd-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f25fd-140">RELATED LINKS</span></span>
