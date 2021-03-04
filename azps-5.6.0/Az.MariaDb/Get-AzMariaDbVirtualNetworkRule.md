---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: dda229292436d07cf5383343cb85472b92881cdf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927937"
---
# <span data-ttu-id="213e2-101">Get-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="213e2-101">Get-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="213e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="213e2-102">SYNOPSIS</span></span>
<span data-ttu-id="213e2-103">Virtuális hálózati szabályt kap.</span><span class="sxs-lookup"><span data-stu-id="213e2-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="213e2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="213e2-104">SYNTAX</span></span>

### <span data-ttu-id="213e2-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="213e2-105">List (Default)</span></span>
```
Get-AzMariaDbVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="213e2-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="213e2-106">Get</span></span>
```
Get-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="213e2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="213e2-107">GetViaIdentity</span></span>
```
Get-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="213e2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="213e2-108">DESCRIPTION</span></span>
<span data-ttu-id="213e2-109">Virtuális hálózati szabályt kap.</span><span class="sxs-lookup"><span data-stu-id="213e2-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="213e2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="213e2-110">EXAMPLES</span></span>

### <span data-ttu-id="213e2-111">1. példa: Az összes virtuális hálózati szabály felsorolása a MariaDB szerint</span><span class="sxs-lookup"><span data-stu-id="213e2-111">Example 1: List all virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
vnetrule-Adsefc Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="213e2-112">Ez a parancs felsorolja a MariaDB alatti összes virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="213e2-112">This command lists all virtual network rule under a MariaDB.</span></span>

### <span data-ttu-id="213e2-113">2. példa: Virtuális hálózati szabály lekérte a MariaDB</span><span class="sxs-lookup"><span data-stu-id="213e2-113">Example 2: Get virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn -Name vnetrule-QdMJpU

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="213e2-114">Ez a parancs a MariaDB alatt virtuális hálózati szabályt kap.</span><span class="sxs-lookup"><span data-stu-id="213e2-114">This command gets virtual network rule under a MariaDB.</span></span>

## <span data-ttu-id="213e2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="213e2-115">PARAMETERS</span></span>

### <span data-ttu-id="213e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="213e2-116">-DefaultProfile</span></span>
<span data-ttu-id="213e2-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="213e2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="213e2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="213e2-118">-InputObject</span></span>
<span data-ttu-id="213e2-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="213e2-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="213e2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="213e2-120">-Name</span></span>
<span data-ttu-id="213e2-121">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="213e2-121">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="213e2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="213e2-122">-PassThru</span></span>
<span data-ttu-id="213e2-123">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="213e2-123">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="213e2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="213e2-124">-ResourceGroupName</span></span>
<span data-ttu-id="213e2-125">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="213e2-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="213e2-126">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="213e2-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="213e2-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="213e2-127">-ServerName</span></span>
<span data-ttu-id="213e2-128">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="213e2-128">The name of the server.</span></span>

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

### <span data-ttu-id="213e2-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="213e2-129">-SubscriptionId</span></span>
<span data-ttu-id="213e2-130">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="213e2-130">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="213e2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="213e2-131">CommonParameters</span></span>
<span data-ttu-id="213e2-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="213e2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="213e2-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="213e2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="213e2-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="213e2-134">INPUTS</span></span>

### <span data-ttu-id="213e2-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="213e2-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="213e2-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="213e2-136">OUTPUTS</span></span>

### <span data-ttu-id="213e2-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="213e2-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="213e2-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="213e2-138">NOTES</span></span>

<span data-ttu-id="213e2-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="213e2-139">ALIASES</span></span>

<span data-ttu-id="213e2-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="213e2-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="213e2-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="213e2-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="213e2-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="213e2-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="213e2-143">INPUTOBJECT: <IMariaDbIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="213e2-143">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="213e2-144">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="213e2-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="213e2-145">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="213e2-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="213e2-146">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="213e2-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="213e2-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="213e2-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="213e2-148">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="213e2-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="213e2-149">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="213e2-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="213e2-150">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="213e2-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="213e2-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="213e2-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="213e2-152">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="213e2-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="213e2-153">`[SubscriptionId <String>]`: Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="213e2-153">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="213e2-154">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="213e2-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="213e2-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="213e2-155">RELATED LINKS</span></span>

