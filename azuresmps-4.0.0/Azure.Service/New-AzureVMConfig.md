---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C6DFD49F-26A5-4199-A844-CA0FC405BEDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f9fc407e2cf7375708fe82253f3d2fb40eb78f60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016197"
---
# <span data-ttu-id="8c27f-101">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="8c27f-101">New-AzureVMConfig</span></span>

## <span data-ttu-id="8c27f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c27f-102">SYNOPSIS</span></span>
<span data-ttu-id="8c27f-103">Azure Virtual Machine Configuration objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="8c27f-103">Creates an Azure virtual machine configuration object.</span></span>

## <span data-ttu-id="8c27f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c27f-104">SYNTAX</span></span>

### <span data-ttu-id="8c27f-105">ImageName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c27f-105">ImageName (Default)</span></span>
```
New-AzureVMConfig [-Name] <String> [-InstanceSize] <String> [[-HostCaching] <String>]
 [[-AvailabilitySetName] <String>] [[-Label] <String>] [-ImageName] <String> [[-MediaLocation] <String>]
 [[-DiskLabel] <String>] [-DisableBootDiagnostics] [-LicenseType <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8c27f-106">DiskName</span><span class="sxs-lookup"><span data-stu-id="8c27f-106">DiskName</span></span>
```
New-AzureVMConfig [-Name] <String> [-InstanceSize] <String> [[-HostCaching] <String>]
 [[-AvailabilitySetName] <String>] [[-Label] <String>] [-DiskName] <String> [-DisableBootDiagnostics]
 [-LicenseType <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8c27f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c27f-107">DESCRIPTION</span></span>
<span data-ttu-id="8c27f-108">A **New-AzureVMConfig** parancsmag létrehoz egy Azure Virtual Machine Configuration objektumot.</span><span class="sxs-lookup"><span data-stu-id="8c27f-108">The **New-AzureVMConfig** cmdlet creates an Azure  virtual machine configuration object.</span></span>
<span data-ttu-id="8c27f-109">Ezzel az objektummal új üzembe helyezheti a rendszert, és új virtuális gépet adhat hozzá egy meglévő példányhoz.</span><span class="sxs-lookup"><span data-stu-id="8c27f-109">You can use this object to perform a new deployment and add a new virtual machine to an existing deployment.</span></span>

## <span data-ttu-id="8c27f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8c27f-110">EXAMPLES</span></span>

### <span data-ttu-id="8c27f-111">Példa 1: a Windows Virtual Machine-konfigurációjának létrehozása</span><span class="sxs-lookup"><span data-stu-id="8c27f-111">Example 1: Create a Windows virtual machine configuration</span></span>
```
PS C:\> $Image = (Get-AzureVMImage)[4].ImageName 
C:\PS> New-AzureVMConfig -Name "MyVM1" -InstanceSize ExtraSmall -ImageName $Image | Add-AzureProvisioningConfig -Windows -Password $AdminPassword | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "Datadisk1" -LUN 0 | New-AzureVM -ServiceName "MySvc1"
```

<span data-ttu-id="8c27f-112">Ez a parancs létrehoz egy Windows Virtual Machine-konfigurációt az operációs rendszer lemezzel, az adatlemezzel és a kiépítési konfigurációval.</span><span class="sxs-lookup"><span data-stu-id="8c27f-112">This command creates a Windows virtual machine configuration with operating system disk, data disk and provisioning configuration.</span></span>
<span data-ttu-id="8c27f-113">Ezzel a beállítással új virtuális gépet hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="8c27f-113">This configuration is then used to create a new virtual machine.</span></span>

### <span data-ttu-id="8c27f-114">2. példa: virtuális számítógép konfigurációjának létrehozása</span><span class="sxs-lookup"><span data-stu-id="8c27f-114">Example 2: Create a Linux virtual machine configuration</span></span>
```
PS C:\> $Image = (Get-AzureVMImage)[7].ImageName
C:\PS> New-AzureVMConfig -Name "MyVM1" -InstanceSize ExtraSmall -ImageName $Image | Add-AzureProvisioningConfig -Linux -LinuxUser $LinuxUser -Password $AdminPassword | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "Datadisk1" -LUN 0 | New-AzureVM -ServiceName "MySvc1"
```

<span data-ttu-id="8c27f-115">Ez a parancs létrehoz egy új, virtuális számítógép-konfigurációt az operációs rendszer lemezzel, az adatlemezzel és a kiépítési konfigurációval.</span><span class="sxs-lookup"><span data-stu-id="8c27f-115">This command creates a new Linux virtual machine configuration with operating system disk, data disk and provisioning configuration.</span></span>
<span data-ttu-id="8c27f-116">Ezzel a beállítással új virtuális gépet hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="8c27f-116">This configuration is then used to create a new virtual machine.</span></span>

## <span data-ttu-id="8c27f-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c27f-117">PARAMETERS</span></span>

### <span data-ttu-id="8c27f-118">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="8c27f-118">-AvailabilitySetName</span></span>
<span data-ttu-id="8c27f-119">Az elérhetőségi készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c27f-119">Specifies the name of the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c27f-120">-DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="8c27f-120">-DisableBootDiagnostics</span></span>
<span data-ttu-id="8c27f-121">Jelzi, hogy a konfiguráció letiltja a boot diagnosticst.</span><span class="sxs-lookup"><span data-stu-id="8c27f-121">Indicates that the configuration disables boot diagnostics.</span></span>
<span data-ttu-id="8c27f-122">A boot Diagnostics alapértelmezés szerint engedélyezve van a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="8c27f-122">By default, boot diagnostics are enabled on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c27f-123">-DiskLabel</span><span class="sxs-lookup"><span data-stu-id="8c27f-123">-DiskLabel</span></span>
<span data-ttu-id="8c27f-124">Az operációs rendszer lemezének címkéjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c27f-124">Specifies a label for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c27f-125">-DiskName</span><span class="sxs-lookup"><span data-stu-id="8c27f-125">-DiskName</span></span>
<span data-ttu-id="8c27f-126">Az operációs rendszer lemezének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c27f-126">Specifies a name for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: DiskName
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c27f-127">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="8c27f-127">-HostCaching</span></span>
<span data-ttu-id="8c27f-128">Az operációs rendszer merevlemezének állomás-gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c27f-128">Specifies the host caching mode for the operating system disk.</span></span>

<span data-ttu-id="8c27f-129">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="8c27f-129">Valid values are:</span></span>

- <span data-ttu-id="8c27f-130">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8c27f-130">ReadOnly</span></span>
- <span data-ttu-id="8c27f-131">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8c27f-131">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c27f-132">-ImageName</span><span class="sxs-lookup"><span data-stu-id="8c27f-132">-ImageName</span></span>
<span data-ttu-id="8c27f-133">Annak a virtuális gépnek a nevét adja meg, amelyet az operációs rendszer lemezéhez szeretne használni.</span><span class="sxs-lookup"><span data-stu-id="8c27f-133">Specifies the name of the virtual machine image to use for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c27f-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8c27f-134">-InformationAction</span></span>
<span data-ttu-id="8c27f-135">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="8c27f-135">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8c27f-136">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8c27f-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c27f-137">Folytassa</span><span class="sxs-lookup"><span data-stu-id="8c27f-137">Continue</span></span>
- <span data-ttu-id="8c27f-138">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="8c27f-138">Ignore</span></span>
- <span data-ttu-id="8c27f-139">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="8c27f-139">Inquire</span></span>
- <span data-ttu-id="8c27f-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8c27f-140">SilentlyContinue</span></span>
- <span data-ttu-id="8c27f-141">állj</span><span class="sxs-lookup"><span data-stu-id="8c27f-141">Stop</span></span>
- <span data-ttu-id="8c27f-142">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="8c27f-142">Suspend</span></span>

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

### <span data-ttu-id="8c27f-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8c27f-143">-InformationVariable</span></span>
<span data-ttu-id="8c27f-144">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="8c27f-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8c27f-145">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="8c27f-145">-InstanceSize</span></span>
<span data-ttu-id="8c27f-146">A példány méretének meghatározása.</span><span class="sxs-lookup"><span data-stu-id="8c27f-146">Specifies the size of the instance.</span></span>

<span data-ttu-id="8c27f-147">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8c27f-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c27f-148">ExtraSmall</span><span class="sxs-lookup"><span data-stu-id="8c27f-148">ExtraSmall</span></span>
- <span data-ttu-id="8c27f-149">Kisvállalati</span><span class="sxs-lookup"><span data-stu-id="8c27f-149">Small</span></span>
- <span data-ttu-id="8c27f-150">Közepes</span><span class="sxs-lookup"><span data-stu-id="8c27f-150">Medium</span></span>
- <span data-ttu-id="8c27f-151">Nagy</span><span class="sxs-lookup"><span data-stu-id="8c27f-151">Large</span></span>
- <span data-ttu-id="8c27f-152">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="8c27f-152">ExtraLarge</span></span>
- <span data-ttu-id="8c27f-153">A5</span><span class="sxs-lookup"><span data-stu-id="8c27f-153">A5</span></span>
- <span data-ttu-id="8c27f-154">A6</span><span class="sxs-lookup"><span data-stu-id="8c27f-154">A6</span></span>
- <span data-ttu-id="8c27f-155">A7</span><span class="sxs-lookup"><span data-stu-id="8c27f-155">A7</span></span>
- <span data-ttu-id="8c27f-156">A8</span><span class="sxs-lookup"><span data-stu-id="8c27f-156">A8</span></span>
- <span data-ttu-id="8c27f-157">A9</span><span class="sxs-lookup"><span data-stu-id="8c27f-157">A9</span></span>
- <span data-ttu-id="8c27f-158">Basic_A0</span><span class="sxs-lookup"><span data-stu-id="8c27f-158">Basic_A0</span></span>
- <span data-ttu-id="8c27f-159">Basic_A1</span><span class="sxs-lookup"><span data-stu-id="8c27f-159">Basic_A1</span></span>
- <span data-ttu-id="8c27f-160">Basic_A2</span><span class="sxs-lookup"><span data-stu-id="8c27f-160">Basic_A2</span></span>
- <span data-ttu-id="8c27f-161">Basic_A3</span><span class="sxs-lookup"><span data-stu-id="8c27f-161">Basic_A3</span></span>
- <span data-ttu-id="8c27f-162">Basic_A4</span><span class="sxs-lookup"><span data-stu-id="8c27f-162">Basic_A4</span></span>
- <span data-ttu-id="8c27f-163">Standard_D1</span><span class="sxs-lookup"><span data-stu-id="8c27f-163">Standard_D1</span></span>
- <span data-ttu-id="8c27f-164">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="8c27f-164">Standard_D2</span></span>
- <span data-ttu-id="8c27f-165">Standard_D3</span><span class="sxs-lookup"><span data-stu-id="8c27f-165">Standard_D3</span></span>
- <span data-ttu-id="8c27f-166">Standard_D4</span><span class="sxs-lookup"><span data-stu-id="8c27f-166">Standard_D4</span></span>
- <span data-ttu-id="8c27f-167">Standard_D11</span><span class="sxs-lookup"><span data-stu-id="8c27f-167">Standard_D11</span></span>
- <span data-ttu-id="8c27f-168">Standard_D12</span><span class="sxs-lookup"><span data-stu-id="8c27f-168">Standard_D12</span></span>
- <span data-ttu-id="8c27f-169">Standard_D13</span><span class="sxs-lookup"><span data-stu-id="8c27f-169">Standard_D13</span></span>
- <span data-ttu-id="8c27f-170">Standard_D14</span><span class="sxs-lookup"><span data-stu-id="8c27f-170">Standard_D14</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c27f-171">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="8c27f-171">-Label</span></span>
<span data-ttu-id="8c27f-172">A virtuális géphez rendelt címkét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c27f-172">Specifies a label to assign to the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c27f-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8c27f-173">-LicenseType</span></span>
<span data-ttu-id="8c27f-174">A helyszíni licenccel rendelkező képek vagy lemezek licencének típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c27f-174">Specifies the type of license for an image or disk that is licensed on-premises.</span></span>
<span data-ttu-id="8c27f-175">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8c27f-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c27f-176">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="8c27f-176">Windows_Client</span></span>
- <span data-ttu-id="8c27f-177">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="8c27f-177">Windows_Server</span></span> 

<span data-ttu-id="8c27f-178">Ezt a paramétert csak a Windows Server operációs rendszert tartalmazó képek esetén adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c27f-178">Specify this parameter only for images that contain the Windows Server operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c27f-179">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="8c27f-179">-MediaLocation</span></span>
<span data-ttu-id="8c27f-180">Az új virtuális gép Azure-tárterületének helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c27f-180">Specifies the Azure storage location for the new virtual machine disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c27f-181">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8c27f-181">-Name</span></span>
<span data-ttu-id="8c27f-182">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c27f-182">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="8c27f-183">-Profil</span><span class="sxs-lookup"><span data-stu-id="8c27f-183">-Profile</span></span>
<span data-ttu-id="8c27f-184">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="8c27f-184">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8c27f-185">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="8c27f-185">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8c27f-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c27f-186">CommonParameters</span></span>
<span data-ttu-id="8c27f-187">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c27f-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c27f-188">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c27f-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c27f-189">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c27f-189">INPUTS</span></span>

## <span data-ttu-id="8c27f-190">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c27f-190">OUTPUTS</span></span>

## <span data-ttu-id="8c27f-191">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c27f-191">NOTES</span></span>

## <span data-ttu-id="8c27f-192">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c27f-192">RELATED LINKS</span></span>

