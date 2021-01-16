---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: babe273e97d2b1b9a1e09959ba252557e2a7e7d0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334241"
---
# <span data-ttu-id="89915-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="89915-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="89915-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89915-102">SYNOPSIS</span></span>
<span data-ttu-id="89915-103">Frissíti a bővítmény tulajdonságait, vagy hozzáad egy bővítményt egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="89915-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="89915-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="89915-104">SYNTAX</span></span>

### <span data-ttu-id="89915-105">Beállítások (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="89915-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89915-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="89915-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89915-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="89915-107">DESCRIPTION</span></span>
<span data-ttu-id="89915-108">A **Set-AzVMExtension** parancsmag frissíti a meglévő virtuálisgép-bővítmények tulajdonságait, vagy bővítményt ad egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="89915-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="89915-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="89915-109">EXAMPLES</span></span>

### <span data-ttu-id="89915-110">1. példa: Beállítások módosítása kivonattáblák használatával</span><span class="sxs-lookup"><span data-stu-id="89915-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="89915-111">Az első két parancs a Windows PowerShell szokásos szintaxisát használja a kivonattáblák létrehozásához, majd ezeket a kivonattáblákat a $Settings és $ProtectedSettings tárolja.</span><span class="sxs-lookup"><span data-stu-id="89915-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="89915-112">További információért írja be a `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="89915-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="89915-113">A második parancs két, korábban létrehozott és változókban tárolt értéket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="89915-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="89915-114">A végleges parancs módosítja a VirtualMachine22 nevű virtuális gép bővítményét az ResourceGroup11-ben a $Settings és $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="89915-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="89915-115">A parancs egyéb kötelező információkat is megad, beleértve a közzétevőt és a bővítmény típusát.</span><span class="sxs-lookup"><span data-stu-id="89915-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="89915-116">2. példa: Beállítások módosítása karakterláncok használatával</span><span class="sxs-lookup"><span data-stu-id="89915-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="89915-117">Az első két parancs olyan karakterláncokat hoz létre, amelyek beállításokat tartalmaznak, majd a változókban $SettingsString $ProtectedSettingsString tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="89915-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="89915-118">A végleges parancs módosítja a VirtualMachine22 nevű virtuális gép bővítményét az ResourceGroup11-ben a $SettingsString és $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="89915-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="89915-119">A parancs egyéb kötelező információkat is megad, beleértve a közzétevőt és a bővítmény típusát.</span><span class="sxs-lookup"><span data-stu-id="89915-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="89915-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89915-120">PARAMETERS</span></span>

### <span data-ttu-id="89915-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89915-121">-AsJob</span></span>
<span data-ttu-id="89915-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="89915-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89915-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89915-123">-DefaultProfile</span></span>
<span data-ttu-id="89915-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89915-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89915-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="89915-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="89915-126">Ez a parancsmag megakadályozza, hogy az Azure vendégügynök automatikusan frissítse a bővítményeket egy újabb alverzióra.</span><span class="sxs-lookup"><span data-stu-id="89915-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="89915-127">Ez a parancsmag alapértelmezés szerint lehetővé teszi a vendégügynöknek a bővítmények frissítését.</span><span class="sxs-lookup"><span data-stu-id="89915-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="89915-128">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="89915-128">-ExtensionType</span></span>
<span data-ttu-id="89915-129">A bővítmény típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="89915-129">Specifies the extension type.</span></span>

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

### <span data-ttu-id="89915-130">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="89915-130">-ForceRerun</span></span>
<span data-ttu-id="89915-131">Azt jelzi, hogy ez a parancsmag a bővítmény eltávolítása és újratelepítése nélkül újrafuttatja ugyanazt a bővítménykonfigurációt a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="89915-131">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="89915-132">Az érték bármilyen karakterlánc lehet, amely nem az aktuális érték.</span><span class="sxs-lookup"><span data-stu-id="89915-132">The value can be any string different from the current value.</span></span>
<span data-ttu-id="89915-133">Ha a forceUpdateTag nem változik, a nyilvános vagy védett beállítások frissítéseit továbbra is alkalmazza a kezelő.</span><span class="sxs-lookup"><span data-stu-id="89915-133">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="89915-134">-Location</span><span class="sxs-lookup"><span data-stu-id="89915-134">-Location</span></span>
<span data-ttu-id="89915-135">A virtuális gép helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="89915-135">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="89915-136">-Name</span><span class="sxs-lookup"><span data-stu-id="89915-136">-Name</span></span>
<span data-ttu-id="89915-137">Egy bővítmény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="89915-137">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="89915-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="89915-138">-NoWait</span></span>
<span data-ttu-id="89915-139">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="89915-139">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="89915-140">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="89915-140">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="89915-141">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="89915-141">-ProtectedSettings</span></span>
<span data-ttu-id="89915-142">A bővítmény privát konfigurációját adja meg kivonattáblaként.</span><span class="sxs-lookup"><span data-stu-id="89915-142">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="89915-143">Ez a parancsmag titkosítja a privát konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="89915-143">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="89915-144">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="89915-144">-ProtectedSettingString</span></span>
<span data-ttu-id="89915-145">A bővítmény magánjellegű konfigurációját adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="89915-145">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="89915-146">Ez a parancsmag titkosítja a privát konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="89915-146">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="89915-147">-Publisher</span><span class="sxs-lookup"><span data-stu-id="89915-147">-Publisher</span></span>
<span data-ttu-id="89915-148">A bővítmény közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="89915-148">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="89915-149">A közzétevő nevet ad, amikor a közzétevő regisztrál egy bővítményt.</span><span class="sxs-lookup"><span data-stu-id="89915-149">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="89915-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89915-150">-ResourceGroupName</span></span>
<span data-ttu-id="89915-151">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="89915-151">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="89915-152">-Beállítások</span><span class="sxs-lookup"><span data-stu-id="89915-152">-Settings</span></span>
<span data-ttu-id="89915-153">A bővítmény nyilvános konfigurációját adja meg kivonattáblaként.</span><span class="sxs-lookup"><span data-stu-id="89915-153">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="89915-154">Ez a parancsmag nem titkosítja a nyilvános konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="89915-154">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="89915-155">-SettingString</span><span class="sxs-lookup"><span data-stu-id="89915-155">-SettingString</span></span>
<span data-ttu-id="89915-156">A bővítmény nyilvános konfigurációját adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="89915-156">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="89915-157">Ez a parancsmag nem titkosítja a nyilvános konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="89915-157">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="89915-158">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="89915-158">-TypeHandlerVersion</span></span>
<span data-ttu-id="89915-159">A bővítménynek a virtuális géphez használt verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="89915-159">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="89915-160">-VMName</span><span class="sxs-lookup"><span data-stu-id="89915-160">-VMName</span></span>
<span data-ttu-id="89915-161">Egy virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="89915-161">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="89915-162">Ez a parancsmag módosítja a paraméter által megadott virtuális gép bővítményét.</span><span class="sxs-lookup"><span data-stu-id="89915-162">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="89915-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89915-163">-Confirm</span></span>
<span data-ttu-id="89915-164">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="89915-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89915-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89915-165">-WhatIf</span></span>
<span data-ttu-id="89915-166">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="89915-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89915-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89915-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89915-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89915-168">CommonParameters</span></span>
<span data-ttu-id="89915-169">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89915-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89915-170">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89915-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89915-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89915-171">INPUTS</span></span>

### <span data-ttu-id="89915-172">System.String</span><span class="sxs-lookup"><span data-stu-id="89915-172">System.String</span></span>

### <span data-ttu-id="89915-173">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="89915-173">System.Collections.Hashtable</span></span>

### <span data-ttu-id="89915-174">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="89915-174">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="89915-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89915-175">OUTPUTS</span></span>

### <span data-ttu-id="89915-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="89915-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="89915-177">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="89915-177">NOTES</span></span>

## <span data-ttu-id="89915-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89915-178">RELATED LINKS</span></span>

[<span data-ttu-id="89915-179">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="89915-179">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="89915-180">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="89915-180">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)


