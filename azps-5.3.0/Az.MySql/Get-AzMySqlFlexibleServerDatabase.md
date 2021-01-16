---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 43b5563a9328a5b8f96c1fdb538dc49e721c428c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468270"
---
# <span data-ttu-id="1e12b-101">Get-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="1e12b-101">Get-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="1e12b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e12b-102">SYNOPSIS</span></span>
<span data-ttu-id="1e12b-103">Információkat kap egy adatbázisról.</span><span class="sxs-lookup"><span data-stu-id="1e12b-103">Gets information about a database.</span></span>

## <span data-ttu-id="1e12b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1e12b-104">SYNTAX</span></span>

### <span data-ttu-id="1e12b-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1e12b-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerDatabase -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1e12b-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="1e12b-106">Get</span></span>
```
Get-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1e12b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1e12b-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1e12b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1e12b-108">DESCRIPTION</span></span>
<span data-ttu-id="1e12b-109">Információkat kap egy adatbázisról.</span><span class="sxs-lookup"><span data-stu-id="1e12b-109">Gets information about a database.</span></span>

## <span data-ttu-id="1e12b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1e12b-110">EXAMPLES</span></span>

### <span data-ttu-id="1e12b-111">1. példa: MySql-adatbázis létrehozása erőforrásnév szerint</span><span class="sxs-lookup"><span data-stu-id="1e12b-111">Example 1: Get a MySql database by resource name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Name flexibleserverdb

Name            Charset     Collation              
----            -------- ------------------
flexibleserverdb latin1   latin1_swedish_ci  
```

<span data-ttu-id="1e12b-112">Ez a parancsmag erőforrásnév szerint kapja meg a MySql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="1e12b-112">This cmdlet gets MySql server by resource name.</span></span>

### <span data-ttu-id="1e12b-113">2. példa: MySql-adatbázisok lekért identitás szerint</span><span class="sxs-lookup"><span data-stu-id="1e12b-113">Example 2: Get MySql databases by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServerDatabase -InputObject $ID

Name             Charset     Collation            
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci 
```

<span data-ttu-id="1e12b-114">Ez a parancsmag identitás alapján kap MySql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="1e12b-114">This cmdlet gets a MySql server by identity.</span></span>

### <span data-ttu-id="1e12b-115">3. példa: A megadott kiszolgáló összes MySql-adatbázisának felsorolása</span><span class="sxs-lookup"><span data-stu-id="1e12b-115">Example 3: Lists all the MySql databases in the specified server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name             Charset     Collation        
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci
```

<span data-ttu-id="1e12b-116">Ez a parancsmag felsorolja a megadott kiszolgáló összes MySql-kiszolgálóját.</span><span class="sxs-lookup"><span data-stu-id="1e12b-116">This cmdlet lists all the MySql servers in specified the server.</span></span>

## <span data-ttu-id="1e12b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e12b-117">PARAMETERS</span></span>

### <span data-ttu-id="1e12b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e12b-118">-DefaultProfile</span></span>
<span data-ttu-id="1e12b-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e12b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e12b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e12b-120">-InputObject</span></span>
<span data-ttu-id="1e12b-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="1e12b-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1e12b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1e12b-122">-Name</span></span>
<span data-ttu-id="1e12b-123">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="1e12b-123">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e12b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e12b-124">-ResourceGroupName</span></span>
<span data-ttu-id="1e12b-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1e12b-125">The name of the resource group.</span></span>
<span data-ttu-id="1e12b-126">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="1e12b-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1e12b-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1e12b-127">-ServerName</span></span>
<span data-ttu-id="1e12b-128">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="1e12b-128">The name of the server.</span></span>

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

### <span data-ttu-id="1e12b-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e12b-129">-SubscriptionId</span></span>
<span data-ttu-id="1e12b-130">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1e12b-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1e12b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e12b-131">CommonParameters</span></span>
<span data-ttu-id="1e12b-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e12b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e12b-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e12b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e12b-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e12b-134">INPUTS</span></span>

### <span data-ttu-id="1e12b-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="1e12b-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="1e12b-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e12b-136">OUTPUTS</span></span>

### <span data-ttu-id="1e12b-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="1e12b-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="1e12b-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1e12b-138">NOTES</span></span>

<span data-ttu-id="1e12b-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="1e12b-139">ALIASES</span></span>

<span data-ttu-id="1e12b-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="1e12b-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1e12b-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="1e12b-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1e12b-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1e12b-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1e12b-143">INPUTOBJECT: <IMySqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="1e12b-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1e12b-144">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="1e12b-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="1e12b-145">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="1e12b-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="1e12b-146">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="1e12b-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="1e12b-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="1e12b-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1e12b-148">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="1e12b-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="1e12b-149">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="1e12b-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="1e12b-150">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1e12b-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1e12b-151">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="1e12b-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="1e12b-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="1e12b-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="1e12b-153">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="1e12b-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="1e12b-154">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1e12b-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1e12b-155">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="1e12b-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="1e12b-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e12b-156">RELATED LINKS</span></span>

