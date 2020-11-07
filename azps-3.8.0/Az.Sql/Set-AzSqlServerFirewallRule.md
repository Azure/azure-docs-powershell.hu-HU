---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 4dea3f8bf91bb4b9c0478c281e6ca9366c49744c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846529"
---
# <span data-ttu-id="5ec02-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5ec02-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="5ec02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ec02-102">SYNOPSIS</span></span>
<span data-ttu-id="5ec02-103">Tűzfal-szabály módosítása az Azure SQL adatbázis-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="5ec02-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="5ec02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ec02-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ec02-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ec02-105">DESCRIPTION</span></span>
<span data-ttu-id="5ec02-106">A **set-AzSqlServerFirewallRule** parancsmag egy Azure SQL-adatbázis-kiszolgálón módosítja a tűzfalszabályok egyikét.</span><span class="sxs-lookup"><span data-stu-id="5ec02-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="5ec02-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5ec02-107">EXAMPLES</span></span>

### <span data-ttu-id="5ec02-108">Példa 1: tűzfalszabály módosítása</span><span class="sxs-lookup"><span data-stu-id="5ec02-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="5ec02-109">Ez a parancs módosítja a Server01 nevű kiszolgálón a Rule01 nevű tűzfalszabályok egyikét.</span><span class="sxs-lookup"><span data-stu-id="5ec02-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="5ec02-110">A parancs módosítja a kezdési és a befejezési IP-címet.</span><span class="sxs-lookup"><span data-stu-id="5ec02-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="5ec02-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ec02-111">PARAMETERS</span></span>

### <span data-ttu-id="5ec02-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ec02-112">-DefaultProfile</span></span>
<span data-ttu-id="5ec02-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5ec02-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ec02-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="5ec02-114">-EndIpAddress</span></span>
<span data-ttu-id="5ec02-115">A szabályhoz tartozó IP-címtartomány utolsó értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ec02-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="5ec02-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="5ec02-116">-FirewallRuleName</span></span>
<span data-ttu-id="5ec02-117">Annak a tűzfal-szabálynak a neve, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="5ec02-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5ec02-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ec02-118">-ResourceGroupName</span></span>
<span data-ttu-id="5ec02-119">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="5ec02-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="5ec02-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="5ec02-120">-ServerName</span></span>
<span data-ttu-id="5ec02-121">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ec02-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="5ec02-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="5ec02-122">-StartIpAddress</span></span>
<span data-ttu-id="5ec02-123">A tűzfalszabály IP-címtartomány kezdetének értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ec02-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="5ec02-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5ec02-124">-Confirm</span></span>
<span data-ttu-id="5ec02-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5ec02-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ec02-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ec02-126">-WhatIf</span></span>
<span data-ttu-id="5ec02-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5ec02-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ec02-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ec02-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ec02-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ec02-129">CommonParameters</span></span>
<span data-ttu-id="5ec02-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ec02-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ec02-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5ec02-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ec02-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ec02-132">INPUTS</span></span>

### <span data-ttu-id="5ec02-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5ec02-133">System.String</span></span>

## <span data-ttu-id="5ec02-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ec02-134">OUTPUTS</span></span>

### <span data-ttu-id="5ec02-135">Microsoft. Azure. Command. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="5ec02-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="5ec02-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ec02-136">NOTES</span></span>

## <span data-ttu-id="5ec02-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ec02-137">RELATED LINKS</span></span>

[<span data-ttu-id="5ec02-138">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5ec02-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="5ec02-139">Új – AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5ec02-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="5ec02-140">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5ec02-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="5ec02-141">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="5ec02-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


