---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 0579220e372a937dd25d5956735a321e84523f69
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203374"
---
# <span data-ttu-id="55097-101">Get-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="55097-101">Get-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="55097-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55097-102">SYNOPSIS</span></span>
<span data-ttu-id="55097-103">Információkat kap a kiszolgáló konfigurációról.</span><span class="sxs-lookup"><span data-stu-id="55097-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="55097-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="55097-104">SYNTAX</span></span>

### <span data-ttu-id="55097-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="55097-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="55097-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="55097-106">Get</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="55097-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="55097-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="55097-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="55097-108">DESCRIPTION</span></span>
<span data-ttu-id="55097-109">Információkat kap a kiszolgáló konfigurációról.</span><span class="sxs-lookup"><span data-stu-id="55097-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="55097-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="55097-110">EXAMPLES</span></span>

### <span data-ttu-id="55097-111">1. példa: A megadott MySql-kiszolgáló összes konfigurációjának felsorolása</span><span class="sxs-lookup"><span data-stu-id="55097-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
archive        OFF    OFF           system-default ON, OFF      Enumeration
...
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="55097-112">Ez a parancsmag felsorolja a megadott MySql-kiszolgáló összes konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="55097-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="55097-113">2. példa: A MySql-konfiguráció név szerint való beállítása</span><span class="sxs-lookup"><span data-stu-id="55097-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="55097-114">Ez a parancsmag név szerint kapja meg a MySql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="55097-114">This cmdlet gets specified MySql configuration by name.</span></span>

### <span data-ttu-id="55097-115">3. példa: Konfiguráció listába sorolás identitás szerint</span><span class="sxs-lookup"><span data-stu-id="55097-115">Example 3: List configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="55097-116">Ez a parancsmag identitás szerint kapja meg a MySql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="55097-116">This cmdlet gets specified MySql configuration by identity.</span></span>

## <span data-ttu-id="55097-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55097-117">PARAMETERS</span></span>

### <span data-ttu-id="55097-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55097-118">-DefaultProfile</span></span>
<span data-ttu-id="55097-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="55097-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55097-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55097-120">-InputObject</span></span>
<span data-ttu-id="55097-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="55097-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="55097-122">-Name</span><span class="sxs-lookup"><span data-stu-id="55097-122">-Name</span></span>
<span data-ttu-id="55097-123">A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="55097-123">The name of the server configuration.</span></span>

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

### <span data-ttu-id="55097-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55097-124">-ResourceGroupName</span></span>
<span data-ttu-id="55097-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="55097-125">The name of the resource group.</span></span>
<span data-ttu-id="55097-126">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="55097-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="55097-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="55097-127">-ServerName</span></span>
<span data-ttu-id="55097-128">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="55097-128">The name of the server.</span></span>

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

### <span data-ttu-id="55097-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55097-129">-SubscriptionId</span></span>
<span data-ttu-id="55097-130">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="55097-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="55097-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55097-131">CommonParameters</span></span>
<span data-ttu-id="55097-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55097-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55097-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55097-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55097-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55097-134">INPUTS</span></span>

### <span data-ttu-id="55097-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="55097-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="55097-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55097-136">OUTPUTS</span></span>

### <span data-ttu-id="55097-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="55097-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="55097-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="55097-138">NOTES</span></span>

<span data-ttu-id="55097-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="55097-139">ALIASES</span></span>

<span data-ttu-id="55097-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="55097-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="55097-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="55097-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="55097-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="55097-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="55097-143">INPUTOBJECT: <IMySqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="55097-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="55097-144">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="55097-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="55097-145">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="55097-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="55097-146">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="55097-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="55097-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="55097-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="55097-148">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="55097-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="55097-149">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="55097-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="55097-150">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="55097-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="55097-151">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="55097-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="55097-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="55097-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="55097-153">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="55097-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="55097-154">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="55097-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="55097-155">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="55097-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="55097-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55097-156">RELATED LINKS</span></span>

