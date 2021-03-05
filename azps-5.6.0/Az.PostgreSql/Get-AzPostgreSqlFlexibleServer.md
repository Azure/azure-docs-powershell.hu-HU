---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 3354014ed0e6e81b1460da061e75e614bbd5f95c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011782"
---
# <span data-ttu-id="7ce86-101">Get-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="7ce86-101">Get-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="7ce86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ce86-102">SYNOPSIS</span></span>
<span data-ttu-id="7ce86-103">Információkat kap a kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="7ce86-103">Gets information about a server.</span></span>

## <span data-ttu-id="7ce86-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7ce86-104">SYNTAX</span></span>

### <span data-ttu-id="7ce86-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7ce86-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlFlexibleServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7ce86-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="7ce86-106">Get</span></span>
```
Get-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7ce86-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7ce86-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ce86-108">Lista</span><span class="sxs-lookup"><span data-stu-id="7ce86-108">List</span></span>
```
Get-AzPostgreSqlFlexibleServer -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7ce86-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7ce86-109">DESCRIPTION</span></span>
<span data-ttu-id="7ce86-110">Információkat kap a kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="7ce86-110">Gets information about a server.</span></span>

## <span data-ttu-id="7ce86-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7ce86-111">EXAMPLES</span></span>

### <span data-ttu-id="7ce86-112">1. példa: A PostgreSql-kiszolgáló lekért beállítása alapértelmezett környezetben</span><span class="sxs-lookup"><span data-stu-id="7ce86-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql-test     12     32768                   Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="7ce86-113">Ez a parancsmag alapértelmezett környezetben kapja meg a PostgreSql-kiszolgálókat.</span><span class="sxs-lookup"><span data-stu-id="7ce86-113">This cmdlet gets PostgreSql servers with default context.</span></span>

### <span data-ttu-id="7ce86-114">2. példa: A PostgreSql-kiszolgáló lekérte erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="7ce86-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql-test     12     32768                   Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="7ce86-115">Ez a parancsmag a PostgreSql-kiszolgálókat erőforráscsoport és kiszolgálónév szerint kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7ce86-115">This cmdlet gets PostgreSql servers by resource group and server name.</span></span>

### <span data-ttu-id="7ce86-116">3. példa: A megadott erőforráscsoport összes PostgreSql-kiszolgálója</span><span class="sxs-lookup"><span data-stu-id="7ce86-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest

Name             Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----             -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test  eastus   postgresql-test     12     32768                   Standard_D2s_v3 GeneralPurpose
postgresql-test2 eastus   postgresql-test     12     32768                   Standard_42s_v3 GeneralPurpose
```

<span data-ttu-id="7ce86-117">Ez a parancsmag felsorolja a megadott erőforráscsoport összes PostgreSql-kiszolgálóját.</span><span class="sxs-lookup"><span data-stu-id="7ce86-117">This cmdlet lists all the PostgreSql servers in the specified resource group.</span></span>

### <span data-ttu-id="7ce86-118">4. példa: A PostgreSql-kiszolgáló identitás alapján való lekérte</span><span class="sxs-lookup"><span data-stu-id="7ce86-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test"
PS C:\> Get-AzPostgreSqlFlexibleServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql-test         12     32768                    Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="7ce86-119">Ez a parancsmaglista identitás alapján kapja meg a PostgreSql-kiszolgálókat.</span><span class="sxs-lookup"><span data-stu-id="7ce86-119">This cmdlet lists gets PostgreSql servers by identity.</span></span>

## <span data-ttu-id="7ce86-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ce86-120">PARAMETERS</span></span>

### <span data-ttu-id="7ce86-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ce86-121">-DefaultProfile</span></span>
<span data-ttu-id="7ce86-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ce86-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ce86-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ce86-123">-InputObject</span></span>
<span data-ttu-id="7ce86-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7ce86-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7ce86-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7ce86-125">-Name</span></span>
<span data-ttu-id="7ce86-126">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="7ce86-126">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce86-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ce86-127">-ResourceGroupName</span></span>
<span data-ttu-id="7ce86-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7ce86-128">The name of the resource group.</span></span>
<span data-ttu-id="7ce86-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="7ce86-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7ce86-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7ce86-130">-SubscriptionId</span></span>
<span data-ttu-id="7ce86-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7ce86-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce86-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ce86-132">CommonParameters</span></span>
<span data-ttu-id="7ce86-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ce86-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ce86-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ce86-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ce86-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ce86-135">INPUTS</span></span>

### <span data-ttu-id="7ce86-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="7ce86-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="7ce86-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ce86-137">OUTPUTS</span></span>

### <span data-ttu-id="7ce86-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="7ce86-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="7ce86-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7ce86-139">NOTES</span></span>

<span data-ttu-id="7ce86-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7ce86-140">ALIASES</span></span>

<span data-ttu-id="7ce86-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="7ce86-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7ce86-142">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="7ce86-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7ce86-143">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7ce86-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7ce86-144">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="7ce86-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7ce86-145">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="7ce86-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="7ce86-146">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="7ce86-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="7ce86-147">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="7ce86-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="7ce86-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="7ce86-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7ce86-149">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="7ce86-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="7ce86-150">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7ce86-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7ce86-151">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="7ce86-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="7ce86-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="7ce86-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="7ce86-153">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="7ce86-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="7ce86-154">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7ce86-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7ce86-155">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="7ce86-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="7ce86-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ce86-156">RELATED LINKS</span></span>

