---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
ms.openlocfilehash: 83a68863b3dce71a091dc5de11377bade7bdc638
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164899"
---
# <span data-ttu-id="3412f-101">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3412f-101">Remove-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="3412f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3412f-102">SYNOPSIS</span></span>
<span data-ttu-id="3412f-103">Tűzfalszabály törlése SQL-adatbázis-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="3412f-103">Deletes a firewall rule from a SQL Database server.</span></span>

## <span data-ttu-id="3412f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3412f-104">SYNTAX</span></span>

```
Remove-AzSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3412f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3412f-105">DESCRIPTION</span></span>
<span data-ttu-id="3412f-106">A **Remove-AzSqlServerFirewallRule** parancsmag törli a tűzfalszabályt a megadott Azure SQL Database-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="3412f-106">The **Remove-AzSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="3412f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3412f-107">EXAMPLES</span></span>

### <span data-ttu-id="3412f-108">1. példa: Szabály törlése</span><span class="sxs-lookup"><span data-stu-id="3412f-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="3412f-109">Ez a parancs törli a Szabály01 nevű tűzfalszabályt a Kiszolgáló01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="3412f-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="3412f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3412f-110">PARAMETERS</span></span>

### <span data-ttu-id="3412f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3412f-111">-DefaultProfile</span></span>
<span data-ttu-id="3412f-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3412f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3412f-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="3412f-113">-FirewallRuleName</span></span>
<span data-ttu-id="3412f-114">A parancsmag által törölt tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="3412f-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="3412f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3412f-115">-Force</span></span>
<span data-ttu-id="3412f-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="3412f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3412f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3412f-117">-ResourceGroupName</span></span>
<span data-ttu-id="3412f-118">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="3412f-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="3412f-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3412f-119">-ServerName</span></span>
<span data-ttu-id="3412f-120">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3412f-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="3412f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3412f-121">-Confirm</span></span>
<span data-ttu-id="3412f-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3412f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3412f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3412f-123">-WhatIf</span></span>
<span data-ttu-id="3412f-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3412f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3412f-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3412f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3412f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3412f-126">CommonParameters</span></span>
<span data-ttu-id="3412f-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3412f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3412f-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3412f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3412f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3412f-129">INPUTS</span></span>

### <span data-ttu-id="3412f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3412f-130">System.String</span></span>

## <span data-ttu-id="3412f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3412f-131">OUTPUTS</span></span>

### <span data-ttu-id="3412f-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="3412f-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="3412f-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3412f-133">NOTES</span></span>

## <span data-ttu-id="3412f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3412f-134">RELATED LINKS</span></span>

[<span data-ttu-id="3412f-135">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3412f-135">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="3412f-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3412f-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="3412f-137">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3412f-137">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="3412f-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3412f-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


