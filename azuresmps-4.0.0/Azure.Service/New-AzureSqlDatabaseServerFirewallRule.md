---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A723D12D-DCF5-4F0C-AAC2-8BADFBAC3328
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0383e451d8346d4b6465390cc78850b270f6ac3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015969"
---
# <span data-ttu-id="892ce-101">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="892ce-101">New-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="892ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="892ce-102">SYNOPSIS</span></span>
<span data-ttu-id="892ce-103">Tűzfal-szabályt hoz létre az Azure SQL adatbázis-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="892ce-103">Creates a firewall rule in Azure SQL Database Server.</span></span>

## <span data-ttu-id="892ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="892ce-104">SYNTAX</span></span>

### <span data-ttu-id="892ce-105">IpRange (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="892ce-105">IpRange (Default)</span></span>
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="892ce-106">AllowAllAzureServices</span><span class="sxs-lookup"><span data-stu-id="892ce-106">AllowAllAzureServices</span></span>
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-AllowAllAzureServices]
 [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="892ce-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="892ce-107">DESCRIPTION</span></span>
<span data-ttu-id="892ce-108">A **New-AzureSqlDatabaseServerFirewallRule** parancsmag a jelenlegi előfizetésben az Azure SQL adatbázis-kiszolgáló meghatározott példányában hoz létre tűzfal-szabályt.</span><span class="sxs-lookup"><span data-stu-id="892ce-108">The **New-AzureSqlDatabaseServerFirewallRule** cmdlet creates a firewall rule in the specified instance of Azure SQL Database Server in the current subscription.</span></span>

<span data-ttu-id="892ce-109">A *StartIpAddress* és a *EndIpAddress* paraméterrel megadhatja, hogy az IP-címek milyen TARTOMÁNNYAL csatlakozzanak az Azure SQL-adatbázis kiszolgálójához.</span><span class="sxs-lookup"><span data-stu-id="892ce-109">Use the *StartIpAddress* and *EndIpAddress* parameters to specify a range of IP addresses that this rule allows to connect to the Azure SQL Database server.</span></span>

<span data-ttu-id="892ce-110">Adja meg a *AllowAllAzureServices* paramétert egy olyan szabály létrehozásához, amely engedélyezi az Azure-kapcsolatokat a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="892ce-110">Specify the *AllowAllAzureServices* parameter to create a rule that allows Azure connections to the server.</span></span>
<span data-ttu-id="892ce-111">A szabály a 0.0.0.0 végződésű IP-cím értékeit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="892ce-111">The rule has starting and ending IP address values of 0.0.0.0.</span></span>
<span data-ttu-id="892ce-112">Ha nem ad meg tűzfal-szabályt, ez a parancsmag az alapértelmezett név AllowAllAzureServices rendeli hozzá.</span><span class="sxs-lookup"><span data-stu-id="892ce-112">If you do not specify a firewall rule name, this cmdlet assigns the default name AllowAllAzureServices.</span></span>

## <span data-ttu-id="892ce-113">Példák</span><span class="sxs-lookup"><span data-stu-id="892ce-113">EXAMPLES</span></span>

### <span data-ttu-id="892ce-114">Példa 1: tűzfalszabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="892ce-114">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.1 -EndIpAddress 10.1.1.2
```

<span data-ttu-id="892ce-115">Ez a parancs létrehoz egy FirewallRule24 a lpqd0zbr8y nevű Azure SQL adatbázis-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="892ce-115">This command creates a firewall rule FirewallRule24 on the Azure SQL Database server named lpqd0zbr8y.</span></span>
<span data-ttu-id="892ce-116">A parancs IP-címtartományt ad meg.</span><span class="sxs-lookup"><span data-stu-id="892ce-116">The command specifies an IP address range.</span></span>

### <span data-ttu-id="892ce-117">2. példa: szabály létrehozása, amely lehetővé teszi az összes Azure-szolgáltatás beállítását</span><span class="sxs-lookup"><span data-stu-id="892ce-117">Example 2: Create a rule that allows all Azure services</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices -RuleName "AzureConnections"
```

<span data-ttu-id="892ce-118">Ez a parancs létrehoz egy AzureConnections nevű tűzfal-szabályt a lpqd0zbr8y nevű kiszolgálón, amely lehetővé teszi az Azure-kapcsolatokat.</span><span class="sxs-lookup"><span data-stu-id="892ce-118">This command creates a firewall rule named AzureConnections on the server named lpqd0zbr8y that allows Azure connections.</span></span>

### <span data-ttu-id="892ce-119">3. példa: szabály létrehozása, amely lehetővé teszi az alapértelmezett nevű összes Azure-szolgáltatás létrehozását, amely lehetővé teszi az alapértelmezett nevet használó összes Azure-szolgáltatás beállítását</span><span class="sxs-lookup"><span data-stu-id="892ce-119">Example 3: Create a rule that allows all Azure services that uses the default name Create a rule that allows all Azure services that uses the default name</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices
```

<span data-ttu-id="892ce-120">A parancs létrehoz egy tűzfal-szabályt a lpqd0zbr8y nevű kiszolgálón, amely lehetővé teszi az Azure-kapcsolatokat.</span><span class="sxs-lookup"><span data-stu-id="892ce-120">This command creates a firewall rule on the specified server named lpqd0zbr8y that allows Azure connections.</span></span>
<span data-ttu-id="892ce-121">A parancs hozzárendeli az alapértelmezett szabály nevét AllowAllAzureServices.</span><span class="sxs-lookup"><span data-stu-id="892ce-121">The command assigns the default rule name AllowAllAzureServices.</span></span>

## <span data-ttu-id="892ce-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="892ce-122">PARAMETERS</span></span>

### <span data-ttu-id="892ce-123">-AllowAllAzureServices</span><span class="sxs-lookup"><span data-stu-id="892ce-123">-AllowAllAzureServices</span></span>
<span data-ttu-id="892ce-124">Jelzi, hogy ez a tűzfalszabály engedélyezi az összes Azure IP-cím elérését a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="892ce-124">Indicates that this firewall rule enables all Azure IP addresses to access the server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892ce-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="892ce-125">-EndIpAddress</span></span>
<span data-ttu-id="892ce-126">A szabályhoz tartozó IP-címtartomány utolsó értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="892ce-126">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892ce-127">-Force</span><span class="sxs-lookup"><span data-stu-id="892ce-127">-Force</span></span>
<span data-ttu-id="892ce-128">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="892ce-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="892ce-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="892ce-129">-Profile</span></span>
<span data-ttu-id="892ce-130">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="892ce-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="892ce-131">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="892ce-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="892ce-132">-RuleName</span><span class="sxs-lookup"><span data-stu-id="892ce-132">-RuleName</span></span>
<span data-ttu-id="892ce-133">Az új tűzfalszabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="892ce-133">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892ce-134">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="892ce-134">-ServerName</span></span>
<span data-ttu-id="892ce-135">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="892ce-135">Specifies the name of a server.</span></span>
<span data-ttu-id="892ce-136">Ez a parancsmag létrehoz egy tűzfal-szabályt azon a kiszolgálón, amelyen a parancsmag meg van határozva.</span><span class="sxs-lookup"><span data-stu-id="892ce-136">This cmdlet creates a firewall rule on the server that this cmdlet specifies.</span></span>
<span data-ttu-id="892ce-137">Adja meg a kiszolgáló nevét, nem a teljesen minősített DNS-nevet.</span><span class="sxs-lookup"><span data-stu-id="892ce-137">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="892ce-138">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="892ce-138">-StartIpAddress</span></span>
<span data-ttu-id="892ce-139">A tűzfalszabály IP-címtartomány kezdetének értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="892ce-139">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892ce-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="892ce-140">-Confirm</span></span>
<span data-ttu-id="892ce-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="892ce-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="892ce-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="892ce-142">-WhatIf</span></span>
<span data-ttu-id="892ce-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="892ce-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="892ce-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="892ce-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="892ce-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="892ce-145">CommonParameters</span></span>
<span data-ttu-id="892ce-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="892ce-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="892ce-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="892ce-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="892ce-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="892ce-148">INPUTS</span></span>

## <span data-ttu-id="892ce-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="892ce-149">OUTPUTS</span></span>

### <span data-ttu-id="892ce-150">Microsoft. WindowsAzure. Command. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="892ce-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="892ce-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="892ce-151">NOTES</span></span>

## <span data-ttu-id="892ce-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="892ce-152">RELATED LINKS</span></span>

[<span data-ttu-id="892ce-153">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="892ce-153">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="892ce-154">Tűzfalszabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="892ce-154">Create Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505712.aspx)

[<span data-ttu-id="892ce-155">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="892ce-155">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="892ce-156">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="892ce-156">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="892ce-157">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="892ce-157">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="892ce-158">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="892ce-158">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


