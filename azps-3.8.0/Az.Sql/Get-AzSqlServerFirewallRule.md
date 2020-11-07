---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
ms.openlocfilehash: c2157521614375bbdeb06aac9a62320ec1e08c70
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845189"
---
# <span data-ttu-id="9a367-101">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9a367-101">Get-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="9a367-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a367-102">SYNOPSIS</span></span>
<span data-ttu-id="9a367-103">Tűzfal-szabályokat kap egy SQL-adatbázis-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="9a367-103">Gets firewall rules for a SQL Database server.</span></span>

## <span data-ttu-id="9a367-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a367-104">SYNTAX</span></span>

```
Get-AzSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a367-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a367-105">DESCRIPTION</span></span>
<span data-ttu-id="9a367-106">A **Get-AzSqlServerFirewallRule** parancsmag tűzfal-szabályokat kap az Azure SQL-adatbázis-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="9a367-106">The **Get-AzSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="9a367-107">Ha megadhatja a tűzfalszabály nevét, ez a parancsmag információt kap az adott tűzfalszabály-szabályról.</span><span class="sxs-lookup"><span data-stu-id="9a367-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="9a367-108">Példák</span><span class="sxs-lookup"><span data-stu-id="9a367-108">EXAMPLES</span></span>

### <span data-ttu-id="9a367-109">Példa 1: a kiszolgáló összes szabályának lekérése</span><span class="sxs-lookup"><span data-stu-id="9a367-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : AllowAllWindowsAzureIps

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule01
```

<span data-ttu-id="9a367-110">Ez a parancs beolvassa a Server01 nevű kiszolgáló összes tűzfal-szabályát.</span><span class="sxs-lookup"><span data-stu-id="9a367-110">This command gets all the firewall rules for the server named Server01.</span></span>

### <span data-ttu-id="9a367-111">2. példa: a kiszolgálók összes szabályának beszerzése szűréssel</span><span class="sxs-lookup"><span data-stu-id="9a367-111">Example 2: Get all rules for a server using filtering</span></span>
```
PS C:\>Get-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule*"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : Rule01

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule02
```

<span data-ttu-id="9a367-112">Ez a parancs a "szabály" kezdetű Server01 nevű kiszolgáló összes tűzfal-szabályát beolvassa.</span><span class="sxs-lookup"><span data-stu-id="9a367-112">This command gets all the firewall rules for the server named Server01 that start with "Rule".</span></span>

## <span data-ttu-id="9a367-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a367-113">PARAMETERS</span></span>

### <span data-ttu-id="9a367-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a367-114">-DefaultProfile</span></span>
<span data-ttu-id="9a367-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9a367-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a367-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="9a367-116">-FirewallRuleName</span></span>
<span data-ttu-id="9a367-117">A tűzfalszabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a367-117">Specifies the name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a367-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a367-118">-ResourceGroupName</span></span>
<span data-ttu-id="9a367-119">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az SQL-kiszolgáló van rendelve.</span><span class="sxs-lookup"><span data-stu-id="9a367-119">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="9a367-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="9a367-120">-ServerName</span></span>
<span data-ttu-id="9a367-121">Az SQL-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a367-121">Specifies the name of the SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a367-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9a367-122">-Confirm</span></span>
<span data-ttu-id="9a367-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9a367-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a367-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a367-124">-WhatIf</span></span>
<span data-ttu-id="9a367-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9a367-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a367-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9a367-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a367-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a367-127">CommonParameters</span></span>
<span data-ttu-id="9a367-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a367-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a367-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9a367-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a367-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a367-130">INPUTS</span></span>

### <span data-ttu-id="9a367-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9a367-131">System.String</span></span>

## <span data-ttu-id="9a367-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a367-132">OUTPUTS</span></span>

### <span data-ttu-id="9a367-133">Microsoft. Azure. Command. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="9a367-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="9a367-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a367-134">NOTES</span></span>

## <span data-ttu-id="9a367-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a367-135">RELATED LINKS</span></span>

[<span data-ttu-id="9a367-136">Új – AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9a367-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="9a367-137">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9a367-137">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="9a367-138">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9a367-138">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="9a367-139">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="9a367-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


