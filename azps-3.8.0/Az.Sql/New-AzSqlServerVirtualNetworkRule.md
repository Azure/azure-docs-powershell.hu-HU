---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 64fc7b3acdc497759b707f024a0fb14c7017c44c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847377"
---
# <span data-ttu-id="4b779-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4b779-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="4b779-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4b779-102">SYNOPSIS</span></span>
<span data-ttu-id="4b779-103">Azure SQL Server virtuális hálózati szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="4b779-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="4b779-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4b779-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b779-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4b779-105">DESCRIPTION</span></span>
<span data-ttu-id="4b779-106">Azure SQL Server virtuális hálózati szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="4b779-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="4b779-107">A virtuális hálózati szabályok segítségével az Azure SQL Server egy adott virtuális hálózathoz kapcsolható, így korlátozhatja, hogy a hozzáférés az Azure SQL Server-kiszolgálón csak a virtuális hálózaton belül legyen elérhető.</span><span class="sxs-lookup"><span data-stu-id="4b779-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="4b779-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4b779-108">EXAMPLES</span></span>

### <span data-ttu-id="4b779-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4b779-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="4b779-110">Azure SQL Server virtuális hálózati szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="4b779-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="4b779-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4b779-111">PARAMETERS</span></span>

### <span data-ttu-id="4b779-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b779-112">-AsJob</span></span>
<span data-ttu-id="4b779-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4b779-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b779-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b779-114">-DefaultProfile</span></span>
<span data-ttu-id="4b779-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4b779-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b779-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b779-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="4b779-117">Tűzfalszabály létrehozása: mielőtt a virtuális hálózat vnet-szolgáltatási végpont engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="4b779-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="4b779-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b779-118">-ResourceGroupName</span></span>
<span data-ttu-id="4b779-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4b779-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="4b779-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="4b779-120">-ServerName</span></span>
<span data-ttu-id="4b779-121">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="4b779-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="4b779-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="4b779-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="4b779-123">Azure SQL Server virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="4b779-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="4b779-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="4b779-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="4b779-125">A Microsoft. Network részleteit megadó virtuális hálózat alhálózati azonosítója</span><span class="sxs-lookup"><span data-stu-id="4b779-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="4b779-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4b779-126">-Confirm</span></span>
<span data-ttu-id="4b779-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4b779-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b779-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b779-128">-WhatIf</span></span>
<span data-ttu-id="4b779-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4b779-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b779-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4b779-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b779-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b779-131">CommonParameters</span></span>
<span data-ttu-id="4b779-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4b779-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b779-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4b779-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b779-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b779-134">INPUTS</span></span>

### <span data-ttu-id="4b779-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4b779-135">System.String</span></span>

## <span data-ttu-id="4b779-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b779-136">OUTPUTS</span></span>

### <span data-ttu-id="4b779-137">Microsoft. Azure. Command. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="4b779-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="4b779-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4b779-138">NOTES</span></span>

## <span data-ttu-id="4b779-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b779-139">RELATED LINKS</span></span>
