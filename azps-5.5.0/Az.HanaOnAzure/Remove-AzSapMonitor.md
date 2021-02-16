---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
ms.openlocfilehash: bcba06d87bce2f9ccc8016afc9f08dff75e29b1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153058"
---
# <span data-ttu-id="a85ab-101">Remove-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="a85ab-101">Remove-AzSapMonitor</span></span>

## <span data-ttu-id="a85ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a85ab-102">SYNOPSIS</span></span>
<span data-ttu-id="a85ab-103">Töröl egy SAP-monitort a megadott előfizetéssel, erőforráscsoporttal és figyelőnévvel.</span><span class="sxs-lookup"><span data-stu-id="a85ab-103">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="a85ab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a85ab-104">SYNTAX</span></span>

### <span data-ttu-id="a85ab-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a85ab-105">Delete (Default)</span></span>
```
Remove-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a85ab-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a85ab-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a85ab-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a85ab-107">DESCRIPTION</span></span>
<span data-ttu-id="a85ab-108">Töröl egy SAP-monitort a megadott előfizetéssel, erőforráscsoporttal és figyelőnévvel.</span><span class="sxs-lookup"><span data-stu-id="a85ab-108">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="a85ab-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a85ab-109">EXAMPLES</span></span>

### <span data-ttu-id="a85ab-110">1. példa: SAP-monitor eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="a85ab-110">Example 1: Remove a SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t02

```

<span data-ttu-id="a85ab-111">Ez a parancs név szerint eltávolítja az SAP-monitorokat.</span><span class="sxs-lookup"><span data-stu-id="a85ab-111">This command removes a SAP monitor by name.</span></span>

### <span data-ttu-id="a85ab-112">2. példa: SAP-monitor eltávolítása objektumról objektumra</span><span class="sxs-lookup"><span data-stu-id="a85ab-112">Example 2: Remove a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Remove-AzSapMonitor -InputObject $sap

```

<span data-ttu-id="a85ab-113">Ez a parancs objektumról objektumra eltávolítja az SAP-monitort.</span><span class="sxs-lookup"><span data-stu-id="a85ab-113">This command removes a SAP monitor by object.</span></span>

## <span data-ttu-id="a85ab-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a85ab-114">PARAMETERS</span></span>

### <span data-ttu-id="a85ab-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a85ab-115">-AsJob</span></span>
<span data-ttu-id="a85ab-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="a85ab-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a85ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a85ab-117">-DefaultProfile</span></span>
<span data-ttu-id="a85ab-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a85ab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a85ab-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a85ab-119">-InputObject</span></span>
<span data-ttu-id="a85ab-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a85ab-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a85ab-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a85ab-121">-Name</span></span>
<span data-ttu-id="a85ab-122">Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a85ab-122">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a85ab-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a85ab-123">-NoWait</span></span>
<span data-ttu-id="a85ab-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="a85ab-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a85ab-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a85ab-125">-PassThru</span></span>
<span data-ttu-id="a85ab-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="a85ab-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a85ab-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a85ab-127">-ResourceGroupName</span></span>
<span data-ttu-id="a85ab-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a85ab-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="a85ab-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a85ab-129">-SubscriptionId</span></span>
<span data-ttu-id="a85ab-130">Előfizetésazonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="a85ab-130">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a85ab-131">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="a85ab-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a85ab-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a85ab-132">-Confirm</span></span>
<span data-ttu-id="a85ab-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a85ab-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a85ab-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a85ab-134">-WhatIf</span></span>
<span data-ttu-id="a85ab-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a85ab-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a85ab-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a85ab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a85ab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a85ab-137">CommonParameters</span></span>
<span data-ttu-id="a85ab-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a85ab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a85ab-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a85ab-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a85ab-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a85ab-140">INPUTS</span></span>

### <span data-ttu-id="a85ab-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="a85ab-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="a85ab-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a85ab-142">OUTPUTS</span></span>

### <span data-ttu-id="a85ab-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a85ab-143">System.Boolean</span></span>

## <span data-ttu-id="a85ab-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a85ab-144">NOTES</span></span>

<span data-ttu-id="a85ab-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a85ab-145">ALIASES</span></span>

<span data-ttu-id="a85ab-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="a85ab-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a85ab-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="a85ab-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a85ab-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a85ab-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a85ab-149">INPUTOBJECT: <IHanaOnAzureIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="a85ab-149">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a85ab-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a85ab-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a85ab-151">`[Location <String>]`: A törölt tároló helye.</span><span class="sxs-lookup"><span data-stu-id="a85ab-151">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="a85ab-152">`[OperationKind <AccessPolicyUpdateKind?>]`: A művelet neve</span><span class="sxs-lookup"><span data-stu-id="a85ab-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="a85ab-153">`[ProviderInstanceName <String>]`: A szolgáltatópéldány neve.</span><span class="sxs-lookup"><span data-stu-id="a85ab-153">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="a85ab-154">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a85ab-154">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="a85ab-155">`[ResourceName <String>]`: Az identitáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a85ab-155">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="a85ab-156">`[SapMonitorName <String>]`: Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a85ab-156">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="a85ab-157">`[Scope <String>]`: Az erőforrás erőforrás-szolgáltatójának hatóköre.</span><span class="sxs-lookup"><span data-stu-id="a85ab-157">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="a85ab-158">Felügyelt identitásokkal bővített szülőerőforrás.</span><span class="sxs-lookup"><span data-stu-id="a85ab-158">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="a85ab-159">`[SubscriptionId <String>]`: Előfizetésazonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="a85ab-159">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a85ab-160">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="a85ab-160">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a85ab-161">`[VaultName <String>]`: A tároló neve</span><span class="sxs-lookup"><span data-stu-id="a85ab-161">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="a85ab-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a85ab-162">RELATED LINKS</span></span>

