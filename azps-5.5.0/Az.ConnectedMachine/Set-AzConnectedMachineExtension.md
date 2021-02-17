---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: b136f5194bdc7e0f4b4dfc969564d7ef8476d9bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209902"
---
# <span data-ttu-id="07818-101">Set-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="07818-101">Set-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="07818-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07818-102">SYNOPSIS</span></span>
<span data-ttu-id="07818-103">A bővítmény létrehozásához vagy frissítéséhez szükséges művelet.</span><span class="sxs-lookup"><span data-stu-id="07818-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="07818-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="07818-104">SYNTAX</span></span>

### <span data-ttu-id="07818-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="07818-105">UpdateExpanded (Default)</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="07818-106">Frissítés</span><span class="sxs-lookup"><span data-stu-id="07818-106">Update</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="07818-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="07818-107">DESCRIPTION</span></span>
<span data-ttu-id="07818-108">A bővítmény létrehozásához vagy frissítéséhez szükséges művelet.</span><span class="sxs-lookup"><span data-stu-id="07818-108">The operation to create or update the extension.</span></span>

## <span data-ttu-id="07818-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="07818-109">EXAMPLES</span></span>

### <span data-ttu-id="07818-110">1. példa: Bővítmény beállítása a számítógépen</span><span class="sxs-lookup"><span data-stu-id="07818-110">Example 1: Set an extension on a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="07818-111">Bővítményt állít be egy gépen.</span><span class="sxs-lookup"><span data-stu-id="07818-111">Sets an extension on a machine.</span></span>

### <span data-ttu-id="07818-112">2. példa: Bővítmény beállítása a folyamaton keresztül megadott bővítményparaméterekkel</span><span class="sxs-lookup"><span data-stu-id="07818-112">Example 2: Set an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="07818-113">Ez a beállítás egy bővítményt a folyamaton keresztül átadott objektum által megadott kiterjesztési paraméterekkel együtt állít be.</span><span class="sxs-lookup"><span data-stu-id="07818-113">This sets an extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="07818-114">Ez akkor lehet nagyszerű, ha meg szeretné ragadni az egyik gép paramétereit, és egy másik gépre szeretné alkalmazni.</span><span class="sxs-lookup"><span data-stu-id="07818-114">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

## <span data-ttu-id="07818-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07818-115">PARAMETERS</span></span>

### <span data-ttu-id="07818-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07818-116">-AsJob</span></span>
<span data-ttu-id="07818-117">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="07818-117">Run the command as a job</span></span>

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

### <span data-ttu-id="07818-118">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="07818-118">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="07818-119">Azt jelzi, hogy a bővítménynek újabb alverziót kell-e használnia, ha elérhető a telepítés során.</span><span class="sxs-lookup"><span data-stu-id="07818-119">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="07818-120">A telepítés után azonban a bővítmény nem frissíti az alverziókat, hacsak újra nem telepíti őket, még akkor sem, ha a tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="07818-120">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07818-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07818-121">-DefaultProfile</span></span>
<span data-ttu-id="07818-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07818-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07818-123">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="07818-123">-ExtensionParameter</span></span>
<span data-ttu-id="07818-124">Gépbővítményt ír le.</span><span class="sxs-lookup"><span data-stu-id="07818-124">Describes a Machine Extension.</span></span>
<span data-ttu-id="07818-125">Az EXTENSIONPARAMETER tulajdonságainak létrehozására és a kivonattáblák létrehozására vonatkozó MEGJEGYZÉSEK szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="07818-125">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07818-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="07818-126">-ExtensionType</span></span>
<span data-ttu-id="07818-127">A bővítmény típusát határozza meg; példa: "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="07818-127">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07818-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="07818-128">-ForceRerun</span></span>
<span data-ttu-id="07818-129">Hogyan kell a bővítménykezelőt frissíteni akkor is, ha a bővítmény konfigurációja nem változott meg.</span><span class="sxs-lookup"><span data-stu-id="07818-129">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07818-130">-Location</span><span class="sxs-lookup"><span data-stu-id="07818-130">-Location</span></span>
<span data-ttu-id="07818-131">Az a földrajzi hely, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="07818-131">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07818-132">-MachineName</span><span class="sxs-lookup"><span data-stu-id="07818-132">-MachineName</span></span>
<span data-ttu-id="07818-133">Annak a gépnek a neve, ahol létre kell hoznunk vagy frissíteni kell a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="07818-133">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07818-134">-Name</span><span class="sxs-lookup"><span data-stu-id="07818-134">-Name</span></span>
<span data-ttu-id="07818-135">A gépbővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="07818-135">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07818-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="07818-136">-NoWait</span></span>
<span data-ttu-id="07818-137">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="07818-137">Run the command asynchronously</span></span>

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

### <span data-ttu-id="07818-138">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="07818-138">-ProtectedSetting</span></span>
<span data-ttu-id="07818-139">A bővítmény tartalmazhat protectedSettings vagy protectedSettingsFromKeyVault beállításokat, vagy egyáltalán nem tartalmazhat védett beállításokat.</span><span class="sxs-lookup"><span data-stu-id="07818-139">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesProtectedSettings
Parameter Sets: UpdateExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07818-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="07818-140">-Publisher</span></span>
<span data-ttu-id="07818-141">A bővítménykezelő közzétevője neve.</span><span class="sxs-lookup"><span data-stu-id="07818-141">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07818-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07818-142">-ResourceGroupName</span></span>
<span data-ttu-id="07818-143">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="07818-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07818-144">-Beállítás</span><span class="sxs-lookup"><span data-stu-id="07818-144">-Setting</span></span>
<span data-ttu-id="07818-145">Json formázott nyilvános beállítások a bővítményhez.</span><span class="sxs-lookup"><span data-stu-id="07818-145">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesSettings
Parameter Sets: UpdateExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07818-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="07818-146">-SubscriptionId</span></span>
<span data-ttu-id="07818-147">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="07818-147">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="07818-148">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="07818-148">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07818-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="07818-149">-Tag</span></span>
<span data-ttu-id="07818-150">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="07818-150">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07818-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="07818-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="07818-152">A parancsprogram-kezelő verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="07818-152">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07818-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07818-153">-Confirm</span></span>
<span data-ttu-id="07818-154">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="07818-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07818-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07818-155">-WhatIf</span></span>
<span data-ttu-id="07818-156">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="07818-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07818-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="07818-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07818-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07818-158">CommonParameters</span></span>
<span data-ttu-id="07818-159">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07818-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07818-160">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07818-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07818-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07818-161">INPUTS</span></span>

### <span data-ttu-id="07818-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="07818-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="07818-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07818-163">OUTPUTS</span></span>

### <span data-ttu-id="07818-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="07818-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="07818-165">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="07818-165">NOTES</span></span>

<span data-ttu-id="07818-166">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="07818-166">ALIASES</span></span>

<span data-ttu-id="07818-167">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="07818-167">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="07818-168">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="07818-168">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="07818-169">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="07818-169">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="07818-170">EXTENSIONPARAMETER: <IMachineExtension> Egy gépbővítményt ismertet.</span><span class="sxs-lookup"><span data-stu-id="07818-170">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="07818-171">`Location <String>`: Az a földrajzi hely, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="07818-171">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="07818-172">`[Tag <ITrackedResourceTags>]`: Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="07818-172">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="07818-173">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="07818-173">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="07818-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Azt jelzi, hogy a bővítménynek újabb alverziót kell-e használnia, ha elérhető a telepítés során.</span><span class="sxs-lookup"><span data-stu-id="07818-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="07818-175">A telepítés után azonban a bővítmény nem frissíti az alverziókat, hacsak újra nem telepíti őket, még akkor sem, ha a tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="07818-175">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="07818-176">`[ForceUpdateTag <String>]`: Hogyan kell a bővítménykezelőt frissíteni akkor is, ha a bővítmény konfigurációja nem változott meg.</span><span class="sxs-lookup"><span data-stu-id="07818-176">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="07818-177">`[MachineExtensionType <String>]`: A bővítmény típusát határozza meg; példa: "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="07818-177">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="07818-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: A bővítmény tartalmazhat protectedSettings vagy protectedSettingsFromKeyVault beállításokat, vagy egyáltalán nem tartalmazhat védett beállításokat.</span><span class="sxs-lookup"><span data-stu-id="07818-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="07818-179">`[Publisher <String>]`: A bővítménykezelő közzétevője neve.</span><span class="sxs-lookup"><span data-stu-id="07818-179">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="07818-180">`[Setting <IMachineExtensionPropertiesSettings>]`: A bővítmény Json által formázott nyilvános beállításai.</span><span class="sxs-lookup"><span data-stu-id="07818-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="07818-181">`[TypeHandlerVersion <String>]`: A parancsprogram-kezelő verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="07818-181">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

## <span data-ttu-id="07818-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07818-182">RELATED LINKS</span></span>

