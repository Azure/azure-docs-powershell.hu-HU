---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 8667de4551e9fc0c4baf623099f70f778ec8f0a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839406"
---
# <span data-ttu-id="bf1a0-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bf1a0-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="bf1a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf1a0-102">SYNOPSIS</span></span>
<span data-ttu-id="bf1a0-103">Azure SQL Server virtuális hálózati szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="bf1a0-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="bf1a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf1a0-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf1a0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf1a0-105">DESCRIPTION</span></span>
<span data-ttu-id="bf1a0-106">Azure SQL Server virtuális hálózati szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="bf1a0-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="bf1a0-107">A virtuális hálózati szabályok segítségével az Azure SQL Server egy adott virtuális hálózathoz kapcsolható, így korlátozhatja, hogy a hozzáférés az Azure SQL Server-kiszolgálón csak a virtuális hálózaton belül legyen elérhető.</span><span class="sxs-lookup"><span data-stu-id="bf1a0-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="bf1a0-108">Példák</span><span class="sxs-lookup"><span data-stu-id="bf1a0-108">EXAMPLES</span></span>

### <span data-ttu-id="bf1a0-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bf1a0-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="bf1a0-110">Azure SQL Server virtuális hálózati szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="bf1a0-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="bf1a0-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf1a0-111">PARAMETERS</span></span>

### <span data-ttu-id="bf1a0-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf1a0-112">-AsJob</span></span>
<span data-ttu-id="bf1a0-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bf1a0-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf1a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf1a0-114">-DefaultProfile</span></span>
<span data-ttu-id="bf1a0-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bf1a0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf1a0-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf1a0-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="bf1a0-117">Tűzfalszabály létrehozása: mielőtt a virtuális hálózat vnet-szolgáltatási végpont engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="bf1a0-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="bf1a0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf1a0-118">-ResourceGroupName</span></span>
<span data-ttu-id="bf1a0-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bf1a0-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="bf1a0-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="bf1a0-120">-ServerName</span></span>
<span data-ttu-id="bf1a0-121">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="bf1a0-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="bf1a0-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="bf1a0-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="bf1a0-123">Azure SQL Server virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="bf1a0-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="bf1a0-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="bf1a0-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="bf1a0-125">A Microsoft. Network részleteit megadó virtuális hálózat alhálózati azonosítója</span><span class="sxs-lookup"><span data-stu-id="bf1a0-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="bf1a0-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bf1a0-126">-Confirm</span></span>
<span data-ttu-id="bf1a0-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bf1a0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf1a0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf1a0-128">-WhatIf</span></span>
<span data-ttu-id="bf1a0-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bf1a0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf1a0-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bf1a0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf1a0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf1a0-131">CommonParameters</span></span>
<span data-ttu-id="bf1a0-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf1a0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf1a0-133">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bf1a0-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf1a0-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf1a0-134">INPUTS</span></span>

### <span data-ttu-id="bf1a0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="bf1a0-135">System.String</span></span>

## <span data-ttu-id="bf1a0-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf1a0-136">OUTPUTS</span></span>

### <span data-ttu-id="bf1a0-137">Microsoft. Azure. Command. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="bf1a0-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="bf1a0-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf1a0-138">NOTES</span></span>

## <span data-ttu-id="bf1a0-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf1a0-139">RELATED LINKS</span></span>
