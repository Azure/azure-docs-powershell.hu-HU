---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/new-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
ms.openlocfilehash: 13095d24bd095e27bac788d0d578bdcdf3e1a0f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480654"
---
# <span data-ttu-id="5d702-101">New-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="5d702-101">New-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="5d702-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d702-102">SYNOPSIS</span></span>
<span data-ttu-id="5d702-103">A bővítmény létrehozásához vagy frissítéséhez szükséges művelet.</span><span class="sxs-lookup"><span data-stu-id="5d702-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="5d702-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5d702-104">SYNTAX</span></span>

### <span data-ttu-id="5d702-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5d702-105">CreateExpanded (Default)</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5d702-106">Létrehozás</span><span class="sxs-lookup"><span data-stu-id="5d702-106">Create</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5d702-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5d702-107">CreateViaIdentity</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtension> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5d702-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5d702-108">CreateViaIdentityExpanded</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> -Location <String>
 [-AutoUpgradeMinorVersion] [-ExtensionType <String>] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>] [-TypeHandlerVersion <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5d702-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5d702-109">DESCRIPTION</span></span>
<span data-ttu-id="5d702-110">A bővítmény létrehozásához vagy frissítéséhez szükséges művelet.</span><span class="sxs-lookup"><span data-stu-id="5d702-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="5d702-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5d702-111">EXAMPLES</span></span>

### <span data-ttu-id="5d702-112">1. példa: Új bővítmény hozzáadása egy géphez</span><span class="sxs-lookup"><span data-stu-id="5d702-112">Example 1: Add a new extension to a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="5d702-113">Bővítményt állít be egy gépen.</span><span class="sxs-lookup"><span data-stu-id="5d702-113">Sets an extension on a machine.</span></span>

### <span data-ttu-id="5d702-114">2. példa: Új bővítmény hozzáadása a folyamaton keresztül megadott bővítményparaméterekkel</span><span class="sxs-lookup"><span data-stu-id="5d702-114">Example 2: Add a new extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="5d702-115">Ez létrehoz egy új bővítményt a folyamaton keresztül átadott objektum által megadott kiterjesztési paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="5d702-115">This creates a new extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="5d702-116">Ez akkor lehet nagyszerű, ha meg szeretné ragadni az egyik gép paramétereit, és egy másik gépre szeretné alkalmazni.</span><span class="sxs-lookup"><span data-stu-id="5d702-116">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

### <span data-ttu-id="5d702-117">3. példa: Új bővítmény hozzáadása a folyamaton keresztül megadott helyekkel</span><span class="sxs-lookup"><span data-stu-id="5d702-117">Example 3: Add a new extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $identity = [Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.ConnectedMachineIdentity]@{
    Id = "/subscriptions/$($SubscriptionId)/resourceGroups/$($ResourceGroupName)/providers/Microsoft.HybridCompute/machines/$MachineName/extensions/$ExtensionName"
}
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> $identity | New-AzConnectedMachineExtension -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="5d702-118">Ez egy új gépbővítményt hoz létre a folyamaton keresztül biztosított identitás használatával.</span><span class="sxs-lookup"><span data-stu-id="5d702-118">This creates a new machine extension using the identity provided via the pipeline.</span></span>
<span data-ttu-id="5d702-119">Ezt valószínűleg nem fogja megtenni, de ez lehetséges.</span><span class="sxs-lookup"><span data-stu-id="5d702-119">You likely won't do this, but it's possible.</span></span>

### <span data-ttu-id="5d702-120">4. példa: Új bővítmény hozzáadása bővítményobjektum használatával a frissítés helyének és paramétereinek felhasználásával</span><span class="sxs-lookup"><span data-stu-id="5d702-120">Example 4: Add a new extension using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $ext = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $ext | New-AzConnectedMachineExtension -ExtensionParameter $ext
```

<span data-ttu-id="5d702-121">Ez egy új gépbővítményt hoz létre a folyamaton keresztül biztosított identitás és a bővítményobjektum által megadott kiterjesztés részletei alapján.</span><span class="sxs-lookup"><span data-stu-id="5d702-121">This creates a new machine extension using the identity provided via the pipeline and the extension details provided by the passed in extension object.</span></span>
<span data-ttu-id="5d702-122">Ezt valószínűleg nem fogja megtenni, de ez lehetséges.</span><span class="sxs-lookup"><span data-stu-id="5d702-122">You likely won't do this, but it's possible.</span></span>

## <span data-ttu-id="5d702-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d702-123">PARAMETERS</span></span>

### <span data-ttu-id="5d702-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d702-124">-AsJob</span></span>
<span data-ttu-id="5d702-125">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="5d702-125">Run the command as a job</span></span>

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

### <span data-ttu-id="5d702-126">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="5d702-126">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="5d702-127">Azt jelzi, hogy a bővítménynek újabb alverziót kell-e használnia, ha elérhető a telepítés során.</span><span class="sxs-lookup"><span data-stu-id="5d702-127">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="5d702-128">A telepítés után azonban a bővítmény nem frissíti az alverziókat, hacsak újra nem telepíti őket, még akkor sem, ha a tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="5d702-128">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d702-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d702-129">-DefaultProfile</span></span>
<span data-ttu-id="5d702-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d702-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d702-131">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="5d702-131">-ExtensionParameter</span></span>
<span data-ttu-id="5d702-132">Gépbővítményt ír le.</span><span class="sxs-lookup"><span data-stu-id="5d702-132">Describes a Machine Extension.</span></span>
<span data-ttu-id="5d702-133">Az EXTENSIONPARAMETER tulajdonságainak létrehozására és a kivonattáblák létrehozására vonatkozó MEGJEGYZÉSEK szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="5d702-133">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d702-134">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="5d702-134">-ExtensionType</span></span>
<span data-ttu-id="5d702-135">A bővítmény típusát határozza meg; példa: "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="5d702-135">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d702-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="5d702-136">-ForceRerun</span></span>
<span data-ttu-id="5d702-137">Hogyan kell a bővítménykezelőt frissíteni akkor is, ha a bővítmény konfigurációja nem változott meg.</span><span class="sxs-lookup"><span data-stu-id="5d702-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d702-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d702-138">-InputObject</span></span>
<span data-ttu-id="5d702-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="5d702-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d702-140">-Location</span><span class="sxs-lookup"><span data-stu-id="5d702-140">-Location</span></span>
<span data-ttu-id="5d702-141">Az a földrajzi hely, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="5d702-141">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d702-142">-MachineName</span><span class="sxs-lookup"><span data-stu-id="5d702-142">-MachineName</span></span>
<span data-ttu-id="5d702-143">Annak a gépnek a neve, ahol létre kell hoznunk vagy frissíteni kell a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="5d702-143">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d702-144">-Name</span><span class="sxs-lookup"><span data-stu-id="5d702-144">-Name</span></span>
<span data-ttu-id="5d702-145">A gépbővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="5d702-145">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d702-146">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5d702-146">-NoWait</span></span>
<span data-ttu-id="5d702-147">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="5d702-147">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5d702-148">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="5d702-148">-ProtectedSetting</span></span>
<span data-ttu-id="5d702-149">A bővítmény tartalmazhat protectedSettings vagy protectedSettingsFromKeyVault beállításokat, vagy egyáltalán nem tartalmazhat védett beállításokat.</span><span class="sxs-lookup"><span data-stu-id="5d702-149">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesProtectedSettings
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d702-150">-Publisher</span><span class="sxs-lookup"><span data-stu-id="5d702-150">-Publisher</span></span>
<span data-ttu-id="5d702-151">A bővítménykezelő közzétevője neve.</span><span class="sxs-lookup"><span data-stu-id="5d702-151">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d702-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d702-152">-ResourceGroupName</span></span>
<span data-ttu-id="5d702-153">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5d702-153">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d702-154">-Beállítás</span><span class="sxs-lookup"><span data-stu-id="5d702-154">-Setting</span></span>
<span data-ttu-id="5d702-155">Json formázott nyilvános beállítások a bővítményhez.</span><span class="sxs-lookup"><span data-stu-id="5d702-155">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesSettings
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d702-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d702-156">-SubscriptionId</span></span>
<span data-ttu-id="5d702-157">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="5d702-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5d702-158">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="5d702-158">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d702-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="5d702-159">-Tag</span></span>
<span data-ttu-id="5d702-160">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="5d702-160">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d702-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="5d702-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="5d702-162">A parancsprogram-kezelő verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="5d702-162">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d702-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d702-163">-Confirm</span></span>
<span data-ttu-id="5d702-164">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5d702-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d702-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d702-165">-WhatIf</span></span>
<span data-ttu-id="5d702-166">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5d702-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d702-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5d702-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d702-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d702-168">CommonParameters</span></span>
<span data-ttu-id="5d702-169">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d702-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d702-170">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d702-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d702-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d702-171">INPUTS</span></span>

### <span data-ttu-id="5d702-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="5d702-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

### <span data-ttu-id="5d702-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="5d702-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="5d702-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d702-174">OUTPUTS</span></span>

### <span data-ttu-id="5d702-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="5d702-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="5d702-176">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5d702-176">NOTES</span></span>

<span data-ttu-id="5d702-177">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="5d702-177">ALIASES</span></span>

<span data-ttu-id="5d702-178">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="5d702-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5d702-179">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="5d702-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5d702-180">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5d702-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5d702-181">EXTENSIONPARAMETER: <IMachineExtension> Egy gépbővítményt ismertet.</span><span class="sxs-lookup"><span data-stu-id="5d702-181">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="5d702-182">`Location <String>`: Az a földrajzi hely, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="5d702-182">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="5d702-183">`[Tag <ITrackedResourceTags>]`: Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="5d702-183">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="5d702-184">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="5d702-184">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="5d702-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Azt jelzi, hogy a bővítménynek újabb alverziót kell-e használnia, ha elérhető a telepítés során.</span><span class="sxs-lookup"><span data-stu-id="5d702-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="5d702-186">A telepítés után azonban a bővítmény nem frissíti az alverziókat, hacsak újra nem telepíti őket, még akkor sem, ha a tulajdonság igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="5d702-186">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="5d702-187">`[ForceUpdateTag <String>]`: Hogyan kell a bővítménykezelőt frissíteni akkor is, ha a bővítmény konfigurációja nem változott meg.</span><span class="sxs-lookup"><span data-stu-id="5d702-187">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="5d702-188">`[MachineExtensionType <String>]`: A bővítmény típusát határozza meg; példa: "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="5d702-188">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="5d702-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: A bővítmény tartalmazhat protectedSettings vagy protectedSettingsFromKeyVault beállításokat, vagy egyáltalán nem tartalmazhat védett beállításokat.</span><span class="sxs-lookup"><span data-stu-id="5d702-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="5d702-190">`[Publisher <String>]`: A bővítménykezelő közzétevője neve.</span><span class="sxs-lookup"><span data-stu-id="5d702-190">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="5d702-191">`[Setting <IMachineExtensionPropertiesSettings>]`: A bővítmény Json által formázott nyilvános beállításai.</span><span class="sxs-lookup"><span data-stu-id="5d702-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="5d702-192">`[TypeHandlerVersion <String>]`: A parancsprogram-kezelő verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="5d702-192">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="5d702-193">INPUTOBJECT: <IConnectedMachineIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="5d702-193">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5d702-194">`[ExtensionName <String>]`: A gépbővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="5d702-194">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="5d702-195">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="5d702-195">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5d702-196">`[Name <String>]`: A hibrid gép neve.</span><span class="sxs-lookup"><span data-stu-id="5d702-196">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="5d702-197">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5d702-197">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="5d702-198">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="5d702-198">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5d702-199">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="5d702-199">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5d702-200">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d702-200">RELATED LINKS</span></span>

