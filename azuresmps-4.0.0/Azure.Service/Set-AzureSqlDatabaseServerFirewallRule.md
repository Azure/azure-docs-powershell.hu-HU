---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F311A7A9-5FE9-4E81-8FF1-8E3A02F2BF4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: ce9d384a5dd7f57fb4444fb173864ec5859b3a81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015863"
---
# <span data-ttu-id="333e0-101">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="333e0-101">Set-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="333e0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="333e0-102">SYNOPSIS</span></span>
<span data-ttu-id="333e0-103">A meglévő tűzfalszabályok módosítása egy Azure SQL-adatbázis-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="333e0-103">Modifies an existing firewall rule in an Azure SQL Database Server.</span></span>

## <span data-ttu-id="333e0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="333e0-104">SYNTAX</span></span>

```
Set-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="333e0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="333e0-105">DESCRIPTION</span></span>
<span data-ttu-id="333e0-106">A **set-AzureSqlDatabaseServerFirewallRule** parancsmag az Azure SQL-adatbázis kiszolgálójának megadott példányában módosítja az IP-cím és a záró IP-cím értékét.</span><span class="sxs-lookup"><span data-stu-id="333e0-106">The **Set-AzureSqlDatabaseServerFirewallRule** cmdlet modifies the start IP address and end IP address values of an existing firewall rule in the specified instance of Azure SQL Database Server.</span></span>

## <span data-ttu-id="333e0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="333e0-107">EXAMPLES</span></span>

### <span data-ttu-id="333e0-108">Példa 1: tűzfalszabály módosítása</span><span class="sxs-lookup"><span data-stu-id="333e0-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\> Set-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.2 -EndIpAddress 10.1.1.4
```

<span data-ttu-id="333e0-109">Ez a parancs módosítja a lpqd0zbr8y nevű Azure SQL adatbázis-kiszolgálón a FirewallRule24 nevű tűzfal-szabály kezdő IP-címét és IP-címét.</span><span class="sxs-lookup"><span data-stu-id="333e0-109">This command modifies the start IP address and end IP address of the firewall rule named FirewallRule24 on the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="333e0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="333e0-110">PARAMETERS</span></span>

### <span data-ttu-id="333e0-111">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="333e0-111">-EndIpAddress</span></span>
<span data-ttu-id="333e0-112">A szabályhoz tartozó IP-címtartomány utolsó értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="333e0-112">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="333e0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="333e0-113">-Force</span></span>
<span data-ttu-id="333e0-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="333e0-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="333e0-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="333e0-115">-Profile</span></span>
<span data-ttu-id="333e0-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="333e0-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="333e0-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="333e0-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="333e0-118">-RuleName</span><span class="sxs-lookup"><span data-stu-id="333e0-118">-RuleName</span></span>
<span data-ttu-id="333e0-119">Annak a tűzfal-szabálynak a neve, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="333e0-119">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="333e0-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="333e0-120">-ServerName</span></span>
<span data-ttu-id="333e0-121">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="333e0-121">Specifies the name of a server.</span></span>
<span data-ttu-id="333e0-122">Ez a parancsmag létrehoz egy tűzfal-szabályt azon a kiszolgálón, amelyen a parancsmag meg van határozva.</span><span class="sxs-lookup"><span data-stu-id="333e0-122">This cmdlet creates a firewall rule on the server that this cmdlet specifies.</span></span>
<span data-ttu-id="333e0-123">Adja meg a kiszolgáló nevét, nem a teljesen minősített DNS-nevet.</span><span class="sxs-lookup"><span data-stu-id="333e0-123">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="333e0-124">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="333e0-124">-StartIpAddress</span></span>
<span data-ttu-id="333e0-125">A tűzfalszabály IP-címtartomány kezdetének értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="333e0-125">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="333e0-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="333e0-126">-Confirm</span></span>
<span data-ttu-id="333e0-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="333e0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="333e0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="333e0-128">-WhatIf</span></span>
<span data-ttu-id="333e0-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="333e0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="333e0-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="333e0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="333e0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="333e0-131">CommonParameters</span></span>
<span data-ttu-id="333e0-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="333e0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="333e0-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="333e0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="333e0-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="333e0-134">INPUTS</span></span>

### <span data-ttu-id="333e0-135">Microsoft. WindowsAzure. Command. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="333e0-135">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="333e0-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="333e0-136">OUTPUTS</span></span>

### <span data-ttu-id="333e0-137">Microsoft. WindowsAzure. Command. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="333e0-137">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="333e0-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="333e0-138">NOTES</span></span>

## <span data-ttu-id="333e0-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="333e0-139">RELATED LINKS</span></span>

[<span data-ttu-id="333e0-140">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="333e0-140">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="333e0-141">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="333e0-141">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="333e0-142">Tűzfalszabály beállítása</span><span class="sxs-lookup"><span data-stu-id="333e0-142">Set Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505707.aspx)

[<span data-ttu-id="333e0-143">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="333e0-143">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="333e0-144">Új – AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="333e0-144">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="333e0-145">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="333e0-145">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)


