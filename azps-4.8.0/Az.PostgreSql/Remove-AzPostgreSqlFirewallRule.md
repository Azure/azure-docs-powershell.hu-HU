---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 27f03ba80a01997d61bc50f6a644b4e3c4cffb7b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172803"
---
# <span data-ttu-id="92d3b-101">Remove-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="92d3b-101">Remove-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="92d3b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="92d3b-103">A kiszolgálói tűzfalszabályok törlése</span><span class="sxs-lookup"><span data-stu-id="92d3b-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="92d3b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92d3b-104">SYNTAX</span></span>

### <span data-ttu-id="92d3b-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="92d3b-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="92d3b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="92d3b-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="92d3b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="92d3b-107">DESCRIPTION</span></span>
<span data-ttu-id="92d3b-108">A kiszolgálói tűzfalszabályok törlése</span><span class="sxs-lookup"><span data-stu-id="92d3b-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="92d3b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="92d3b-109">EXAMPLES</span></span>

### <span data-ttu-id="92d3b-110">1. példa: a PostgreSql-tűzfal szabályának eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="92d3b-110">Example 1: Remove PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="92d3b-111">Ez a parancsmag eltávolítja a PostgreSql-tűzfal szabályát név szerint.</span><span class="sxs-lookup"><span data-stu-id="92d3b-111">This cmdlet removes PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="92d3b-112">2. példa: a PostgreSql-tűzfal szabályának eltávolítása identitással</span><span class="sxs-lookup"><span data-stu-id="92d3b-112">Example 2: Remove PostgreSql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Remove-AzPostgreSqlFirewallRule -InputObject $ID
 
```

<span data-ttu-id="92d3b-113">Ezek a parancsmagok eltávolítják a PostgreSql-tűzfal szabályát identitás szerint.</span><span class="sxs-lookup"><span data-stu-id="92d3b-113">These cmdlets remove PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="92d3b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92d3b-114">PARAMETERS</span></span>

### <span data-ttu-id="92d3b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92d3b-115">-AsJob</span></span>
<span data-ttu-id="92d3b-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="92d3b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="92d3b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92d3b-117">-DefaultProfile</span></span>
<span data-ttu-id="92d3b-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92d3b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92d3b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92d3b-119">-InputObject</span></span>
<span data-ttu-id="92d3b-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="92d3b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92d3b-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="92d3b-121">-Name</span></span>
<span data-ttu-id="92d3b-122">A kiszolgáló tűzfal-szabályának neve.</span><span class="sxs-lookup"><span data-stu-id="92d3b-122">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d3b-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="92d3b-123">-NoWait</span></span>
<span data-ttu-id="92d3b-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="92d3b-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="92d3b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92d3b-125">-PassThru</span></span>
<span data-ttu-id="92d3b-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="92d3b-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="92d3b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92d3b-127">-ResourceGroupName</span></span>
<span data-ttu-id="92d3b-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="92d3b-128">The name of the resource group.</span></span>
<span data-ttu-id="92d3b-129">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="92d3b-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d3b-130">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="92d3b-130">-ServerName</span></span>
<span data-ttu-id="92d3b-131">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="92d3b-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d3b-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92d3b-132">-SubscriptionId</span></span>
<span data-ttu-id="92d3b-133">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="92d3b-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d3b-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="92d3b-134">-Confirm</span></span>
<span data-ttu-id="92d3b-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="92d3b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92d3b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92d3b-136">-WhatIf</span></span>
<span data-ttu-id="92d3b-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="92d3b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92d3b-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="92d3b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92d3b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92d3b-139">CommonParameters</span></span>
<span data-ttu-id="92d3b-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92d3b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92d3b-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="92d3b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92d3b-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92d3b-142">INPUTS</span></span>

### <span data-ttu-id="92d3b-143">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="92d3b-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="92d3b-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92d3b-144">OUTPUTS</span></span>

### <span data-ttu-id="92d3b-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="92d3b-145">System.Boolean</span></span>

## <span data-ttu-id="92d3b-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92d3b-146">NOTES</span></span>

<span data-ttu-id="92d3b-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="92d3b-147">ALIASES</span></span>

<span data-ttu-id="92d3b-148">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="92d3b-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="92d3b-149">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="92d3b-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="92d3b-150">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="92d3b-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="92d3b-151">INPUTOBJECT <IPostgreSqlIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="92d3b-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="92d3b-152">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="92d3b-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="92d3b-153">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="92d3b-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="92d3b-154">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="92d3b-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="92d3b-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="92d3b-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="92d3b-156">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="92d3b-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="92d3b-157">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="92d3b-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="92d3b-158">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="92d3b-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="92d3b-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="92d3b-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="92d3b-160">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="92d3b-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="92d3b-161">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="92d3b-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="92d3b-162">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="92d3b-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="92d3b-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92d3b-163">RELATED LINKS</span></span>

