---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
ms.openlocfilehash: 7274eb30cd7a96e6cf3c46dd37ebab2ddb283c64
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467136"
---
# <span data-ttu-id="81bb3-101">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="81bb3-101">New-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="81bb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="81bb3-103">Tűzfalszabályt hoz létre egy SQL-adatbázis-kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="81bb3-103">Creates a firewall rule for a SQL Database server.</span></span>

## <span data-ttu-id="81bb3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="81bb3-104">SYNTAX</span></span>

### <span data-ttu-id="81bb3-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="81bb3-105">UserSpecifiedRuleSet</span></span>
```
New-AzSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81bb3-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="81bb3-106">AzureIpRuleSet</span></span>
```
New-AzSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81bb3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="81bb3-107">DESCRIPTION</span></span>
<span data-ttu-id="81bb3-108">A **New-AzSqlServerFirewallRule** parancsmag tűzfalszabályt hoz létre a megadott Azure SQL Database-kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="81bb3-108">The **New-AzSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="81bb3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="81bb3-109">EXAMPLES</span></span>

### <span data-ttu-id="81bb3-110">1. példa: Tűzfalszabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="81bb3-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="81bb3-111">Ez a parancs létrehoz egy Szabály01 nevű tűzfalszabályt a Kiszolgáló01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="81bb3-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="81bb3-112">A szabály tartalmazza a megadott kezdő és záró IP-címeket.</span><span class="sxs-lookup"><span data-stu-id="81bb3-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="81bb3-113">2. példa: Tűzfalszabály létrehozása, amely lehetővé teszi, hogy az összes Azure IP-cím hozzáférjen a kiszolgálóhoz</span><span class="sxs-lookup"><span data-stu-id="81bb3-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="81bb3-114">Ez a parancs létrehoz egy tűzfalszabályt a Server01 nevű kiszolgálón, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="81bb3-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="81bb3-115">Mivel az *AllowAllAzureIPs* paraméter használatos, a tűzfalszabály lehetővé teszi, hogy az összes Azure IP-cím hozzáférjen a kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="81bb3-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="81bb3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81bb3-116">PARAMETERS</span></span>

### <span data-ttu-id="81bb3-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="81bb3-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="81bb3-118">Azt jelzi, hogy ez a tűzfalszabály lehetővé teszi, hogy az összes Azure IP-cím hozzáférjen a kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="81bb3-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="81bb3-119">Ez a paraméter nem használható, ha a *FirewallRuleName,* *a StartIpAddress* és az *EndIpAddress* paramétert szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="81bb3-119">You cannot use this parameter if you intend to use the *FirewallRuleName*, *StartIpAddress*, and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="81bb3-120">Ha engedélyezni szeretné az Azure IP-nek a kiszolgálóhoz való hozzáférését, ezt a paramétert egy külön parancsmaghívásban kell használnia, amely nem használja a *FirewallRuleName,* a *StartIpAddress* és az *EndIpAddress* paramétert.</span><span class="sxs-lookup"><span data-stu-id="81bb3-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName*, *StartIpAddress*, and *EndIpAddress* parameters.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIpRuleSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81bb3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81bb3-121">-DefaultProfile</span></span>
<span data-ttu-id="81bb3-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="81bb3-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81bb3-123">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="81bb3-123">-EndIpAddress</span></span>
<span data-ttu-id="81bb3-124">A szabály IP-címtartományának záró értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="81bb3-124">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81bb3-125">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="81bb3-125">-FirewallRuleName</span></span>
<span data-ttu-id="81bb3-126">Az új tűzfalszabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="81bb3-126">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81bb3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81bb3-127">-ResourceGroupName</span></span>
<span data-ttu-id="81bb3-128">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="81bb3-128">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="81bb3-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="81bb3-129">-ServerName</span></span>
<span data-ttu-id="81bb3-130">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="81bb3-130">Specifies the name of a server.</span></span>
<span data-ttu-id="81bb3-131">A kiszolgáló nevét adja meg, ne a teljes DNS-nevet.</span><span class="sxs-lookup"><span data-stu-id="81bb3-131">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="81bb3-132">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="81bb3-132">-StartIpAddress</span></span>
<span data-ttu-id="81bb3-133">A tűzfalszabály IP-címtartományának kezdőértéke.</span><span class="sxs-lookup"><span data-stu-id="81bb3-133">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81bb3-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81bb3-134">-Confirm</span></span>
<span data-ttu-id="81bb3-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="81bb3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81bb3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81bb3-136">-WhatIf</span></span>
<span data-ttu-id="81bb3-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="81bb3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81bb3-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81bb3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81bb3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81bb3-139">CommonParameters</span></span>
<span data-ttu-id="81bb3-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81bb3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81bb3-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81bb3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81bb3-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81bb3-142">INPUTS</span></span>

### <span data-ttu-id="81bb3-143">System.String</span><span class="sxs-lookup"><span data-stu-id="81bb3-143">System.String</span></span>

## <span data-ttu-id="81bb3-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81bb3-144">OUTPUTS</span></span>

### <span data-ttu-id="81bb3-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="81bb3-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="81bb3-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="81bb3-146">NOTES</span></span>

## <span data-ttu-id="81bb3-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81bb3-147">RELATED LINKS</span></span>

[<span data-ttu-id="81bb3-148">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="81bb3-148">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="81bb3-149">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="81bb3-149">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="81bb3-150">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="81bb3-150">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="81bb3-151">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="81bb3-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


