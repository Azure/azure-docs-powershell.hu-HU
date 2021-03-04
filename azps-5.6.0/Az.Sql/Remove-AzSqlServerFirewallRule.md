---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
ms.openlocfilehash: 0b76faf383e8cd3c70d6ff1e7e38de367850ac8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926290"
---
# <span data-ttu-id="a1ea3-101">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a1ea3-101">Remove-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="a1ea3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="a1ea3-103">Tűzfalszabály törlése SQL-adatbázis-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="a1ea3-103">Deletes a firewall rule from a SQL Database server.</span></span>

## <span data-ttu-id="a1ea3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a1ea3-104">SYNTAX</span></span>

```
Remove-AzSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1ea3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a1ea3-105">DESCRIPTION</span></span>
<span data-ttu-id="a1ea3-106">A **Remove-AzSqlServerFirewallRule** parancsmag törli a tűzfalszabályt a megadott Azure SQL Database-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="a1ea3-106">The **Remove-AzSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="a1ea3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a1ea3-107">EXAMPLES</span></span>

### <span data-ttu-id="a1ea3-108">1. példa: Szabály törlése</span><span class="sxs-lookup"><span data-stu-id="a1ea3-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="a1ea3-109">Ez a parancs törli a Szabály01 nevű tűzfalszabályt a Kiszolgáló01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="a1ea3-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="a1ea3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1ea3-110">PARAMETERS</span></span>

### <span data-ttu-id="a1ea3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1ea3-111">-DefaultProfile</span></span>
<span data-ttu-id="a1ea3-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a1ea3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1ea3-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="a1ea3-113">-FirewallRuleName</span></span>
<span data-ttu-id="a1ea3-114">Annak a tűzfalszabálynak a nevét adja meg, amelyből a parancsmag töröl.</span><span class="sxs-lookup"><span data-stu-id="a1ea3-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="a1ea3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a1ea3-115">-Force</span></span>
<span data-ttu-id="a1ea3-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="a1ea3-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a1ea3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1ea3-117">-ResourceGroupName</span></span>
<span data-ttu-id="a1ea3-118">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="a1ea3-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a1ea3-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a1ea3-119">-ServerName</span></span>
<span data-ttu-id="a1ea3-120">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1ea3-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="a1ea3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1ea3-121">-Confirm</span></span>
<span data-ttu-id="a1ea3-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a1ea3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1ea3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1ea3-123">-WhatIf</span></span>
<span data-ttu-id="a1ea3-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a1ea3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1ea3-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1ea3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1ea3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1ea3-126">CommonParameters</span></span>
<span data-ttu-id="a1ea3-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1ea3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1ea3-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1ea3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1ea3-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1ea3-129">INPUTS</span></span>

### <span data-ttu-id="a1ea3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a1ea3-130">System.String</span></span>

## <span data-ttu-id="a1ea3-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1ea3-131">OUTPUTS</span></span>

### <span data-ttu-id="a1ea3-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="a1ea3-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="a1ea3-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a1ea3-133">NOTES</span></span>

## <span data-ttu-id="a1ea3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1ea3-134">RELATED LINKS</span></span>

[<span data-ttu-id="a1ea3-135">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a1ea3-135">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="a1ea3-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a1ea3-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="a1ea3-137">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a1ea3-137">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="a1ea3-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a1ea3-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


