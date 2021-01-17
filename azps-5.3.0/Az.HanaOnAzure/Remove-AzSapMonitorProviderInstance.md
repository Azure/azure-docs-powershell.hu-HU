---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 53f251b001b4e2f6319840079e9db3111c00b006
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386873"
---
# <span data-ttu-id="1bcc4-101">Remove-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="1bcc4-101">Remove-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="1bcc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bcc4-102">SYNOPSIS</span></span>
<span data-ttu-id="1bcc4-103">Törli a megadott előfizetéshez, erőforráscsoporthoz, SapMonitor névhez és erőforrásnévhez megadott szolgáltatópéldányt.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-103">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="1bcc4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1bcc4-104">SYNTAX</span></span>

### <span data-ttu-id="1bcc4-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1bcc4-105">Delete (Default)</span></span>
```
Remove-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1bcc4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1bcc4-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1bcc4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1bcc4-107">DESCRIPTION</span></span>
<span data-ttu-id="1bcc4-108">Törli a megadott előfizetéshez, erőforráscsoporthoz, SapMonitor névhez és erőforrásnévhez megadott szolgáltatópéldányt.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-108">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="1bcc4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1bcc4-109">EXAMPLES</span></span>

### <span data-ttu-id="1bcc4-110">1. példa: Az SAP-monitor példányának eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="1bcc4-110">Example 1: Remove instance of SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

```

<span data-ttu-id="1bcc4-111">Ez a parancs név szerint eltávolítja az SAP-monitor példányát.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-111">This command removes instance of SAP monitor by name.</span></span>

### <span data-ttu-id="1bcc4-112">2. példa: Az SAP-monitor példányának eltávolítása objektumról objektumra</span><span class="sxs-lookup"><span data-stu-id="1bcc4-112">Example 2: Remove instance of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t01
PS C:\> Remove-AzSapMonitorProviderInstance -InputObject $sapIns

```

<span data-ttu-id="1bcc4-113">Ez a parancs objektumról objektumra eltávolítja az SAP-monitor példányát.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-113">This command removes instance of SAP monitor by object.</span></span>

## <span data-ttu-id="1bcc4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1bcc4-114">PARAMETERS</span></span>

### <span data-ttu-id="1bcc4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bcc4-115">-AsJob</span></span>
<span data-ttu-id="1bcc4-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="1bcc4-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1bcc4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bcc4-117">-DefaultProfile</span></span>
<span data-ttu-id="1bcc4-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bcc4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bcc4-119">-InputObject</span></span>
<span data-ttu-id="1bcc4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1bcc4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1bcc4-121">-Name</span></span>
<span data-ttu-id="1bcc4-122">A szolgáltatópéldány neve.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-122">Name of the provider instance.</span></span>

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

### <span data-ttu-id="1bcc4-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1bcc4-123">-NoWait</span></span>
<span data-ttu-id="1bcc4-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="1bcc4-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1bcc4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bcc4-125">-PassThru</span></span>
<span data-ttu-id="1bcc4-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="1bcc4-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1bcc4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bcc4-127">-ResourceGroupName</span></span>
<span data-ttu-id="1bcc4-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="1bcc4-129">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="1bcc4-129">-SapMonitorName</span></span>
<span data-ttu-id="1bcc4-130">Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-130">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="1bcc4-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1bcc4-131">-SubscriptionId</span></span>
<span data-ttu-id="1bcc4-132">Előfizetésazonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-132">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1bcc4-133">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1bcc4-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1bcc4-134">-Confirm</span></span>
<span data-ttu-id="1bcc4-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bcc4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bcc4-136">-WhatIf</span></span>
<span data-ttu-id="1bcc4-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bcc4-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bcc4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bcc4-139">CommonParameters</span></span>
<span data-ttu-id="1bcc4-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bcc4-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1bcc4-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bcc4-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1bcc4-142">INPUTS</span></span>

### <span data-ttu-id="1bcc4-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="1bcc4-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="1bcc4-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1bcc4-144">OUTPUTS</span></span>

### <span data-ttu-id="1bcc4-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1bcc4-145">System.Boolean</span></span>

## <span data-ttu-id="1bcc4-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1bcc4-146">NOTES</span></span>

<span data-ttu-id="1bcc4-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="1bcc4-147">ALIASES</span></span>

<span data-ttu-id="1bcc4-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="1bcc4-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1bcc4-149">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1bcc4-150">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1bcc4-151">INPUTOBJECT: <IHanaOnAzureIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="1bcc4-151">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1bcc4-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="1bcc4-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1bcc4-153">`[Location <String>]`: A törölt tároló helye.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-153">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="1bcc4-154">`[OperationKind <AccessPolicyUpdateKind?>]`: A művelet neve</span><span class="sxs-lookup"><span data-stu-id="1bcc4-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="1bcc4-155">`[ProviderInstanceName <String>]`: A szolgáltatópéldány neve.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-155">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="1bcc4-156">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="1bcc4-157">`[ResourceName <String>]`: Az identitáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-157">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="1bcc4-158">`[SapMonitorName <String>]`: Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-158">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="1bcc4-159">`[Scope <String>]`: Az erőforrás erőforrás-szolgáltatójának hatóköre.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-159">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="1bcc4-160">Felügyelt identitásokkal bővített szülőerőforrás.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-160">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="1bcc4-161">`[SubscriptionId <String>]`: Előfizetésazonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-161">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1bcc4-162">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="1bcc4-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="1bcc4-163">`[VaultName <String>]`: A tároló neve</span><span class="sxs-lookup"><span data-stu-id="1bcc4-163">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="1bcc4-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1bcc4-164">RELATED LINKS</span></span>

