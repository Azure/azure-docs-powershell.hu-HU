---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FDEDBF4F-7507-43FF-A983-7E431C0C1950
online version: ''
schema: 2.0.0
ms.openlocfilehash: 967fbaf83efa12bd305fc9fe075a9abffdd62dc3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015735"
---
# <span data-ttu-id="42e58-101">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="42e58-101">Add-AzureDataDisk</span></span>

## <span data-ttu-id="42e58-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="42e58-102">SYNOPSIS</span></span>
<span data-ttu-id="42e58-103">Adatlemez felvétele virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="42e58-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="42e58-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="42e58-104">SYNTAX</span></span>

### <span data-ttu-id="42e58-105">CreateNew (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="42e58-105">CreateNew (Default)</span></span>
```
Add-AzureDataDisk [-CreateNew] [-DiskSizeInGB] <Int32> [-DiskLabel] <String> [-LUN] <Int32>
 [-MediaLocation <String>] [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="42e58-106">Importálása</span><span class="sxs-lookup"><span data-stu-id="42e58-106">Import</span></span>
```
Add-AzureDataDisk [-Import] [-DiskName] <String> [-LUN] <Int32> [-HostCaching <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="42e58-107">ImportFrom</span><span class="sxs-lookup"><span data-stu-id="42e58-107">ImportFrom</span></span>
```
Add-AzureDataDisk [-ImportFrom] [-DiskLabel] <String> [-LUN] <Int32> -MediaLocation <String>
 [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="42e58-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="42e58-108">DESCRIPTION</span></span>
<span data-ttu-id="42e58-109">Az **Add-AzureDataDisk** parancsmag új vagy meglévő adatlemezt ad hozzá egy Azure Virtual Machine objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="42e58-109">The **Add-AzureDataDisk** cmdlet adds a new or existing data disk to an Azure virtual machine object.</span></span>
<span data-ttu-id="42e58-110">A *createnew* paraméterrel új adatlemezt hozhat létre, amelyben a megadott méret és címke található.</span><span class="sxs-lookup"><span data-stu-id="42e58-110">Use the *CreateNew* parameter to create a new data disk that has a specified size and label.</span></span>
<span data-ttu-id="42e58-111">Az *importálási* paraméter segítségével egy meglévő lemezt csatolhat a képtárházból.</span><span class="sxs-lookup"><span data-stu-id="42e58-111">Use the *Import* parameter to attach an existing disk from the image repository.</span></span>
<span data-ttu-id="42e58-112">A *ImportFrom* paraméterrel meglévő merevlemezt csatolhat a tároló fiókban lévő blob-fájlokhoz.</span><span class="sxs-lookup"><span data-stu-id="42e58-112">Use the *ImportFrom* parameter to attach an existing disk from a blob in a storage account.</span></span>
<span data-ttu-id="42e58-113">Megadhatja a csatolt adatlemez Host-cache üzemmódját is.</span><span class="sxs-lookup"><span data-stu-id="42e58-113">You can specify the host-cache mode of the attached data disk.</span></span>

## <span data-ttu-id="42e58-114">Példák</span><span class="sxs-lookup"><span data-stu-id="42e58-114">EXAMPLES</span></span>

### <span data-ttu-id="42e58-115">1. példa: adatlemez importálása a tárházból</span><span class="sxs-lookup"><span data-stu-id="42e58-115">Example 1: Import a data disk from the repository</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Add-AzureDataDisk -Import -DiskName "Disk68" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="42e58-116">Ez a parancs a **Get-AzureVM** parancsmag használatával kap egy virtuálisgép-objektumot a VirtualMachine07 nevű virtuális géphez a ContosoService Felhőbeli szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="42e58-116">This command gets a virtual machine object for the virtual machine named VirtualMachine07 in the ContosoService cloud service by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="42e58-117">A parancs a csővezeték-kezelő segítségével átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="42e58-117">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="42e58-118">A parancs egy meglévő adatlemezt csatol a tárházból a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="42e58-118">That command attaches an existing data disk from the repository to the virtual machine.</span></span>
<span data-ttu-id="42e58-119">Az adatlemez 0 logikai egységgel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="42e58-119">The data disk has a LUN of 0.</span></span>
<span data-ttu-id="42e58-120">A parancs frissíti a virtuális gépet a módosítások tükrözéséhez a **Update-AzureVM** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="42e58-120">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

### <span data-ttu-id="42e58-121">2. példa: új adatlemez hozzáadása</span><span class="sxs-lookup"><span data-stu-id="42e58-121">Example 2: Add a new data disk</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine08" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 128 -DiskLabel "main" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="42e58-122">Ez a parancs egy virtuálisgép-objektumot kap a VirtualMachine08 nevű virtuális gépnek.</span><span class="sxs-lookup"><span data-stu-id="42e58-122">This command gets a virtual machine object for the virtual machine named VirtualMachine08.</span></span>
<span data-ttu-id="42e58-123">A parancs átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="42e58-123">The command passes it to the current cmdlet.</span></span>
<span data-ttu-id="42e58-124">A parancs a MyNewDisk. vhd nevű új adatlemezt csatolja.</span><span class="sxs-lookup"><span data-stu-id="42e58-124">That command attaches a new data disk named MyNewDisk.vhd.</span></span>
<span data-ttu-id="42e58-125">A parancsmag a jelenlegi előfizetés alapértelmezett tárolási fiókjában hozza létre a merevlemezt a VHD-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="42e58-125">The cmdlet creates the disk in the vhds container in the default storage account of the current subscription.</span></span>
<span data-ttu-id="42e58-126">A parancs frissíti a virtuális gépet a módosítások tükrözéséhez.</span><span class="sxs-lookup"><span data-stu-id="42e58-126">The command updates the virtual machine to reflect your changes.</span></span>

### <span data-ttu-id="42e58-127">3. példa: adatlemez hozzáadása adott helyről</span><span class="sxs-lookup"><span data-stu-id="42e58-127">Example 3: Add a data disk from a specified location</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "Database" | Add-AzureDataDisk -ImportFrom -MediaLocation "https://contosostorage.blob.core.windows.net/container07/Disk14.vhd" -DiskLabel "main" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="42e58-128">Ez a parancs egy virtuálisgép-objektumot kap az adatbázis nevű virtuális gépnek.</span><span class="sxs-lookup"><span data-stu-id="42e58-128">This command gets a virtual machine object for the virtual machine named Database.</span></span>
<span data-ttu-id="42e58-129">A parancs átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="42e58-129">The command passes it to the current cmdlet.</span></span>
<span data-ttu-id="42e58-130">A parancs egy Disk14. vhd nevű meglévő adatlemezt csatol a megadott helyről.</span><span class="sxs-lookup"><span data-stu-id="42e58-130">That command attaches an existing data disk named Disk14.vhd from the specified location.</span></span>
<span data-ttu-id="42e58-131">A parancs frissíti a virtuális gépet a módosítások tükrözéséhez.</span><span class="sxs-lookup"><span data-stu-id="42e58-131">The command updates the virtual machine to reflect your changes.</span></span>

## <span data-ttu-id="42e58-132">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="42e58-132">PARAMETERS</span></span>

### <span data-ttu-id="42e58-133">-CreateNew</span><span class="sxs-lookup"><span data-stu-id="42e58-133">-CreateNew</span></span>
<span data-ttu-id="42e58-134">Azt jelzi, hogy ez a parancsmag adatlemezt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="42e58-134">Indicates that this cmdlet creates a data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e58-135">-DiskLabel</span><span class="sxs-lookup"><span data-stu-id="42e58-135">-DiskLabel</span></span>
<span data-ttu-id="42e58-136">Egy új adatlemez lemezének címkéjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="42e58-136">Specifies the disk label for a new data disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateNew, ImportFrom
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e58-137">-DiskName</span><span class="sxs-lookup"><span data-stu-id="42e58-137">-DiskName</span></span>
<span data-ttu-id="42e58-138">A lemezkezelő adatlemezének a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="42e58-138">Specifies the name of a data disk in the disk repository.</span></span>

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42e58-139">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="42e58-139">-DiskSizeInGB</span></span>
<span data-ttu-id="42e58-140">A logikai méretet adja meg az új adatlemezhez gigabájtban.</span><span class="sxs-lookup"><span data-stu-id="42e58-140">Specifies the logical disk size, in gigabytes, for a new data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e58-141">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="42e58-141">-HostCaching</span></span>
<span data-ttu-id="42e58-142">Az állomás szintű gyorsítótár-beállításokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="42e58-142">Specifies the host level caching settings of the disk.</span></span>
<span data-ttu-id="42e58-143">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="42e58-143">Valid values are:</span></span> 

- <span data-ttu-id="42e58-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="42e58-144">None</span></span> 
- <span data-ttu-id="42e58-145">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="42e58-145">ReadOnly</span></span> 
- <span data-ttu-id="42e58-146">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="42e58-146">ReadWrite</span></span>

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

### <span data-ttu-id="42e58-147">-Import</span><span class="sxs-lookup"><span data-stu-id="42e58-147">-Import</span></span>
<span data-ttu-id="42e58-148">Jelzi, hogy ez a parancsmag egy meglévő adatlemezt importál a képtárházból.</span><span class="sxs-lookup"><span data-stu-id="42e58-148">Indicates that this cmdlet imports an existing data disk from the image repository.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Import
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e58-149">-ImportFrom</span><span class="sxs-lookup"><span data-stu-id="42e58-149">-ImportFrom</span></span>
<span data-ttu-id="42e58-150">Azt jelzi, hogy ez a parancsmag egy meglévő adatlemezt importál egy tárolóban lévő blobból.</span><span class="sxs-lookup"><span data-stu-id="42e58-150">Indicates that this cmdlet imports an existing data disk from a blob in a storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e58-151">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="42e58-151">-InformationAction</span></span>
<span data-ttu-id="42e58-152">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="42e58-152">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="42e58-153">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="42e58-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="42e58-154">Folytassa</span><span class="sxs-lookup"><span data-stu-id="42e58-154">Continue</span></span>
- <span data-ttu-id="42e58-155">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="42e58-155">Ignore</span></span>
- <span data-ttu-id="42e58-156">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="42e58-156">Inquire</span></span>
- <span data-ttu-id="42e58-157">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="42e58-157">SilentlyContinue</span></span>
- <span data-ttu-id="42e58-158">állj</span><span class="sxs-lookup"><span data-stu-id="42e58-158">Stop</span></span>
- <span data-ttu-id="42e58-159">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="42e58-159">Suspend</span></span>

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

### <span data-ttu-id="42e58-160">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="42e58-160">-InformationVariable</span></span>
<span data-ttu-id="42e58-161">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="42e58-161">Specifies an information variable.</span></span>

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

### <span data-ttu-id="42e58-162">-LUN</span><span class="sxs-lookup"><span data-stu-id="42e58-162">-LUN</span></span>
<span data-ttu-id="42e58-163">Annak a logikai egységnek a logikai egység számát adja meg, amely a virtuális gép adatmeghajtójának logikai egysége.</span><span class="sxs-lookup"><span data-stu-id="42e58-163">Specifies the logical unit number (LUN) for the data drive in the virtual machine.</span></span>
<span data-ttu-id="42e58-164">Az érvényes értékek a következők: 0 – 15.</span><span class="sxs-lookup"><span data-stu-id="42e58-164">Valid values are: 0 through 15.</span></span>
<span data-ttu-id="42e58-165">Az egyes adatlemezeknek egyedi logikai egységgel kell rendelkezniük.</span><span class="sxs-lookup"><span data-stu-id="42e58-165">Each data disk must have a unique LUN.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e58-166">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="42e58-166">-MediaLocation</span></span>
<span data-ttu-id="42e58-167">Megadja a blob helyét az Azure Storage-fiókban, ahol ez a parancsmag tárolja az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="42e58-167">Specifies the location of the blob in an Azure storage account where this cmdlet stores the data disk.</span></span>
<span data-ttu-id="42e58-168">Ha nem ad meg helyet, a parancsmag az aktuális előfizetés alapértelmezett tárolási fiókjának VHD-tárolójában tárolja az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="42e58-168">If you do not specify a location, the cmdlet stores the data disk in the vhds container in the default storage account for the current subscription.</span></span>
<span data-ttu-id="42e58-169">Ha egy VHD-tároló nem létezik, a parancsmag létrehoz egy VHD-tárolót.</span><span class="sxs-lookup"><span data-stu-id="42e58-169">If a vhds container does not exist, the cmdlet creates a vhds container.</span></span>

```yaml
Type: String
Parameter Sets: CreateNew
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42e58-170">-Profil</span><span class="sxs-lookup"><span data-stu-id="42e58-170">-Profile</span></span>
<span data-ttu-id="42e58-171">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="42e58-171">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="42e58-172">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="42e58-172">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="42e58-173">-VM</span><span class="sxs-lookup"><span data-stu-id="42e58-173">-VM</span></span>
<span data-ttu-id="42e58-174">Annak a virtuális gépnek az objektumát adja meg, amelyre a parancsmag adatlemezt csatol.</span><span class="sxs-lookup"><span data-stu-id="42e58-174">Specifies the virtual machine object to which this cmdlet attaches a data disk.</span></span>
<span data-ttu-id="42e58-175">Virtuális gép objektum beszerzéséhez használja a **Get-AzureVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="42e58-175">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="42e58-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42e58-176">CommonParameters</span></span>
<span data-ttu-id="42e58-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="42e58-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42e58-178">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42e58-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42e58-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="42e58-179">INPUTS</span></span>

## <span data-ttu-id="42e58-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42e58-180">OUTPUTS</span></span>

## <span data-ttu-id="42e58-181">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="42e58-181">NOTES</span></span>

## <span data-ttu-id="42e58-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42e58-182">RELATED LINKS</span></span>

[<span data-ttu-id="42e58-183">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="42e58-183">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="42e58-184">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="42e58-184">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="42e58-185">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="42e58-185">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="42e58-186">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="42e58-186">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="42e58-187">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="42e58-187">Update-AzureVM</span></span>](./Update-AzureVM.md)


