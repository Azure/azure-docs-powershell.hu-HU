---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 64fc7b3acdc497759b707f024a0fb14c7017c44c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467135"
---
# <span data-ttu-id="2583f-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2583f-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="2583f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2583f-102">SYNOPSIS</span></span>
<span data-ttu-id="2583f-103">Azure SQL Server virtuális hálózati szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2583f-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="2583f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2583f-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2583f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2583f-105">DESCRIPTION</span></span>
<span data-ttu-id="2583f-106">Azure SQL Server virtuális hálózati szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2583f-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="2583f-107">A virtuális hálózati szabályok az Azure SQL Server egy adott virtuális hálózathoz való csatlakoztatására szolgálnak annak érdekében, hogy az Azure SQL Serveren keresztüli hozzáférés csak a virtuális hálózaton belül legyen elérhető.</span><span class="sxs-lookup"><span data-stu-id="2583f-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="2583f-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2583f-108">EXAMPLES</span></span>

### <span data-ttu-id="2583f-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="2583f-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="2583f-110">Virtuális Azure SQL Server-szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="2583f-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="2583f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2583f-111">PARAMETERS</span></span>

### <span data-ttu-id="2583f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2583f-112">-AsJob</span></span>
<span data-ttu-id="2583f-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2583f-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2583f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2583f-114">-DefaultProfile</span></span>
<span data-ttu-id="2583f-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2583f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2583f-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="2583f-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="2583f-117">Hozzon létre tűzfalszabályt, mielőtt a virtuális hálózat engedélyezné a vnet-szolgáltatás végpontját.</span><span class="sxs-lookup"><span data-stu-id="2583f-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="2583f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2583f-118">-ResourceGroupName</span></span>
<span data-ttu-id="2583f-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2583f-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2583f-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2583f-120">-ServerName</span></span>
<span data-ttu-id="2583f-121">Az Azure Sql Server neve.</span><span class="sxs-lookup"><span data-stu-id="2583f-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="2583f-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="2583f-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="2583f-123">Azure Sql Server virtuális hálózat szabályának neve.</span><span class="sxs-lookup"><span data-stu-id="2583f-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="2583f-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="2583f-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="2583f-125">A Virtuális hálózat alhálózati azonosítója, amely megadja a Microsoft.Network adatait</span><span class="sxs-lookup"><span data-stu-id="2583f-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="2583f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2583f-126">-Confirm</span></span>
<span data-ttu-id="2583f-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2583f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2583f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2583f-128">-WhatIf</span></span>
<span data-ttu-id="2583f-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2583f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2583f-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2583f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2583f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2583f-131">CommonParameters</span></span>
<span data-ttu-id="2583f-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2583f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2583f-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2583f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2583f-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2583f-134">INPUTS</span></span>

### <span data-ttu-id="2583f-135">System.String</span><span class="sxs-lookup"><span data-stu-id="2583f-135">System.String</span></span>

## <span data-ttu-id="2583f-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2583f-136">OUTPUTS</span></span>

### <span data-ttu-id="2583f-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="2583f-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="2583f-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2583f-138">NOTES</span></span>

## <span data-ttu-id="2583f-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2583f-139">RELATED LINKS</span></span>
