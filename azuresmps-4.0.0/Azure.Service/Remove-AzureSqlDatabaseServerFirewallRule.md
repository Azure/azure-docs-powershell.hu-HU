---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383DD041-78DC-4170-9529-1FD6F13BC178
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29cbf01629ef772fc41436f3916a2077c1535329
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016106"
---
# <span data-ttu-id="f484a-101">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f484a-101">Remove-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="f484a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f484a-102">SYNOPSIS</span></span>
<span data-ttu-id="f484a-103">Tűzfal-szabály eltávolítása Azure SQL-adatbázis-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="f484a-103">Removes a firewall rule from an Azure SQL Database server.</span></span>

## <span data-ttu-id="f484a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f484a-104">SYNTAX</span></span>

```
Remove-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f484a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f484a-105">DESCRIPTION</span></span>
<span data-ttu-id="f484a-106">A **Remove-AzureSqlDatabaseServerFirewallRule** parancsmag a jelenlegi előfizetésben az Azure SQL adatbázis-kiszolgáló példányaiból távolítja el a tűzfalszabályok egyikét.</span><span class="sxs-lookup"><span data-stu-id="f484a-106">The **Remove-AzureSqlDatabaseServerFirewallRule** cmdlet removes a firewall rule from an instance of Azure SQL Database Server in the current subscription.</span></span>

## <span data-ttu-id="f484a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f484a-107">EXAMPLES</span></span>

### <span data-ttu-id="f484a-108">1. példa: szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f484a-108">Example 1: Remove a rule</span></span>
```
PS C:\>Remove-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

<span data-ttu-id="f484a-109">Ez a parancs eltávolítja a FirewallRule24 nevű tűzfal-szabályt a lpqd0zbr8y nevű Azure SQL adatbázis-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="f484a-109">This command removes the firewall rule named FirewallRule24 from the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="f484a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f484a-110">PARAMETERS</span></span>

### <span data-ttu-id="f484a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="f484a-111">-Force</span></span>
<span data-ttu-id="f484a-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="f484a-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f484a-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="f484a-113">-Profile</span></span>
<span data-ttu-id="f484a-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="f484a-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f484a-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="f484a-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f484a-116">-RuleName</span><span class="sxs-lookup"><span data-stu-id="f484a-116">-RuleName</span></span>
<span data-ttu-id="f484a-117">A parancsmag által eltávolított tűzfalszabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f484a-117">Specifies the name of the firewall rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f484a-118">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f484a-118">-ServerName</span></span>
<span data-ttu-id="f484a-119">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f484a-119">Specifies the name of a server.</span></span>
<span data-ttu-id="f484a-120">Ez a parancsmag eltávolítja a tűzfal szabályát abban a kiszolgálón, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="f484a-120">This cmdlet removes a firewall rule from the server that this parameter specifies.</span></span>

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

### <span data-ttu-id="f484a-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f484a-121">-Confirm</span></span>
<span data-ttu-id="f484a-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f484a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f484a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f484a-123">-WhatIf</span></span>
<span data-ttu-id="f484a-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f484a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f484a-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f484a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f484a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f484a-126">CommonParameters</span></span>
<span data-ttu-id="f484a-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f484a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f484a-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f484a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f484a-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f484a-129">INPUTS</span></span>

### <span data-ttu-id="f484a-130">Microsoft. WindowsAzure. Command. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="f484a-130">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="f484a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f484a-131">OUTPUTS</span></span>

## <span data-ttu-id="f484a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f484a-132">NOTES</span></span>

## <span data-ttu-id="f484a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f484a-133">RELATED LINKS</span></span>

[<span data-ttu-id="f484a-134">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="f484a-134">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="f484a-135">Tűzfalszabály törlése</span><span class="sxs-lookup"><span data-stu-id="f484a-135">Delete Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505706.aspx)

[<span data-ttu-id="f484a-136">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="f484a-136">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="f484a-137">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f484a-137">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="f484a-138">Új – AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f484a-138">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="f484a-139">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f484a-139">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


