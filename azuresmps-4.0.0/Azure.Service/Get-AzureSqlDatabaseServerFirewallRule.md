---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: BE00A25D-3ECE-4B27-9D79-78128CFEBDB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 100202df1871610aff3af1fe90bb7d603c141d62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015572"
---
# <span data-ttu-id="c855a-101">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c855a-101">Get-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="c855a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c855a-102">SYNOPSIS</span></span>
<span data-ttu-id="c855a-103">Tűzfal-szabályok beolvasása az Azure SQL adatbázis-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="c855a-103">Gets firewall rules for Azure SQL Database Server.</span></span>

## <span data-ttu-id="c855a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c855a-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c855a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c855a-105">DESCRIPTION</span></span>
<span data-ttu-id="c855a-106">A **Get-AzureSqlDatabaseServerFirewallRule** parancsmag tűzfal-szabályokat kap az Azure SQL-adatbázis-kiszolgálók egy példányához.</span><span class="sxs-lookup"><span data-stu-id="c855a-106">The **Get-AzureSqlDatabaseServerFirewallRule** cmdlet gets firewall rules for an instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="c855a-107">Ha a tűzfal szabályát név szerint adja meg, ez a parancsmag információt ad a tűzfalszabályról.</span><span class="sxs-lookup"><span data-stu-id="c855a-107">If you specify a firewall rule by name, this cmdlet returns information about that firewall rule.</span></span>
<span data-ttu-id="c855a-108">Máskülönben a parancsmag információt ad a megadott Azure SQL-adatbázis-kiszolgálón lévő összes tűzfal-szabályról.</span><span class="sxs-lookup"><span data-stu-id="c855a-108">Otherwise, the cmdlet returns information about all the firewall rules on the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="c855a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c855a-109">EXAMPLES</span></span>

### <span data-ttu-id="c855a-110">Példa 1: a tűzfal összes szabályának beolvasása a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="c855a-110">Example 1: Get all firewall rules on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="c855a-111">Ez a parancs a lpqd0zbr8y nevű Azure SQL adatbázis-kiszolgálón a tűzfalszabályok összes szabályát megkapja.</span><span class="sxs-lookup"><span data-stu-id="c855a-111">This command gets all the firewall rules on the Azure SQL Database server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="c855a-112">2. példa: tűzfalszabály beszerzése a neve alapján</span><span class="sxs-lookup"><span data-stu-id="c855a-112">Example 2: Get a firewall rule by using its name</span></span>
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

<span data-ttu-id="c855a-113">Ez a parancs a FirewallRule24 nevű tűzfal-szabályt a lpqd0zbr8y nevű kiszolgálón kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c855a-113">This command gets the firewall rule named FirewallRule24 on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="c855a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c855a-114">PARAMETERS</span></span>

### <span data-ttu-id="c855a-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="c855a-115">-Profile</span></span>
<span data-ttu-id="c855a-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="c855a-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c855a-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="c855a-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c855a-118">-RuleName</span><span class="sxs-lookup"><span data-stu-id="c855a-118">-RuleName</span></span>
<span data-ttu-id="c855a-119">Annak a tűzfal-szabálynak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="c855a-119">Specifies the name of the firewall rule that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c855a-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="c855a-120">-ServerName</span></span>
<span data-ttu-id="c855a-121">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c855a-121">Specifies the name of a server.</span></span>
<span data-ttu-id="c855a-122">Ez a parancsmag tűzfal-szabályokat kap a kiszolgálótól, amelyre ez a paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="c855a-122">This cmdlet gets firewall rules from the server that this parameter specifies.</span></span>
<span data-ttu-id="c855a-123">Adja meg a kiszolgáló nevét, nem a teljesen minősített DNS-nevet.</span><span class="sxs-lookup"><span data-stu-id="c855a-123">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="c855a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c855a-124">CommonParameters</span></span>
<span data-ttu-id="c855a-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c855a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c855a-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c855a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c855a-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c855a-127">INPUTS</span></span>

### <span data-ttu-id="c855a-128">Microsoft. WindowsAzure. Command. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="c855a-128">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="c855a-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c855a-129">OUTPUTS</span></span>

### <span data-ttu-id="c855a-130">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\></span><span class="sxs-lookup"><span data-stu-id="c855a-130">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\></span></span>

## <span data-ttu-id="c855a-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c855a-131">NOTES</span></span>

## <span data-ttu-id="c855a-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c855a-132">RELATED LINKS</span></span>

[<span data-ttu-id="c855a-133">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="c855a-133">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="c855a-134">Tűzfal-szabályok listázása</span><span class="sxs-lookup"><span data-stu-id="c855a-134">List Firewall Rules</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505715.aspx)

[<span data-ttu-id="c855a-135">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="c855a-135">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="c855a-136">Új – AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c855a-136">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="c855a-137">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c855a-137">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="c855a-138">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c855a-138">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


