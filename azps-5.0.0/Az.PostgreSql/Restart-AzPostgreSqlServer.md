---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restart-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
ms.openlocfilehash: aa5e58522aaeb1094ef2a7280b33b45e20fe03fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188222"
---
# <span data-ttu-id="f2b77-101">Restart-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="f2b77-101">Restart-AzPostgreSqlServer</span></span>

## <span data-ttu-id="f2b77-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f2b77-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b77-103">Kiszolgáló újraindítása.</span><span class="sxs-lookup"><span data-stu-id="f2b77-103">Restarts a server.</span></span>

## <span data-ttu-id="f2b77-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f2b77-104">SYNTAX</span></span>

### <span data-ttu-id="f2b77-105">Újraindítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f2b77-105">Restart (Default)</span></span>
```
Restart-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f2b77-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f2b77-106">RestartViaIdentity</span></span>
```
Restart-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f2b77-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f2b77-107">DESCRIPTION</span></span>
<span data-ttu-id="f2b77-108">Kiszolgáló újraindítása.</span><span class="sxs-lookup"><span data-stu-id="f2b77-108">Restarts a server.</span></span>

## <span data-ttu-id="f2b77-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f2b77-109">EXAMPLES</span></span>

### <span data-ttu-id="f2b77-110">1. példa: a PostgreSql-kiszolgáló újraindítása erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="f2b77-110">Example 1: Restart PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Restart-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

```

<span data-ttu-id="f2b77-111">Ez a parancsmag az erőforráscsoport és a kiszolgáló neve alapján indítja el a PostgreSql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="f2b77-111">This cmdlet restarts PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="f2b77-112">2. példa: a PostgreSql-kiszolgáló újraindítása identitással</span><span class="sxs-lookup"><span data-stu-id="f2b77-112">Example 2: Restart PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/restart"
PS C:\> Restart-AzPostgreSqlServer -InputObject $ID
 
```

<span data-ttu-id="f2b77-113">Ezek a parancsmagok identitással indítják újra a PostgreSql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="f2b77-113">These cmdlets restart PostgreSql server by identity.</span></span>

## <span data-ttu-id="f2b77-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f2b77-114">PARAMETERS</span></span>

### <span data-ttu-id="f2b77-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2b77-115">-AsJob</span></span>
<span data-ttu-id="f2b77-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="f2b77-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f2b77-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2b77-117">-DefaultProfile</span></span>
<span data-ttu-id="f2b77-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2b77-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2b77-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2b77-119">-InputObject</span></span>
<span data-ttu-id="f2b77-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f2b77-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2b77-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f2b77-121">-Name</span></span>
<span data-ttu-id="f2b77-122">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="f2b77-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b77-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="f2b77-123">-NoWait</span></span>
<span data-ttu-id="f2b77-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="f2b77-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f2b77-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2b77-125">-PassThru</span></span>
<span data-ttu-id="f2b77-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="f2b77-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f2b77-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2b77-127">-ResourceGroupName</span></span>
<span data-ttu-id="f2b77-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f2b77-128">The name of the resource group.</span></span>
<span data-ttu-id="f2b77-129">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="f2b77-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b77-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2b77-130">-SubscriptionId</span></span>
<span data-ttu-id="f2b77-131">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f2b77-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b77-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f2b77-132">-Confirm</span></span>
<span data-ttu-id="f2b77-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f2b77-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2b77-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2b77-134">-WhatIf</span></span>
<span data-ttu-id="f2b77-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f2b77-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2b77-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f2b77-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2b77-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b77-137">CommonParameters</span></span>
<span data-ttu-id="f2b77-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f2b77-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b77-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f2b77-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b77-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2b77-140">INPUTS</span></span>

### <span data-ttu-id="f2b77-141">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="f2b77-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="f2b77-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2b77-142">OUTPUTS</span></span>

### <span data-ttu-id="f2b77-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f2b77-143">System.Boolean</span></span>

## <span data-ttu-id="f2b77-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f2b77-144">NOTES</span></span>

<span data-ttu-id="f2b77-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f2b77-145">ALIASES</span></span>

<span data-ttu-id="f2b77-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="f2b77-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f2b77-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f2b77-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f2b77-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="f2b77-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f2b77-149">INPUTOBJECT <IPostgreSqlIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="f2b77-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f2b77-150">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="f2b77-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f2b77-151">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="f2b77-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f2b77-152">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="f2b77-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f2b77-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f2b77-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f2b77-154">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="f2b77-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f2b77-155">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f2b77-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f2b77-156">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="f2b77-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="f2b77-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="f2b77-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f2b77-158">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="f2b77-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f2b77-159">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f2b77-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f2b77-160">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="f2b77-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f2b77-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2b77-161">RELATED LINKS</span></span>

