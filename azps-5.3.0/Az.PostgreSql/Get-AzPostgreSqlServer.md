---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
ms.openlocfilehash: 71fb10b0aeed85a716a834b42b1bdae3e5f7b270
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378460"
---
# <span data-ttu-id="e8684-101">Get-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="e8684-101">Get-AzPostgreSqlServer</span></span>

## <span data-ttu-id="e8684-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8684-102">SYNOPSIS</span></span>
<span data-ttu-id="e8684-103">Információkat kap a kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="e8684-103">Gets information about a server.</span></span>

## <span data-ttu-id="e8684-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e8684-104">SYNTAX</span></span>

### <span data-ttu-id="e8684-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e8684-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e8684-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="e8684-106">Get</span></span>
```
Get-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e8684-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e8684-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e8684-108">Lista</span><span class="sxs-lookup"><span data-stu-id="e8684-108">List</span></span>
```
Get-AzPostgreSqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8684-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e8684-109">DESCRIPTION</span></span>
<span data-ttu-id="e8684-110">Információkat kap a kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="e8684-110">Gets information about a server.</span></span>

## <span data-ttu-id="e8684-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e8684-111">EXAMPLES</span></span>

### <span data-ttu-id="e8684-112">1. példa: A PostgreSql-kiszolgáló lekérte az alapértelmezett környezetben</span><span class="sxs-lookup"><span data-stu-id="e8684-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="e8684-113">Ez a parancsmag alapértelmezett környezetben kapja meg a PostgreSql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="e8684-113">This cmdlet gets PostgreSql server with default context.</span></span>

### <span data-ttu-id="e8684-114">2. példa: A PostgreSql-kiszolgáló lekérte erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="e8684-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="e8684-115">Ez a parancsmag a PostgreSql-kiszolgálót erőforráscsoport és kiszolgálónév szerint kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e8684-115">This cmdlet gets PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="e8684-116">3. példa: A megadott erőforráscsoport összes PostgreSql-kiszolgálója</span><span class="sxs-lookup"><span data-stu-id="e8684-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="e8684-117">Ez a parancsmag felsorolja a megadott erőforráscsoport összes PostgreSql-kiszolgálóját.</span><span class="sxs-lookup"><span data-stu-id="e8684-117">This cmdlet lists all the PostgreSql servers in specified resource group.</span></span>

### <span data-ttu-id="e8684-118">4. példa: A PostgreSql-kiszolgáló identitás alapján való lekérte</span><span class="sxs-lookup"><span data-stu-id="e8684-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/postgresqltestserver"
PS C:\> Get-AzPostgreSqlServer -InputObject $ID

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="e8684-119">Ez a parancsmaglista identitás alapján kapja meg a PostgreSql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="e8684-119">This cmdlet lists gets PostgreSql server by identity.</span></span>

## <span data-ttu-id="e8684-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8684-120">PARAMETERS</span></span>

### <span data-ttu-id="e8684-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8684-121">-DefaultProfile</span></span>
<span data-ttu-id="e8684-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8684-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8684-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8684-123">-InputObject</span></span>
<span data-ttu-id="e8684-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e8684-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e8684-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e8684-125">-Name</span></span>
<span data-ttu-id="e8684-126">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="e8684-126">The name of the server.</span></span>

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

### <span data-ttu-id="e8684-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8684-127">-ResourceGroupName</span></span>
<span data-ttu-id="e8684-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e8684-128">The name of the resource group.</span></span>
<span data-ttu-id="e8684-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="e8684-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e8684-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e8684-130">-SubscriptionId</span></span>
<span data-ttu-id="e8684-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e8684-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e8684-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8684-132">CommonParameters</span></span>
<span data-ttu-id="e8684-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8684-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8684-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8684-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8684-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8684-135">INPUTS</span></span>

### <span data-ttu-id="e8684-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="e8684-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="e8684-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8684-137">OUTPUTS</span></span>

### <span data-ttu-id="e8684-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="e8684-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="e8684-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e8684-139">NOTES</span></span>

<span data-ttu-id="e8684-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e8684-140">ALIASES</span></span>

<span data-ttu-id="e8684-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="e8684-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e8684-142">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="e8684-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e8684-143">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e8684-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e8684-144">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e8684-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e8684-145">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="e8684-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e8684-146">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="e8684-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e8684-147">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="e8684-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e8684-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e8684-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e8684-149">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="e8684-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e8684-150">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e8684-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e8684-151">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="e8684-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="e8684-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="e8684-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e8684-153">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="e8684-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e8684-154">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e8684-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e8684-155">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="e8684-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e8684-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8684-156">RELATED LINKS</span></span>

