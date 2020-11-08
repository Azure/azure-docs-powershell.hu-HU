---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 53f251b001b4e2f6319840079e9db3111c00b006
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187390"
---
# <span data-ttu-id="e2b92-101">Remove-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="e2b92-101">Remove-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="e2b92-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2b92-102">SYNOPSIS</span></span>
<span data-ttu-id="e2b92-103">A megadott előfizetéshez, erőforráscsoporthez, SapMonitor és erőforrás nevéhez tartozó szolgáltató példány törlése.</span><span class="sxs-lookup"><span data-stu-id="e2b92-103">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="e2b92-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2b92-104">SYNTAX</span></span>

### <span data-ttu-id="e2b92-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e2b92-105">Delete (Default)</span></span>
```
Remove-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e2b92-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e2b92-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e2b92-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2b92-107">DESCRIPTION</span></span>
<span data-ttu-id="e2b92-108">A megadott előfizetéshez, erőforráscsoporthez, SapMonitor és erőforrás nevéhez tartozó szolgáltató példány törlése.</span><span class="sxs-lookup"><span data-stu-id="e2b92-108">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="e2b92-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e2b92-109">EXAMPLES</span></span>

### <span data-ttu-id="e2b92-110">1. példa: az SAP-monitor példányának eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="e2b92-110">Example 1: Remove instance of SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

```

<span data-ttu-id="e2b92-111">Ez a parancs eltávolítja az SAP-figyelés példányát név szerint.</span><span class="sxs-lookup"><span data-stu-id="e2b92-111">This command removes instance of SAP monitor by name.</span></span>

### <span data-ttu-id="e2b92-112">2. példa: az SAP-monitor példányának eltávolítása objektumból</span><span class="sxs-lookup"><span data-stu-id="e2b92-112">Example 2: Remove instance of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t01
PS C:\> Remove-AzSapMonitorProviderInstance -InputObject $sapIns

```

<span data-ttu-id="e2b92-113">Ez a parancs eltávolítja az objektum által létrehozott SAP-monitor példányát.</span><span class="sxs-lookup"><span data-stu-id="e2b92-113">This command removes instance of SAP monitor by object.</span></span>

## <span data-ttu-id="e2b92-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2b92-114">PARAMETERS</span></span>

### <span data-ttu-id="e2b92-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2b92-115">-AsJob</span></span>
<span data-ttu-id="e2b92-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="e2b92-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e2b92-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2b92-117">-DefaultProfile</span></span>
<span data-ttu-id="e2b92-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2b92-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2b92-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2b92-119">-InputObject</span></span>
<span data-ttu-id="e2b92-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e2b92-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b92-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e2b92-121">-Name</span></span>
<span data-ttu-id="e2b92-122">A szolgáltató példányának neve.</span><span class="sxs-lookup"><span data-stu-id="e2b92-122">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b92-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="e2b92-123">-NoWait</span></span>
<span data-ttu-id="e2b92-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="e2b92-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e2b92-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2b92-125">-PassThru</span></span>
<span data-ttu-id="e2b92-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="e2b92-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e2b92-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2b92-127">-ResourceGroupName</span></span>
<span data-ttu-id="e2b92-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e2b92-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="e2b92-129">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="e2b92-129">-SapMonitorName</span></span>
<span data-ttu-id="e2b92-130">Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e2b92-130">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="e2b92-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2b92-131">-SubscriptionId</span></span>
<span data-ttu-id="e2b92-132">Előfizetési azonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="e2b92-132">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e2b92-133">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e2b92-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e2b92-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e2b92-134">-Confirm</span></span>
<span data-ttu-id="e2b92-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e2b92-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2b92-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2b92-136">-WhatIf</span></span>
<span data-ttu-id="e2b92-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e2b92-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2b92-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e2b92-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2b92-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2b92-139">CommonParameters</span></span>
<span data-ttu-id="e2b92-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2b92-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2b92-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e2b92-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2b92-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2b92-142">INPUTS</span></span>

### <span data-ttu-id="e2b92-143">Microsoft. Azure. PowerShell. parancsmagok. HanaOnAzure. models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="e2b92-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="e2b92-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2b92-144">OUTPUTS</span></span>

### <span data-ttu-id="e2b92-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2b92-145">System.Boolean</span></span>

## <span data-ttu-id="e2b92-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2b92-146">NOTES</span></span>

<span data-ttu-id="e2b92-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e2b92-147">ALIASES</span></span>

<span data-ttu-id="e2b92-148">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="e2b92-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e2b92-149">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="e2b92-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e2b92-150">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="e2b92-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e2b92-151">INPUTOBJECT <IHanaOnAzureIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="e2b92-151">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e2b92-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e2b92-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e2b92-153">`[Location <String>]`: A törölt boltozat helye.</span><span class="sxs-lookup"><span data-stu-id="e2b92-153">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="e2b92-154">`[OperationKind <AccessPolicyUpdateKind?>]`: A művelet neve</span><span class="sxs-lookup"><span data-stu-id="e2b92-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="e2b92-155">`[ProviderInstanceName <String>]`: A szolgáltató példányának neve.</span><span class="sxs-lookup"><span data-stu-id="e2b92-155">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="e2b92-156">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e2b92-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="e2b92-157">`[ResourceName <String>]`: Az identitás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e2b92-157">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="e2b92-158">`[SapMonitorName <String>]`: Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e2b92-158">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="e2b92-159">`[Scope <String>]`: Az erőforrás-szolgáltató hatóköre.</span><span class="sxs-lookup"><span data-stu-id="e2b92-159">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="e2b92-160">A fölérendelt erőforrás a felügyelt identitások segítségével meghosszabbodik.</span><span class="sxs-lookup"><span data-stu-id="e2b92-160">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="e2b92-161">`[SubscriptionId <String>]`: Az előfizetés azonosítója, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="e2b92-161">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e2b92-162">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e2b92-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e2b92-163">`[VaultName <String>]`: A boltozat neve</span><span class="sxs-lookup"><span data-stu-id="e2b92-163">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="e2b92-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2b92-164">RELATED LINKS</span></span>

