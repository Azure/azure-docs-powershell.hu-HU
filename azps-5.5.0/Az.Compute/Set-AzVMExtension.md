---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: dc19566a9baaee7aa70dc03e5d9effa22df8d758
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204727"
---
# <span data-ttu-id="a8ebf-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a8ebf-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="a8ebf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ebf-103">Frissíti a bővítmény tulajdonságait, vagy hozzáad egy bővítményt egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="a8ebf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a8ebf-104">SYNTAX</span></span>

### <span data-ttu-id="a8ebf-105">Beállítások (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a8ebf-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8ebf-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="a8ebf-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8ebf-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a8ebf-107">DESCRIPTION</span></span>
<span data-ttu-id="a8ebf-108">A **Set-AzVMExtension** parancsmag frissíti a meglévő virtuálisgép-bővítmények tulajdonságait, vagy bővítményt ad egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="a8ebf-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a8ebf-109">EXAMPLES</span></span>

### <span data-ttu-id="a8ebf-110">1. példa: Beállítások módosítása kivonattáblák használatával</span><span class="sxs-lookup"><span data-stu-id="a8ebf-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="a8ebf-111">Az első két parancs a Windows PowerShell szokásos szintaxisát használja a kivonattáblák létrehozásához, majd ezeket a kivonattáblákat a $Settings és $ProtectedSettings tárolja.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="a8ebf-112">További információért írja be a `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="a8ebf-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="a8ebf-113">A második parancs két, korábban létrehozott és változókban tárolt értéket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="a8ebf-114">A végleges parancs módosítja a VirtualMachine22 nevű virtuális gép bővítményét az ResourceGroup11-ben a $Settings és $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="a8ebf-115">A parancs egyéb kötelező információkat is megad, beleértve a közzétevőt és a bővítmény típusát.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="a8ebf-116">2. példa: Beállítások módosítása karakterláncok használatával</span><span class="sxs-lookup"><span data-stu-id="a8ebf-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="a8ebf-117">Az első két parancs olyan karakterláncokat hoz létre, amelyek beállításokat tartalmaznak, majd a változókban $SettingsString $ProtectedSettingsString tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="a8ebf-118">A végleges parancs módosítja a VirtualMachine22 nevű virtuális gép bővítményét az ResourceGroup11-ben a $SettingsString és $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="a8ebf-119">A parancs egyéb kötelező információkat is megad, beleértve a közzétevőt és a bővítmény típusát.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="a8ebf-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8ebf-120">PARAMETERS</span></span>

### <span data-ttu-id="a8ebf-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8ebf-121">-AsJob</span></span>
<span data-ttu-id="a8ebf-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a8ebf-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8ebf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ebf-123">-DefaultProfile</span></span>
<span data-ttu-id="a8ebf-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ebf-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a8ebf-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="a8ebf-126">Ez a parancsmag megakadályozza, hogy az Azure vendégügynök automatikusan frissítse a bővítményeket egy újabb alverzióra.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="a8ebf-127">Ez a parancsmag alapértelmezés szerint lehetővé teszi a vendégügynöknek a bővítmények frissítését.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ebf-128">-EnableAutomaticUpgrade</span><span class="sxs-lookup"><span data-stu-id="a8ebf-128">-EnableAutomaticUpgrade</span></span>
<span data-ttu-id="a8ebf-129">Azt jelzi, hogy a platformnak automatikusan frissítenie kell-e a bővítményt, ha elérhető a bővítmény újabb verziója.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-129">Indicates whether the extension should be automatically upgraded by the platform if there is a newer version of the extension available.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ebf-130">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="a8ebf-130">-ExtensionType</span></span>
<span data-ttu-id="a8ebf-131">A bővítmény típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-131">Specifies the extension type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Type

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ebf-132">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="a8ebf-132">-ForceRerun</span></span>
<span data-ttu-id="a8ebf-133">Azt jelzi, hogy ez a parancsmag a bővítmény eltávolítása és újratelepítése nélkül újrafuttatja ugyanazt a bővítménykonfigurációt a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-133">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="a8ebf-134">Az érték bármilyen karakterlánc lehet, amely nem az aktuális érték.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-134">The value can be any string different from the current value.</span></span>
<span data-ttu-id="a8ebf-135">Ha a forceUpdateTag nem változik, a nyilvános vagy védett beállítások frissítéseit továbbra is alkalmazza a kezelő.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-135">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ebf-136">-Location</span><span class="sxs-lookup"><span data-stu-id="a8ebf-136">-Location</span></span>
<span data-ttu-id="a8ebf-137">A virtuális gép helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-137">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ebf-138">-Name</span><span class="sxs-lookup"><span data-stu-id="a8ebf-138">-Name</span></span>
<span data-ttu-id="a8ebf-139">Egy bővítmény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-139">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ebf-140">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a8ebf-140">-NoWait</span></span>
<span data-ttu-id="a8ebf-141">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-141">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a8ebf-142">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-142">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a8ebf-143">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="a8ebf-143">-ProtectedSettings</span></span>
<span data-ttu-id="a8ebf-144">A bővítmény privát konfigurációját adja meg kivonattáblaként.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-144">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="a8ebf-145">Ez a parancsmag titkosítja a privát konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-145">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ebf-146">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="a8ebf-146">-ProtectedSettingString</span></span>
<span data-ttu-id="a8ebf-147">A bővítmény magánjellegű konfigurációját adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-147">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="a8ebf-148">Ez a parancsmag titkosítja a privát konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-148">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ebf-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a8ebf-149">-Publisher</span></span>
<span data-ttu-id="a8ebf-150">A bővítmény közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-150">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="a8ebf-151">A közzétevő nevet ad, amikor a közzétevő regisztrál egy bővítményt.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-151">The publisher provides a name when the publisher registers an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ebf-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8ebf-152">-ResourceGroupName</span></span>
<span data-ttu-id="a8ebf-153">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-153">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ebf-154">-Beállítások</span><span class="sxs-lookup"><span data-stu-id="a8ebf-154">-Settings</span></span>
<span data-ttu-id="a8ebf-155">A bővítmény nyilvános konfigurációját adja meg kivonattáblaként.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-155">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="a8ebf-156">Ez a parancsmag nem titkosítja a nyilvános konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-156">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ebf-157">-SettingString</span><span class="sxs-lookup"><span data-stu-id="a8ebf-157">-SettingString</span></span>
<span data-ttu-id="a8ebf-158">A bővítmény nyilvános konfigurációját adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-158">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="a8ebf-159">Ez a parancsmag nem titkosítja a nyilvános konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-159">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ebf-160">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a8ebf-160">-TypeHandlerVersion</span></span>
<span data-ttu-id="a8ebf-161">A virtuális géphez használni használt bővítmény verziója.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-161">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ebf-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="a8ebf-162">-VMName</span></span>
<span data-ttu-id="a8ebf-163">Egy virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-163">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="a8ebf-164">Ez a parancsmag módosítja a paraméter által megadott virtuális gép bővítményét.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-164">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ebf-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8ebf-165">-Confirm</span></span>
<span data-ttu-id="a8ebf-166">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ebf-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8ebf-167">-WhatIf</span></span>
<span data-ttu-id="a8ebf-168">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8ebf-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-169">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ebf-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ebf-170">CommonParameters</span></span>
<span data-ttu-id="a8ebf-171">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ebf-172">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8ebf-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ebf-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8ebf-173">INPUTS</span></span>

### <span data-ttu-id="a8ebf-174">System.String</span><span class="sxs-lookup"><span data-stu-id="a8ebf-174">System.String</span></span>

### <span data-ttu-id="a8ebf-175">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a8ebf-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a8ebf-176">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a8ebf-176">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a8ebf-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8ebf-177">OUTPUTS</span></span>

### <span data-ttu-id="a8ebf-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a8ebf-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a8ebf-179">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a8ebf-179">NOTES</span></span>

## <span data-ttu-id="a8ebf-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8ebf-180">RELATED LINKS</span></span>

[<span data-ttu-id="a8ebf-181">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a8ebf-181">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="a8ebf-182">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a8ebf-182">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)


