---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/new-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
ms.openlocfilehash: 13095d24bd095e27bac788d0d578bdcdf3e1a0f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194449"
---
# <span data-ttu-id="81a74-101">New-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="81a74-101">New-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="81a74-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81a74-102">SYNOPSIS</span></span>
<span data-ttu-id="81a74-103">A bővítmény létrehozásának vagy frissítésének művelete.</span><span class="sxs-lookup"><span data-stu-id="81a74-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="81a74-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81a74-104">SYNTAX</span></span>

### <span data-ttu-id="81a74-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="81a74-105">CreateExpanded (Default)</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="81a74-106">Létrehozása</span><span class="sxs-lookup"><span data-stu-id="81a74-106">Create</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="81a74-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="81a74-107">CreateViaIdentity</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtension> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="81a74-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="81a74-108">CreateViaIdentityExpanded</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> -Location <String>
 [-AutoUpgradeMinorVersion] [-ExtensionType <String>] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>] [-TypeHandlerVersion <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="81a74-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="81a74-109">DESCRIPTION</span></span>
<span data-ttu-id="81a74-110">A bővítmény létrehozásának vagy frissítésének művelete.</span><span class="sxs-lookup"><span data-stu-id="81a74-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="81a74-111">Példák</span><span class="sxs-lookup"><span data-stu-id="81a74-111">EXAMPLES</span></span>

### <span data-ttu-id="81a74-112">1. példa: új bővítmény hozzáadása a géphez</span><span class="sxs-lookup"><span data-stu-id="81a74-112">Example 1: Add a new extension to a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="81a74-113">Beállítja a számítógépen a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="81a74-113">Sets an extension on a machine.</span></span>

### <span data-ttu-id="81a74-114">2. példa: új kiterjesztés hozzáadása a csővezetéken keresztül megadott kiterjesztési paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="81a74-114">Example 2: Add a new extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="81a74-115">Ezzel új bővítményt hoz létre a csővezetéken keresztül továbbított objektum által megadott kiterjesztési paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="81a74-115">This creates a new extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="81a74-116">Ez nagyszerű, ha egy gép paramétereit egy másik gépre szeretné alkalmazni.</span><span class="sxs-lookup"><span data-stu-id="81a74-116">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

### <span data-ttu-id="81a74-117">3. példa: új kiterjesztés hozzáadása a csővezetéken keresztül megadott helyhez</span><span class="sxs-lookup"><span data-stu-id="81a74-117">Example 3: Add a new extension with location specified via the pipeline</span></span>
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

<span data-ttu-id="81a74-118">Ezzel létrehoz egy új számítógép-kiterjesztést a csővezetéken keresztül kapott identitással.</span><span class="sxs-lookup"><span data-stu-id="81a74-118">This creates a new machine extension using the identity provided via the pipeline.</span></span>
<span data-ttu-id="81a74-119">Valószínűleg nem fog megjelenni, de lehetséges.</span><span class="sxs-lookup"><span data-stu-id="81a74-119">You likely won't do this, but it's possible.</span></span>

### <span data-ttu-id="81a74-120">4. példa: új bővítmény hozzáadása egy bővítmény-objektumból a frissítés helyének és paramétereinek a megadásához</span><span class="sxs-lookup"><span data-stu-id="81a74-120">Example 4: Add a new extension using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $ext = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $ext | New-AzConnectedMachineExtension -ExtensionParameter $ext
```

<span data-ttu-id="81a74-121">Ezzel létrehoz egy új számítógép-kiterjesztést a csővezetéken keresztül megadott identitással, valamint az átadott kiterjesztési objektum által megadott kiterjesztési adatokkal.</span><span class="sxs-lookup"><span data-stu-id="81a74-121">This creates a new machine extension using the identity provided via the pipeline and the extension details provided by the passed in extension object.</span></span>
<span data-ttu-id="81a74-122">Valószínűleg nem fog megjelenni, de lehetséges.</span><span class="sxs-lookup"><span data-stu-id="81a74-122">You likely won't do this, but it's possible.</span></span>

## <span data-ttu-id="81a74-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81a74-123">PARAMETERS</span></span>

### <span data-ttu-id="81a74-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81a74-124">-AsJob</span></span>
<span data-ttu-id="81a74-125">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="81a74-125">Run the command as a job</span></span>

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

### <span data-ttu-id="81a74-126">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="81a74-126">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="81a74-127">Azt jelzi, hogy a kiterjesztésnek egy újabb alverziót kell-e használnia, ha a bevezetési időben elérhető.</span><span class="sxs-lookup"><span data-stu-id="81a74-127">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="81a74-128">Miután telepítette a bővítményt, a bővítmény nem frissíti az alverziókat, hacsak a tulajdonság értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="81a74-128">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="81a74-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a74-129">-DefaultProfile</span></span>
<span data-ttu-id="81a74-130">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81a74-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81a74-131">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="81a74-131">-ExtensionParameter</span></span>
<span data-ttu-id="81a74-132">A gép bővítményét ismerteti.</span><span class="sxs-lookup"><span data-stu-id="81a74-132">Describes a Machine Extension.</span></span>
<span data-ttu-id="81a74-133">A kivitelezéshez tekintse meg a EXTENSIONPARAMETER tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="81a74-133">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="81a74-134">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="81a74-134">-ExtensionType</span></span>
<span data-ttu-id="81a74-135">A kiterjesztés típusát adja meg; egy példa "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="81a74-135">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="81a74-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="81a74-136">-ForceRerun</span></span>
<span data-ttu-id="81a74-137">A bővítmények konfigurációjának frissítése a bővítmények beállításai között akkor is, ha a bővítmény konfigurációja nem változott.</span><span class="sxs-lookup"><span data-stu-id="81a74-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="81a74-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81a74-138">-InputObject</span></span>
<span data-ttu-id="81a74-139">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="81a74-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="81a74-140">-Hely</span><span class="sxs-lookup"><span data-stu-id="81a74-140">-Location</span></span>
<span data-ttu-id="81a74-141">Az a földrajzi hely, ahol az erőforrás él</span><span class="sxs-lookup"><span data-stu-id="81a74-141">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="81a74-142">-Számítógépnév</span><span class="sxs-lookup"><span data-stu-id="81a74-142">-MachineName</span></span>
<span data-ttu-id="81a74-143">Annak a gépnek a neve, ahol a kiterjesztést létre kell tenni vagy frissíteni kell.</span><span class="sxs-lookup"><span data-stu-id="81a74-143">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="81a74-144">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="81a74-144">-Name</span></span>
<span data-ttu-id="81a74-145">A gép mellékének neve.</span><span class="sxs-lookup"><span data-stu-id="81a74-145">The name of the machine extension.</span></span>

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

### <span data-ttu-id="81a74-146">-Várva</span><span class="sxs-lookup"><span data-stu-id="81a74-146">-NoWait</span></span>
<span data-ttu-id="81a74-147">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="81a74-147">Run the command asynchronously</span></span>

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

### <span data-ttu-id="81a74-148">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="81a74-148">-ProtectedSetting</span></span>
<span data-ttu-id="81a74-149">A bővítmény a protectedSettings vagy a protectedSettingsFromKeyVault, illetve a nem védett beállításokat egyaránt tartalmazhatja.</span><span class="sxs-lookup"><span data-stu-id="81a74-149">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="81a74-150">-Publisher</span><span class="sxs-lookup"><span data-stu-id="81a74-150">-Publisher</span></span>
<span data-ttu-id="81a74-151">A bővítő kezelő közzétevő neve.</span><span class="sxs-lookup"><span data-stu-id="81a74-151">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="81a74-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81a74-152">-ResourceGroupName</span></span>
<span data-ttu-id="81a74-153">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="81a74-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="81a74-154">-Beállítás</span><span class="sxs-lookup"><span data-stu-id="81a74-154">-Setting</span></span>
<span data-ttu-id="81a74-155">JSON formázott nyilvános beállítások a bővítményhez.</span><span class="sxs-lookup"><span data-stu-id="81a74-155">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="81a74-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81a74-156">-SubscriptionId</span></span>
<span data-ttu-id="81a74-157">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="81a74-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="81a74-158">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="81a74-158">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="81a74-159">-Címke</span><span class="sxs-lookup"><span data-stu-id="81a74-159">-Tag</span></span>
<span data-ttu-id="81a74-160">Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="81a74-160">Resource tags.</span></span>

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

### <span data-ttu-id="81a74-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="81a74-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="81a74-162">A parancsfájl-kezelő verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="81a74-162">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="81a74-163">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="81a74-163">-Confirm</span></span>
<span data-ttu-id="81a74-164">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81a74-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81a74-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81a74-165">-WhatIf</span></span>
<span data-ttu-id="81a74-166">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="81a74-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81a74-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81a74-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81a74-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a74-168">CommonParameters</span></span>
<span data-ttu-id="81a74-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81a74-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a74-170">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="81a74-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a74-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81a74-171">INPUTS</span></span>

### <span data-ttu-id="81a74-172">Microsoft. Azure. PowerShell. parancsmagok. ConnectedMachine. modellek. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="81a74-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

### <span data-ttu-id="81a74-173">Microsoft. Azure. PowerShell. parancsmagok. ConnectedMachine. models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="81a74-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="81a74-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81a74-174">OUTPUTS</span></span>

### <span data-ttu-id="81a74-175">Microsoft. Azure. PowerShell. parancsmagok. ConnectedMachine. modellek. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="81a74-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="81a74-176">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81a74-176">NOTES</span></span>

<span data-ttu-id="81a74-177">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="81a74-177">ALIASES</span></span>

<span data-ttu-id="81a74-178">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="81a74-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="81a74-179">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="81a74-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="81a74-180">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="81a74-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="81a74-181">EXTENSIONPARAMETER <IMachineExtension> : a gép kiterjesztését ismerteti.</span><span class="sxs-lookup"><span data-stu-id="81a74-181">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="81a74-182">`Location <String>`: A földrajzi hely, ahol az erőforrás él</span><span class="sxs-lookup"><span data-stu-id="81a74-182">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="81a74-183">`[Tag <ITrackedResourceTags>]`: Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="81a74-183">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="81a74-184">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="81a74-184">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="81a74-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Azt jelzi, hogy a kiterjesztésnek egy újabb alverziót kell-e használnia, ha a bevezetési időben elérhető.</span><span class="sxs-lookup"><span data-stu-id="81a74-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="81a74-186">Miután telepítette a bővítményt, a bővítmény nem frissíti az alverziókat, hacsak a tulajdonság értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="81a74-186">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="81a74-187">`[ForceUpdateTag <String>]`: A bővítmények frissítése akkor is szükséges, ha a bővítmény konfigurációja nem változott.</span><span class="sxs-lookup"><span data-stu-id="81a74-187">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="81a74-188">`[MachineExtensionType <String>]`: A bővítmény típusát adja meg; egy példa "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="81a74-188">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="81a74-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: A bővítmény a protectedSettings vagy a protectedSettingsFromKeyVault, illetve a nem védett beállításokat egyaránt tartalmazhatja.</span><span class="sxs-lookup"><span data-stu-id="81a74-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="81a74-190">`[Publisher <String>]`: A bővítő-kezelő közzétevő neve.</span><span class="sxs-lookup"><span data-stu-id="81a74-190">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="81a74-191">`[Setting <IMachineExtensionPropertiesSettings>]`: JSON formázott nyilvános beállítások a bővítményhez.</span><span class="sxs-lookup"><span data-stu-id="81a74-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="81a74-192">`[TypeHandlerVersion <String>]`: A parancsfájl-kezelő verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="81a74-192">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="81a74-193">INPUTOBJECT <IConnectedMachineIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="81a74-193">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="81a74-194">`[ExtensionName <String>]`: A gép mellékének neve.</span><span class="sxs-lookup"><span data-stu-id="81a74-194">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="81a74-195">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="81a74-195">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="81a74-196">`[Name <String>]`: A hibrid gép neve.</span><span class="sxs-lookup"><span data-stu-id="81a74-196">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="81a74-197">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="81a74-197">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="81a74-198">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="81a74-198">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="81a74-199">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="81a74-199">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="81a74-200">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81a74-200">RELATED LINKS</span></span>

