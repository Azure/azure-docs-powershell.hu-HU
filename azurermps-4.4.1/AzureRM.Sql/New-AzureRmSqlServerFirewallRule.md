---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: b40ac97f5658758fa77900dfc31da5f77fb5d0e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672187"
---
# <span data-ttu-id="2b5b7-101">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2b5b7-101">New-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="2b5b7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b5b7-102">SYNOPSIS</span></span>
<span data-ttu-id="2b5b7-103">Tűzfal-szabályt hoz létre egy SQL-adatbázis-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="2b5b7-103">Creates a firewall rule for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b5b7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b5b7-104">SYNTAX</span></span>

### <span data-ttu-id="2b5b7-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b5b7-105">UserSpecifiedRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b5b7-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b5b7-106">AzureIpRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b5b7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b5b7-107">DESCRIPTION</span></span>
<span data-ttu-id="2b5b7-108">A **New-AzureRmSqlServerFirewallRule** parancsmag létrehoz egy tűzfal-szabályt a megadott Azure SQL-adatbázis-kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="2b5b7-108">The **New-AzureRmSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="2b5b7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2b5b7-109">EXAMPLES</span></span>

### <span data-ttu-id="2b5b7-110">Példa 1: tűzfalszabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="2b5b7-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="2b5b7-111">Ez a parancs létrehoz egy Rule01 nevű tűzfal-szabályt a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="2b5b7-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="2b5b7-112">A szabály a megadott kezdési és befejezési IP-címeket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2b5b7-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="2b5b7-113">2. példa: tűzfalszabály létrehozása, amely lehetővé teszi, hogy az összes Azure IP-cím elérje a kiszolgálót</span><span class="sxs-lookup"><span data-stu-id="2b5b7-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="2b5b7-114">A parancs létrehoz egy tűzfal-szabályt a Server01 nevű kiszolgálón, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="2b5b7-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="2b5b7-115">Mivel a *AllowAllAzureIPs* paramétert használja, a tűzfalszabály lehetővé teszi, hogy az összes Azure IP-cím elérje a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="2b5b7-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="2b5b7-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b5b7-116">PARAMETERS</span></span>

### <span data-ttu-id="2b5b7-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="2b5b7-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="2b5b7-118">Jelzi, hogy ez a tűzfalszabály engedélyezi az összes Azure IP-cím elérését a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="2b5b7-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="2b5b7-119">Ezt a paramétert nem használhatja, ha a *FirewallRuleName* , az *StartIpAddress* és a *EndIpAddress* paramétert szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="2b5b7-119">You cannot use this parameter if you intend to use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="2b5b7-120">Ha engedélyezni szeretné az Azure IPs számára a kiszolgáló elérését, ezt a paramétert külön parancsmagi hívásban kell használni, amely nem használja az *FirewallRuleName* , az *StartIpAddress* és a *EndIpAddress* paramétert.</span><span class="sxs-lookup"><span data-stu-id="2b5b7-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>

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

### <span data-ttu-id="2b5b7-121">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="2b5b7-121">-EndIpAddress</span></span>
<span data-ttu-id="2b5b7-122">A szabályhoz tartozó IP-címtartomány utolsó értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b5b7-122">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="2b5b7-123">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="2b5b7-123">-FirewallRuleName</span></span>
<span data-ttu-id="2b5b7-124">Az új tűzfalszabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b5b7-124">Specifies the name of the new firewall rule.</span></span>

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

### <span data-ttu-id="2b5b7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b5b7-125">-ResourceGroupName</span></span>
<span data-ttu-id="2b5b7-126">Annak a csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="2b5b7-126">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="2b5b7-127">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="2b5b7-127">-ServerName</span></span>
<span data-ttu-id="2b5b7-128">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b5b7-128">Specifies the name of a server.</span></span>
<span data-ttu-id="2b5b7-129">Adja meg a kiszolgáló nevét, nem a teljesen minősített DNS-nevet.</span><span class="sxs-lookup"><span data-stu-id="2b5b7-129">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="2b5b7-130">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="2b5b7-130">-StartIpAddress</span></span>
<span data-ttu-id="2b5b7-131">A tűzfalszabály IP-címtartomány kezdetének értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b5b7-131">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="2b5b7-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2b5b7-132">-Confirm</span></span>
<span data-ttu-id="2b5b7-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2b5b7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b5b7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b5b7-134">-WhatIf</span></span>
<span data-ttu-id="2b5b7-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2b5b7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b5b7-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2b5b7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b5b7-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b5b7-137">-DefaultProfile</span></span>
<span data-ttu-id="2b5b7-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b5b7-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b5b7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b5b7-139">CommonParameters</span></span>
<span data-ttu-id="2b5b7-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b5b7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b5b7-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b5b7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b5b7-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b5b7-142">INPUTS</span></span>

## <span data-ttu-id="2b5b7-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b5b7-143">OUTPUTS</span></span>

### <span data-ttu-id="2b5b7-144">Microsoft. Azure. Command. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="2b5b7-144">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="2b5b7-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b5b7-145">NOTES</span></span>

## <span data-ttu-id="2b5b7-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b5b7-146">RELATED LINKS</span></span>

[<span data-ttu-id="2b5b7-147">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2b5b7-147">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="2b5b7-148">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2b5b7-148">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="2b5b7-149">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2b5b7-149">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="2b5b7-150">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="2b5b7-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


