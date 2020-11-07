---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 2955834fdb5c902b7495fe212cb9e697b0cee940
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672828"
---
# <span data-ttu-id="e311f-101">New-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e311f-101">New-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="e311f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e311f-102">SYNOPSIS</span></span>
<span data-ttu-id="e311f-103">Azure SQL Server virtuális hálózati szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="e311f-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e311f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e311f-104">SYNTAX</span></span>

```
New-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e311f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e311f-105">DESCRIPTION</span></span>
<span data-ttu-id="e311f-106">Azure SQL Server virtuális hálózati szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="e311f-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="e311f-107">A virtuális hálózati szabályok segítségével az Azure SQL Server egy adott virtuális hálózathoz kapcsolható, így korlátozhatja, hogy a hozzáférés az Azure SQL Server-kiszolgálón csak a virtuális hálózaton belül legyen elérhető.</span><span class="sxs-lookup"><span data-stu-id="e311f-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="e311f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e311f-108">EXAMPLES</span></span>

### <span data-ttu-id="e311f-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e311f-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="e311f-110">Azure SQL Server virtuális hálózati szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="e311f-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="e311f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e311f-111">PARAMETERS</span></span>

### <span data-ttu-id="e311f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e311f-112">-AsJob</span></span>
<span data-ttu-id="e311f-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e311f-113">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e311f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e311f-114">-DefaultProfile</span></span>
<span data-ttu-id="e311f-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e311f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e311f-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e311f-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="e311f-117">Tűzfalszabály létrehozása: mielőtt a virtuális hálózat vnet-szolgáltatási végpont engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="e311f-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e311f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e311f-118">-ResourceGroupName</span></span>
<span data-ttu-id="e311f-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e311f-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e311f-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="e311f-120">-ServerName</span></span>
<span data-ttu-id="e311f-121">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="e311f-121">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e311f-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="e311f-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="e311f-123">Azure SQL Server virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="e311f-123">Azure Sql Server Virtual Network Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e311f-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="e311f-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="e311f-125">A Microsoft. Network részleteit megadó virtuális hálózat alhálózati azonosítója</span><span class="sxs-lookup"><span data-stu-id="e311f-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e311f-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e311f-126">-Confirm</span></span>
<span data-ttu-id="e311f-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e311f-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e311f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e311f-128">-WhatIf</span></span>
<span data-ttu-id="e311f-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e311f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e311f-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e311f-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e311f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e311f-131">CommonParameters</span></span>
<span data-ttu-id="e311f-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e311f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e311f-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e311f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e311f-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e311f-134">INPUTS</span></span>

### <span data-ttu-id="e311f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e311f-135">System.String</span></span>

## <span data-ttu-id="e311f-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e311f-136">OUTPUTS</span></span>

### <span data-ttu-id="e311f-137">Microsoft. Azure. Command. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="e311f-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="e311f-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e311f-138">NOTES</span></span>

## <span data-ttu-id="e311f-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e311f-139">RELATED LINKS</span></span>
