---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
ms.openlocfilehash: c2157521614375bbdeb06aac9a62320ec1e08c70
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168738"
---
# <span data-ttu-id="8f6eb-101">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8f6eb-101">Get-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="8f6eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f6eb-102">SYNOPSIS</span></span>
<span data-ttu-id="8f6eb-103">Tűzfalszabályokat kap egy SQL-adatbázis-kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-103">Gets firewall rules for a SQL Database server.</span></span>

## <span data-ttu-id="8f6eb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8f6eb-104">SYNTAX</span></span>

```
Get-AzSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f6eb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8f6eb-105">DESCRIPTION</span></span>
<span data-ttu-id="8f6eb-106">A **Get-AzSqlServerFirewallRule** parancsmag tűzfalszabályt kap egy Azure SQL Database-kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-106">The **Get-AzSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="8f6eb-107">Ha megadja egy tűzfalszabály nevét, ez a parancsmag információt kap az adott tűzfalszabályról.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="8f6eb-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8f6eb-108">EXAMPLES</span></span>

### <span data-ttu-id="8f6eb-109">1. példa: A kiszolgáló összes szabályának lekérte</span><span class="sxs-lookup"><span data-stu-id="8f6eb-109">Example 1: Get all rules for a server</span></span>
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

<span data-ttu-id="8f6eb-110">Ez a parancs a Kiszolgáló01 nevű kiszolgáló összes tűzfalszabályát beveszi.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-110">This command gets all the firewall rules for the server named Server01.</span></span>

### <span data-ttu-id="8f6eb-111">2. példa: Egy kiszolgáló összes szabályának be szereznie szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="8f6eb-111">Example 2: Get all rules for a server using filtering</span></span>
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

<span data-ttu-id="8f6eb-112">Ez a parancs a Kiszolgáló01 kiszolgálóhoz a "Szabály" kezdetű összes tűzfalszabályt beveszi.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-112">This command gets all the firewall rules for the server named Server01 that start with "Rule".</span></span>

## <span data-ttu-id="8f6eb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f6eb-113">PARAMETERS</span></span>

### <span data-ttu-id="8f6eb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f6eb-114">-DefaultProfile</span></span>
<span data-ttu-id="8f6eb-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8f6eb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f6eb-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="8f6eb-116">-FirewallRuleName</span></span>
<span data-ttu-id="8f6eb-117">A tűzfalszabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-117">Specifies the name of the firewall rule.</span></span>

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

### <span data-ttu-id="8f6eb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f6eb-118">-ResourceGroupName</span></span>
<span data-ttu-id="8f6eb-119">Annak az erőforráscsoportnak a neve, amelyhez az SQL Server hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-119">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="8f6eb-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8f6eb-120">-ServerName</span></span>
<span data-ttu-id="8f6eb-121">Az SQL Server nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-121">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="8f6eb-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f6eb-122">-Confirm</span></span>
<span data-ttu-id="8f6eb-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f6eb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f6eb-124">-WhatIf</span></span>
<span data-ttu-id="8f6eb-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f6eb-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f6eb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f6eb-127">CommonParameters</span></span>
<span data-ttu-id="8f6eb-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f6eb-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f6eb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f6eb-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f6eb-130">INPUTS</span></span>

### <span data-ttu-id="8f6eb-131">System.String</span><span class="sxs-lookup"><span data-stu-id="8f6eb-131">System.String</span></span>

## <span data-ttu-id="8f6eb-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f6eb-132">OUTPUTS</span></span>

### <span data-ttu-id="8f6eb-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="8f6eb-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="8f6eb-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8f6eb-134">NOTES</span></span>

## <span data-ttu-id="8f6eb-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f6eb-135">RELATED LINKS</span></span>

[<span data-ttu-id="8f6eb-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8f6eb-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="8f6eb-137">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8f6eb-137">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="8f6eb-138">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8f6eb-138">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="8f6eb-139">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="8f6eb-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


