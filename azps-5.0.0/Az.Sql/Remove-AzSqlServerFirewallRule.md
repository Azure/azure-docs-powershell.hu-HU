---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
ms.openlocfilehash: 83a68863b3dce71a091dc5de11377bade7bdc638
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186522"
---
# <span data-ttu-id="4b67d-101">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4b67d-101">Remove-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="4b67d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4b67d-102">SYNOPSIS</span></span>
<span data-ttu-id="4b67d-103">Tűzfal-szabály törlése SQL-adatbázis-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="4b67d-103">Deletes a firewall rule from a SQL Database server.</span></span>

## <span data-ttu-id="4b67d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4b67d-104">SYNTAX</span></span>

```
Remove-AzSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b67d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4b67d-105">DESCRIPTION</span></span>
<span data-ttu-id="4b67d-106">A **Remove-AzSqlServerFirewallRule** parancsmag a megadott Azure SQL adatbázis-kiszolgálóról törli a tűzfalszabályok egyikét.</span><span class="sxs-lookup"><span data-stu-id="4b67d-106">The **Remove-AzSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="4b67d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4b67d-107">EXAMPLES</span></span>

### <span data-ttu-id="4b67d-108">Példa 1: szabály törlése</span><span class="sxs-lookup"><span data-stu-id="4b67d-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="4b67d-109">Ez a parancs törli a Rule01 nevű tűzfal-szabályt a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="4b67d-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="4b67d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4b67d-110">PARAMETERS</span></span>

### <span data-ttu-id="4b67d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b67d-111">-DefaultProfile</span></span>
<span data-ttu-id="4b67d-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4b67d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b67d-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="4b67d-113">-FirewallRuleName</span></span>
<span data-ttu-id="4b67d-114">Annak a tűzfal-szabálynak a neve, amelyet a parancsmag töröl.</span><span class="sxs-lookup"><span data-stu-id="4b67d-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="4b67d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4b67d-115">-Force</span></span>
<span data-ttu-id="4b67d-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="4b67d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4b67d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b67d-117">-ResourceGroupName</span></span>
<span data-ttu-id="4b67d-118">Annak a csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="4b67d-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="4b67d-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="4b67d-119">-ServerName</span></span>
<span data-ttu-id="4b67d-120">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4b67d-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="4b67d-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4b67d-121">-Confirm</span></span>
<span data-ttu-id="4b67d-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4b67d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b67d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b67d-123">-WhatIf</span></span>
<span data-ttu-id="4b67d-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4b67d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b67d-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4b67d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b67d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b67d-126">CommonParameters</span></span>
<span data-ttu-id="4b67d-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4b67d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b67d-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4b67d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b67d-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b67d-129">INPUTS</span></span>

### <span data-ttu-id="4b67d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4b67d-130">System.String</span></span>

## <span data-ttu-id="4b67d-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b67d-131">OUTPUTS</span></span>

### <span data-ttu-id="4b67d-132">Microsoft. Azure. Command. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="4b67d-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="4b67d-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4b67d-133">NOTES</span></span>

## <span data-ttu-id="4b67d-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b67d-134">RELATED LINKS</span></span>

[<span data-ttu-id="4b67d-135">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4b67d-135">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="4b67d-136">Új – AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4b67d-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="4b67d-137">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4b67d-137">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="4b67d-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="4b67d-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

