---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 08d14217cff370557009167e09cd7e5396df4e2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493320"
---
# <span data-ttu-id="a5be9-101">New-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a5be9-101">New-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="a5be9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5be9-102">SYNOPSIS</span></span>
<span data-ttu-id="a5be9-103">Azure SQL Server virtuális hálózati szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="a5be9-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5be9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5be9-104">SYNTAX</span></span>

```
New-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5be9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5be9-105">DESCRIPTION</span></span>
<span data-ttu-id="a5be9-106">Azure SQL Server virtuális hálózati szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="a5be9-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="a5be9-107">A virtuális hálózati szabályok segítségével az Azure SQL Server egy adott virtuális hálózathoz kapcsolható, így korlátozhatja, hogy a hozzáférés az Azure SQL Server-kiszolgálón csak a virtuális hálózaton belül legyen elérhető.</span><span class="sxs-lookup"><span data-stu-id="a5be9-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="a5be9-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a5be9-108">EXAMPLES</span></span>

### <span data-ttu-id="a5be9-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a5be9-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="a5be9-110">Azure SQL Server virtuális hálózati szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="a5be9-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="a5be9-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5be9-111">PARAMETERS</span></span>

### <span data-ttu-id="a5be9-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5be9-112">-ResourceGroupName</span></span>
<span data-ttu-id="a5be9-113">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a5be9-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="a5be9-114">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a5be9-114">-ServerName</span></span>
<span data-ttu-id="a5be9-115">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="a5be9-115">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="a5be9-116">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="a5be9-116">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="a5be9-117">Azure SQL Server virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="a5be9-117">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="a5be9-118">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="a5be9-118">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="a5be9-119">A Microsoft. Network részleteit megadó virtuális hálózat alhálózati azonosítója</span><span class="sxs-lookup"><span data-stu-id="a5be9-119">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="a5be9-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a5be9-120">-Confirm</span></span>
<span data-ttu-id="a5be9-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5be9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5be9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5be9-122">-WhatIf</span></span>
<span data-ttu-id="a5be9-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a5be9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5be9-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5be9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5be9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5be9-125">-DefaultProfile</span></span>
<span data-ttu-id="a5be9-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5be9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5be9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5be9-127">CommonParameters</span></span>
<span data-ttu-id="a5be9-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5be9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5be9-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5be9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5be9-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5be9-130">INPUTS</span></span>

### <span data-ttu-id="a5be9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a5be9-131">System.String</span></span>

## <span data-ttu-id="a5be9-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5be9-132">OUTPUTS</span></span>

### <span data-ttu-id="a5be9-133">Microsoft. Azure. Command. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="a5be9-133">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="a5be9-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5be9-134">NOTES</span></span>

## <span data-ttu-id="a5be9-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5be9-135">RELATED LINKS</span></span>

