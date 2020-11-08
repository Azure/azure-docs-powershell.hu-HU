---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
ms.openlocfilehash: e2187c95237cdb89915c47fc7089fd5f9d38cff1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183474"
---
# <span data-ttu-id="7ccec-101">Get-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="7ccec-101">Get-AzMySqlServer</span></span>

## <span data-ttu-id="7ccec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ccec-102">SYNOPSIS</span></span>
<span data-ttu-id="7ccec-103">Információt kap a kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="7ccec-103">Gets information about a server.</span></span>

## <span data-ttu-id="7ccec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ccec-104">SYNTAX</span></span>

### <span data-ttu-id="7ccec-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7ccec-105">List1 (Default)</span></span>
```
Get-AzMySqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7ccec-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="7ccec-106">Get</span></span>
```
Get-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7ccec-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7ccec-107">GetViaIdentity</span></span>
```
Get-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7ccec-108">Lista</span><span class="sxs-lookup"><span data-stu-id="7ccec-108">List</span></span>
```
Get-AzMySqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ccec-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ccec-109">DESCRIPTION</span></span>
<span data-ttu-id="7ccec-110">Információt kap a kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="7ccec-110">Gets information about a server.</span></span>

## <span data-ttu-id="7ccec-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7ccec-111">EXAMPLES</span></span>

### <span data-ttu-id="7ccec-112">1. példa: a MySql-kiszolgáló beolvasása alapértelmezett környezettel</span><span class="sxs-lookup"><span data-stu-id="7ccec-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="7ccec-113">Ezt a parancsmagot a MySql-kiszolgáló alapértelmezett környezettel kapja.</span><span class="sxs-lookup"><span data-stu-id="7ccec-113">This cmdlet gets MySql server with default context.</span></span>

### <span data-ttu-id="7ccec-114">2. példa: a MySql-kiszolgáló beolvasása erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="7ccec-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="7ccec-115">Ez a parancsmag az erőforráscsoport és a kiszolgáló neve alapján kapja meg a MySql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="7ccec-115">This cmdlet gets MySql server by resource group and server name.</span></span>

### <span data-ttu-id="7ccec-116">3. példa: a megadott erőforráscsoport összes MySql-kiszolgálójának listája</span><span class="sxs-lookup"><span data-stu-id="7ccec-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="7ccec-117">Ez a parancsmag felsorolja a megadott erőforráscsoport összes MySql-kiszolgálóját.</span><span class="sxs-lookup"><span data-stu-id="7ccec-117">This cmdlet lists all the MySql servers in specified resource group.</span></span>

### <span data-ttu-id="7ccec-118">4. példa: a MySql-kiszolgáló beolvasása identitással</span><span class="sxs-lookup"><span data-stu-id="7ccec-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Get-AzMySqlServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="7ccec-119">Ez a parancsmag a MySql-kiszolgálót identitás szerint jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="7ccec-119">This cmdlet lists gets MySql server by identity.</span></span>

## <span data-ttu-id="7ccec-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ccec-120">PARAMETERS</span></span>

### <span data-ttu-id="7ccec-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ccec-121">-DefaultProfile</span></span>
<span data-ttu-id="7ccec-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ccec-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ccec-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ccec-123">-InputObject</span></span>
<span data-ttu-id="7ccec-124">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7ccec-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7ccec-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7ccec-125">-Name</span></span>
<span data-ttu-id="7ccec-126">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="7ccec-126">The name of the server.</span></span>

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

### <span data-ttu-id="7ccec-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ccec-127">-ResourceGroupName</span></span>
<span data-ttu-id="7ccec-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7ccec-128">The name of the resource group.</span></span>
<span data-ttu-id="7ccec-129">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="7ccec-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7ccec-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7ccec-130">-SubscriptionId</span></span>
<span data-ttu-id="7ccec-131">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7ccec-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7ccec-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ccec-132">CommonParameters</span></span>
<span data-ttu-id="7ccec-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ccec-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ccec-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7ccec-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ccec-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ccec-135">INPUTS</span></span>

### <span data-ttu-id="7ccec-136">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="7ccec-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="7ccec-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ccec-137">OUTPUTS</span></span>

### <span data-ttu-id="7ccec-138">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="7ccec-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="7ccec-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ccec-139">NOTES</span></span>

<span data-ttu-id="7ccec-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7ccec-140">ALIASES</span></span>

<span data-ttu-id="7ccec-141">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="7ccec-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7ccec-142">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="7ccec-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7ccec-143">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="7ccec-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7ccec-144">INPUTOBJECT <IMySqlIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="7ccec-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7ccec-145">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="7ccec-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="7ccec-146">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="7ccec-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="7ccec-147">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="7ccec-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="7ccec-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="7ccec-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7ccec-149">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="7ccec-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="7ccec-150">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7ccec-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7ccec-151">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="7ccec-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="7ccec-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="7ccec-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="7ccec-153">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="7ccec-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="7ccec-154">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7ccec-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7ccec-155">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="7ccec-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="7ccec-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ccec-156">RELATED LINKS</span></span>

