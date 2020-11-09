---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 85690d3602744f6bde45a5f08b5a927124a8460a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296774"
---
# <span data-ttu-id="5eafe-101">Remove-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5eafe-101">Remove-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="5eafe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5eafe-102">SYNOPSIS</span></span>
<span data-ttu-id="5eafe-103">A virtuális hálózati szabály törlése a megadott névvel</span><span class="sxs-lookup"><span data-stu-id="5eafe-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="5eafe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5eafe-104">SYNTAX</span></span>

### <span data-ttu-id="5eafe-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5eafe-105">Delete (Default)</span></span>
```
Remove-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5eafe-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5eafe-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5eafe-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5eafe-107">DESCRIPTION</span></span>
<span data-ttu-id="5eafe-108">A virtuális hálózati szabály törlése a megadott névvel</span><span class="sxs-lookup"><span data-stu-id="5eafe-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="5eafe-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5eafe-109">EXAMPLES</span></span>

### <span data-ttu-id="5eafe-110">1. példa: a MySql-kiszolgáló virtuális hálózati szabályának eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="5eafe-110">Example 1: Remove MySql server Virtual Network Rule by name</span></span>
```powershell
PS C:\> Remove-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest-ServerName mysql-test

```

<span data-ttu-id="5eafe-111">Ez a parancsmag eltávolítja a MySql-kiszolgáló virtuális hálózati szabályát név szerint.</span><span class="sxs-lookup"><span data-stu-id="5eafe-111">This cmdlet removes MySql server Virtual Network Rule by name.</span></span>

### <span data-ttu-id="5eafe-112">2. példa: a MySql-kiszolgáló virtuális hálózati szabályának eltávolítása identitással</span><span class="sxs-lookup"><span data-stu-id="5eafe-112">Example 2: Remove MySql server Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Remove-AzMySqlVirtualNetworkRule -InputObject $ID
 
```

<span data-ttu-id="5eafe-113">Ezek a parancsmagok a MySql-kiszolgáló virtuális hálózati szabályait identitással távolítják el.</span><span class="sxs-lookup"><span data-stu-id="5eafe-113">These cmdlets remove MySql server Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="5eafe-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5eafe-114">PARAMETERS</span></span>

### <span data-ttu-id="5eafe-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5eafe-115">-AsJob</span></span>
<span data-ttu-id="5eafe-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="5eafe-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5eafe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eafe-117">-DefaultProfile</span></span>
<span data-ttu-id="5eafe-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5eafe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eafe-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5eafe-119">-InputObject</span></span>
<span data-ttu-id="5eafe-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5eafe-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5eafe-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5eafe-121">-Name</span></span>
<span data-ttu-id="5eafe-122">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="5eafe-122">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="5eafe-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="5eafe-123">-NoWait</span></span>
<span data-ttu-id="5eafe-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="5eafe-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5eafe-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5eafe-125">-PassThru</span></span>
<span data-ttu-id="5eafe-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="5eafe-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5eafe-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eafe-127">-ResourceGroupName</span></span>
<span data-ttu-id="5eafe-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5eafe-128">The name of the resource group.</span></span>
<span data-ttu-id="5eafe-129">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="5eafe-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5eafe-130">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="5eafe-130">-ServerName</span></span>
<span data-ttu-id="5eafe-131">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="5eafe-131">The name of the server.</span></span>

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

### <span data-ttu-id="5eafe-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5eafe-132">-SubscriptionId</span></span>
<span data-ttu-id="5eafe-133">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5eafe-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5eafe-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5eafe-134">-Confirm</span></span>
<span data-ttu-id="5eafe-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5eafe-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5eafe-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eafe-136">-WhatIf</span></span>
<span data-ttu-id="5eafe-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5eafe-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5eafe-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5eafe-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5eafe-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eafe-139">CommonParameters</span></span>
<span data-ttu-id="5eafe-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5eafe-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eafe-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5eafe-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eafe-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5eafe-142">INPUTS</span></span>

### <span data-ttu-id="5eafe-143">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="5eafe-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="5eafe-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5eafe-144">OUTPUTS</span></span>

### <span data-ttu-id="5eafe-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5eafe-145">System.Boolean</span></span>

## <span data-ttu-id="5eafe-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5eafe-146">NOTES</span></span>

<span data-ttu-id="5eafe-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="5eafe-147">ALIASES</span></span>

<span data-ttu-id="5eafe-148">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="5eafe-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5eafe-149">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="5eafe-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5eafe-150">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="5eafe-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5eafe-151">INPUTOBJECT <IMySqlIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="5eafe-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5eafe-152">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="5eafe-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="5eafe-153">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="5eafe-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="5eafe-154">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="5eafe-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="5eafe-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="5eafe-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5eafe-156">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="5eafe-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="5eafe-157">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5eafe-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5eafe-158">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="5eafe-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="5eafe-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="5eafe-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="5eafe-160">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="5eafe-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="5eafe-161">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5eafe-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5eafe-162">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="5eafe-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="5eafe-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5eafe-163">RELATED LINKS</span></span>

