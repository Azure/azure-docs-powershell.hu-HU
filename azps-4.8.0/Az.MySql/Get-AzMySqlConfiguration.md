---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
ms.openlocfilehash: b92390969c4650d60d5c4a6954520fbbf3f26c71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184413"
---
# <span data-ttu-id="d3354-101">Get-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3354-101">Get-AzMySqlConfiguration</span></span>

## <span data-ttu-id="d3354-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d3354-102">SYNOPSIS</span></span>
<span data-ttu-id="d3354-103">Információt kap a kiszolgáló konfigurációjáról.</span><span class="sxs-lookup"><span data-stu-id="d3354-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="d3354-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d3354-104">SYNTAX</span></span>

### <span data-ttu-id="d3354-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d3354-105">List (Default)</span></span>
```
Get-AzMySqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d3354-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="d3354-106">Get</span></span>
```
Get-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d3354-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d3354-107">GetViaIdentity</span></span>
```
Get-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d3354-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d3354-108">DESCRIPTION</span></span>
<span data-ttu-id="d3354-109">Információt kap a kiszolgáló konfigurációjáról.</span><span class="sxs-lookup"><span data-stu-id="d3354-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="d3354-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d3354-110">EXAMPLES</span></span>

### <span data-ttu-id="d3354-111">Példa 1: a megadott MySql-kiszolgáló összes konfigurációjának listázása</span><span class="sxs-lookup"><span data-stu-id="d3354-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name                                     Type
----                                     ----
audit_log_enabled                        Microsoft.DBforMySQL/servers/configurations
audit_log_events                         Microsoft.DBforMySQL/servers/configurations
audit_log_exclude_users                  Microsoft.DBforMySQL/servers/configurations
audit_log_include_users                  Microsoft.DBforMySQL/servers/configurations
...
transaction_prealloc_size                Microsoft.DBforMySQL/servers/configurations
tx_isolation                             Microsoft.DBforMySQL/servers/configurations
updatable_views_with_limit               Microsoft.DBforMySQL/servers/configurations
wait_timeout                             Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="d3354-112">Ez a parancsmag a megadott MySql-kiszolgáló összes konfigurációját felsorolja.</span><span class="sxs-lookup"><span data-stu-id="d3354-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="d3354-113">2. példa: a megadott MySql-konfiguráció beolvasása név szerint</span><span class="sxs-lookup"><span data-stu-id="d3354-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -Name time_zone -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name      Type
----      ----
time_zone Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="d3354-114">Ez a parancsmag név szerint adja meg a MySql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="d3354-114">This cmdlet gets specified MySql configuration by name.</span></span>

## <span data-ttu-id="d3354-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d3354-115">PARAMETERS</span></span>

### <span data-ttu-id="d3354-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3354-116">-DefaultProfile</span></span>
<span data-ttu-id="d3354-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3354-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3354-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3354-118">-InputObject</span></span>
<span data-ttu-id="d3354-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d3354-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3354-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d3354-120">-Name</span></span>
<span data-ttu-id="d3354-121">A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="d3354-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="d3354-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3354-122">-ResourceGroupName</span></span>
<span data-ttu-id="d3354-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d3354-123">The name of the resource group.</span></span>
<span data-ttu-id="d3354-124">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="d3354-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d3354-125">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="d3354-125">-ServerName</span></span>
<span data-ttu-id="d3354-126">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="d3354-126">The name of the server.</span></span>

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

### <span data-ttu-id="d3354-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d3354-127">-SubscriptionId</span></span>
<span data-ttu-id="d3354-128">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d3354-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d3354-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3354-129">CommonParameters</span></span>
<span data-ttu-id="d3354-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d3354-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3354-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d3354-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3354-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3354-132">INPUTS</span></span>

### <span data-ttu-id="d3354-133">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d3354-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="d3354-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3354-134">OUTPUTS</span></span>

### <span data-ttu-id="d3354-135">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3354-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="d3354-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d3354-136">NOTES</span></span>

<span data-ttu-id="d3354-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d3354-137">ALIASES</span></span>

<span data-ttu-id="d3354-138">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="d3354-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d3354-139">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d3354-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d3354-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="d3354-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d3354-141">INPUTOBJECT <IMySqlIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="d3354-141">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d3354-142">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="d3354-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d3354-143">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d3354-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d3354-144">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="d3354-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d3354-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d3354-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d3354-146">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="d3354-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d3354-147">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d3354-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d3354-148">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="d3354-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="d3354-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="d3354-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d3354-150">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="d3354-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d3354-151">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d3354-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d3354-152">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="d3354-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d3354-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3354-153">RELATED LINKS</span></span>

