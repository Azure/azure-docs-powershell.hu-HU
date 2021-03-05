---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
ms.openlocfilehash: cbbe321f23fb95bca8a4a70dd59f30ec098cf2d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012006"
---
# <span data-ttu-id="bd714-101">Get-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="bd714-101">Get-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="bd714-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd714-102">SYNOPSIS</span></span>
<span data-ttu-id="bd714-103">Információkat kap a kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="bd714-103">Gets information about a server.</span></span>

## <span data-ttu-id="bd714-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bd714-104">SYNTAX</span></span>

### <span data-ttu-id="bd714-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bd714-105">List1 (Default)</span></span>
```
Get-AzMySqlFlexibleServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bd714-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="bd714-106">Get</span></span>
```
Get-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bd714-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bd714-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bd714-108">Lista</span><span class="sxs-lookup"><span data-stu-id="bd714-108">List</span></span>
```
Get-AzMySqlFlexibleServer -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="bd714-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bd714-109">DESCRIPTION</span></span>
<span data-ttu-id="bd714-110">Információkat kap a kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="bd714-110">Gets information about a server.</span></span>

## <span data-ttu-id="bd714-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bd714-111">EXAMPLES</span></span>

### <span data-ttu-id="bd714-112">1. példa: A MySql-kiszolgáló lekért beállítása alapértelmezett környezetben</span><span class="sxs-lookup"><span data-stu-id="bd714-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11  westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="bd714-113">Ez a parancsmag az alapértelmezett környezetben kapja meg a MySql-kiszolgálókat.</span><span class="sxs-lookup"><span data-stu-id="bd714-113">This cmdlet gets MySql servers with default context.</span></span>

### <span data-ttu-id="bd714-114">2. példa: A MySql-kiszolgáló lekérte erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="bd714-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test     westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="bd714-115">Ez a parancsmag a MySql-kiszolgálókat erőforráscsoport és kiszolgálónév szerint kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bd714-115">This cmdlet gets MySql servers by resource group and server name.</span></span>

### <span data-ttu-id="bd714-116">3. példa: A mySql-kiszolgálók listája a megadott erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="bd714-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11 westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
mysql-test-12 westus2   mysql_test2        5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="bd714-117">Ez a parancsmag felsorolja a megadott erőforráscsoport összes MySql-kiszolgálóját.</span><span class="sxs-lookup"><span data-stu-id="bd714-117">This cmdlet lists all the MySql servers in the specified resource group.</span></span>

### <span data-ttu-id="bd714-118">4. példa: A MySql-kiszolgáló lekért identitás szerint</span><span class="sxs-lookup"><span data-stu-id="bd714-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="bd714-119">Ez a parancsmaglista identitás alapján kapja meg a MySql-kiszolgálókat.</span><span class="sxs-lookup"><span data-stu-id="bd714-119">This cmdlet lists gets MySql servers by identity.</span></span>

## <span data-ttu-id="bd714-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd714-120">PARAMETERS</span></span>

### <span data-ttu-id="bd714-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd714-121">-DefaultProfile</span></span>
<span data-ttu-id="bd714-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd714-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd714-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd714-123">-InputObject</span></span>
<span data-ttu-id="bd714-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="bd714-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bd714-125">-Name</span><span class="sxs-lookup"><span data-stu-id="bd714-125">-Name</span></span>
<span data-ttu-id="bd714-126">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="bd714-126">The name of the server.</span></span>

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

### <span data-ttu-id="bd714-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd714-127">-ResourceGroupName</span></span>
<span data-ttu-id="bd714-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bd714-128">The name of the resource group.</span></span>
<span data-ttu-id="bd714-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="bd714-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bd714-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bd714-130">-SubscriptionId</span></span>
<span data-ttu-id="bd714-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bd714-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bd714-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd714-132">CommonParameters</span></span>
<span data-ttu-id="bd714-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd714-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd714-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd714-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd714-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd714-135">INPUTS</span></span>

### <span data-ttu-id="bd714-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="bd714-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="bd714-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd714-137">OUTPUTS</span></span>

### <span data-ttu-id="bd714-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="bd714-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="bd714-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bd714-139">NOTES</span></span>

<span data-ttu-id="bd714-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="bd714-140">ALIASES</span></span>

<span data-ttu-id="bd714-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="bd714-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bd714-142">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="bd714-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bd714-143">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bd714-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bd714-144">INPUTOBJECT: <IMySqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="bd714-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bd714-145">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="bd714-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="bd714-146">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="bd714-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="bd714-147">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="bd714-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="bd714-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="bd714-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bd714-149">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="bd714-149">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="bd714-150">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="bd714-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="bd714-151">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bd714-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bd714-152">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="bd714-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="bd714-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="bd714-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="bd714-154">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="bd714-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="bd714-155">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bd714-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bd714-156">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="bd714-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="bd714-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd714-157">RELATED LINKS</span></span>

