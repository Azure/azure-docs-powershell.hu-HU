---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/remove-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 630393d0c535a5f44f8a5e7dcf49cc491552f185
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013333"
---
# <span data-ttu-id="8de53-101">Remove-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="8de53-101">Remove-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="8de53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8de53-102">SYNOPSIS</span></span>
<span data-ttu-id="8de53-103">Törli a megadott előfizetéshez, erőforráscsoporthoz, SapMonitor névhez és erőforrásnévhez megadott szolgáltatópéldányt.</span><span class="sxs-lookup"><span data-stu-id="8de53-103">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="8de53-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8de53-104">SYNTAX</span></span>

### <span data-ttu-id="8de53-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8de53-105">Delete (Default)</span></span>
```
Remove-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8de53-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8de53-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8de53-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8de53-107">DESCRIPTION</span></span>
<span data-ttu-id="8de53-108">Törli a megadott előfizetéshez, erőforráscsoporthoz, SapMonitor névhez és erőforrásnévhez megadott szolgáltatópéldányt.</span><span class="sxs-lookup"><span data-stu-id="8de53-108">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="8de53-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8de53-109">EXAMPLES</span></span>

### <span data-ttu-id="8de53-110">1. példa: Az SAP-monitor példányának eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="8de53-110">Example 1: Remove instance of SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

```

<span data-ttu-id="8de53-111">Ez a parancs név szerint eltávolítja az SAP-monitor példányát.</span><span class="sxs-lookup"><span data-stu-id="8de53-111">This command removes instance of SAP monitor by name.</span></span>

### <span data-ttu-id="8de53-112">2. példa: Az SAP-monitor példányának eltávolítása objektumról objektumra</span><span class="sxs-lookup"><span data-stu-id="8de53-112">Example 2: Remove instance of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t01
PS C:\> Remove-AzSapMonitorProviderInstance -InputObject $sapIns

```

<span data-ttu-id="8de53-113">Ez a parancs objektumról objektumra eltávolítja az SAP-monitor példányát.</span><span class="sxs-lookup"><span data-stu-id="8de53-113">This command removes instance of SAP monitor by object.</span></span>

## <span data-ttu-id="8de53-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8de53-114">PARAMETERS</span></span>

### <span data-ttu-id="8de53-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8de53-115">-AsJob</span></span>
<span data-ttu-id="8de53-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="8de53-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8de53-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8de53-117">-DefaultProfile</span></span>
<span data-ttu-id="8de53-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8de53-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8de53-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8de53-119">-InputObject</span></span>
<span data-ttu-id="8de53-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="8de53-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8de53-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8de53-121">-Name</span></span>
<span data-ttu-id="8de53-122">A szolgáltatópéldány neve.</span><span class="sxs-lookup"><span data-stu-id="8de53-122">Name of the provider instance.</span></span>

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

### <span data-ttu-id="8de53-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8de53-123">-NoWait</span></span>
<span data-ttu-id="8de53-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="8de53-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8de53-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8de53-125">-PassThru</span></span>
<span data-ttu-id="8de53-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="8de53-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8de53-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8de53-127">-ResourceGroupName</span></span>
<span data-ttu-id="8de53-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8de53-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="8de53-129">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="8de53-129">-SapMonitorName</span></span>
<span data-ttu-id="8de53-130">Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="8de53-130">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="8de53-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8de53-131">-SubscriptionId</span></span>
<span data-ttu-id="8de53-132">Előfizetésazonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="8de53-132">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8de53-133">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="8de53-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8de53-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8de53-134">-Confirm</span></span>
<span data-ttu-id="8de53-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8de53-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8de53-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8de53-136">-WhatIf</span></span>
<span data-ttu-id="8de53-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8de53-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8de53-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8de53-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8de53-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de53-139">CommonParameters</span></span>
<span data-ttu-id="8de53-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8de53-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de53-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8de53-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de53-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8de53-142">INPUTS</span></span>

### <span data-ttu-id="8de53-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="8de53-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="8de53-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8de53-144">OUTPUTS</span></span>

### <span data-ttu-id="8de53-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8de53-145">System.Boolean</span></span>

## <span data-ttu-id="8de53-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8de53-146">NOTES</span></span>

<span data-ttu-id="8de53-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="8de53-147">ALIASES</span></span>

<span data-ttu-id="8de53-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="8de53-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8de53-149">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="8de53-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8de53-150">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8de53-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8de53-151">INPUTOBJECT: <IHanaOnAzureIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="8de53-151">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8de53-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="8de53-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8de53-153">`[Location <String>]`: A törölt tároló helye.</span><span class="sxs-lookup"><span data-stu-id="8de53-153">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="8de53-154">`[OperationKind <AccessPolicyUpdateKind?>]`: A művelet neve</span><span class="sxs-lookup"><span data-stu-id="8de53-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="8de53-155">`[ProviderInstanceName <String>]`: A szolgáltatópéldány neve.</span><span class="sxs-lookup"><span data-stu-id="8de53-155">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="8de53-156">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8de53-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="8de53-157">`[ResourceName <String>]`: Az identitáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="8de53-157">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="8de53-158">`[SapMonitorName <String>]`: Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="8de53-158">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="8de53-159">`[Scope <String>]`: Az erőforrás erőforrás-szolgáltatójának hatóköre.</span><span class="sxs-lookup"><span data-stu-id="8de53-159">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="8de53-160">Felügyelt identitásokkal bővített szülőerőforrás.</span><span class="sxs-lookup"><span data-stu-id="8de53-160">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="8de53-161">`[SubscriptionId <String>]`: Előfizetésazonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="8de53-161">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8de53-162">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="8de53-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8de53-163">`[VaultName <String>]`: A tároló neve</span><span class="sxs-lookup"><span data-stu-id="8de53-163">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="8de53-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8de53-164">RELATED LINKS</span></span>

