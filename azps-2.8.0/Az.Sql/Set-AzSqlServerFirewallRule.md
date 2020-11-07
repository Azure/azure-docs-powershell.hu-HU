---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 5c079adea8079807374d4538f6259cd995103694
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839325"
---
# <span data-ttu-id="107cf-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="107cf-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="107cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="107cf-102">SYNOPSIS</span></span>
<span data-ttu-id="107cf-103">Tűzfal-szabály módosítása az Azure SQL adatbázis-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="107cf-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="107cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="107cf-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="107cf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="107cf-105">DESCRIPTION</span></span>
<span data-ttu-id="107cf-106">A **set-AzSqlServerFirewallRule** parancsmag egy Azure SQL-adatbázis-kiszolgálón módosítja a tűzfalszabályok egyikét.</span><span class="sxs-lookup"><span data-stu-id="107cf-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="107cf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="107cf-107">EXAMPLES</span></span>

### <span data-ttu-id="107cf-108">Példa 1: tűzfalszabály módosítása</span><span class="sxs-lookup"><span data-stu-id="107cf-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="107cf-109">Ez a parancs módosítja a Server01 nevű kiszolgálón a Rule01 nevű tűzfalszabályok egyikét.</span><span class="sxs-lookup"><span data-stu-id="107cf-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="107cf-110">A parancs módosítja a kezdési és a befejezési IP-címet.</span><span class="sxs-lookup"><span data-stu-id="107cf-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="107cf-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="107cf-111">PARAMETERS</span></span>

### <span data-ttu-id="107cf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="107cf-112">-DefaultProfile</span></span>
<span data-ttu-id="107cf-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="107cf-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="107cf-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="107cf-114">-EndIpAddress</span></span>
<span data-ttu-id="107cf-115">A szabályhoz tartozó IP-címtartomány utolsó értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="107cf-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="107cf-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="107cf-116">-FirewallRuleName</span></span>
<span data-ttu-id="107cf-117">Annak a tűzfal-szabálynak a neve, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="107cf-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="107cf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="107cf-118">-ResourceGroupName</span></span>
<span data-ttu-id="107cf-119">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="107cf-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="107cf-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="107cf-120">-ServerName</span></span>
<span data-ttu-id="107cf-121">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="107cf-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="107cf-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="107cf-122">-StartIpAddress</span></span>
<span data-ttu-id="107cf-123">A tűzfalszabály IP-címtartomány kezdetének értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="107cf-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="107cf-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="107cf-124">-Confirm</span></span>
<span data-ttu-id="107cf-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="107cf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="107cf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="107cf-126">-WhatIf</span></span>
<span data-ttu-id="107cf-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="107cf-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="107cf-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="107cf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="107cf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="107cf-129">CommonParameters</span></span>
<span data-ttu-id="107cf-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="107cf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="107cf-131">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="107cf-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="107cf-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="107cf-132">INPUTS</span></span>

### <span data-ttu-id="107cf-133">System. String</span><span class="sxs-lookup"><span data-stu-id="107cf-133">System.String</span></span>

## <span data-ttu-id="107cf-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="107cf-134">OUTPUTS</span></span>

### <span data-ttu-id="107cf-135">Microsoft. Azure. Command. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="107cf-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="107cf-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="107cf-136">NOTES</span></span>

## <span data-ttu-id="107cf-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="107cf-137">RELATED LINKS</span></span>

[<span data-ttu-id="107cf-138">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="107cf-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="107cf-139">Új – AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="107cf-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="107cf-140">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="107cf-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="107cf-141">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="107cf-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


