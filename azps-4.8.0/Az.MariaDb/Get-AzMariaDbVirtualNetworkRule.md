---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 7ae1159c3cd5f5feea3d836a421dd9fe08c78da8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181809"
---
# <span data-ttu-id="6602e-101">Get-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6602e-101">Get-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="6602e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6602e-102">SYNOPSIS</span></span>
<span data-ttu-id="6602e-103">Virtuális hálózati szabály kap.</span><span class="sxs-lookup"><span data-stu-id="6602e-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="6602e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6602e-104">SYNTAX</span></span>

### <span data-ttu-id="6602e-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6602e-105">List (Default)</span></span>
```
Get-AzMariaDbVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="6602e-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="6602e-106">Get</span></span>
```
Get-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="6602e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6602e-107">GetViaIdentity</span></span>
```
Get-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="6602e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6602e-108">DESCRIPTION</span></span>
<span data-ttu-id="6602e-109">Virtuális hálózati szabály kap.</span><span class="sxs-lookup"><span data-stu-id="6602e-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="6602e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6602e-110">EXAMPLES</span></span>

### <span data-ttu-id="6602e-111">Példa 1: az összes virtuális hálózati szabály listázása egy MariaDB alatt</span><span class="sxs-lookup"><span data-stu-id="6602e-111">Example 1: List all virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
vnetrule-Adsefc Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="6602e-112">Ez a parancs felsorolja az összes virtuális hálózati szabályt egy MariaDB alatt.</span><span class="sxs-lookup"><span data-stu-id="6602e-112">This command lists all virtual network rule under a MariaDB.</span></span>

### <span data-ttu-id="6602e-113">2. példa: virtuális hálózati szabály beolvasása egy MariaDB alatt</span><span class="sxs-lookup"><span data-stu-id="6602e-113">Example 2: Get virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn -Name vnetrule-QdMJpU

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="6602e-114">Ez a parancs a virtuális hálózati szabályt egy MariaDB alatt kapja.</span><span class="sxs-lookup"><span data-stu-id="6602e-114">This command gets virtual network rule under a MariaDB.</span></span>

## <span data-ttu-id="6602e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6602e-115">PARAMETERS</span></span>

### <span data-ttu-id="6602e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6602e-116">-DefaultProfile</span></span>
<span data-ttu-id="6602e-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6602e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6602e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6602e-118">-InputObject</span></span>
<span data-ttu-id="6602e-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6602e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6602e-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6602e-120">-Name</span></span>
<span data-ttu-id="6602e-121">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="6602e-121">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="6602e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6602e-122">-PassThru</span></span>
<span data-ttu-id="6602e-123">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="6602e-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6602e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6602e-124">-ResourceGroupName</span></span>
<span data-ttu-id="6602e-125">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6602e-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6602e-126">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="6602e-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6602e-127">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="6602e-127">-ServerName</span></span>
<span data-ttu-id="6602e-128">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6602e-128">The name of the server.</span></span>

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

### <span data-ttu-id="6602e-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6602e-129">-SubscriptionId</span></span>
<span data-ttu-id="6602e-130">Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="6602e-130">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="6602e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6602e-131">CommonParameters</span></span>
<span data-ttu-id="6602e-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6602e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6602e-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6602e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6602e-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6602e-134">INPUTS</span></span>

### <span data-ttu-id="6602e-135">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="6602e-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="6602e-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6602e-136">OUTPUTS</span></span>

### <span data-ttu-id="6602e-137">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. modellek. Api20180601Preview. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6602e-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="6602e-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6602e-138">NOTES</span></span>

<span data-ttu-id="6602e-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6602e-139">ALIASES</span></span>

<span data-ttu-id="6602e-140">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="6602e-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6602e-141">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="6602e-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6602e-142">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="6602e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6602e-143">INPUTOBJECT <IMariaDbIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="6602e-143">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6602e-144">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="6602e-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6602e-145">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6602e-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6602e-146">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="6602e-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6602e-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6602e-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6602e-148">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="6602e-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6602e-149">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6602e-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="6602e-150">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="6602e-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="6602e-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="6602e-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6602e-152">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6602e-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6602e-153">`[SubscriptionId <String>]`: Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="6602e-153">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="6602e-154">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="6602e-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6602e-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6602e-155">RELATED LINKS</span></span>

