---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: bafd0e20530198da87c1fa3ece36905e73307a42
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187570"
---
# <span data-ttu-id="a2eab-101">New-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a2eab-101">New-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="a2eab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2eab-102">SYNOPSIS</span></span>
<span data-ttu-id="a2eab-103">Új tűzfalszabály létrehozása vagy meglévő tűzfalszabály frissítése</span><span class="sxs-lookup"><span data-stu-id="a2eab-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="a2eab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2eab-104">SYNTAX</span></span>

### <span data-ttu-id="a2eab-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2eab-105">CreateExpanded (Default)</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a2eab-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="a2eab-106">AllowAll</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a2eab-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="a2eab-107">ClientIPAddress</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a2eab-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2eab-108">DESCRIPTION</span></span>
<span data-ttu-id="a2eab-109">Új tűzfalszabály létrehozása vagy meglévő tűzfalszabály frissítése</span><span class="sxs-lookup"><span data-stu-id="a2eab-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="a2eab-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a2eab-110">EXAMPLES</span></span>

### <span data-ttu-id="a2eab-111">1. példa: új PostgreSql-kiszolgáló tűzfal-szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="a2eab-111">Example 1: Create a new PostgreSql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="a2eab-112">Ezzel a parancsmaggal létrehozhatja a PostgreSql Server-tűzfalszabályok szabályát.</span><span class="sxs-lookup"><span data-stu-id="a2eab-112">This cmdlets create a PostgreSql server Firewall Rule.</span></span>

### <span data-ttu-id="a2eab-113">2. példa: új PostgreSql-tűzfalszabályok létrehozása a-ClientIPAddress használatával.</span><span class="sxs-lookup"><span data-stu-id="a2eab-113">Example 2: Create a new PostgreSql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="a2eab-114">Ezzel a parancsmaggal létrehozhatja a PostgreSql-tűzfal szabályát a-ClientIPAddress-ban.</span><span class="sxs-lookup"><span data-stu-id="a2eab-114">This cmdlets create a PostgreSql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="a2eab-115">3. példa: új PostgreSql-tűzfal szabály létrehozása az összes IPs engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="a2eab-115">Example 3: Create a new PostgreSql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="a2eab-116">Ezzel a parancsmaggal új PostgreSql-tűzfalszabályok hozhatók létre az összes IP-hez.</span><span class="sxs-lookup"><span data-stu-id="a2eab-116">This cmdlets create a new PostgreSql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="a2eab-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2eab-117">PARAMETERS</span></span>

### <span data-ttu-id="a2eab-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="a2eab-118">-AllowAll</span></span>
<span data-ttu-id="a2eab-119">A 0.0.0.0-től a 255.255.255.255-ig terjedő összes IP-t engedélyezni kell.</span><span class="sxs-lookup"><span data-stu-id="a2eab-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AllowAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2eab-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2eab-120">-AsJob</span></span>
<span data-ttu-id="a2eab-121">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="a2eab-121">Run the command as a job</span></span>

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

### <span data-ttu-id="a2eab-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="a2eab-122">-ClientIPAddress</span></span>
<span data-ttu-id="a2eab-123">Ügyfél: a kiszolgálói tűzfalszabályok egyetlen IP-címe van megadva.</span><span class="sxs-lookup"><span data-stu-id="a2eab-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="a2eab-124">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="a2eab-124">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2eab-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2eab-125">-DefaultProfile</span></span>
<span data-ttu-id="a2eab-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2eab-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2eab-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="a2eab-127">-EndIPAddress</span></span>
<span data-ttu-id="a2eab-128">A kiszolgáló tűzfal-szabályának End IP-címe.</span><span class="sxs-lookup"><span data-stu-id="a2eab-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="a2eab-129">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="a2eab-129">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2eab-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a2eab-130">-Name</span></span>
<span data-ttu-id="a2eab-131">A kiszolgáló tűzfal-szabályának neve.</span><span class="sxs-lookup"><span data-stu-id="a2eab-131">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2eab-132">-Várva</span><span class="sxs-lookup"><span data-stu-id="a2eab-132">-NoWait</span></span>
<span data-ttu-id="a2eab-133">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="a2eab-133">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a2eab-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2eab-134">-ResourceGroupName</span></span>
<span data-ttu-id="a2eab-135">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a2eab-135">The name of the resource group.</span></span>
<span data-ttu-id="a2eab-136">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="a2eab-136">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2eab-137">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a2eab-137">-ServerName</span></span>
<span data-ttu-id="a2eab-138">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="a2eab-138">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2eab-139">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="a2eab-139">-StartIPAddress</span></span>
<span data-ttu-id="a2eab-140">A kiszolgáló tűzfal-szabályának kezdő IP-címe.</span><span class="sxs-lookup"><span data-stu-id="a2eab-140">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="a2eab-141">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="a2eab-141">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2eab-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2eab-142">-SubscriptionId</span></span>
<span data-ttu-id="a2eab-143">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a2eab-143">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2eab-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a2eab-144">-Confirm</span></span>
<span data-ttu-id="a2eab-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a2eab-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2eab-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2eab-146">-WhatIf</span></span>
<span data-ttu-id="a2eab-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a2eab-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2eab-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2eab-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2eab-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2eab-149">CommonParameters</span></span>
<span data-ttu-id="a2eab-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2eab-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2eab-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a2eab-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2eab-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2eab-152">INPUTS</span></span>

## <span data-ttu-id="a2eab-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2eab-153">OUTPUTS</span></span>

### <span data-ttu-id="a2eab-154">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a2eab-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="a2eab-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2eab-155">NOTES</span></span>

<span data-ttu-id="a2eab-156">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a2eab-156">ALIASES</span></span>

## <span data-ttu-id="a2eab-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2eab-157">RELATED LINKS</span></span>

