---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
ms.openlocfilehash: 10a3ca97d5f4bba9bf47eff5b2e4bdbb29b8ff24
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157290"
---
# <span data-ttu-id="9d6ba-101">Get-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="9d6ba-101">Get-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="9d6ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d6ba-102">SYNOPSIS</span></span>
<span data-ttu-id="9d6ba-103">Információkat kap egy kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-103">Gets information about a server.</span></span>

## <span data-ttu-id="9d6ba-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9d6ba-104">SYNTAX</span></span>

### <span data-ttu-id="9d6ba-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9d6ba-105">List1 (Default)</span></span>
```
Get-AzMySqlFlexibleServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9d6ba-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="9d6ba-106">Get</span></span>
```
Get-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9d6ba-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9d6ba-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9d6ba-108">Lista</span><span class="sxs-lookup"><span data-stu-id="9d6ba-108">List</span></span>
```
Get-AzMySqlFlexibleServer -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9d6ba-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9d6ba-109">DESCRIPTION</span></span>
<span data-ttu-id="9d6ba-110">Információkat kap egy kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-110">Gets information about a server.</span></span>

## <span data-ttu-id="9d6ba-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9d6ba-111">EXAMPLES</span></span>

### <span data-ttu-id="9d6ba-112">1. példa: A MySql-kiszolgáló lekért beállítása alapértelmezett környezetben</span><span class="sxs-lookup"><span data-stu-id="9d6ba-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11  westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="9d6ba-113">Ez a parancsmag az alapértelmezett környezetben kapja meg a MySql-kiszolgálókat.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-113">This cmdlet gets MySql servers with default context.</span></span>

### <span data-ttu-id="9d6ba-114">2. példa: A MySql-kiszolgáló lekérte erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="9d6ba-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test     westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="9d6ba-115">Ez a parancsmag a MySql-kiszolgálókat erőforráscsoport és kiszolgálónév szerint kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-115">This cmdlet gets MySql servers by resource group and server name.</span></span>

### <span data-ttu-id="9d6ba-116">3. példa: A mySql-kiszolgálók listája a megadott erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="9d6ba-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11 westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
mysql-test-12 westus2   mysql_test2        5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="9d6ba-117">Ez a parancsmag felsorolja a megadott erőforráscsoport összes MySql-kiszolgálóját.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-117">This cmdlet lists all the MySql servers in the specified resource group.</span></span>

### <span data-ttu-id="9d6ba-118">4. példa: A MySql-kiszolgáló lekért identitás szerint</span><span class="sxs-lookup"><span data-stu-id="9d6ba-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="9d6ba-119">Ez a parancsmaglista identitás alapján kapja meg a MySql-kiszolgálókat.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-119">This cmdlet lists gets MySql servers by identity.</span></span>

## <span data-ttu-id="9d6ba-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d6ba-120">PARAMETERS</span></span>

### <span data-ttu-id="9d6ba-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d6ba-121">-DefaultProfile</span></span>
<span data-ttu-id="9d6ba-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d6ba-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d6ba-123">-InputObject</span></span>
<span data-ttu-id="9d6ba-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9d6ba-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9d6ba-125">-Name</span></span>
<span data-ttu-id="9d6ba-126">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-126">The name of the server.</span></span>

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

### <span data-ttu-id="9d6ba-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d6ba-127">-ResourceGroupName</span></span>
<span data-ttu-id="9d6ba-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-128">The name of the resource group.</span></span>
<span data-ttu-id="9d6ba-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="9d6ba-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9d6ba-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9d6ba-130">-SubscriptionId</span></span>
<span data-ttu-id="9d6ba-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9d6ba-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d6ba-132">CommonParameters</span></span>
<span data-ttu-id="9d6ba-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d6ba-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d6ba-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d6ba-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d6ba-135">INPUTS</span></span>

### <span data-ttu-id="9d6ba-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="9d6ba-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="9d6ba-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d6ba-137">OUTPUTS</span></span>

### <span data-ttu-id="9d6ba-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="9d6ba-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="9d6ba-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9d6ba-139">NOTES</span></span>

<span data-ttu-id="9d6ba-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9d6ba-140">ALIASES</span></span>

<span data-ttu-id="9d6ba-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="9d6ba-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9d6ba-142">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9d6ba-143">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9d6ba-144">INPUTOBJECT: <IMySqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="9d6ba-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9d6ba-145">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9d6ba-146">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9d6ba-147">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9d6ba-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="9d6ba-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9d6ba-149">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-149">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="9d6ba-150">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9d6ba-151">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9d6ba-152">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="9d6ba-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="9d6ba-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9d6ba-154">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9d6ba-155">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9d6ba-156">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="9d6ba-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9d6ba-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d6ba-157">RELATED LINKS</span></span>

