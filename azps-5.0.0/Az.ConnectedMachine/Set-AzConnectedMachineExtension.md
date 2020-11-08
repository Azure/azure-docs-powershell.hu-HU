---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: b136f5194bdc7e0f4b4dfc969564d7ef8476d9bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194442"
---
# <span data-ttu-id="878c6-101">Set-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="878c6-101">Set-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="878c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="878c6-102">SYNOPSIS</span></span>
<span data-ttu-id="878c6-103">A bővítmény létrehozásának vagy frissítésének művelete.</span><span class="sxs-lookup"><span data-stu-id="878c6-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="878c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="878c6-104">SYNTAX</span></span>

### <span data-ttu-id="878c6-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="878c6-105">UpdateExpanded (Default)</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="878c6-106">Frissítés</span><span class="sxs-lookup"><span data-stu-id="878c6-106">Update</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="878c6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="878c6-107">DESCRIPTION</span></span>
<span data-ttu-id="878c6-108">A bővítmény létrehozásának vagy frissítésének művelete.</span><span class="sxs-lookup"><span data-stu-id="878c6-108">The operation to create or update the extension.</span></span>

## <span data-ttu-id="878c6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="878c6-109">EXAMPLES</span></span>

### <span data-ttu-id="878c6-110">1. példa: bővítmény beállítása a számítógépen</span><span class="sxs-lookup"><span data-stu-id="878c6-110">Example 1: Set an extension on a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="878c6-111">Beállítja a számítógépen a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="878c6-111">Sets an extension on a machine.</span></span>

### <span data-ttu-id="878c6-112">2. példa: bővítmény beállítása a csővezetéken keresztül megadott kiterjesztési paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="878c6-112">Example 2: Set an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="878c6-113">Ezzel a beállítással megadhatja, hogy milyen bővítmények jelennek meg a csővezetéken keresztül továbbított objektum által megadott kiterjesztési paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="878c6-113">This sets an extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="878c6-114">Ez nagyszerű, ha egy gép paramétereit egy másik gépre szeretné alkalmazni.</span><span class="sxs-lookup"><span data-stu-id="878c6-114">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

## <span data-ttu-id="878c6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="878c6-115">PARAMETERS</span></span>

### <span data-ttu-id="878c6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="878c6-116">-AsJob</span></span>
<span data-ttu-id="878c6-117">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="878c6-117">Run the command as a job</span></span>

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

### <span data-ttu-id="878c6-118">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="878c6-118">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="878c6-119">Azt jelzi, hogy a kiterjesztésnek egy újabb alverziót kell-e használnia, ha a bevezetési időben elérhető.</span><span class="sxs-lookup"><span data-stu-id="878c6-119">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="878c6-120">Miután telepítette a bővítményt, a bővítmény nem frissíti az alverziókat, hacsak a tulajdonság értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="878c6-120">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="878c6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="878c6-121">-DefaultProfile</span></span>
<span data-ttu-id="878c6-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="878c6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="878c6-123">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="878c6-123">-ExtensionParameter</span></span>
<span data-ttu-id="878c6-124">A gép bővítményét ismerteti.</span><span class="sxs-lookup"><span data-stu-id="878c6-124">Describes a Machine Extension.</span></span>
<span data-ttu-id="878c6-125">A kivitelezéshez tekintse meg a EXTENSIONPARAMETER tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="878c6-125">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="878c6-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="878c6-126">-ExtensionType</span></span>
<span data-ttu-id="878c6-127">A kiterjesztés típusát adja meg; egy példa "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="878c6-127">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="878c6-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="878c6-128">-ForceRerun</span></span>
<span data-ttu-id="878c6-129">A bővítmények konfigurációjának frissítése a bővítmények beállításai között akkor is, ha a bővítmény konfigurációja nem változott.</span><span class="sxs-lookup"><span data-stu-id="878c6-129">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="878c6-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="878c6-130">-Location</span></span>
<span data-ttu-id="878c6-131">Az a földrajzi hely, ahol az erőforrás él</span><span class="sxs-lookup"><span data-stu-id="878c6-131">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="878c6-132">-Számítógépnév</span><span class="sxs-lookup"><span data-stu-id="878c6-132">-MachineName</span></span>
<span data-ttu-id="878c6-133">Annak a gépnek a neve, ahol a kiterjesztést létre kell tenni vagy frissíteni kell.</span><span class="sxs-lookup"><span data-stu-id="878c6-133">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="878c6-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="878c6-134">-Name</span></span>
<span data-ttu-id="878c6-135">A gép mellékének neve.</span><span class="sxs-lookup"><span data-stu-id="878c6-135">The name of the machine extension.</span></span>

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

### <span data-ttu-id="878c6-136">-Várva</span><span class="sxs-lookup"><span data-stu-id="878c6-136">-NoWait</span></span>
<span data-ttu-id="878c6-137">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="878c6-137">Run the command asynchronously</span></span>

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

### <span data-ttu-id="878c6-138">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="878c6-138">-ProtectedSetting</span></span>
<span data-ttu-id="878c6-139">A bővítmény a protectedSettings vagy a protectedSettingsFromKeyVault, illetve a nem védett beállításokat egyaránt tartalmazhatja.</span><span class="sxs-lookup"><span data-stu-id="878c6-139">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="878c6-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="878c6-140">-Publisher</span></span>
<span data-ttu-id="878c6-141">A bővítő kezelő közzétevő neve.</span><span class="sxs-lookup"><span data-stu-id="878c6-141">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="878c6-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="878c6-142">-ResourceGroupName</span></span>
<span data-ttu-id="878c6-143">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="878c6-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="878c6-144">-Beállítás</span><span class="sxs-lookup"><span data-stu-id="878c6-144">-Setting</span></span>
<span data-ttu-id="878c6-145">JSON formázott nyilvános beállítások a bővítményhez.</span><span class="sxs-lookup"><span data-stu-id="878c6-145">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="878c6-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="878c6-146">-SubscriptionId</span></span>
<span data-ttu-id="878c6-147">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="878c6-147">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="878c6-148">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="878c6-148">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="878c6-149">-Címke</span><span class="sxs-lookup"><span data-stu-id="878c6-149">-Tag</span></span>
<span data-ttu-id="878c6-150">Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="878c6-150">Resource tags.</span></span>

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

### <span data-ttu-id="878c6-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="878c6-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="878c6-152">A parancsfájl-kezelő verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="878c6-152">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="878c6-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="878c6-153">-Confirm</span></span>
<span data-ttu-id="878c6-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="878c6-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="878c6-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="878c6-155">-WhatIf</span></span>
<span data-ttu-id="878c6-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="878c6-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="878c6-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="878c6-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="878c6-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="878c6-158">CommonParameters</span></span>
<span data-ttu-id="878c6-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="878c6-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="878c6-160">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="878c6-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="878c6-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="878c6-161">INPUTS</span></span>

### <span data-ttu-id="878c6-162">Microsoft. Azure. PowerShell. parancsmagok. ConnectedMachine. modellek. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="878c6-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="878c6-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="878c6-163">OUTPUTS</span></span>

### <span data-ttu-id="878c6-164">Microsoft. Azure. PowerShell. parancsmagok. ConnectedMachine. modellek. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="878c6-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="878c6-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="878c6-165">NOTES</span></span>

<span data-ttu-id="878c6-166">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="878c6-166">ALIASES</span></span>

<span data-ttu-id="878c6-167">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="878c6-167">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="878c6-168">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="878c6-168">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="878c6-169">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="878c6-169">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="878c6-170">EXTENSIONPARAMETER <IMachineExtension> : a gép kiterjesztését ismerteti.</span><span class="sxs-lookup"><span data-stu-id="878c6-170">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="878c6-171">`Location <String>`: A földrajzi hely, ahol az erőforrás él</span><span class="sxs-lookup"><span data-stu-id="878c6-171">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="878c6-172">`[Tag <ITrackedResourceTags>]`: Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="878c6-172">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="878c6-173">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="878c6-173">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="878c6-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Azt jelzi, hogy a kiterjesztésnek egy újabb alverziót kell-e használnia, ha a bevezetési időben elérhető.</span><span class="sxs-lookup"><span data-stu-id="878c6-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="878c6-175">Miután telepítette a bővítményt, a bővítmény nem frissíti az alverziókat, hacsak a tulajdonság értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="878c6-175">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="878c6-176">`[ForceUpdateTag <String>]`: A bővítmények frissítése akkor is szükséges, ha a bővítmény konfigurációja nem változott.</span><span class="sxs-lookup"><span data-stu-id="878c6-176">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="878c6-177">`[MachineExtensionType <String>]`: A bővítmény típusát adja meg; egy példa "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="878c6-177">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="878c6-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: A bővítmény a protectedSettings vagy a protectedSettingsFromKeyVault, illetve a nem védett beállításokat egyaránt tartalmazhatja.</span><span class="sxs-lookup"><span data-stu-id="878c6-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="878c6-179">`[Publisher <String>]`: A bővítő-kezelő közzétevő neve.</span><span class="sxs-lookup"><span data-stu-id="878c6-179">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="878c6-180">`[Setting <IMachineExtensionPropertiesSettings>]`: JSON formázott nyilvános beállítások a bővítményhez.</span><span class="sxs-lookup"><span data-stu-id="878c6-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="878c6-181">`[TypeHandlerVersion <String>]`: A parancsfájl-kezelő verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="878c6-181">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

## <span data-ttu-id="878c6-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="878c6-182">RELATED LINKS</span></span>

