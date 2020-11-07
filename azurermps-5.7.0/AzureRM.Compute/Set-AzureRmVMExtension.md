---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
ms.openlocfilehash: 1f758f77fc7162f8110f0e2d5887eadb55d7f7c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672030"
---
# <span data-ttu-id="f7b68-101">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f7b68-101">Set-AzureRmVMExtension</span></span>

## <span data-ttu-id="f7b68-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7b68-102">SYNOPSIS</span></span>
<span data-ttu-id="f7b68-103">Frissíti a bővítmény tulajdonságait, vagy bővítményt ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="f7b68-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7b68-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7b68-104">SYNTAX</span></span>

### <span data-ttu-id="f7b68-105">Beállítások (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f7b68-105">Settings (Default)</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7b68-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="f7b68-106">SettingString</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7b68-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7b68-107">DESCRIPTION</span></span>
<span data-ttu-id="f7b68-108">A **set-AzureRmVMExtension** parancsmag frissíti a meglévő virtuálisgép-bővítmények tulajdonságait, vagy bővítményt ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="f7b68-108">The **Set-AzureRmVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="f7b68-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f7b68-109">EXAMPLES</span></span>

### <span data-ttu-id="f7b68-110">Példa 1: a beállítások módosítása hash-táblázatokkal</span><span class="sxs-lookup"><span data-stu-id="f7b68-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="f7b68-111">Az első két parancs a Windows PowerShell szintaxisát használja a kivonatoló táblázatok létrehozásához, majd ezeket a kivonatoló táblázatokat az $Settings és $ProtectedSettings változókba menti.</span><span class="sxs-lookup"><span data-stu-id="f7b68-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="f7b68-112">További információért írja be a következőt: `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="f7b68-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="f7b68-113">A második parancs két, korábban létrehozott és változóban tárolt értéket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="f7b68-113">The second command includes two values previously created and stored in variables.</span></span>

<span data-ttu-id="f7b68-114">A végleges parancs a VirtualMachine22-ban a ResourceGroup11 nevű virtuális gép meghosszabbítását a $Settings és a $ProtectedSettings tartalmának megfelelően módosítja.</span><span class="sxs-lookup"><span data-stu-id="f7b68-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="f7b68-115">A parancs a közzétevőt és a kiterjesztés típust tartalmazó további szükséges információkat adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7b68-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="f7b68-116">2. példa: beállítások módosítása karakterláncok használatával</span><span class="sxs-lookup"><span data-stu-id="f7b68-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="f7b68-117">Az első két parancs beállításokat tartalmazó karakterláncokat hoz létre, majd a $SettingsString és $ProtectedSettingsString változók között tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="f7b68-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>

<span data-ttu-id="f7b68-118">A végleges parancs a VirtualMachine22-ban a ResourceGroup11 nevű virtuális gép meghosszabbítását a $SettingsString és a $ProtectedSettingsString tartalmának megfelelően módosítja.</span><span class="sxs-lookup"><span data-stu-id="f7b68-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="f7b68-119">A parancs a közzétevőt és a kiterjesztés típust tartalmazó további szükséges információkat adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7b68-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="f7b68-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7b68-120">PARAMETERS</span></span>

### <span data-ttu-id="f7b68-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f7b68-121">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="f7b68-122">Jelzi, hogy ez a parancsmag megakadályozza, hogy az Azure Guest Agent automatikusan frissítse a bővítményeket egy újabb alverzióra.</span><span class="sxs-lookup"><span data-stu-id="f7b68-122">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="f7b68-123">Ez a parancsmag alapértelmezés szerint lehetővé teszi a Guest Agent számára a bővítmények frissítését.</span><span class="sxs-lookup"><span data-stu-id="f7b68-123">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b68-124">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="f7b68-124">-ExtensionType</span></span>
<span data-ttu-id="f7b68-125">A bővítmény típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7b68-125">Specifies the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Type

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b68-126">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="f7b68-126">-ForceRerun</span></span>
<span data-ttu-id="f7b68-127">Azt jelzi, hogy ez a parancsmag a virtuális gép ugyanezt a bővítményét futtatja újra a bővítmény eltávolítása és újratelepítése nélkül.</span><span class="sxs-lookup"><span data-stu-id="f7b68-127">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="f7b68-128">Az érték tetszőleges karakterlánc lehet, amely az aktuális értéktől eltérő lehet.</span><span class="sxs-lookup"><span data-stu-id="f7b68-128">The value can be any string different from the current value.</span></span>

<span data-ttu-id="f7b68-129">Ha a forceUpdateTag nem változik, a kezelő továbbra is alkalmazza a nyilvános vagy a védett beállításokra vonatkozó frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="f7b68-129">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b68-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="f7b68-130">-Location</span></span>
<span data-ttu-id="f7b68-131">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7b68-131">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b68-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f7b68-132">-Name</span></span>
<span data-ttu-id="f7b68-133">A kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7b68-133">Specifies the name of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b68-134">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="f7b68-134">-ProtectedSettings</span></span>
<span data-ttu-id="f7b68-135">A bővítmény privát konfigurációját adja meg kivonatoló táblázatként.</span><span class="sxs-lookup"><span data-stu-id="f7b68-135">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="f7b68-136">Ez a parancsmag titkosítja a magánjellegű konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="f7b68-136">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b68-137">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="f7b68-137">-ProtectedSettingString</span></span>
<span data-ttu-id="f7b68-138">A bővítmény privát konfigurációját adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="f7b68-138">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="f7b68-139">Ez a parancsmag titkosítja a magánjellegű konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="f7b68-139">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b68-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f7b68-140">-Publisher</span></span>
<span data-ttu-id="f7b68-141">A bővítmény közzétevőének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7b68-141">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="f7b68-142">A Publisher olyan nevet ad, amikor a Publisher a bővítményt regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="f7b68-142">The publisher provides a name when the publisher registers an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b68-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7b68-143">-ResourceGroupName</span></span>
<span data-ttu-id="f7b68-144">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7b68-144">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b68-145">-Beállítások</span><span class="sxs-lookup"><span data-stu-id="f7b68-145">-Settings</span></span>
<span data-ttu-id="f7b68-146">A bővítmény nyilvános konfigurációját adja meg ujjlenyomat-táblázatként.</span><span class="sxs-lookup"><span data-stu-id="f7b68-146">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="f7b68-147">Ez a parancsmag nem titkosítja a nyilvános konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="f7b68-147">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b68-148">-SettingString</span><span class="sxs-lookup"><span data-stu-id="f7b68-148">-SettingString</span></span>
<span data-ttu-id="f7b68-149">A bővítmény nyilvános konfigurációját adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="f7b68-149">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="f7b68-150">Ez a parancsmag nem titkosítja a nyilvános konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="f7b68-150">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b68-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f7b68-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="f7b68-152">Annak a bővítménynek a verziószámát adja meg, amelyet a virtuális géphez használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="f7b68-152">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b68-153">-VMName</span><span class="sxs-lookup"><span data-stu-id="f7b68-153">-VMName</span></span>
<span data-ttu-id="f7b68-154">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7b68-154">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f7b68-155">Ez a parancsmag módosítja a virtuális gép kiterjesztését, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="f7b68-155">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b68-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f7b68-156">-Confirm</span></span>
<span data-ttu-id="f7b68-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f7b68-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7b68-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7b68-158">-WhatIf</span></span>
<span data-ttu-id="f7b68-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f7b68-159">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f7b68-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f7b68-160">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7b68-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b68-161">CommonParameters</span></span>
<span data-ttu-id="f7b68-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7b68-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b68-163">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7b68-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b68-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7b68-164">INPUTS</span></span>

### <span data-ttu-id="f7b68-165">Nincs</span><span class="sxs-lookup"><span data-stu-id="f7b68-165">None</span></span>
<span data-ttu-id="f7b68-166">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="f7b68-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f7b68-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7b68-167">OUTPUTS</span></span>

## <span data-ttu-id="f7b68-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7b68-168">NOTES</span></span>

## <span data-ttu-id="f7b68-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7b68-169">RELATED LINKS</span></span>

[<span data-ttu-id="f7b68-170">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f7b68-170">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="f7b68-171">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f7b68-171">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)


