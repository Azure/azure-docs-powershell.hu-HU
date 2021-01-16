---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 4dea3f8bf91bb4b9c0478c281e6ca9366c49744c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333269"
---
# <span data-ttu-id="6e4c5-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6e4c5-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="6e4c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e4c5-102">SYNOPSIS</span></span>
<span data-ttu-id="6e4c5-103">Módosít egy tűzfalszabályt az Azure SQL-adatbázis-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="6e4c5-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="6e4c5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6e4c5-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e4c5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6e4c5-105">DESCRIPTION</span></span>
<span data-ttu-id="6e4c5-106">A **Set-AzSqlServerFirewallRule** parancsmag módosít egy tűzfalszabályt egy Azure SQL Database-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="6e4c5-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="6e4c5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6e4c5-107">EXAMPLES</span></span>

### <span data-ttu-id="6e4c5-108">1. példa: Tűzfalszabály módosítása</span><span class="sxs-lookup"><span data-stu-id="6e4c5-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="6e4c5-109">Ez a parancs módosítja a Szabály01 nevű tűzfalszabályt a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="6e4c5-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="6e4c5-110">A parancs módosítja a kezdő és a záró IP-címet.</span><span class="sxs-lookup"><span data-stu-id="6e4c5-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="6e4c5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e4c5-111">PARAMETERS</span></span>

### <span data-ttu-id="6e4c5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e4c5-112">-DefaultProfile</span></span>
<span data-ttu-id="6e4c5-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6e4c5-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e4c5-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="6e4c5-114">-EndIpAddress</span></span>
<span data-ttu-id="6e4c5-115">A szabály IP-címtartományának záró értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e4c5-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="6e4c5-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="6e4c5-116">-FirewallRuleName</span></span>
<span data-ttu-id="6e4c5-117">Annak a tűzfalszabálynak a nevét adja meg, amely a parancsmagot módosítja.</span><span class="sxs-lookup"><span data-stu-id="6e4c5-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e4c5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e4c5-118">-ResourceGroupName</span></span>
<span data-ttu-id="6e4c5-119">Annak az erőforráscsoportnak a neve, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="6e4c5-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="6e4c5-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6e4c5-120">-ServerName</span></span>
<span data-ttu-id="6e4c5-121">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e4c5-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="6e4c5-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="6e4c5-122">-StartIpAddress</span></span>
<span data-ttu-id="6e4c5-123">A tűzfalszabály IP-címtartományának kezdőértéke.</span><span class="sxs-lookup"><span data-stu-id="6e4c5-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="6e4c5-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e4c5-124">-Confirm</span></span>
<span data-ttu-id="6e4c5-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6e4c5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e4c5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e4c5-126">-WhatIf</span></span>
<span data-ttu-id="6e4c5-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6e4c5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e4c5-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6e4c5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e4c5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e4c5-129">CommonParameters</span></span>
<span data-ttu-id="6e4c5-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e4c5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e4c5-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e4c5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e4c5-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e4c5-132">INPUTS</span></span>

### <span data-ttu-id="6e4c5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6e4c5-133">System.String</span></span>

## <span data-ttu-id="6e4c5-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e4c5-134">OUTPUTS</span></span>

### <span data-ttu-id="6e4c5-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="6e4c5-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="6e4c5-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6e4c5-136">NOTES</span></span>

## <span data-ttu-id="6e4c5-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e4c5-137">RELATED LINKS</span></span>

[<span data-ttu-id="6e4c5-138">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6e4c5-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="6e4c5-139">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6e4c5-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="6e4c5-140">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6e4c5-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="6e4c5-141">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="6e4c5-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


