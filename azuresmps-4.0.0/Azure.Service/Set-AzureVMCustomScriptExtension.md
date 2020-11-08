---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6A8F07D1-AC20-4950-9019-BDFB4FD3CF69
online version: ''
schema: 2.0.0
ms.openlocfilehash: a7569e203369bf1177b4eecc2bd689f3e20dcd48
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016037"
---
# <span data-ttu-id="1c270-101">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="1c270-101">Set-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="1c270-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1c270-102">SYNOPSIS</span></span>
<span data-ttu-id="1c270-103">Az Azure Virtual Machine egyéni parancsfájl-bővítményének adatait határozza meg.</span><span class="sxs-lookup"><span data-stu-id="1c270-103">Sets information for an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="1c270-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1c270-104">SYNTAX</span></span>

### <span data-ttu-id="1c270-105">SetCustomScriptExtensionByContainerAndFileNames (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1c270-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-ContainerName] <String>
 [-FileName] <String[]> [[-StorageAccountName] <String>] [[-StorageEndpointSuffix] <String>]
 [[-StorageAccountKey] <String>] [[-Run] <String>] [[-Argument] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c270-106">DisableCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="1c270-106">DisableCustomScriptExtension</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Disable] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1c270-107">UninstalleCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="1c270-107">UninstalleCustomScriptExtension</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Uninstall] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1c270-108">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="1c270-108">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [[-FileUri] <String[]>]
 [-Run] <String> [[-Argument] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1c270-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="1c270-109">DESCRIPTION</span></span>
<span data-ttu-id="1c270-110">A **set-AzureVMCustomScriptExtension** parancsmag az Azure Virtual Machine egyéni parancsfájl-bővítményének adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="1c270-110">The **Set-AzureVMCustomScriptExtension** cmdlet sets information for an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="1c270-111">Példák</span><span class="sxs-lookup"><span data-stu-id="1c270-111">EXAMPLES</span></span>

### <span data-ttu-id="1c270-112">Példa 1: a virtuális gép egyéni parancsfájl-bővítményének beállítása</span><span class="sxs-lookup"><span data-stu-id="1c270-112">Example 1: Set information for a virtual machine custom script extension</span></span>
```
PS C:\> $VM = Set-AzureVMCustomScriptExtension -VM $VM -ContainerName "Container01" -FileName "script1.ps1","script2.ps1" -Run "script1.ps1" -Argument "arg1 arg2";
PS C:\> New-AzureVM -Location "West US" -ServiceName $SVC -VM $VM;
```

<span data-ttu-id="1c270-113">Ez a parancs a virtuális gép egyéni parancsfájl-bővítményének adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="1c270-113">This command sets information for a virtual machine custom script extension.</span></span>

### <span data-ttu-id="1c270-114">2. példa: a virtuális gép egyéni parancsfájl-kiterjesztésére vonatkozó információk beállítása a fájl elérési útján</span><span class="sxs-lookup"><span data-stu-id="1c270-114">Example 2: Set information for a virtual machine custom script extension using a file path</span></span>
```
PS C:\> Set-AzureVMCustomScriptExtension -VM $VM -FileUri "http://www.blob.core.contoso.net/bar/script1.ps1","http://www.blob.core.contoso.net/baz/script2.ps1" -Run "script1.ps1" -Argument "arg1 arg2";
PS C:\> Update-AzureVM -ServiceName $SVC -Name $Name -VM VM;
```

<span data-ttu-id="1c270-115">Ez a parancs a virtuális gép egyéni parancsfájl-kiterjesztésére vonatkozó információkat több fájl URL-címének használatával állítja be.</span><span class="sxs-lookup"><span data-stu-id="1c270-115">This command sets information for a virtual machine custom script extension using multiple file URLs.</span></span>

## <span data-ttu-id="1c270-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1c270-116">PARAMETERS</span></span>

### <span data-ttu-id="1c270-117">-Argumentum</span><span class="sxs-lookup"><span data-stu-id="1c270-117">-Argument</span></span>
<span data-ttu-id="1c270-118">Olyan karakterláncot ad meg, amely egy olyan argumentumot ad meg, amely a parancsmag futását a virtuális gépen futtatja.</span><span class="sxs-lookup"><span data-stu-id="1c270-118">Specifies a string that supplies an argument that this cmdlet runs on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames, SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c270-119">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="1c270-119">-ContainerName</span></span>
<span data-ttu-id="1c270-120">A tároló nevét adja meg a tároló fiókon belül.</span><span class="sxs-lookup"><span data-stu-id="1c270-120">Specifies the container name within the storage account.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c270-121">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="1c270-121">-Disable</span></span>
<span data-ttu-id="1c270-122">Jelzi, hogy ez a parancsmag letiltja a bővítmény állapotát.</span><span class="sxs-lookup"><span data-stu-id="1c270-122">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableCustomScriptExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c270-123">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="1c270-123">-FileName</span></span>
<span data-ttu-id="1c270-124">A megadott tárolóban lévő blob-fájlok nevét tartalmazó karakterlánc-tömböt ad meg.</span><span class="sxs-lookup"><span data-stu-id="1c270-124">Specifies a string array that contains the names of the blob files in the specified container.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c270-125">-FileUri</span><span class="sxs-lookup"><span data-stu-id="1c270-125">-FileUri</span></span>
<span data-ttu-id="1c270-126">A blob-fájlok URL-címét tartalmazó karakterlánc-tömböt ad meg.</span><span class="sxs-lookup"><span data-stu-id="1c270-126">Specifies a string array that contains the URLs of the blob files.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c270-127">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="1c270-127">-ForceUpdate</span></span>
<span data-ttu-id="1c270-128">Azt jelzi, hogy ez a parancsmag újra alkalmazza a konfigurációt a bővítményre, ha a konfiguráció még nincs frissítve.</span><span class="sxs-lookup"><span data-stu-id="1c270-128">Indicates that this cmdlet re-apply a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c270-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1c270-129">-InformationAction</span></span>
<span data-ttu-id="1c270-130">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="1c270-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1c270-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="1c270-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1c270-132">Folytassa</span><span class="sxs-lookup"><span data-stu-id="1c270-132">Continue</span></span>
- <span data-ttu-id="1c270-133">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="1c270-133">Ignore</span></span>
- <span data-ttu-id="1c270-134">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="1c270-134">Inquire</span></span>
- <span data-ttu-id="1c270-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1c270-135">SilentlyContinue</span></span>
- <span data-ttu-id="1c270-136">állj</span><span class="sxs-lookup"><span data-stu-id="1c270-136">Stop</span></span>
- <span data-ttu-id="1c270-137">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="1c270-137">Suspend</span></span>

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

### <span data-ttu-id="1c270-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1c270-138">-InformationVariable</span></span>
<span data-ttu-id="1c270-139">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="1c270-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1c270-140">-Profil</span><span class="sxs-lookup"><span data-stu-id="1c270-140">-Profile</span></span>
<span data-ttu-id="1c270-141">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="1c270-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1c270-142">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="1c270-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1c270-143">-Hivatkozásnév</span><span class="sxs-lookup"><span data-stu-id="1c270-143">-ReferenceName</span></span>
<span data-ttu-id="1c270-144">A kiterjesztés hivatkozási nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c270-144">Specifies the reference name for the extension.</span></span>

<span data-ttu-id="1c270-145">Ez a paraméter egy felhasználó által definiált karakterlánc, amellyel hivatkozhat a bővítményekre.</span><span class="sxs-lookup"><span data-stu-id="1c270-145">This parameter is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="1c270-146">A program akkor adja meg, ha a bővítményt első alkalommal felveszi a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="1c270-146">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="1c270-147">A későbbi frissítésekhez a kiterjesztés frissítésekor meg kell adnia a korábban használt hivatkozási nevet.</span><span class="sxs-lookup"><span data-stu-id="1c270-147">For subsequent updates, you need to specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="1c270-148">A bővítményhez rendelt *hivatkozásnév* a **Get-AzureVM** parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="1c270-148">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c270-149">-Run (Futtatás)</span><span class="sxs-lookup"><span data-stu-id="1c270-149">-Run</span></span>
<span data-ttu-id="1c270-150">Azt a parancsot adja meg, amelyet a parancsmag a virtuális gép bővítménye által futtat.</span><span class="sxs-lookup"><span data-stu-id="1c270-150">Specifies the command this cmdlet runs by the extension on the virtual machine.</span></span>
<span data-ttu-id="1c270-151">Csak a "powershell.exe" támogatott.</span><span class="sxs-lookup"><span data-stu-id="1c270-151">Only "powershell.exe" is supported.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: RunFile, Command

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: RunFile, Command

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c270-152">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="1c270-152">-StorageAccountKey</span></span>
<span data-ttu-id="1c270-153">A tárolási fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c270-153">Specifies the storage account key</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c270-154">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1c270-154">-StorageAccountName</span></span>
<span data-ttu-id="1c270-155">A tárolási fiók nevét adja meg az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="1c270-155">Specifies the storage account name in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c270-156">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1c270-156">-StorageEndpointSuffix</span></span>
<span data-ttu-id="1c270-157">A tárterület-szolgáltatási végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c270-157">Specifies the storage service endpoint.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c270-158">-Uninstall</span><span class="sxs-lookup"><span data-stu-id="1c270-158">-Uninstall</span></span>
<span data-ttu-id="1c270-159">Azt jelzi, hogy ez a parancsmag eltávolítja az egyéni parancsfájl-kiterjesztést a virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="1c270-159">Indicates that this cmdlet uninstalls the custom script extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstalleCustomScriptExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c270-160">-Verzió</span><span class="sxs-lookup"><span data-stu-id="1c270-160">-Version</span></span>
<span data-ttu-id="1c270-161">Az egyéni parancsfájl-kiterjesztés verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c270-161">Specifies the version of the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c270-162">-VM</span><span class="sxs-lookup"><span data-stu-id="1c270-162">-VM</span></span>
<span data-ttu-id="1c270-163">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c270-163">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="1c270-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c270-164">CommonParameters</span></span>
<span data-ttu-id="1c270-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1c270-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c270-166">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c270-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c270-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c270-167">INPUTS</span></span>

## <span data-ttu-id="1c270-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c270-168">OUTPUTS</span></span>

## <span data-ttu-id="1c270-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1c270-169">NOTES</span></span>

## <span data-ttu-id="1c270-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c270-170">RELATED LINKS</span></span>

[<span data-ttu-id="1c270-171">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="1c270-171">Get-AzureVMCustomScriptExtension</span></span>](./Get-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="1c270-172">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="1c270-172">Remove-AzureVMCustomScriptExtension</span></span>](./Remove-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="1c270-173">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="1c270-173">Get-AzureVM</span></span>](./Get-AzureVM.md)


