---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 3b318e08e4dbf900b54581b18f551a3accb75480
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839486"
---
# <span data-ttu-id="5251b-101">Set-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5251b-101">Set-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="5251b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5251b-102">SYNOPSIS</span></span>
<span data-ttu-id="5251b-103">Módosítja egy Azure SQL Server virtuális hálózati szabály konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="5251b-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="5251b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5251b-104">SYNTAX</span></span>

```
Set-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5251b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5251b-105">DESCRIPTION</span></span>
<span data-ttu-id="5251b-106">Ez a parancs módosítja egy Azure SQL Server virtuális hálózati szabály konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="5251b-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="5251b-107">A kiszolgálón lévő virtuális hálózati szabályok beállításához használja inkább a "AzSqlServerVirtualNetworkRule" és a "Remove-AzSqlServerVirtualNetworkRule" parancsot.</span><span class="sxs-lookup"><span data-stu-id="5251b-107">To control the set of virtual network rules in the server, use 'Add-AzSqlServerVirtualNetworkRule' and 'Remove-AzSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="5251b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5251b-108">EXAMPLES</span></span>

### <span data-ttu-id="5251b-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5251b-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="5251b-110">Módosítja egy meglévő virtuális hálózati szabályt az új virtuális hálózat alhálózati azonosítójával, amely az új virtuális hálózatról tartalmaz információkat.</span><span class="sxs-lookup"><span data-stu-id="5251b-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="5251b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5251b-111">PARAMETERS</span></span>

### <span data-ttu-id="5251b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5251b-112">-AsJob</span></span>
<span data-ttu-id="5251b-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5251b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5251b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5251b-114">-DefaultProfile</span></span>
<span data-ttu-id="5251b-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5251b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5251b-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="5251b-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="5251b-117">Tűzfalszabály létrehozása: mielőtt a virtuális hálózat vnet-szolgáltatási végpont engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="5251b-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="5251b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5251b-118">-ResourceGroupName</span></span>
<span data-ttu-id="5251b-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5251b-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="5251b-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="5251b-120">-ServerName</span></span>
<span data-ttu-id="5251b-121">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="5251b-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="5251b-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="5251b-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="5251b-123">Az Azure SQL Server virtuális hálózati szabályának neve.</span><span class="sxs-lookup"><span data-stu-id="5251b-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="5251b-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="5251b-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="5251b-125">A szabály virtuális hálózati alhálózati azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5251b-125">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="5251b-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5251b-126">-Confirm</span></span>
<span data-ttu-id="5251b-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5251b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5251b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5251b-128">-WhatIf</span></span>
<span data-ttu-id="5251b-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5251b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5251b-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5251b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5251b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5251b-131">CommonParameters</span></span>
<span data-ttu-id="5251b-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5251b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5251b-133">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5251b-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5251b-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5251b-134">INPUTS</span></span>

### <span data-ttu-id="5251b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5251b-135">System.String</span></span>

## <span data-ttu-id="5251b-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5251b-136">OUTPUTS</span></span>

### <span data-ttu-id="5251b-137">Microsoft. Azure. Command. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="5251b-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="5251b-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5251b-138">NOTES</span></span>

## <span data-ttu-id="5251b-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5251b-139">RELATED LINKS</span></span>
