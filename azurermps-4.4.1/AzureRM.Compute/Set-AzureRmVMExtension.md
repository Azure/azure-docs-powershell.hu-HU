---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
ms.openlocfilehash: da46aa0e6518c9a9eb9ebea58962f3da593ad264
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497111"
---
# <span data-ttu-id="224f3-101">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="224f3-101">Set-AzureRmVMExtension</span></span>

## <span data-ttu-id="224f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="224f3-102">SYNOPSIS</span></span>
<span data-ttu-id="224f3-103">Frissíti a bővítmény tulajdonságait, vagy bővítményt ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="224f3-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="224f3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="224f3-104">SYNTAX</span></span>

### <span data-ttu-id="224f3-105">Beállítások (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="224f3-105">Settings (Default)</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="224f3-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="224f3-106">SettingString</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="224f3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="224f3-107">DESCRIPTION</span></span>
<span data-ttu-id="224f3-108">A **set-AzureRmVMExtension** parancsmag frissíti a meglévő virtuálisgép-bővítmények tulajdonságait, vagy bővítményt ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="224f3-108">The **Set-AzureRmVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="224f3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="224f3-109">EXAMPLES</span></span>

### <span data-ttu-id="224f3-110">Példa 1: a beállítások módosítása hash-táblázatokkal</span><span class="sxs-lookup"><span data-stu-id="224f3-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="224f3-111">Az első két parancs a Windows PowerShell szintaxisát használja a kivonatoló táblázatok létrehozásához, majd ezeket a kivonatoló táblázatokat az $Settings és $ProtectedSettings változókba menti.</span><span class="sxs-lookup"><span data-stu-id="224f3-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="224f3-112">További információért írja be a következőt: `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="224f3-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="224f3-113">A második parancs két, korábban létrehozott és változóban tárolt értéket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="224f3-113">The second command includes two values previously created and stored in variables.</span></span>

<span data-ttu-id="224f3-114">A végleges parancs a VirtualMachine22-ban a ResourceGroup11 nevű virtuális gép meghosszabbítását a $Settings és a $ProtectedSettings tartalmának megfelelően módosítja.</span><span class="sxs-lookup"><span data-stu-id="224f3-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="224f3-115">A parancs a közzétevőt és a kiterjesztés típust tartalmazó további szükséges információkat adja meg.</span><span class="sxs-lookup"><span data-stu-id="224f3-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="224f3-116">2. példa: beállítások módosítása karakterláncok használatával</span><span class="sxs-lookup"><span data-stu-id="224f3-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="224f3-117">Az első két parancs beállításokat tartalmazó karakterláncokat hoz létre, majd a $SettingsString és $ProtectedSettingsString változók között tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="224f3-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>

<span data-ttu-id="224f3-118">A végleges parancs a VirtualMachine22-ban a ResourceGroup11 nevű virtuális gép meghosszabbítását a $SettingsString és a $ProtectedSettingsString tartalmának megfelelően módosítja.</span><span class="sxs-lookup"><span data-stu-id="224f3-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="224f3-119">A parancs a közzétevőt és a kiterjesztés típust tartalmazó további szükséges információkat adja meg.</span><span class="sxs-lookup"><span data-stu-id="224f3-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="224f3-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="224f3-120">PARAMETERS</span></span>

### <span data-ttu-id="224f3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="224f3-121">-DefaultProfile</span></span>
<span data-ttu-id="224f3-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="224f3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="224f3-123">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="224f3-123">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="224f3-124">Jelzi, hogy ez a parancsmag megakadályozza, hogy az Azure Guest Agent automatikusan frissítse a bővítményeket egy újabb alverzióra.</span><span class="sxs-lookup"><span data-stu-id="224f3-124">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="224f3-125">Ez a parancsmag alapértelmezés szerint lehetővé teszi a Guest Agent számára a bővítmények frissítését.</span><span class="sxs-lookup"><span data-stu-id="224f3-125">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="224f3-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="224f3-126">-ExtensionType</span></span>
<span data-ttu-id="224f3-127">A bővítmény típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="224f3-127">Specifies the extension type.</span></span>

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

### <span data-ttu-id="224f3-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="224f3-128">-ForceRerun</span></span>
<span data-ttu-id="224f3-129">Azt jelzi, hogy ez a parancsmag a virtuális gép ugyanezt a bővítményét futtatja újra a bővítmény eltávolítása és újratelepítése nélkül.</span><span class="sxs-lookup"><span data-stu-id="224f3-129">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="224f3-130">Az érték tetszőleges karakterlánc lehet, amely az aktuális értéktől eltérő lehet.</span><span class="sxs-lookup"><span data-stu-id="224f3-130">The value can be any string different from the current value.</span></span>

<span data-ttu-id="224f3-131">Ha a forceUpdateTag nem változik, a kezelő továbbra is alkalmazza a nyilvános vagy a védett beállításokra vonatkozó frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="224f3-131">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="224f3-132">-Hely</span><span class="sxs-lookup"><span data-stu-id="224f3-132">-Location</span></span>
<span data-ttu-id="224f3-133">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="224f3-133">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="224f3-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="224f3-134">-Name</span></span>
<span data-ttu-id="224f3-135">A kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="224f3-135">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="224f3-136">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="224f3-136">-ProtectedSettings</span></span>
<span data-ttu-id="224f3-137">A bővítmény privát konfigurációját adja meg kivonatoló táblázatként.</span><span class="sxs-lookup"><span data-stu-id="224f3-137">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="224f3-138">Ez a parancsmag titkosítja a magánjellegű konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="224f3-138">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="224f3-139">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="224f3-139">-ProtectedSettingString</span></span>
<span data-ttu-id="224f3-140">A bővítmény privát konfigurációját adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="224f3-140">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="224f3-141">Ez a parancsmag titkosítja a magánjellegű konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="224f3-141">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="224f3-142">-Publisher</span><span class="sxs-lookup"><span data-stu-id="224f3-142">-Publisher</span></span>
<span data-ttu-id="224f3-143">A bővítmény közzétevőének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="224f3-143">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="224f3-144">A Publisher olyan nevet ad, amikor a Publisher a bővítményt regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="224f3-144">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="224f3-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="224f3-145">-ResourceGroupName</span></span>
<span data-ttu-id="224f3-146">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="224f3-146">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="224f3-147">-Beállítások</span><span class="sxs-lookup"><span data-stu-id="224f3-147">-Settings</span></span>
<span data-ttu-id="224f3-148">A bővítmény nyilvános konfigurációját adja meg ujjlenyomat-táblázatként.</span><span class="sxs-lookup"><span data-stu-id="224f3-148">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="224f3-149">Ez a parancsmag nem titkosítja a nyilvános konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="224f3-149">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="224f3-150">-SettingString</span><span class="sxs-lookup"><span data-stu-id="224f3-150">-SettingString</span></span>
<span data-ttu-id="224f3-151">A bővítmény nyilvános konfigurációját adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="224f3-151">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="224f3-152">Ez a parancsmag nem titkosítja a nyilvános konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="224f3-152">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="224f3-153">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="224f3-153">-TypeHandlerVersion</span></span>
<span data-ttu-id="224f3-154">Annak a bővítménynek a verziószámát adja meg, amelyet a virtuális géphez használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="224f3-154">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="224f3-155">-VMName</span><span class="sxs-lookup"><span data-stu-id="224f3-155">-VMName</span></span>
<span data-ttu-id="224f3-156">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="224f3-156">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="224f3-157">Ez a parancsmag módosítja a virtuális gép kiterjesztését, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="224f3-157">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="224f3-158">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="224f3-158">-Confirm</span></span>
<span data-ttu-id="224f3-159">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="224f3-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="224f3-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="224f3-160">-WhatIf</span></span>
<span data-ttu-id="224f3-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="224f3-161">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="224f3-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="224f3-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="224f3-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="224f3-163">CommonParameters</span></span>
<span data-ttu-id="224f3-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="224f3-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="224f3-165">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="224f3-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="224f3-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="224f3-166">INPUTS</span></span>

## <span data-ttu-id="224f3-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="224f3-167">OUTPUTS</span></span>

## <span data-ttu-id="224f3-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="224f3-168">NOTES</span></span>

## <span data-ttu-id="224f3-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="224f3-169">RELATED LINKS</span></span>

[<span data-ttu-id="224f3-170">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="224f3-170">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="224f3-171">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="224f3-171">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)


