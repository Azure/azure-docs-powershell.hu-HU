---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
ms.openlocfilehash: c2157521614375bbdeb06aac9a62320ec1e08c70
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350045"
---
# <span data-ttu-id="f3f93-101">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f3f93-101">Get-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="f3f93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3f93-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f93-103">Tűzfalszabályokat kap egy SQL-adatbázis-kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="f3f93-103">Gets firewall rules for a SQL Database server.</span></span>

## <span data-ttu-id="f3f93-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f3f93-104">SYNTAX</span></span>

```
Get-AzSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3f93-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f3f93-105">DESCRIPTION</span></span>
<span data-ttu-id="f3f93-106">A **Get-AzSqlServerFirewallRule parancsmag** tűzfalszabályt kap egy Azure SQL Database-kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="f3f93-106">The **Get-AzSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="f3f93-107">Ha megadja egy tűzfalszabály nevét, ez a parancsmag információt kap az adott tűzfalszabályról.</span><span class="sxs-lookup"><span data-stu-id="f3f93-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="f3f93-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f3f93-108">EXAMPLES</span></span>

### <span data-ttu-id="f3f93-109">1. példa: A kiszolgáló összes szabályának lekérte</span><span class="sxs-lookup"><span data-stu-id="f3f93-109">Example 1: Get all rules for a server</span></span>
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

<span data-ttu-id="f3f93-110">Ez a parancs a Kiszolgáló01 nevű kiszolgáló összes tűzfalszabályát beveszi.</span><span class="sxs-lookup"><span data-stu-id="f3f93-110">This command gets all the firewall rules for the server named Server01.</span></span>

### <span data-ttu-id="f3f93-111">2. példa: Egy kiszolgáló összes szabályának be szereznie szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="f3f93-111">Example 2: Get all rules for a server using filtering</span></span>
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

<span data-ttu-id="f3f93-112">Ez a parancs a Kiszolgáló01 kiszolgálóhoz a "Szabály" kezdetű összes tűzfalszabályt beveszi.</span><span class="sxs-lookup"><span data-stu-id="f3f93-112">This command gets all the firewall rules for the server named Server01 that start with "Rule".</span></span>

## <span data-ttu-id="f3f93-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3f93-113">PARAMETERS</span></span>

### <span data-ttu-id="f3f93-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3f93-114">-DefaultProfile</span></span>
<span data-ttu-id="f3f93-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f3f93-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3f93-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="f3f93-116">-FirewallRuleName</span></span>
<span data-ttu-id="f3f93-117">A tűzfalszabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3f93-117">Specifies the name of the firewall rule.</span></span>

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

### <span data-ttu-id="f3f93-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3f93-118">-ResourceGroupName</span></span>
<span data-ttu-id="f3f93-119">Annak az erőforráscsoportnak a neve, amelyhez az SQL Server hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="f3f93-119">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="f3f93-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f3f93-120">-ServerName</span></span>
<span data-ttu-id="f3f93-121">Az SQL Server nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3f93-121">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="f3f93-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3f93-122">-Confirm</span></span>
<span data-ttu-id="f3f93-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f3f93-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3f93-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3f93-124">-WhatIf</span></span>
<span data-ttu-id="f3f93-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f3f93-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3f93-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3f93-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3f93-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f93-127">CommonParameters</span></span>
<span data-ttu-id="f3f93-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3f93-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f93-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3f93-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f93-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3f93-130">INPUTS</span></span>

### <span data-ttu-id="f3f93-131">System.String</span><span class="sxs-lookup"><span data-stu-id="f3f93-131">System.String</span></span>

## <span data-ttu-id="f3f93-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3f93-132">OUTPUTS</span></span>

### <span data-ttu-id="f3f93-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="f3f93-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="f3f93-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f3f93-134">NOTES</span></span>

## <span data-ttu-id="f3f93-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3f93-135">RELATED LINKS</span></span>

[<span data-ttu-id="f3f93-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f3f93-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="f3f93-137">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f3f93-137">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="f3f93-138">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f3f93-138">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="f3f93-139">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f3f93-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


