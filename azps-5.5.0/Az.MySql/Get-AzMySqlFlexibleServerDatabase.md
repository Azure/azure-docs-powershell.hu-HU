---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 43b5563a9328a5b8f96c1fdb538dc49e721c428c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203363"
---
# <span data-ttu-id="fb1da-101">Get-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="fb1da-101">Get-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="fb1da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb1da-102">SYNOPSIS</span></span>
<span data-ttu-id="fb1da-103">Információkat kap egy adatbázisról.</span><span class="sxs-lookup"><span data-stu-id="fb1da-103">Gets information about a database.</span></span>

## <span data-ttu-id="fb1da-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fb1da-104">SYNTAX</span></span>

### <span data-ttu-id="fb1da-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fb1da-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerDatabase -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fb1da-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="fb1da-106">Get</span></span>
```
Get-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fb1da-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fb1da-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb1da-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fb1da-108">DESCRIPTION</span></span>
<span data-ttu-id="fb1da-109">Információkat kap egy adatbázisról.</span><span class="sxs-lookup"><span data-stu-id="fb1da-109">Gets information about a database.</span></span>

## <span data-ttu-id="fb1da-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fb1da-110">EXAMPLES</span></span>

### <span data-ttu-id="fb1da-111">1. példa: MySql-adatbázis lehozása erőforrásnév alapján</span><span class="sxs-lookup"><span data-stu-id="fb1da-111">Example 1: Get a MySql database by resource name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Name flexibleserverdb

Name            Charset     Collation              
----            -------- ------------------
flexibleserverdb latin1   latin1_swedish_ci  
```

<span data-ttu-id="fb1da-112">Ez a parancsmag erőforrásnév szerint kapja meg a MySql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="fb1da-112">This cmdlet gets MySql server by resource name.</span></span>

### <span data-ttu-id="fb1da-113">2. példa: MySql-adatbázisok lehozása identitás alapján</span><span class="sxs-lookup"><span data-stu-id="fb1da-113">Example 2: Get MySql databases by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServerDatabase -InputObject $ID

Name             Charset     Collation            
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci 
```

<span data-ttu-id="fb1da-114">Ez a parancsmag identitás alapján kap MySql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="fb1da-114">This cmdlet gets a MySql server by identity.</span></span>

### <span data-ttu-id="fb1da-115">3. példa: A megadott kiszolgáló összes MySql-adatbázisának felsorolása</span><span class="sxs-lookup"><span data-stu-id="fb1da-115">Example 3: Lists all the MySql databases in the specified server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name             Charset     Collation        
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci
```

<span data-ttu-id="fb1da-116">Ez a parancsmag felsorolja a megadott kiszolgáló összes MySql-kiszolgálóját.</span><span class="sxs-lookup"><span data-stu-id="fb1da-116">This cmdlet lists all the MySql servers in specified the server.</span></span>

## <span data-ttu-id="fb1da-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb1da-117">PARAMETERS</span></span>

### <span data-ttu-id="fb1da-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb1da-118">-DefaultProfile</span></span>
<span data-ttu-id="fb1da-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb1da-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb1da-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb1da-120">-InputObject</span></span>
<span data-ttu-id="fb1da-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="fb1da-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fb1da-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fb1da-122">-Name</span></span>
<span data-ttu-id="fb1da-123">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="fb1da-123">The name of the database.</span></span>

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

### <span data-ttu-id="fb1da-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb1da-124">-ResourceGroupName</span></span>
<span data-ttu-id="fb1da-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fb1da-125">The name of the resource group.</span></span>
<span data-ttu-id="fb1da-126">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="fb1da-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fb1da-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fb1da-127">-ServerName</span></span>
<span data-ttu-id="fb1da-128">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="fb1da-128">The name of the server.</span></span>

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

### <span data-ttu-id="fb1da-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fb1da-129">-SubscriptionId</span></span>
<span data-ttu-id="fb1da-130">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fb1da-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fb1da-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb1da-131">CommonParameters</span></span>
<span data-ttu-id="fb1da-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb1da-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb1da-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb1da-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb1da-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb1da-134">INPUTS</span></span>

### <span data-ttu-id="fb1da-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="fb1da-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="fb1da-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb1da-136">OUTPUTS</span></span>

### <span data-ttu-id="fb1da-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="fb1da-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="fb1da-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fb1da-138">NOTES</span></span>

<span data-ttu-id="fb1da-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="fb1da-139">ALIASES</span></span>

<span data-ttu-id="fb1da-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="fb1da-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fb1da-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="fb1da-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fb1da-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fb1da-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fb1da-143">INPUTOBJECT: <IMySqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="fb1da-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fb1da-144">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="fb1da-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="fb1da-145">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="fb1da-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="fb1da-146">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="fb1da-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="fb1da-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="fb1da-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fb1da-148">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="fb1da-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="fb1da-149">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="fb1da-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="fb1da-150">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fb1da-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fb1da-151">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="fb1da-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="fb1da-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="fb1da-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="fb1da-153">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="fb1da-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="fb1da-154">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fb1da-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fb1da-155">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="fb1da-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="fb1da-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb1da-156">RELATED LINKS</span></span>

