---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 2365cb4f6dedeb0620a2bdb1c1549eb0cd25d0c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939386"
---
# <span data-ttu-id="11c22-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="11c22-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="11c22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11c22-102">SYNOPSIS</span></span>
<span data-ttu-id="11c22-103">Módosít egy tűzfalszabályt az Azure SQL-adatbázis-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="11c22-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="11c22-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="11c22-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11c22-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="11c22-105">DESCRIPTION</span></span>
<span data-ttu-id="11c22-106">A **Set-AzSqlServerFirewallRule** parancsmag módosít egy tűzfalszabályt egy Azure SQL Database-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="11c22-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="11c22-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="11c22-107">EXAMPLES</span></span>

### <span data-ttu-id="11c22-108">1. példa: Tűzfalszabály módosítása</span><span class="sxs-lookup"><span data-stu-id="11c22-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="11c22-109">Ez a parancs módosítja a Szabály01 nevű tűzfalszabályt a Kiszolgáló01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="11c22-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="11c22-110">A parancs módosítja a kezdő és a záró IP-címet.</span><span class="sxs-lookup"><span data-stu-id="11c22-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="11c22-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11c22-111">PARAMETERS</span></span>

### <span data-ttu-id="11c22-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11c22-112">-DefaultProfile</span></span>
<span data-ttu-id="11c22-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="11c22-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11c22-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="11c22-114">-EndIpAddress</span></span>
<span data-ttu-id="11c22-115">A szabály IP-címtartományának záró értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="11c22-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="11c22-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="11c22-116">-FirewallRuleName</span></span>
<span data-ttu-id="11c22-117">Annak a tűzfalszabálynak a nevét adja meg, amely módosítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="11c22-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="11c22-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11c22-118">-ResourceGroupName</span></span>
<span data-ttu-id="11c22-119">Annak az erőforráscsoportnak a neve, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="11c22-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="11c22-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="11c22-120">-ServerName</span></span>
<span data-ttu-id="11c22-121">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="11c22-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="11c22-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="11c22-122">-StartIpAddress</span></span>
<span data-ttu-id="11c22-123">A tűzfalszabály IP-címtartományának kezdőértéke.</span><span class="sxs-lookup"><span data-stu-id="11c22-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="11c22-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11c22-124">-Confirm</span></span>
<span data-ttu-id="11c22-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="11c22-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11c22-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11c22-126">-WhatIf</span></span>
<span data-ttu-id="11c22-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="11c22-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11c22-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11c22-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11c22-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11c22-129">CommonParameters</span></span>
<span data-ttu-id="11c22-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11c22-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11c22-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11c22-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11c22-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11c22-132">INPUTS</span></span>

### <span data-ttu-id="11c22-133">System.String</span><span class="sxs-lookup"><span data-stu-id="11c22-133">System.String</span></span>

## <span data-ttu-id="11c22-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11c22-134">OUTPUTS</span></span>

### <span data-ttu-id="11c22-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="11c22-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="11c22-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="11c22-136">NOTES</span></span>

## <span data-ttu-id="11c22-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11c22-137">RELATED LINKS</span></span>

[<span data-ttu-id="11c22-138">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="11c22-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="11c22-139">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="11c22-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="11c22-140">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="11c22-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="11c22-141">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="11c22-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


