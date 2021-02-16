---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: 95334b4f67685183e499518b068f1003f5bb6547
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144619"
---
# <span data-ttu-id="31773-101">Update-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="31773-101">Update-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="31773-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31773-102">SYNOPSIS</span></span>
<span data-ttu-id="31773-103">A bővítmény létrehozásához vagy frissítéséhez szükséges művelet.</span><span class="sxs-lookup"><span data-stu-id="31773-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="31773-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="31773-104">SYNTAX</span></span>

### <span data-ttu-id="31773-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="31773-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="31773-106">Frissítés</span><span class="sxs-lookup"><span data-stu-id="31773-106">Update</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="31773-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="31773-107">UpdateViaIdentity</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="31773-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="31773-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="31773-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="31773-109">DESCRIPTION</span></span>
<span data-ttu-id="31773-110">A bővítmény létrehozására vagy frissítésére használt művelet.</span><span class="sxs-lookup"><span data-stu-id="31773-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="31773-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="31773-111">EXAMPLES</span></span>

### <span data-ttu-id="31773-112">1. példa: Bővítmény frissítése</span><span class="sxs-lookup"><span data-stu-id="31773-112">Example 1: Update an extension</span></span>
```powershell
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
            Settings = @{
                commandToExecute = "ls -l"
            }
        }
PS C:\> Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="31773-113">Frissíti a bővítményt egy adott gépen.</span><span class="sxs-lookup"><span data-stu-id="31773-113">Updates an extension on a specific machine.</span></span>

### <span data-ttu-id="31773-114">2. példa: Bővítmény frissítése a folyamaton keresztül megadott helyről</span><span class="sxs-lookup"><span data-stu-id="31773-114">Example 2: Update an extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="31773-115">Frissíti a folyamaton keresztül átadott adott bővítményt.</span><span class="sxs-lookup"><span data-stu-id="31773-115">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="31773-116">Itt a folyamaton keresztül átadott bővítményt használjuk annak azonosítására, hogy melyik bővítményen kívánunk működni, és meg szeretnénk adni, hogy mit módosítsunk a normál paramétereken (például ) keresztül. `-Settings`</span><span class="sxs-lookup"><span data-stu-id="31773-116">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on and are specifying what we want to change via the normal parameters (like `-Settings`)</span></span>

### <span data-ttu-id="31773-117">3. példa: Bővítmény frissítése a folyamaton keresztül megadott bővítményparaméterekkel</span><span class="sxs-lookup"><span data-stu-id="31773-117">Example 3: Update an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
        }
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="31773-118">Frissíti a folyamaton keresztül átadott adott bővítményt.</span><span class="sxs-lookup"><span data-stu-id="31773-118">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="31773-119">A folyamaton keresztül átadott bővítményt használjuk a bővítményen végrehajtott módosítások felhasználásával.</span><span class="sxs-lookup"><span data-stu-id="31773-119">Here we are using the extension passed in via the pipeline to provide the changes we want to make on the extension.</span></span>
<span data-ttu-id="31773-120">A bővítmény helyét a program nem a folyamaton keresztül olvassa be, hanem a szokásos módon (a splat paraméterrel) megadott paramétereken keresztül.</span><span class="sxs-lookup"><span data-stu-id="31773-120">The location of the extension is not retrieved via the pipeline but rather via the parameters specified normally (by the splat parameter).</span></span>

### <span data-ttu-id="31773-121">4. példa: Bővítményobjektum használata helyként és paraméterekként a frissítéshez</span><span class="sxs-lookup"><span data-stu-id="31773-121">Example 4: Using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="31773-122">Frissíti a folyamaton keresztül átadott adott bővítményt.</span><span class="sxs-lookup"><span data-stu-id="31773-122">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="31773-123">Itt a folyamaton keresztül átadott bővítményt használjuk annak azonosításához, hogy melyik bővítményen kívánunk működni.</span><span class="sxs-lookup"><span data-stu-id="31773-123">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on.</span></span>
<span data-ttu-id="31773-124">A bővítményobjektum paraméterein kívül a frissíteni kívánt objektumokat is meghatározjuk.</span><span class="sxs-lookup"><span data-stu-id="31773-124">In addition to that, we are using the parameters of the extension object to specify what to update.</span></span>

## <span data-ttu-id="31773-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31773-125">PARAMETERS</span></span>

### <span data-ttu-id="31773-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31773-126">-AsJob</span></span>
<span data-ttu-id="31773-127">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="31773-127">Run the command as a job</span></span>

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

### <span data-ttu-id="31773-128">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="31773-128">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="31773-129">Azt jelzi, hogy a bővítménynek újabb alverziót kell-e használnia, ha elérhető a telepítés során.</span><span class="sxs-lookup"><span data-stu-id="31773-129">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="31773-130">A telepítés után azonban a bővítmény nem frissíti az alverziókat, hacsak újra nem telepíti őket, még akkor sem, ha a tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="31773-130">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31773-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31773-131">-DefaultProfile</span></span>
<span data-ttu-id="31773-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31773-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31773-133">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="31773-133">-ExtensionParameter</span></span>
<span data-ttu-id="31773-134">Gépi bővítmény frissítését ismerteti.</span><span class="sxs-lookup"><span data-stu-id="31773-134">Describes a Machine Extension Update.</span></span>
<span data-ttu-id="31773-135">Az EXTENSIONPARAMETER tulajdonságainak létrehozására és a kivonattáblák létrehozására vonatkozó MEGJEGYZÉSEK szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="31773-135">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31773-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="31773-136">-ForceRerun</span></span>
<span data-ttu-id="31773-137">Hogyan kell a bővítménykezelőt frissíteni akkor is, ha a bővítmény konfigurációja nem változott meg.</span><span class="sxs-lookup"><span data-stu-id="31773-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31773-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31773-138">-InputObject</span></span>
<span data-ttu-id="31773-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="31773-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31773-140">-MachineName</span><span class="sxs-lookup"><span data-stu-id="31773-140">-MachineName</span></span>
<span data-ttu-id="31773-141">Annak a gépnek a neve, ahol létre kell hoznunk vagy frissíteni kell a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="31773-141">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31773-142">-Name</span><span class="sxs-lookup"><span data-stu-id="31773-142">-Name</span></span>
<span data-ttu-id="31773-143">A gépbővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="31773-143">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31773-144">-NoWait</span><span class="sxs-lookup"><span data-stu-id="31773-144">-NoWait</span></span>
<span data-ttu-id="31773-145">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="31773-145">Run the command asynchronously</span></span>

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

### <span data-ttu-id="31773-146">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="31773-146">-ProtectedSetting</span></span>
<span data-ttu-id="31773-147">A bővítmény tartalmazhat protectedSettings vagy protectedSettingsFromKeyVault beállításokat, vagy egyáltalán nem tartalmazhat védett beállításokat.</span><span class="sxs-lookup"><span data-stu-id="31773-147">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesProtectedSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31773-148">-Publisher</span><span class="sxs-lookup"><span data-stu-id="31773-148">-Publisher</span></span>
<span data-ttu-id="31773-149">A bővítménykezelő közzétevője neve.</span><span class="sxs-lookup"><span data-stu-id="31773-149">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31773-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31773-150">-ResourceGroupName</span></span>
<span data-ttu-id="31773-151">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="31773-151">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31773-152">-Beállítás</span><span class="sxs-lookup"><span data-stu-id="31773-152">-Setting</span></span>
<span data-ttu-id="31773-153">A bővítmény json formátumú nyilvános beállításai.</span><span class="sxs-lookup"><span data-stu-id="31773-153">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31773-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31773-154">-SubscriptionId</span></span>
<span data-ttu-id="31773-155">Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="31773-155">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="31773-156">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="31773-156">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31773-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="31773-157">-Tag</span></span>
<span data-ttu-id="31773-158">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="31773-158">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31773-159">-Type</span><span class="sxs-lookup"><span data-stu-id="31773-159">-Type</span></span>
<span data-ttu-id="31773-160">A bővítmény típusát határozza meg; példa: "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="31773-160">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31773-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="31773-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="31773-162">A parancsprogram-kezelő verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="31773-162">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31773-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31773-163">-Confirm</span></span>
<span data-ttu-id="31773-164">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="31773-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31773-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31773-165">-WhatIf</span></span>
<span data-ttu-id="31773-166">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="31773-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31773-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="31773-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31773-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31773-168">CommonParameters</span></span>
<span data-ttu-id="31773-169">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31773-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31773-170">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31773-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31773-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31773-171">INPUTS</span></span>

### <span data-ttu-id="31773-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span><span class="sxs-lookup"><span data-stu-id="31773-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span></span>

### <span data-ttu-id="31773-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="31773-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="31773-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31773-174">OUTPUTS</span></span>

### <span data-ttu-id="31773-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="31773-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="31773-176">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="31773-176">NOTES</span></span>

<span data-ttu-id="31773-177">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="31773-177">ALIASES</span></span>

<span data-ttu-id="31773-178">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="31773-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="31773-179">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="31773-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="31773-180">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="31773-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="31773-181">EXTENSIONPARAMETER: <IMachineExtensionUpdate> Gépi bővítményfrissítést ismertet.</span><span class="sxs-lookup"><span data-stu-id="31773-181">EXTENSIONPARAMETER <IMachineExtensionUpdate>: Describes a Machine Extension Update.</span></span>
  - <span data-ttu-id="31773-182">`[Tag <IUpdateResourceTags>]`: Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="31773-182">`[Tag <IUpdateResourceTags>]`: Resource tags</span></span>
    - <span data-ttu-id="31773-183">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="31773-183">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="31773-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Azt jelzi, hogy a bővítménynek újabb alverziót kell-e használnia, ha elérhető a telepítés során.</span><span class="sxs-lookup"><span data-stu-id="31773-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="31773-185">A telepítés után azonban a bővítmény nem frissíti az alverziókat, hacsak újra nem telepíti őket, még akkor sem, ha a tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="31773-185">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="31773-186">`[ForceUpdateTag <String>]`: Hogyan kell a bővítménykezelőt frissíteni akkor is, ha a bővítmény konfigurációja nem változott meg.</span><span class="sxs-lookup"><span data-stu-id="31773-186">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="31773-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: A bővítmény tartalmazhat protectedSettings vagy protectedSettingsFromKeyVault beállításokat, vagy egyáltalán nem tartalmazhat védett beállításokat.</span><span class="sxs-lookup"><span data-stu-id="31773-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="31773-188">`[Publisher <String>]`: A bővítménykezelő közzétevője neve.</span><span class="sxs-lookup"><span data-stu-id="31773-188">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="31773-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: A bővítmény Json által formázott nyilvános beállításai.</span><span class="sxs-lookup"><span data-stu-id="31773-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="31773-190">`[Type <String>]`: A bővítmény típusát határozza meg; példa: "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="31773-190">`[Type <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="31773-191">`[TypeHandlerVersion <String>]`: A parancsprogram-kezelő verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="31773-191">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="31773-192">INPUTOBJECT: <IConnectedMachineIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="31773-192">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="31773-193">`[ExtensionName <String>]`: A gépbővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="31773-193">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="31773-194">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="31773-194">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="31773-195">`[Name <String>]`: A hibrid gép neve.</span><span class="sxs-lookup"><span data-stu-id="31773-195">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="31773-196">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="31773-196">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="31773-197">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="31773-197">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="31773-198">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="31773-198">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="31773-199">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31773-199">RELATED LINKS</span></span>

