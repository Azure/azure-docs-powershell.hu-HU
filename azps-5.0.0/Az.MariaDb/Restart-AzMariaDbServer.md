---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restart-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
ms.openlocfilehash: 19a2c0f8638d74f47acb9d639a8de9275667155a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194608"
---
# <span data-ttu-id="f71b1-101">Restart-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="f71b1-101">Restart-AzMariaDbServer</span></span>

## <span data-ttu-id="f71b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f71b1-102">SYNOPSIS</span></span>
<span data-ttu-id="f71b1-103">Kiszolgáló újraindítása.</span><span class="sxs-lookup"><span data-stu-id="f71b1-103">Restarts a server.</span></span>

## <span data-ttu-id="f71b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f71b1-104">SYNTAX</span></span>

### <span data-ttu-id="f71b1-105">Kiszolgálónév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f71b1-105">ServerName (Default)</span></span>
```
Restart-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f71b1-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="f71b1-106">ServerObject</span></span>
```
Restart-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f71b1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f71b1-107">DESCRIPTION</span></span>
<span data-ttu-id="f71b1-108">Kiszolgáló újraindítása.</span><span class="sxs-lookup"><span data-stu-id="f71b1-108">Restarts a server.</span></span>

## <span data-ttu-id="f71b1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f71b1-109">EXAMPLES</span></span>

### <span data-ttu-id="f71b1-110">1. példa: MariaDB újraindítása</span><span class="sxs-lookup"><span data-stu-id="f71b1-110">Example 1: Restart a MariaDB</span></span>
```powershell
PS C:\> Restart-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="f71b1-111">Ez a parancs újraindítja a MariaDB.</span><span class="sxs-lookup"><span data-stu-id="f71b1-111">This command restart a MariaDB.</span></span>

### <span data-ttu-id="f71b1-112">2. példa: MariaDB újraindítása</span><span class="sxs-lookup"><span data-stu-id="f71b1-112">Example 2: Restart a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | Restart-AzMariaDbServer

```

<span data-ttu-id="f71b1-113">Ez a parancs újraindítja a MariaDB.</span><span class="sxs-lookup"><span data-stu-id="f71b1-113">This command restart a MariaDB.</span></span>

## <span data-ttu-id="f71b1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f71b1-114">PARAMETERS</span></span>

### <span data-ttu-id="f71b1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f71b1-115">-AsJob</span></span>
<span data-ttu-id="f71b1-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="f71b1-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f71b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f71b1-117">-DefaultProfile</span></span>
<span data-ttu-id="f71b1-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f71b1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f71b1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f71b1-119">-InputObject</span></span>
<span data-ttu-id="f71b1-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f71b1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f71b1-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f71b1-121">-Name</span></span>
<span data-ttu-id="f71b1-122">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="f71b1-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f71b1-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="f71b1-123">-NoWait</span></span>
<span data-ttu-id="f71b1-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="f71b1-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f71b1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f71b1-125">-PassThru</span></span>
<span data-ttu-id="f71b1-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="f71b1-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f71b1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f71b1-127">-ResourceGroupName</span></span>
<span data-ttu-id="f71b1-128">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f71b1-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f71b1-129">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="f71b1-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f71b1-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f71b1-130">-SubscriptionId</span></span>
<span data-ttu-id="f71b1-131">Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="f71b1-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f71b1-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f71b1-132">-Confirm</span></span>
<span data-ttu-id="f71b1-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f71b1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f71b1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f71b1-134">-WhatIf</span></span>
<span data-ttu-id="f71b1-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f71b1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f71b1-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f71b1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f71b1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f71b1-137">CommonParameters</span></span>
<span data-ttu-id="f71b1-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f71b1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f71b1-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f71b1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f71b1-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f71b1-140">INPUTS</span></span>

### <span data-ttu-id="f71b1-141">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="f71b1-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="f71b1-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f71b1-142">OUTPUTS</span></span>

### <span data-ttu-id="f71b1-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f71b1-143">System.Boolean</span></span>

## <span data-ttu-id="f71b1-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f71b1-144">NOTES</span></span>

<span data-ttu-id="f71b1-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f71b1-145">ALIASES</span></span>

<span data-ttu-id="f71b1-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="f71b1-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f71b1-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f71b1-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f71b1-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="f71b1-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f71b1-149">INPUTOBJECT <IMariaDbIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="f71b1-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f71b1-150">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="f71b1-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f71b1-151">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="f71b1-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f71b1-152">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="f71b1-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f71b1-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f71b1-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f71b1-154">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="f71b1-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f71b1-155">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f71b1-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="f71b1-156">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="f71b1-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="f71b1-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="f71b1-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f71b1-158">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="f71b1-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f71b1-159">`[SubscriptionId <String>]`: Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="f71b1-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="f71b1-160">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="f71b1-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f71b1-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f71b1-161">RELATED LINKS</span></span>
