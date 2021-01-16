---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
ms.openlocfilehash: 4308f2ec3da458f03e53d17a873d92ea5d775ff4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367386"
---
# <span data-ttu-id="fee07-101">Get-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="fee07-101">Get-AzMySqlServer</span></span>

## <span data-ttu-id="fee07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fee07-102">SYNOPSIS</span></span>
<span data-ttu-id="fee07-103">Információkat kap a kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="fee07-103">Gets information about a server.</span></span>

## <span data-ttu-id="fee07-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fee07-104">SYNTAX</span></span>

### <span data-ttu-id="fee07-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fee07-105">List1 (Default)</span></span>
```
Get-AzMySqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fee07-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="fee07-106">Get</span></span>
```
Get-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fee07-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fee07-107">GetViaIdentity</span></span>
```
Get-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fee07-108">Lista</span><span class="sxs-lookup"><span data-stu-id="fee07-108">List</span></span>
```
Get-AzMySqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="fee07-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fee07-109">DESCRIPTION</span></span>
<span data-ttu-id="fee07-110">Információkat kap a kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="fee07-110">Gets information about a server.</span></span>

## <span data-ttu-id="fee07-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fee07-111">EXAMPLES</span></span>

### <span data-ttu-id="fee07-112">1. példa: A MySql-kiszolgáló lekért beállítása alapértelmezett környezetben</span><span class="sxs-lookup"><span data-stu-id="fee07-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="fee07-113">Ez a parancsmag az alapértelmezett környezetben kapja meg a MySql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="fee07-113">This cmdlet gets MySql server with default context.</span></span>

### <span data-ttu-id="fee07-114">2. példa: A MySql-kiszolgáló lekérte erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="fee07-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="fee07-115">Ez a parancsmag a MySql-kiszolgálót erőforráscsoport és kiszolgálónév szerint kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fee07-115">This cmdlet gets MySql server by resource group and server name.</span></span>

### <span data-ttu-id="fee07-116">3. példa: A mySql-kiszolgálók listája a megadott erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="fee07-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="fee07-117">Ez a parancsmag a megadott erőforráscsoport összes MySql-kiszolgálóját felsorolja.</span><span class="sxs-lookup"><span data-stu-id="fee07-117">This cmdlet lists all the MySql servers in specified resource group.</span></span>

### <span data-ttu-id="fee07-118">4. példa: A MySql-kiszolgáló lekért identitás szerint</span><span class="sxs-lookup"><span data-stu-id="fee07-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Get-AzMySqlServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="fee07-119">Ez a parancsmaglista identitás alapján kapja meg a MySql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="fee07-119">This cmdlet lists gets MySql server by identity.</span></span>

## <span data-ttu-id="fee07-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fee07-120">PARAMETERS</span></span>

### <span data-ttu-id="fee07-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee07-121">-DefaultProfile</span></span>
<span data-ttu-id="fee07-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fee07-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fee07-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fee07-123">-InputObject</span></span>
<span data-ttu-id="fee07-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="fee07-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fee07-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fee07-125">-Name</span></span>
<span data-ttu-id="fee07-126">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="fee07-126">The name of the server.</span></span>

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

### <span data-ttu-id="fee07-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fee07-127">-ResourceGroupName</span></span>
<span data-ttu-id="fee07-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fee07-128">The name of the resource group.</span></span>
<span data-ttu-id="fee07-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="fee07-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fee07-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fee07-130">-SubscriptionId</span></span>
<span data-ttu-id="fee07-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fee07-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fee07-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee07-132">CommonParameters</span></span>
<span data-ttu-id="fee07-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fee07-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee07-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fee07-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee07-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fee07-135">INPUTS</span></span>

### <span data-ttu-id="fee07-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="fee07-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="fee07-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fee07-137">OUTPUTS</span></span>

### <span data-ttu-id="fee07-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="fee07-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="fee07-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fee07-139">NOTES</span></span>

<span data-ttu-id="fee07-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="fee07-140">ALIASES</span></span>

<span data-ttu-id="fee07-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="fee07-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fee07-142">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="fee07-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fee07-143">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fee07-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fee07-144">INPUTOBJECT: <IMySqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="fee07-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fee07-145">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="fee07-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="fee07-146">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="fee07-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="fee07-147">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="fee07-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="fee07-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="fee07-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fee07-149">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="fee07-149">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="fee07-150">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="fee07-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="fee07-151">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fee07-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fee07-152">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="fee07-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="fee07-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="fee07-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="fee07-154">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="fee07-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="fee07-155">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fee07-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fee07-156">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="fee07-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="fee07-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fee07-157">RELATED LINKS</span></span>

