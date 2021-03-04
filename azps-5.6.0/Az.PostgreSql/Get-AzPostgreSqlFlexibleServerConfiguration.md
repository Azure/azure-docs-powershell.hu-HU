---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConfiguration.md
ms.openlocfilehash: 31f99de8a0afaf77345fbdc20782bdd725cb660b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927849"
---
# <span data-ttu-id="44b89-101">Get-AzPostgreSqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="44b89-101">Get-AzPostgreSqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="44b89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44b89-102">SYNOPSIS</span></span>
<span data-ttu-id="44b89-103">Információkat kap a kiszolgáló konfigurációról.</span><span class="sxs-lookup"><span data-stu-id="44b89-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="44b89-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="44b89-104">SYNTAX</span></span>

### <span data-ttu-id="44b89-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="44b89-105">List (Default)</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="44b89-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="44b89-106">Get</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="44b89-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="44b89-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="44b89-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="44b89-108">DESCRIPTION</span></span>
<span data-ttu-id="44b89-109">Információkat kap a kiszolgáló konfigurációról.</span><span class="sxs-lookup"><span data-stu-id="44b89-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="44b89-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="44b89-110">EXAMPLES</span></span>

### <span data-ttu-id="44b89-111">1. példa: A PostgreSql-konfiguráció név szerint való beállítása</span><span class="sxs-lookup"><span data-stu-id="44b89-111">Example 1: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem        4096  4096         system-default 4096-2097151   Integer
```

<span data-ttu-id="44b89-112">Ez a parancsmag név szerint kapja meg a PostgreSql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="44b89-112">This cmdlet gets specified PostgreSql configuration by name.</span></span>

### <span data-ttu-id="44b89-113">2. példa: A megadott PostgreSql-kiszolgáló összes konfigurációjának felsorolása</span><span class="sxs-lookup"><span data-stu-id="44b89-113">Example 2: List all configurations in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
application_name  ""    ""           system-default [A-Za-z0-9._-]*      String
...
pgbouncer.enabled   false  false         system-default true, false   Boolean
```

<span data-ttu-id="44b89-114">Ez a parancsmag felsorolja a megadott PostgreSql-kiszolgáló összes konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="44b89-114">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

## <span data-ttu-id="44b89-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44b89-115">PARAMETERS</span></span>

### <span data-ttu-id="44b89-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44b89-116">-DefaultProfile</span></span>
<span data-ttu-id="44b89-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44b89-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44b89-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44b89-118">-InputObject</span></span>
<span data-ttu-id="44b89-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="44b89-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="44b89-120">-Name</span><span class="sxs-lookup"><span data-stu-id="44b89-120">-Name</span></span>
<span data-ttu-id="44b89-121">A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="44b89-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="44b89-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44b89-122">-ResourceGroupName</span></span>
<span data-ttu-id="44b89-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="44b89-123">The name of the resource group.</span></span>
<span data-ttu-id="44b89-124">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="44b89-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="44b89-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="44b89-125">-ServerName</span></span>
<span data-ttu-id="44b89-126">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="44b89-126">The name of the server.</span></span>

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

### <span data-ttu-id="44b89-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44b89-127">-SubscriptionId</span></span>
<span data-ttu-id="44b89-128">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="44b89-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="44b89-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44b89-129">CommonParameters</span></span>
<span data-ttu-id="44b89-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44b89-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44b89-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44b89-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44b89-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44b89-132">INPUTS</span></span>

### <span data-ttu-id="44b89-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="44b89-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="44b89-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44b89-134">OUTPUTS</span></span>

### <span data-ttu-id="44b89-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="44b89-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="44b89-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="44b89-136">NOTES</span></span>

<span data-ttu-id="44b89-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="44b89-137">ALIASES</span></span>

<span data-ttu-id="44b89-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="44b89-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="44b89-139">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="44b89-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="44b89-140">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="44b89-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="44b89-141">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="44b89-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="44b89-142">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="44b89-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="44b89-143">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="44b89-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="44b89-144">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="44b89-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="44b89-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="44b89-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="44b89-146">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="44b89-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="44b89-147">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="44b89-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="44b89-148">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="44b89-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="44b89-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="44b89-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="44b89-150">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="44b89-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="44b89-151">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="44b89-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="44b89-152">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="44b89-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="44b89-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44b89-153">RELATED LINKS</span></span>

