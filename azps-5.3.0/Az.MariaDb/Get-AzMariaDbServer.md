---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
ms.openlocfilehash: 43af6a438a36df5360fd062aaf22e85e95fa62a1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469437"
---
# <span data-ttu-id="497ae-101">Get-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="497ae-101">Get-AzMariaDbServer</span></span>

## <span data-ttu-id="497ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="497ae-102">SYNOPSIS</span></span>
<span data-ttu-id="497ae-103">Információkat kap a kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="497ae-103">Gets information about a server.</span></span>

## <span data-ttu-id="497ae-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="497ae-104">SYNTAX</span></span>

### <span data-ttu-id="497ae-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="497ae-105">List1 (Default)</span></span>
```
Get-AzMariaDbServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="497ae-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="497ae-106">Get</span></span>
```
Get-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="497ae-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="497ae-107">GetViaIdentity</span></span>
```
Get-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="497ae-108">Lista</span><span class="sxs-lookup"><span data-stu-id="497ae-108">List</span></span>
```
Get-AzMariaDbServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="497ae-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="497ae-109">DESCRIPTION</span></span>
<span data-ttu-id="497ae-110">Információkat kap a kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="497ae-110">Gets information about a server.</span></span>

## <span data-ttu-id="497ae-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="497ae-111">EXAMPLES</span></span>

### <span data-ttu-id="497ae-112">1. példa: Az előfizetések teljes MariaDB-előfizetésének felsorolása</span><span class="sxs-lookup"><span data-stu-id="497ae-112">Example 1: List all MariaDB under a subscriptions</span></span>
```powershell
PS C:\> Get-AzMariaDbServer

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName    SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------    -------        --------------
mrdb01                     eastus   dolauli            10.2    5120                    B_Gen5_1   Basic          Enabled
wyunchi-10                 eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
wyunchi                    eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
wyunchi-eastus             eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-h3pame        eastus   qiszomtkpf         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-4rmtig        eastus   xofavpndqj         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-szp6dt        eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-9pebvn        eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-asd-01             eastus   adminuser          10.2    5120                    B_Gen5_1   Basic          Enabled
rst-001                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rst-002                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-003           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-004           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
```

<span data-ttu-id="497ae-113">Ez a parancs felsorolja az előfizetések alatt található összes MariaDB-t.</span><span class="sxs-lookup"><span data-stu-id="497ae-113">This command lists all MariaDB under a subscriptions.</span></span>

### <span data-ttu-id="497ae-114">2. példa: Az erőforráscsoport teljes MariaDB-ének felsorolása</span><span class="sxs-lookup"><span data-stu-id="497ae-114">Example 2: List all MariaDB under a resource group</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName    SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------    -------        --------------
mariadb-test-h3pame        eastus   qiszomtkpf         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-4rmtig        eastus   xofavpndqj         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-szp6dt        eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-9pebvn        eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-asd-01             eastus   adminuser          10.2    5120                    B_Gen5_1   Basic          Enabled
rst-001                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rst-002                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-003           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-004           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
```

<span data-ttu-id="497ae-115">Ez a parancs felsorolja egy erőforráscsoport összes MariaDB-ét.</span><span class="sxs-lookup"><span data-stu-id="497ae-115">This command lists all MariaDB under a resource group.</span></span>

### <span data-ttu-id="497ae-116">3. példa: A MariaDB lekérte</span><span class="sxs-lookup"><span data-stu-id="497ae-116">Example 3: Get a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0 -Name mariadb-test-h3pame

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-h3pame eastus   qiszomtkpf         10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="497ae-117">Ez a parancs egy MariaDB-t kap.</span><span class="sxs-lookup"><span data-stu-id="497ae-117">This command gets a MariaDB.</span></span>

## <span data-ttu-id="497ae-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="497ae-118">PARAMETERS</span></span>

### <span data-ttu-id="497ae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="497ae-119">-DefaultProfile</span></span>
<span data-ttu-id="497ae-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="497ae-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="497ae-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="497ae-121">-InputObject</span></span>
<span data-ttu-id="497ae-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="497ae-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="497ae-123">-Name</span><span class="sxs-lookup"><span data-stu-id="497ae-123">-Name</span></span>
<span data-ttu-id="497ae-124">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="497ae-124">The name of the server.</span></span>

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

### <span data-ttu-id="497ae-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="497ae-125">-ResourceGroupName</span></span>
<span data-ttu-id="497ae-126">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="497ae-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="497ae-127">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="497ae-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="497ae-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="497ae-128">-SubscriptionId</span></span>
<span data-ttu-id="497ae-129">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="497ae-129">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="497ae-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="497ae-130">CommonParameters</span></span>
<span data-ttu-id="497ae-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="497ae-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="497ae-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="497ae-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="497ae-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="497ae-133">INPUTS</span></span>

### <span data-ttu-id="497ae-134">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="497ae-134">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="497ae-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="497ae-135">OUTPUTS</span></span>

### <span data-ttu-id="497ae-136">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="497ae-136">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="497ae-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="497ae-137">NOTES</span></span>

<span data-ttu-id="497ae-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="497ae-138">ALIASES</span></span>

<span data-ttu-id="497ae-139">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="497ae-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="497ae-140">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="497ae-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="497ae-141">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="497ae-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="497ae-142">INPUTOBJECT: <IMariaDbIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="497ae-142">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="497ae-143">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="497ae-143">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="497ae-144">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="497ae-144">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="497ae-145">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="497ae-145">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="497ae-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="497ae-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="497ae-147">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="497ae-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="497ae-148">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="497ae-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="497ae-149">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="497ae-149">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="497ae-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="497ae-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="497ae-151">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="497ae-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="497ae-152">`[SubscriptionId <String>]`: Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="497ae-152">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="497ae-153">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="497ae-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="497ae-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="497ae-154">RELATED LINKS</span></span>

