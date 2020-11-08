---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
ms.openlocfilehash: 7fdc31b4a64733ce686b38ccfb176f754f3f84ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187929"
---
# <span data-ttu-id="fac60-101">Get-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="fac60-101">Get-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="fac60-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fac60-102">SYNOPSIS</span></span>
<span data-ttu-id="fac60-103">Információt kap a kiszolgáló konfigurációjáról.</span><span class="sxs-lookup"><span data-stu-id="fac60-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="fac60-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fac60-104">SYNTAX</span></span>

### <span data-ttu-id="fac60-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fac60-105">List (Default)</span></span>
```
Get-AzPostgreSqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fac60-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="fac60-106">Get</span></span>
```
Get-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fac60-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fac60-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="fac60-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fac60-108">DESCRIPTION</span></span>
<span data-ttu-id="fac60-109">Információt kap a kiszolgáló konfigurációjáról.</span><span class="sxs-lookup"><span data-stu-id="fac60-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="fac60-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fac60-110">EXAMPLES</span></span>

### <span data-ttu-id="fac60-111">1. példa: a PostgreSql-kiszolgáló összes konfigurációjának listázása</span><span class="sxs-lookup"><span data-stu-id="fac60-111">Example 1: List all configurations in PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                                  Value
----                                  -----
array_nulls                           on
backslash_quote                       safe_encoding
bytea_output                          hex
check_function_bodies                 on
client_encoding                       sql_ascii
...
azure.replication_support             REPLICA
max_wal_senders                       10
max_replication_slots                 10
hot_standby_feedback                  off
logging_collector                     on
```

<span data-ttu-id="fac60-112">Ez a parancsmag a megadott PostgreSql-kiszolgáló összes konfigurációját felsorolja.</span><span class="sxs-lookup"><span data-stu-id="fac60-112">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

### <span data-ttu-id="fac60-113">2. példa: meghatározott PostgreSql-konfiguráció beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="fac60-113">Example 2: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -Name timezone -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name     Value
----     -----
timezone UTC
```

<span data-ttu-id="fac60-114">Ez a parancsmag név szerint adja meg a PostgreSql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="fac60-114">This cmdlet gets specified PostgreSql configuration by name.</span></span>

## <span data-ttu-id="fac60-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fac60-115">PARAMETERS</span></span>

### <span data-ttu-id="fac60-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fac60-116">-DefaultProfile</span></span>
<span data-ttu-id="fac60-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fac60-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fac60-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fac60-118">-InputObject</span></span>
<span data-ttu-id="fac60-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fac60-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fac60-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fac60-120">-Name</span></span>
<span data-ttu-id="fac60-121">A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="fac60-121">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac60-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fac60-122">-ResourceGroupName</span></span>
<span data-ttu-id="fac60-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fac60-123">The name of the resource group.</span></span>
<span data-ttu-id="fac60-124">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="fac60-124">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac60-125">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="fac60-125">-ServerName</span></span>
<span data-ttu-id="fac60-126">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="fac60-126">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac60-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fac60-127">-SubscriptionId</span></span>
<span data-ttu-id="fac60-128">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fac60-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac60-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fac60-129">CommonParameters</span></span>
<span data-ttu-id="fac60-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fac60-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fac60-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fac60-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fac60-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fac60-132">INPUTS</span></span>

### <span data-ttu-id="fac60-133">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="fac60-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="fac60-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fac60-134">OUTPUTS</span></span>

### <span data-ttu-id="fac60-135">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="fac60-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="fac60-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fac60-136">NOTES</span></span>

<span data-ttu-id="fac60-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="fac60-137">ALIASES</span></span>

<span data-ttu-id="fac60-138">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="fac60-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fac60-139">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="fac60-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fac60-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="fac60-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fac60-141">INPUTOBJECT <IPostgreSqlIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="fac60-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fac60-142">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="fac60-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="fac60-143">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="fac60-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="fac60-144">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="fac60-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="fac60-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="fac60-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fac60-146">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="fac60-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="fac60-147">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fac60-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fac60-148">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="fac60-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="fac60-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="fac60-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="fac60-150">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="fac60-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="fac60-151">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fac60-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fac60-152">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="fac60-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="fac60-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fac60-153">RELATED LINKS</span></span>

