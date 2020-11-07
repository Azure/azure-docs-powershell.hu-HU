---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: c3637ade50258370c37e559ba5e4befbb677d0b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836649"
---
# <span data-ttu-id="819de-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="819de-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="819de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="819de-102">SYNOPSIS</span></span>
<span data-ttu-id="819de-103">Frissíti a bővítmény tulajdonságait, vagy bővítményt ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="819de-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="819de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="819de-104">SYNTAX</span></span>

### <span data-ttu-id="819de-105">Beállítások (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="819de-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="819de-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="819de-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="819de-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="819de-107">DESCRIPTION</span></span>
<span data-ttu-id="819de-108">A **set-AzVMExtension** parancsmag frissíti a meglévő virtuálisgép-bővítmények tulajdonságait, vagy bővítményt ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="819de-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="819de-109">Példák</span><span class="sxs-lookup"><span data-stu-id="819de-109">EXAMPLES</span></span>

### <span data-ttu-id="819de-110">Példa 1: a beállítások módosítása hash-táblázatokkal</span><span class="sxs-lookup"><span data-stu-id="819de-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="819de-111">Az első két parancs a Windows PowerShell szintaxisát használja a kivonatoló táblázatok létrehozásához, majd ezeket a kivonatoló táblázatokat az $Settings és $ProtectedSettings változókba menti.</span><span class="sxs-lookup"><span data-stu-id="819de-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="819de-112">További információért írja be a következőt: `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="819de-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="819de-113">A második parancs két, korábban létrehozott és változóban tárolt értéket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="819de-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="819de-114">A végleges parancs a VirtualMachine22-ban a ResourceGroup11 nevű virtuális gép meghosszabbítását a $Settings és a $ProtectedSettings tartalmának megfelelően módosítja.</span><span class="sxs-lookup"><span data-stu-id="819de-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="819de-115">A parancs a közzétevőt és a kiterjesztés típust tartalmazó további szükséges információkat adja meg.</span><span class="sxs-lookup"><span data-stu-id="819de-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="819de-116">2. példa: beállítások módosítása karakterláncok használatával</span><span class="sxs-lookup"><span data-stu-id="819de-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="819de-117">Az első két parancs beállításokat tartalmazó karakterláncokat hoz létre, majd a $SettingsString és $ProtectedSettingsString változók között tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="819de-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="819de-118">A végleges parancs a VirtualMachine22-ban a ResourceGroup11 nevű virtuális gép meghosszabbítását a $SettingsString és a $ProtectedSettingsString tartalmának megfelelően módosítja.</span><span class="sxs-lookup"><span data-stu-id="819de-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="819de-119">A parancs a közzétevőt és a kiterjesztés típust tartalmazó további szükséges információkat adja meg.</span><span class="sxs-lookup"><span data-stu-id="819de-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="819de-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="819de-120">PARAMETERS</span></span>

### <span data-ttu-id="819de-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="819de-121">-AsJob</span></span>
<span data-ttu-id="819de-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="819de-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="819de-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="819de-123">-DefaultProfile</span></span>
<span data-ttu-id="819de-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="819de-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="819de-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="819de-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="819de-126">Jelzi, hogy ez a parancsmag megakadályozza, hogy az Azure Guest Agent automatikusan frissítse a bővítményeket egy újabb alverzióra.</span><span class="sxs-lookup"><span data-stu-id="819de-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="819de-127">Ez a parancsmag alapértelmezés szerint lehetővé teszi a Guest Agent számára a bővítmények frissítését.</span><span class="sxs-lookup"><span data-stu-id="819de-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="819de-128">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="819de-128">-ExtensionType</span></span>
<span data-ttu-id="819de-129">A bővítmény típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="819de-129">Specifies the extension type.</span></span>

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

### <span data-ttu-id="819de-130">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="819de-130">-ForceRerun</span></span>
<span data-ttu-id="819de-131">Azt jelzi, hogy ez a parancsmag a virtuális gép ugyanezt a bővítményét futtatja újra a bővítmény eltávolítása és újratelepítése nélkül.</span><span class="sxs-lookup"><span data-stu-id="819de-131">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="819de-132">Az érték tetszőleges karakterlánc lehet, amely az aktuális értéktől eltérő lehet.</span><span class="sxs-lookup"><span data-stu-id="819de-132">The value can be any string different from the current value.</span></span>
<span data-ttu-id="819de-133">Ha a forceUpdateTag nem változik, a kezelő továbbra is alkalmazza a nyilvános vagy a védett beállításokra vonatkozó frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="819de-133">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="819de-134">-Hely</span><span class="sxs-lookup"><span data-stu-id="819de-134">-Location</span></span>
<span data-ttu-id="819de-135">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="819de-135">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="819de-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="819de-136">-Name</span></span>
<span data-ttu-id="819de-137">A kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="819de-137">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="819de-138">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="819de-138">-ProtectedSettings</span></span>
<span data-ttu-id="819de-139">A bővítmény privát konfigurációját adja meg kivonatoló táblázatként.</span><span class="sxs-lookup"><span data-stu-id="819de-139">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="819de-140">Ez a parancsmag titkosítja a magánjellegű konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="819de-140">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="819de-141">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="819de-141">-ProtectedSettingString</span></span>
<span data-ttu-id="819de-142">A bővítmény privát konfigurációját adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="819de-142">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="819de-143">Ez a parancsmag titkosítja a magánjellegű konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="819de-143">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="819de-144">-Publisher</span><span class="sxs-lookup"><span data-stu-id="819de-144">-Publisher</span></span>
<span data-ttu-id="819de-145">A bővítmény közzétevőének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="819de-145">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="819de-146">A Publisher olyan nevet ad, amikor a Publisher a bővítményt regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="819de-146">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="819de-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="819de-147">-ResourceGroupName</span></span>
<span data-ttu-id="819de-148">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="819de-148">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="819de-149">-Beállítások</span><span class="sxs-lookup"><span data-stu-id="819de-149">-Settings</span></span>
<span data-ttu-id="819de-150">A bővítmény nyilvános konfigurációját adja meg ujjlenyomat-táblázatként.</span><span class="sxs-lookup"><span data-stu-id="819de-150">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="819de-151">Ez a parancsmag nem titkosítja a nyilvános konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="819de-151">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="819de-152">-SettingString</span><span class="sxs-lookup"><span data-stu-id="819de-152">-SettingString</span></span>
<span data-ttu-id="819de-153">A bővítmény nyilvános konfigurációját adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="819de-153">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="819de-154">Ez a parancsmag nem titkosítja a nyilvános konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="819de-154">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="819de-155">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="819de-155">-TypeHandlerVersion</span></span>
<span data-ttu-id="819de-156">Annak a bővítménynek a verziószámát adja meg, amelyet a virtuális géphez használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="819de-156">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="819de-157">-VMName</span><span class="sxs-lookup"><span data-stu-id="819de-157">-VMName</span></span>
<span data-ttu-id="819de-158">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="819de-158">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="819de-159">Ez a parancsmag módosítja a virtuális gép kiterjesztését, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="819de-159">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="819de-160">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="819de-160">-Confirm</span></span>
<span data-ttu-id="819de-161">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="819de-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="819de-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="819de-162">-WhatIf</span></span>
<span data-ttu-id="819de-163">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="819de-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="819de-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="819de-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="819de-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="819de-165">CommonParameters</span></span>
<span data-ttu-id="819de-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="819de-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="819de-167">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="819de-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="819de-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="819de-168">INPUTS</span></span>

### <span data-ttu-id="819de-169">System. String</span><span class="sxs-lookup"><span data-stu-id="819de-169">System.String</span></span>

### <span data-ttu-id="819de-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="819de-170">System.Collections.Hashtable</span></span>

### <span data-ttu-id="819de-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="819de-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="819de-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="819de-172">OUTPUTS</span></span>

### <span data-ttu-id="819de-173">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="819de-173">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="819de-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="819de-174">NOTES</span></span>

## <span data-ttu-id="819de-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="819de-175">RELATED LINKS</span></span>

[<span data-ttu-id="819de-176">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="819de-176">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="819de-177">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="819de-177">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)


