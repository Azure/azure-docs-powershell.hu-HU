---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 97E9FB22-43A8-4D07-AF48-5884E4593CA9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35f3baea7440d58812056999ea4f271acf80b8d4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015446"
---
# <span data-ttu-id="7ab51-101">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="7ab51-101">Set-AzureVMExtension</span></span>

## <span data-ttu-id="7ab51-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ab51-102">SYNOPSIS</span></span>
<span data-ttu-id="7ab51-103">A virtuális gépek erőforrás-bővítményeinek beállítása.</span><span class="sxs-lookup"><span data-stu-id="7ab51-103">Sets resource extensions for virtual machines.</span></span>

## <span data-ttu-id="7ab51-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ab51-104">SYNTAX</span></span>

### <span data-ttu-id="7ab51-105">SetByExtensionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7ab51-105">SetByExtensionName (Default)</span></span>
```
Set-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [[-ReferenceName] <String>] [[-PublicConfiguration] <String>] [[-PrivateConfiguration] <String>] [-Disable]
 [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ab51-106">SetByExtensionNameAndConfigFile</span><span class="sxs-lookup"><span data-stu-id="7ab51-106">SetByExtensionNameAndConfigFile</span></span>
```
Set-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [[-ReferenceName] <String>] [[-PublicConfigPath] <String>] [[-PrivateConfigPath] <String>] [-Disable]
 [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ab51-107">SetByReferenceName</span><span class="sxs-lookup"><span data-stu-id="7ab51-107">SetByReferenceName</span></span>
```
Set-AzureVMExtension [-ReferenceName] <String> [[-PublicConfiguration] <String>]
 [[-PrivateConfiguration] <String>] [-Disable] [-Uninstall] [[-PublicConfigKey] <String>]
 [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7ab51-108">SetByReferenceNameAndConfigFile</span><span class="sxs-lookup"><span data-stu-id="7ab51-108">SetByReferenceNameAndConfigFile</span></span>
```
Set-AzureVMExtension [-ReferenceName] <String> [[-PublicConfigPath] <String>] [[-PrivateConfigPath] <String>]
 [-Disable] [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7ab51-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ab51-109">DESCRIPTION</span></span>
<span data-ttu-id="7ab51-110">A **set-AzureVMExtension** parancsmag a virtuális gépek erőforrás-kiterjesztését állítja be.</span><span class="sxs-lookup"><span data-stu-id="7ab51-110">The **Set-AzureVMExtension** cmdlet sets resource extensions for virtual machines.</span></span>

## <span data-ttu-id="7ab51-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7ab51-111">EXAMPLES</span></span>

### <span data-ttu-id="7ab51-112">Példa 1: virtuális gép létrehozása az alkalmazott erőforrás-kiterjesztésekkel</span><span class="sxs-lookup"><span data-stu-id="7ab51-112">Example 1: Create a virtual machine with resource extensions applied</span></span>
```
PS C:\> $X = New-AzureVMConfig -Name $VM -InstanceSize Small -ImageName $IMG;$X = Add-AzureProvisioningConfig -VM $X -Password $PWD -AdminUsername $USR -Windows;$X = Set-AzureVMExtension -VM $X -ExtensionName $Ext1 -Publisher $Publisher -Version $VER -PublicConfiguration $P1 -PrivateConfiguration $P2;$X = Set-AzureVMExtension -VM $X -ExtensionName $Ext2 -Publisher $Publisher -Version $VER -PublicConfiguration $P3 -PrivateConfiguration $P4;New-AzureVM -Location $LOC -ServiceName $SVC -VM $X;
```

<span data-ttu-id="7ab51-113">Ez a parancs létrehoz egy virtuális gépet az erőforrás-kiterjesztések alkalmazásával.</span><span class="sxs-lookup"><span data-stu-id="7ab51-113">This command creates a virtual machine with resource extensions applied.</span></span>

## <span data-ttu-id="7ab51-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ab51-114">PARAMETERS</span></span>

### <span data-ttu-id="7ab51-115">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="7ab51-115">-Disable</span></span>
<span data-ttu-id="7ab51-116">Jelzi, hogy ez a parancsmag letiltja a bővítmény állapotát.</span><span class="sxs-lookup"><span data-stu-id="7ab51-116">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab51-117">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="7ab51-117">-ExtensionName</span></span>
<span data-ttu-id="7ab51-118">A virtuális gép mellékének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ab51-118">Specifies the extension name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab51-119">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="7ab51-119">-ForceUpdate</span></span>
<span data-ttu-id="7ab51-120">Jelzi, hogy ez a parancsmag újra alkalmazza a konfigurációt, ha a konfiguráció még nincs frissítve.</span><span class="sxs-lookup"><span data-stu-id="7ab51-120">Indicates that this cmdlet re-applies a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab51-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7ab51-121">-InformationAction</span></span>
<span data-ttu-id="7ab51-122">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="7ab51-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7ab51-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7ab51-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7ab51-124">Folytassa</span><span class="sxs-lookup"><span data-stu-id="7ab51-124">Continue</span></span>
- <span data-ttu-id="7ab51-125">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="7ab51-125">Ignore</span></span>
- <span data-ttu-id="7ab51-126">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="7ab51-126">Inquire</span></span>
- <span data-ttu-id="7ab51-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7ab51-127">SilentlyContinue</span></span>
- <span data-ttu-id="7ab51-128">állj</span><span class="sxs-lookup"><span data-stu-id="7ab51-128">Stop</span></span>
- <span data-ttu-id="7ab51-129">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="7ab51-129">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab51-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7ab51-130">-InformationVariable</span></span>
<span data-ttu-id="7ab51-131">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="7ab51-131">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab51-132">-PrivateConfigKey</span><span class="sxs-lookup"><span data-stu-id="7ab51-132">-PrivateConfigKey</span></span>
<span data-ttu-id="7ab51-133">Privát konfigurációs kulcsot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7ab51-133">Specifies a private configuration key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab51-134">-PrivateConfigPath</span><span class="sxs-lookup"><span data-stu-id="7ab51-134">-PrivateConfigPath</span></span>
<span data-ttu-id="7ab51-135">A privát konfiguráció elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ab51-135">Specifies the private configuration path.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionNameAndConfigFile, SetByReferenceNameAndConfigFile
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab51-136">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ab51-136">-PrivateConfiguration</span></span>
<span data-ttu-id="7ab51-137">A privát konfiguráció szövegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ab51-137">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByReferenceName
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab51-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="7ab51-138">-Profile</span></span>
<span data-ttu-id="7ab51-139">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="7ab51-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7ab51-140">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="7ab51-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab51-141">-PublicConfigKey</span><span class="sxs-lookup"><span data-stu-id="7ab51-141">-PublicConfigKey</span></span>
<span data-ttu-id="7ab51-142">A nyilvános konfigurációs kulcsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ab51-142">Specifies the public configuration key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab51-143">-PublicConfigPath</span><span class="sxs-lookup"><span data-stu-id="7ab51-143">-PublicConfigPath</span></span>
<span data-ttu-id="7ab51-144">A nyilvános konfiguráció elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ab51-144">Specifies the public configuration path.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionNameAndConfigFile, SetByReferenceNameAndConfigFile
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab51-145">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ab51-145">-PublicConfiguration</span></span>
<span data-ttu-id="7ab51-146">A nyilvános konfiguráció szövegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ab51-146">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByReferenceName
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab51-147">-Publisher</span><span class="sxs-lookup"><span data-stu-id="7ab51-147">-Publisher</span></span>
<span data-ttu-id="7ab51-148">A bővítmény közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ab51-148">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab51-149">-Hivatkozásnév</span><span class="sxs-lookup"><span data-stu-id="7ab51-149">-ReferenceName</span></span>
<span data-ttu-id="7ab51-150">A kiterjesztés hivatkozási nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ab51-150">Specifies the reference name of the extension.</span></span>

<span data-ttu-id="7ab51-151">Ez egy felhasználó által definiált karakterlánc, amellyel hivatkozhat a bővítményekre.</span><span class="sxs-lookup"><span data-stu-id="7ab51-151">This is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="7ab51-152">Ha a bővítményt első alkalommal hozzáadja a virtuális géphez, meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="7ab51-152">You need to specify it when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="7ab51-153">A későbbi frissítésekhez a kiterjesztés frissítésekor meg kell adnia a korábban használt hivatkozási nevet.</span><span class="sxs-lookup"><span data-stu-id="7ab51-153">For subsequent updates, you need to specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="7ab51-154">A bővítményhez rendelt hivatkozásnév a **Get-AzureVM** parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="7ab51-154">The ReferenceName assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByReferenceName, SetByReferenceNameAndConfigFile
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab51-155">-Uninstall</span><span class="sxs-lookup"><span data-stu-id="7ab51-155">-Uninstall</span></span>
<span data-ttu-id="7ab51-156">Azt jelzi, hogy ez a parancsmag eltávolítja az erőforrás-kiterjesztést a virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="7ab51-156">Indicates that this cmdlet uninstalls the resource extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab51-157">-Verzió</span><span class="sxs-lookup"><span data-stu-id="7ab51-157">-Version</span></span>
<span data-ttu-id="7ab51-158">A bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ab51-158">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab51-159">-VM</span><span class="sxs-lookup"><span data-stu-id="7ab51-159">-VM</span></span>
<span data-ttu-id="7ab51-160">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ab51-160">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab51-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab51-161">CommonParameters</span></span>
<span data-ttu-id="7ab51-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ab51-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ab51-163">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ab51-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ab51-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ab51-164">INPUTS</span></span>

## <span data-ttu-id="7ab51-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ab51-165">OUTPUTS</span></span>

## <span data-ttu-id="7ab51-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ab51-166">NOTES</span></span>

## <span data-ttu-id="7ab51-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ab51-167">RELATED LINKS</span></span>

[<span data-ttu-id="7ab51-168">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="7ab51-168">Get-AzureVMExtension</span></span>](./Get-AzureVMExtension.md)

[<span data-ttu-id="7ab51-169">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="7ab51-169">Remove-AzureVMExtension</span></span>](./Remove-AzureVMExtension.md)

[<span data-ttu-id="7ab51-170">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="7ab51-170">Get-AzureVM</span></span>](./Get-AzureVM.md)


