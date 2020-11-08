---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
ms.openlocfilehash: 71fb10b0aeed85a716a834b42b1bdae3e5f7b270
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024490"
---
# <span data-ttu-id="41999-101">Get-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="41999-101">Get-AzPostgreSqlServer</span></span>

## <span data-ttu-id="41999-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41999-102">SYNOPSIS</span></span>
<span data-ttu-id="41999-103">Információt kap a kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="41999-103">Gets information about a server.</span></span>

## <span data-ttu-id="41999-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41999-104">SYNTAX</span></span>

### <span data-ttu-id="41999-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="41999-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="41999-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="41999-106">Get</span></span>
```
Get-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="41999-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="41999-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="41999-108">Lista</span><span class="sxs-lookup"><span data-stu-id="41999-108">List</span></span>
```
Get-AzPostgreSqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="41999-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="41999-109">DESCRIPTION</span></span>
<span data-ttu-id="41999-110">Információt kap a kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="41999-110">Gets information about a server.</span></span>

## <span data-ttu-id="41999-111">Példák</span><span class="sxs-lookup"><span data-stu-id="41999-111">EXAMPLES</span></span>

### <span data-ttu-id="41999-112">1. példa: a PostgreSql-kiszolgáló beolvasása alapértelmezett környezettel</span><span class="sxs-lookup"><span data-stu-id="41999-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="41999-113">Ez a parancsmag a PostgreSql Server alapértelmezett környezetét kapja.</span><span class="sxs-lookup"><span data-stu-id="41999-113">This cmdlet gets PostgreSql server with default context.</span></span>

### <span data-ttu-id="41999-114">2. példa: a PostgreSql-kiszolgáló beolvasása erőforráscsoport szerint és kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="41999-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="41999-115">Ez a parancsmag az erőforráscsoport és a kiszolgáló neve alapján kapja meg a PostgreSql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="41999-115">This cmdlet gets PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="41999-116">3. példa: a megadott erőforráscsoport összes PostgreSql-kiszolgálójának felsorolása</span><span class="sxs-lookup"><span data-stu-id="41999-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="41999-117">Ez a parancsmag felsorolja a megadott erőforráscsoport összes PostgreSql-kiszolgálóját.</span><span class="sxs-lookup"><span data-stu-id="41999-117">This cmdlet lists all the PostgreSql servers in specified resource group.</span></span>

### <span data-ttu-id="41999-118">4. példa: a PostgreSql-kiszolgáló beolvasása identitással</span><span class="sxs-lookup"><span data-stu-id="41999-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/postgresqltestserver"
PS C:\> Get-AzPostgreSqlServer -InputObject $ID

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="41999-119">Ez a parancsmag a PostgreSql-kiszolgálót identitás szerint jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="41999-119">This cmdlet lists gets PostgreSql server by identity.</span></span>

## <span data-ttu-id="41999-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41999-120">PARAMETERS</span></span>

### <span data-ttu-id="41999-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41999-121">-DefaultProfile</span></span>
<span data-ttu-id="41999-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41999-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41999-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41999-123">-InputObject</span></span>
<span data-ttu-id="41999-124">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="41999-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="41999-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="41999-125">-Name</span></span>
<span data-ttu-id="41999-126">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="41999-126">The name of the server.</span></span>

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

### <span data-ttu-id="41999-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41999-127">-ResourceGroupName</span></span>
<span data-ttu-id="41999-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="41999-128">The name of the resource group.</span></span>
<span data-ttu-id="41999-129">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="41999-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="41999-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41999-130">-SubscriptionId</span></span>
<span data-ttu-id="41999-131">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="41999-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="41999-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41999-132">CommonParameters</span></span>
<span data-ttu-id="41999-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41999-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41999-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="41999-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41999-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41999-135">INPUTS</span></span>

### <span data-ttu-id="41999-136">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="41999-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="41999-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41999-137">OUTPUTS</span></span>

### <span data-ttu-id="41999-138">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="41999-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="41999-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41999-139">NOTES</span></span>

<span data-ttu-id="41999-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="41999-140">ALIASES</span></span>

<span data-ttu-id="41999-141">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="41999-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="41999-142">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="41999-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="41999-143">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="41999-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="41999-144">INPUTOBJECT <IPostgreSqlIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="41999-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="41999-145">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="41999-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="41999-146">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="41999-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="41999-147">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="41999-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="41999-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="41999-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="41999-149">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="41999-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="41999-150">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="41999-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="41999-151">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="41999-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="41999-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="41999-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="41999-153">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="41999-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="41999-154">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="41999-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="41999-155">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="41999-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="41999-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41999-156">RELATED LINKS</span></span>

