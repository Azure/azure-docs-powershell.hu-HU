---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlServer.md
ms.openlocfilehash: 86cc2a249479807adc14ad0faa4c682d1fef4725
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194107"
---
# <span data-ttu-id="04714-101">Remove-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="04714-101">Remove-AzMySqlServer</span></span>

## <span data-ttu-id="04714-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04714-102">SYNOPSIS</span></span>
<span data-ttu-id="04714-103">Kiszolgáló törlése</span><span class="sxs-lookup"><span data-stu-id="04714-103">Deletes a server.</span></span>

## <span data-ttu-id="04714-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04714-104">SYNTAX</span></span>

### <span data-ttu-id="04714-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="04714-105">Delete (Default)</span></span>
```
Remove-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="04714-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="04714-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="04714-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="04714-107">DESCRIPTION</span></span>
<span data-ttu-id="04714-108">Kiszolgáló törlése</span><span class="sxs-lookup"><span data-stu-id="04714-108">Deletes a server.</span></span>

## <span data-ttu-id="04714-109">Példák</span><span class="sxs-lookup"><span data-stu-id="04714-109">EXAMPLES</span></span>

### <span data-ttu-id="04714-110">1. példa: a MySql-kiszolgáló eltávolítása a resourceGroup és a kiszolgáló nevével</span><span class="sxs-lookup"><span data-stu-id="04714-110">Example 1: Remove MySql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

```

<span data-ttu-id="04714-111">Ez a parancsmag eltávolítja a MySql szervert a resourceGroup és a kiszolgálónév alapján.</span><span class="sxs-lookup"><span data-stu-id="04714-111">This cmdlet removes MySql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="04714-112">2. példa: a MySql-kiszolgáló eltávolítása identitással</span><span class="sxs-lookup"><span data-stu-id="04714-112">Example 2: Remove MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Remove-AzMySqlServer -InputObject $ID
 
```

<span data-ttu-id="04714-113">Ezek a parancsmagok a MySql szervert identitással távolítják el.</span><span class="sxs-lookup"><span data-stu-id="04714-113">These cmdlets remove MySql server by identity.</span></span>

## <span data-ttu-id="04714-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04714-114">PARAMETERS</span></span>

### <span data-ttu-id="04714-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04714-115">-AsJob</span></span>
<span data-ttu-id="04714-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="04714-116">Run the command as a job</span></span>

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

### <span data-ttu-id="04714-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04714-117">-DefaultProfile</span></span>
<span data-ttu-id="04714-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04714-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04714-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04714-119">-InputObject</span></span>
<span data-ttu-id="04714-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="04714-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="04714-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="04714-121">-Name</span></span>
<span data-ttu-id="04714-122">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="04714-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04714-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="04714-123">-NoWait</span></span>
<span data-ttu-id="04714-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="04714-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="04714-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04714-125">-PassThru</span></span>
<span data-ttu-id="04714-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="04714-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="04714-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04714-127">-ResourceGroupName</span></span>
<span data-ttu-id="04714-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="04714-128">The name of the resource group.</span></span>
<span data-ttu-id="04714-129">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="04714-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="04714-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="04714-130">-SubscriptionId</span></span>
<span data-ttu-id="04714-131">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="04714-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="04714-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="04714-132">-Confirm</span></span>
<span data-ttu-id="04714-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="04714-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04714-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04714-134">-WhatIf</span></span>
<span data-ttu-id="04714-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="04714-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04714-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="04714-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04714-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04714-137">CommonParameters</span></span>
<span data-ttu-id="04714-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04714-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04714-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="04714-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04714-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04714-140">INPUTS</span></span>

### <span data-ttu-id="04714-141">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="04714-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="04714-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04714-142">OUTPUTS</span></span>

### <span data-ttu-id="04714-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04714-143">System.Boolean</span></span>

## <span data-ttu-id="04714-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04714-144">NOTES</span></span>

<span data-ttu-id="04714-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="04714-145">ALIASES</span></span>

<span data-ttu-id="04714-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="04714-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="04714-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="04714-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="04714-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="04714-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="04714-149">INPUTOBJECT <IMySqlIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="04714-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="04714-150">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="04714-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="04714-151">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="04714-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="04714-152">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="04714-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="04714-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="04714-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="04714-154">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="04714-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="04714-155">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="04714-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="04714-156">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="04714-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="04714-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="04714-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="04714-158">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="04714-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="04714-159">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="04714-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="04714-160">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="04714-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="04714-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04714-161">RELATED LINKS</span></span>
