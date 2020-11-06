---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: cc0d7163b9251037f4127d8fc6894f74f103436b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498720"
---
# <span data-ttu-id="a89ed-101">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a89ed-101">New-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="a89ed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a89ed-102">SYNOPSIS</span></span>
<span data-ttu-id="a89ed-103">Tűzfal-szabályt hoz létre egy SQL-adatbázis-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="a89ed-103">Creates a firewall rule for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a89ed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a89ed-104">SYNTAX</span></span>

### <span data-ttu-id="a89ed-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="a89ed-105">UserSpecifiedRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a89ed-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="a89ed-106">AzureIpRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a89ed-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a89ed-107">DESCRIPTION</span></span>
<span data-ttu-id="a89ed-108">A **New-AzureRmSqlServerFirewallRule** parancsmag létrehoz egy tűzfal-szabályt a megadott Azure SQL-adatbázis-kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="a89ed-108">The **New-AzureRmSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="a89ed-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a89ed-109">EXAMPLES</span></span>

### <span data-ttu-id="a89ed-110">Példa 1: tűzfalszabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="a89ed-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="a89ed-111">Ez a parancs létrehoz egy Rule01 nevű tűzfal-szabályt a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="a89ed-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="a89ed-112">A szabály a megadott kezdési és befejezési IP-címeket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a89ed-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="a89ed-113">2. példa: tűzfalszabály létrehozása, amely lehetővé teszi, hogy az összes Azure IP-cím elérje a kiszolgálót</span><span class="sxs-lookup"><span data-stu-id="a89ed-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="a89ed-114">A parancs létrehoz egy tűzfal-szabályt a Server01 nevű kiszolgálón, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="a89ed-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="a89ed-115">Mivel a *AllowAllAzureIPs* paramétert használja, a tűzfalszabály lehetővé teszi, hogy az összes Azure IP-cím elérje a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="a89ed-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="a89ed-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a89ed-116">PARAMETERS</span></span>

### <span data-ttu-id="a89ed-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="a89ed-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="a89ed-118">Jelzi, hogy ez a tűzfalszabály engedélyezi az összes Azure IP-cím elérését a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="a89ed-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="a89ed-119">Ezt a paramétert nem használhatja, ha a *FirewallRuleName* , az *StartIpAddress* és a *EndIpAddress* paramétert szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="a89ed-119">You cannot use this parameter if you intend to use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="a89ed-120">Ha engedélyezni szeretné az Azure IPs számára a kiszolgáló elérését, ezt a paramétert külön parancsmagi hívásban kell használni, amely nem használja az *FirewallRuleName* , az *StartIpAddress* és a *EndIpAddress* paramétert.</span><span class="sxs-lookup"><span data-stu-id="a89ed-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureIpRuleSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89ed-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a89ed-121">-DefaultProfile</span></span>
<span data-ttu-id="a89ed-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a89ed-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89ed-123">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="a89ed-123">-EndIpAddress</span></span>
<span data-ttu-id="a89ed-124">A szabályhoz tartozó IP-címtartomány utolsó értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a89ed-124">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89ed-125">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="a89ed-125">-FirewallRuleName</span></span>
<span data-ttu-id="a89ed-126">Az új tűzfalszabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a89ed-126">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: UserSpecifiedRuleSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89ed-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a89ed-127">-ResourceGroupName</span></span>
<span data-ttu-id="a89ed-128">Annak a csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="a89ed-128">Specifies the name of a resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a89ed-129">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a89ed-129">-ServerName</span></span>
<span data-ttu-id="a89ed-130">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a89ed-130">Specifies the name of a server.</span></span>
<span data-ttu-id="a89ed-131">Adja meg a kiszolgáló nevét, nem a teljesen minősített DNS-nevet.</span><span class="sxs-lookup"><span data-stu-id="a89ed-131">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a89ed-132">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="a89ed-132">-StartIpAddress</span></span>
<span data-ttu-id="a89ed-133">A tűzfalszabály IP-címtartomány kezdetének értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a89ed-133">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89ed-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a89ed-134">-Confirm</span></span>
<span data-ttu-id="a89ed-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a89ed-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89ed-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a89ed-136">-WhatIf</span></span>
<span data-ttu-id="a89ed-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a89ed-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a89ed-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a89ed-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89ed-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a89ed-139">CommonParameters</span></span>
<span data-ttu-id="a89ed-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a89ed-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a89ed-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a89ed-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a89ed-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a89ed-142">INPUTS</span></span>

### <span data-ttu-id="a89ed-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="a89ed-143">None</span></span>
<span data-ttu-id="a89ed-144">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a89ed-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a89ed-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a89ed-145">OUTPUTS</span></span>

### <span data-ttu-id="a89ed-146">Microsoft. Azure. Command. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="a89ed-146">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="a89ed-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a89ed-147">NOTES</span></span>

## <span data-ttu-id="a89ed-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a89ed-148">RELATED LINKS</span></span>

[<span data-ttu-id="a89ed-149">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a89ed-149">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="a89ed-150">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a89ed-150">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="a89ed-151">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a89ed-151">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="a89ed-152">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a89ed-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


