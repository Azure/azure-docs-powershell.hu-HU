---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 474b4dc71658c1b8d79577f029d7ce0e098cca91
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194350"
---
# <span data-ttu-id="a7f57-101">Remove-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a7f57-101">Remove-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="a7f57-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a7f57-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f57-103">A virtuális hálózati szabály törlése a megadott névvel</span><span class="sxs-lookup"><span data-stu-id="a7f57-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="a7f57-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a7f57-104">SYNTAX</span></span>

### <span data-ttu-id="a7f57-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a7f57-105">Delete (Default)</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a7f57-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a7f57-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a7f57-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a7f57-107">DESCRIPTION</span></span>
<span data-ttu-id="a7f57-108">A virtuális hálózati szabály törlése a megadott névvel</span><span class="sxs-lookup"><span data-stu-id="a7f57-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="a7f57-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a7f57-109">EXAMPLES</span></span>

### <span data-ttu-id="a7f57-110">Példa 1: virtuális hálózati szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a7f57-110">Example 1: Remove a virtual network rule</span></span>
```powershell
PS C:\> Remove-AzMariaDbVirtualNetworkRule -Name vnet-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

```

<span data-ttu-id="a7f57-111">Ez a parancs eltávolítja a virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="a7f57-111">This command removes a virtual network rule.</span></span>

## <span data-ttu-id="a7f57-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a7f57-112">PARAMETERS</span></span>

### <span data-ttu-id="a7f57-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7f57-113">-AsJob</span></span>
<span data-ttu-id="a7f57-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="a7f57-114">Run the command as a job</span></span>

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

### <span data-ttu-id="a7f57-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f57-115">-DefaultProfile</span></span>
<span data-ttu-id="a7f57-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a7f57-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7f57-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7f57-117">-InputObject</span></span>
<span data-ttu-id="a7f57-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a7f57-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f57-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a7f57-119">-Name</span></span>
<span data-ttu-id="a7f57-120">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="a7f57-120">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f57-121">-Várva</span><span class="sxs-lookup"><span data-stu-id="a7f57-121">-NoWait</span></span>
<span data-ttu-id="a7f57-122">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="a7f57-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a7f57-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7f57-123">-PassThru</span></span>
<span data-ttu-id="a7f57-124">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="a7f57-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a7f57-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f57-125">-ResourceGroupName</span></span>
<span data-ttu-id="a7f57-126">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a7f57-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a7f57-127">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="a7f57-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f57-128">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a7f57-128">-ServerName</span></span>
<span data-ttu-id="a7f57-129">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="a7f57-129">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f57-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a7f57-130">-SubscriptionId</span></span>
<span data-ttu-id="a7f57-131">Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="a7f57-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f57-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a7f57-132">-Confirm</span></span>
<span data-ttu-id="a7f57-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a7f57-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f57-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7f57-134">-WhatIf</span></span>
<span data-ttu-id="a7f57-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a7f57-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7f57-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a7f57-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f57-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f57-137">CommonParameters</span></span>
<span data-ttu-id="a7f57-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a7f57-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f57-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a7f57-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f57-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7f57-140">INPUTS</span></span>

### <span data-ttu-id="a7f57-141">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="a7f57-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="a7f57-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7f57-142">OUTPUTS</span></span>

### <span data-ttu-id="a7f57-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a7f57-143">System.Boolean</span></span>

## <span data-ttu-id="a7f57-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a7f57-144">NOTES</span></span>

<span data-ttu-id="a7f57-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a7f57-145">ALIASES</span></span>

<span data-ttu-id="a7f57-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="a7f57-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a7f57-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="a7f57-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a7f57-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="a7f57-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a7f57-149">INPUTOBJECT <IMariaDbIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="a7f57-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a7f57-150">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="a7f57-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a7f57-151">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="a7f57-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a7f57-152">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="a7f57-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a7f57-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a7f57-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a7f57-154">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="a7f57-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a7f57-155">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a7f57-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a7f57-156">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="a7f57-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a7f57-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="a7f57-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a7f57-158">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="a7f57-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a7f57-159">`[SubscriptionId <String>]`: Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="a7f57-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="a7f57-160">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="a7f57-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a7f57-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7f57-161">RELATED LINKS</span></span>
