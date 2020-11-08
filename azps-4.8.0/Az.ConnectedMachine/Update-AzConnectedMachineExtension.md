---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: 95334b4f67685183e499518b068f1003f5bb6547
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024794"
---
# <span data-ttu-id="27188-101">Update-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="27188-101">Update-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="27188-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27188-102">SYNOPSIS</span></span>
<span data-ttu-id="27188-103">A bővítmény létrehozásának vagy frissítésének művelete.</span><span class="sxs-lookup"><span data-stu-id="27188-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="27188-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27188-104">SYNTAX</span></span>

### <span data-ttu-id="27188-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="27188-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="27188-106">Frissítés</span><span class="sxs-lookup"><span data-stu-id="27188-106">Update</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="27188-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="27188-107">UpdateViaIdentity</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="27188-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="27188-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="27188-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="27188-109">DESCRIPTION</span></span>
<span data-ttu-id="27188-110">A bővítmény létrehozásának vagy frissítésének művelete.</span><span class="sxs-lookup"><span data-stu-id="27188-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="27188-111">Példák</span><span class="sxs-lookup"><span data-stu-id="27188-111">EXAMPLES</span></span>

### <span data-ttu-id="27188-112">Példa 1: bővítmény frissítése</span><span class="sxs-lookup"><span data-stu-id="27188-112">Example 1: Update an extension</span></span>
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

<span data-ttu-id="27188-113">Egy adott gépen frissíti a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="27188-113">Updates an extension on a specific machine.</span></span>

### <span data-ttu-id="27188-114">2. példa: a bővítmény frissítése a csővezetéken keresztül megadott helyre</span><span class="sxs-lookup"><span data-stu-id="27188-114">Example 2: Update an extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="27188-115">Frissíti a csővezetéken keresztül átadott bővítményt.</span><span class="sxs-lookup"><span data-stu-id="27188-115">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="27188-116">Itt fogjuk használni a bővítményen keresztül átadott bővítményt, hogy segítsenek az üzemeltetéshez, és a normál paraméterek (például) segítségével megadhatja, hogy mit kívánunk módosítani `-Settings` .</span><span class="sxs-lookup"><span data-stu-id="27188-116">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on and are specifying what we want to change via the normal parameters (like `-Settings`)</span></span>

### <span data-ttu-id="27188-117">3. példa: bővítmény frissítése a csővezetéken keresztül megadott kiterjesztési paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="27188-117">Example 3: Update an extension with extension parameters specified via the pipeline</span></span>
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

<span data-ttu-id="27188-118">Frissíti a csővezetéken keresztül átadott bővítményt.</span><span class="sxs-lookup"><span data-stu-id="27188-118">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="27188-119">Az alábbi lépésekkel a csővezetéken keresztül továbbított bővítményt használjuk, hogy a bővítményen végezze el a kívánt módosításokat.</span><span class="sxs-lookup"><span data-stu-id="27188-119">Here we are using the extension passed in via the pipeline to provide the changes we want to make on the extension.</span></span>
<span data-ttu-id="27188-120">A bővítmény helyét a csővezetéken keresztül nem lehet beolvasni, inkább a szokásos módon (a hibajel paraméterrel) megadott paramétereken keresztül.</span><span class="sxs-lookup"><span data-stu-id="27188-120">The location of the extension is not retrieved via the pipeline but rather via the parameters specified normally (by the splat parameter).</span></span>

### <span data-ttu-id="27188-121">Példa 4: Extension objektum használata a frissítés helyének és paraméterének egyaránt</span><span class="sxs-lookup"><span data-stu-id="27188-121">Example 4: Using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="27188-122">Frissíti a csővezetéken keresztül átadott bővítményt.</span><span class="sxs-lookup"><span data-stu-id="27188-122">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="27188-123">Az alábbi lépésekkel kiderítheti, hogy milyen bővítményt szeretne működtetni a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="27188-123">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on.</span></span>
<span data-ttu-id="27188-124">Ezen kívül a bővítmény objektum paramétereit használjuk a frissítendő adatok megadására.</span><span class="sxs-lookup"><span data-stu-id="27188-124">In addition to that, we are using the parameters of the extension object to specify what to update.</span></span>

## <span data-ttu-id="27188-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27188-125">PARAMETERS</span></span>

### <span data-ttu-id="27188-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27188-126">-AsJob</span></span>
<span data-ttu-id="27188-127">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="27188-127">Run the command as a job</span></span>

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

### <span data-ttu-id="27188-128">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="27188-128">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="27188-129">Azt jelzi, hogy a kiterjesztésnek egy újabb alverziót kell-e használnia, ha a bevezetési időben elérhető.</span><span class="sxs-lookup"><span data-stu-id="27188-129">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="27188-130">Miután telepítette a bővítményt, a bővítmény nem frissíti az alverziókat, hacsak a tulajdonság értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="27188-130">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="27188-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27188-131">-DefaultProfile</span></span>
<span data-ttu-id="27188-132">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27188-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27188-133">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="27188-133">-ExtensionParameter</span></span>
<span data-ttu-id="27188-134">Ez a témakör a számítógép-bővítmények frissítését ismerteti.</span><span class="sxs-lookup"><span data-stu-id="27188-134">Describes a Machine Extension Update.</span></span>
<span data-ttu-id="27188-135">A kivitelezéshez tekintse meg a EXTENSIONPARAMETER tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="27188-135">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="27188-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="27188-136">-ForceRerun</span></span>
<span data-ttu-id="27188-137">A bővítmények konfigurációjának frissítése a bővítmények beállításai között akkor is, ha a bővítmény konfigurációja nem változott.</span><span class="sxs-lookup"><span data-stu-id="27188-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="27188-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27188-138">-InputObject</span></span>
<span data-ttu-id="27188-139">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="27188-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="27188-140">-Számítógépnév</span><span class="sxs-lookup"><span data-stu-id="27188-140">-MachineName</span></span>
<span data-ttu-id="27188-141">Annak a gépnek a neve, ahol a kiterjesztést létre kell tenni vagy frissíteni kell.</span><span class="sxs-lookup"><span data-stu-id="27188-141">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="27188-142">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="27188-142">-Name</span></span>
<span data-ttu-id="27188-143">A gép mellékének neve.</span><span class="sxs-lookup"><span data-stu-id="27188-143">The name of the machine extension.</span></span>

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

### <span data-ttu-id="27188-144">-Várva</span><span class="sxs-lookup"><span data-stu-id="27188-144">-NoWait</span></span>
<span data-ttu-id="27188-145">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="27188-145">Run the command asynchronously</span></span>

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

### <span data-ttu-id="27188-146">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="27188-146">-ProtectedSetting</span></span>
<span data-ttu-id="27188-147">A bővítmény a protectedSettings vagy a protectedSettingsFromKeyVault, illetve a nem védett beállításokat egyaránt tartalmazhatja.</span><span class="sxs-lookup"><span data-stu-id="27188-147">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="27188-148">-Publisher</span><span class="sxs-lookup"><span data-stu-id="27188-148">-Publisher</span></span>
<span data-ttu-id="27188-149">A bővítő kezelő közzétevő neve.</span><span class="sxs-lookup"><span data-stu-id="27188-149">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="27188-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27188-150">-ResourceGroupName</span></span>
<span data-ttu-id="27188-151">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="27188-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="27188-152">-Beállítás</span><span class="sxs-lookup"><span data-stu-id="27188-152">-Setting</span></span>
<span data-ttu-id="27188-153">JSON formázott nyilvános beállítások a bővítményhez.</span><span class="sxs-lookup"><span data-stu-id="27188-153">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="27188-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27188-154">-SubscriptionId</span></span>
<span data-ttu-id="27188-155">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="27188-155">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="27188-156">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="27188-156">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="27188-157">-Címke</span><span class="sxs-lookup"><span data-stu-id="27188-157">-Tag</span></span>
<span data-ttu-id="27188-158">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="27188-158">Resource tags</span></span>

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

### <span data-ttu-id="27188-159">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="27188-159">-Type</span></span>
<span data-ttu-id="27188-160">A kiterjesztés típusát adja meg; egy példa "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="27188-160">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="27188-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="27188-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="27188-162">A parancsfájl-kezelő verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="27188-162">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="27188-163">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="27188-163">-Confirm</span></span>
<span data-ttu-id="27188-164">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="27188-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27188-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27188-165">-WhatIf</span></span>
<span data-ttu-id="27188-166">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="27188-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27188-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="27188-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27188-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27188-168">CommonParameters</span></span>
<span data-ttu-id="27188-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27188-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27188-170">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="27188-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27188-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27188-171">INPUTS</span></span>

### <span data-ttu-id="27188-172">Microsoft. Azure. PowerShell. parancsmagok. ConnectedMachine. modellek. Api20200802. IMachineExtensionUpdate</span><span class="sxs-lookup"><span data-stu-id="27188-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span></span>

### <span data-ttu-id="27188-173">Microsoft. Azure. PowerShell. parancsmagok. ConnectedMachine. models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="27188-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="27188-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27188-174">OUTPUTS</span></span>

### <span data-ttu-id="27188-175">Microsoft. Azure. PowerShell. parancsmagok. ConnectedMachine. modellek. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="27188-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="27188-176">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27188-176">NOTES</span></span>

<span data-ttu-id="27188-177">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="27188-177">ALIASES</span></span>

<span data-ttu-id="27188-178">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="27188-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="27188-179">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="27188-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="27188-180">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="27188-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="27188-181">EXTENSIONPARAMETER <IMachineExtensionUpdate> : a számítógép-bővítmények frissítését ismerteti.</span><span class="sxs-lookup"><span data-stu-id="27188-181">EXTENSIONPARAMETER <IMachineExtensionUpdate>: Describes a Machine Extension Update.</span></span>
  - <span data-ttu-id="27188-182">`[Tag <IUpdateResourceTags>]`: Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="27188-182">`[Tag <IUpdateResourceTags>]`: Resource tags</span></span>
    - <span data-ttu-id="27188-183">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="27188-183">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="27188-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Azt jelzi, hogy a kiterjesztésnek egy újabb alverziót kell-e használnia, ha a bevezetési időben elérhető.</span><span class="sxs-lookup"><span data-stu-id="27188-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="27188-185">Miután telepítette a bővítményt, a bővítmény nem frissíti az alverziókat, hacsak a tulajdonság értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="27188-185">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="27188-186">`[ForceUpdateTag <String>]`: A bővítmények frissítése akkor is szükséges, ha a bővítmény konfigurációja nem változott.</span><span class="sxs-lookup"><span data-stu-id="27188-186">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="27188-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: A bővítmény a protectedSettings vagy a protectedSettingsFromKeyVault, illetve a nem védett beállításokat egyaránt tartalmazhatja.</span><span class="sxs-lookup"><span data-stu-id="27188-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="27188-188">`[Publisher <String>]`: A bővítő-kezelő közzétevő neve.</span><span class="sxs-lookup"><span data-stu-id="27188-188">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="27188-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: JSON formázott nyilvános beállítások a bővítményhez.</span><span class="sxs-lookup"><span data-stu-id="27188-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="27188-190">`[Type <String>]`: A bővítmény típusát adja meg; egy példa "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="27188-190">`[Type <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="27188-191">`[TypeHandlerVersion <String>]`: A parancsfájl-kezelő verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="27188-191">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="27188-192">INPUTOBJECT <IConnectedMachineIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="27188-192">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="27188-193">`[ExtensionName <String>]`: A gép mellékének neve.</span><span class="sxs-lookup"><span data-stu-id="27188-193">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="27188-194">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="27188-194">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="27188-195">`[Name <String>]`: A hibrid gép neve.</span><span class="sxs-lookup"><span data-stu-id="27188-195">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="27188-196">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="27188-196">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="27188-197">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="27188-197">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="27188-198">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="27188-198">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="27188-199">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27188-199">RELATED LINKS</span></span>

