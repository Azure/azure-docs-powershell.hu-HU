---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
ms.openlocfilehash: 036628943afc8b2c5f07b30f2db14f27229364c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181783"
---
# <span data-ttu-id="5c4c5-101">New-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5c4c5-101">New-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="5c4c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5c4c5-102">SYNOPSIS</span></span>
<span data-ttu-id="5c4c5-103">Új tűzfalszabály létrehozása vagy meglévő tűzfalszabály frissítése</span><span class="sxs-lookup"><span data-stu-id="5c4c5-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="5c4c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5c4c5-104">SYNTAX</span></span>

### <span data-ttu-id="5c4c5-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5c4c5-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5c4c5-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="5c4c5-106">AllowAll</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5c4c5-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="5c4c5-107">ClientIPAddress</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5c4c5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5c4c5-108">DESCRIPTION</span></span>
<span data-ttu-id="5c4c5-109">Új tűzfalszabály létrehozása vagy meglévő tűzfalszabály frissítése</span><span class="sxs-lookup"><span data-stu-id="5c4c5-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="5c4c5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5c4c5-110">EXAMPLES</span></span>

### <span data-ttu-id="5c4c5-111">Példa 1: új MySql-kiszolgáló tűzfalszabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="5c4c5-111">Example 1: Create a new MySql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="5c4c5-112">Ezzel a parancsmaggal létrehozhatja a MySql-kiszolgáló tűzfalszabályok szabályát.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-112">This cmdlets create a MySql server Firewall Rule.</span></span>

### <span data-ttu-id="5c4c5-113">2. példa: hozzon létre egy új MySql tűzfal-szabályt a-ClientIPAddress-ban.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-113">Example 2: Create a new MySql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="5c4c5-114">Ezzel a parancsmaggal létrehozhatja a MySql tűzfal-szabályt a-ClientIPAddress-ban.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-114">This cmdlets create a MySql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="5c4c5-115">3. példa: új MySql tűzfalszabály létrehozása az összes IPs engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="5c4c5-115">Example 3: Create a new MySql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="5c4c5-116">Ezzel a parancsmaggal létrehozhatja az összes IP-hez az új MySql-tűzfalszabályok használatát.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-116">This cmdlets create a new MySql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="5c4c5-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5c4c5-117">PARAMETERS</span></span>

### <span data-ttu-id="5c4c5-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="5c4c5-118">-AllowAll</span></span>
<span data-ttu-id="5c4c5-119">A 0.0.0.0-től a 255.255.255.255-ig terjedő összes IP-t engedélyezni kell.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="5c4c5-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c4c5-120">-AsJob</span></span>
<span data-ttu-id="5c4c5-121">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="5c4c5-121">Run the command as a job</span></span>

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

### <span data-ttu-id="5c4c5-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="5c4c5-122">-ClientIPAddress</span></span>
<span data-ttu-id="5c4c5-123">Ügyfél: a kiszolgálói tűzfalszabályok egyetlen IP-címe van megadva.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="5c4c5-124">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="5c4c5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c4c5-125">-DefaultProfile</span></span>
<span data-ttu-id="5c4c5-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c4c5-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="5c4c5-127">-EndIPAddress</span></span>
<span data-ttu-id="5c4c5-128">A kiszolgáló tűzfal-szabályának End IP-címe.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="5c4c5-129">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="5c4c5-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5c4c5-130">-Name</span></span>
<span data-ttu-id="5c4c5-131">A kiszolgáló tűzfal-szabályának neve.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="5c4c5-132">Ha nincs megadva, az alapértelmezett érték nincs definiálva.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="5c4c5-133">Ha a AllowAll létezik, az alapértelmezett név AllowAll_yyyy-MM-dd_HH-mm-SS.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="5c4c5-134">-Várva</span><span class="sxs-lookup"><span data-stu-id="5c4c5-134">-NoWait</span></span>
<span data-ttu-id="5c4c5-135">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="5c4c5-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5c4c5-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c4c5-136">-ResourceGroupName</span></span>
<span data-ttu-id="5c4c5-137">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-137">The name of the resource group.</span></span>
<span data-ttu-id="5c4c5-138">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-138">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5c4c5-139">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="5c4c5-139">-ServerName</span></span>
<span data-ttu-id="5c4c5-140">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-140">The name of the server.</span></span>

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

### <span data-ttu-id="5c4c5-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="5c4c5-141">-StartIPAddress</span></span>
<span data-ttu-id="5c4c5-142">A kiszolgáló tűzfal-szabályának kezdő IP-címe.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="5c4c5-143">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="5c4c5-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5c4c5-144">-SubscriptionId</span></span>
<span data-ttu-id="5c4c5-145">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5c4c5-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5c4c5-146">-Confirm</span></span>
<span data-ttu-id="5c4c5-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c4c5-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c4c5-148">-WhatIf</span></span>
<span data-ttu-id="5c4c5-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c4c5-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c4c5-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c4c5-151">CommonParameters</span></span>
<span data-ttu-id="5c4c5-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5c4c5-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c4c5-153">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c4c5-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c4c5-154">INPUTS</span></span>

## <span data-ttu-id="5c4c5-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c4c5-155">OUTPUTS</span></span>

### <span data-ttu-id="5c4c5-156">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5c4c5-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="5c4c5-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5c4c5-157">NOTES</span></span>

<span data-ttu-id="5c4c5-158">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="5c4c5-158">ALIASES</span></span>

## <span data-ttu-id="5c4c5-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c4c5-159">RELATED LINKS</span></span>

