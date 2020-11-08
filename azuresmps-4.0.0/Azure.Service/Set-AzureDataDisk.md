---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 64EF867E-5142-4317-9552-8BC94117208D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 899ecd0256bc3d6f88b8f942fa488db444a9bb41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016066"
---
# <span data-ttu-id="52361-101">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="52361-101">Set-AzureDataDisk</span></span>

## <span data-ttu-id="52361-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="52361-102">SYNOPSIS</span></span>
<span data-ttu-id="52361-103">Módosítja egy meglévő adatlemez gyorsítótárát egy Azure virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="52361-103">Modifies the host caching of an existing data disk on an Azure virtual machine.</span></span>

## <span data-ttu-id="52361-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="52361-104">SYNTAX</span></span>

### <span data-ttu-id="52361-105">Átméretezés</span><span class="sxs-lookup"><span data-stu-id="52361-105">NoResize</span></span>
```
Set-AzureDataDisk [-HostCaching] <String> [-LUN] <Int32> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="52361-106">Átméretezése</span><span class="sxs-lookup"><span data-stu-id="52361-106">Resize</span></span>
```
Set-AzureDataDisk [-DiskName] <String> [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="52361-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="52361-107">DESCRIPTION</span></span>
<span data-ttu-id="52361-108">A **set-AzureDataDisk** parancsmag módosította egy meglévő adatlemez gyorsítótár-attribútumait egy Azure virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="52361-108">The **Set-AzureDataDisk** cmdlet modifies the cache attributes of an existing data disk on an Azure virtual machine.</span></span>
<span data-ttu-id="52361-109">Adja meg, hogy melyik adatlemezen frissüljön a logikai egység száma (LUN).</span><span class="sxs-lookup"><span data-stu-id="52361-109">Specify which data disk to update by its logical unit number (LUN).</span></span>

## <span data-ttu-id="52361-110">Példák</span><span class="sxs-lookup"><span data-stu-id="52361-110">EXAMPLES</span></span>

### <span data-ttu-id="52361-111">Példa 1: az állomás gyorsítótárának módosítása adatlemezhez</span><span class="sxs-lookup"><span data-stu-id="52361-111">Example 1: Modify the host caching for a data disk</span></span>
```
PS C:\> Get-AzureVM "ContosoService" | Set-AzureDataDisk -VM "VirtualMachine07" -LUN 2 -HostCaching ReadOnly | Update-AzureVM
```

<span data-ttu-id="52361-112">Ez a parancs a **Get-AzureVM** parancsmag segítségével a ContosoService nevű szolgáltatáson futó virtuális gépeket kapja.</span><span class="sxs-lookup"><span data-stu-id="52361-112">This command gets the virtual machines that run on the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="52361-113">A parancs a csővezeték-kezelő segítségével átadja őket az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="52361-113">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="52361-114">Ez a parancsmag a VirtualMachine07 nevű virtuális gép 2-es verziójában lévő adatlemezt állítja be a ReadOnly-Host gyorsítótárazási szolgáltatás használatára.</span><span class="sxs-lookup"><span data-stu-id="52361-114">That cmdlet sets the data disk at LUN 2 of the virtual machine named VirtualMachine07 to use ReadOnly host caching.</span></span>
<span data-ttu-id="52361-115">A parancs frissíti a virtuális gépet a módosítások tükrözéséhez a **Update-AzureVM** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="52361-115">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

### <span data-ttu-id="52361-116">2. példa: az állomás gyorsítótárának módosítása a virtuális gép minden adatlemezén</span><span class="sxs-lookup"><span data-stu-id="52361-116">Example 2: Modify the host caching for all data disks on a virtual machine</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk | Set-AzureDataDisk -HostCaching ReadWrite | Update-AzureVM
```

<span data-ttu-id="52361-117">Ez a parancs a VirtualMachine07 nevű virtuális gép objektumát kapja a ContosoService felhő szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="52361-117">This command gets an object for the virtual machine named VirtualMachine07 on the ContosoService cloud service.</span></span>
<span data-ttu-id="52361-118">A parancs a **Get-AzureDataDisk** parancsmagot adja át, amely a virtuális gép adatlemezeit kapja.</span><span class="sxs-lookup"><span data-stu-id="52361-118">The command passes it to the **Get-AzureDataDisk** cmdlet, which gets the data disks for that virtual machine.</span></span>
<span data-ttu-id="52361-119">Az aktuális parancsmag ekkor beállítja az egyes adatlemezek állomás-gyorsítótárazási módját a ReadWrite-ra.</span><span class="sxs-lookup"><span data-stu-id="52361-119">The current cmdlet then sets the host caching mode of each data disks to ReadWrite.</span></span>
<span data-ttu-id="52361-120">A parancs frissíti a virtuális gépet a módosítások tükrözéséhez.</span><span class="sxs-lookup"><span data-stu-id="52361-120">The command updates the virtual machine to reflect your changes.</span></span>

## <span data-ttu-id="52361-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="52361-121">PARAMETERS</span></span>

### <span data-ttu-id="52361-122">-DiskName</span><span class="sxs-lookup"><span data-stu-id="52361-122">-DiskName</span></span>
<span data-ttu-id="52361-123">A parancsmag által módosított adatlemez-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="52361-123">Specifies the name of the data disk configuration that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: Resize
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52361-124">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="52361-124">-HostCaching</span></span>

> [!WARNING]
> <span data-ttu-id="52361-125">A lemezek gyorsítótárazása nem támogatott a 4 TiB és a nagyobb lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="52361-125">Disk Caching is not supported for disks 4 TiB and larger.</span></span> <span data-ttu-id="52361-126">Ha több lemez van csatlakoztatva a VM-hez, akkor a 4 TiB-nál kisebb lemezek mindegyike támogatja a gyorsítótárazást.</span><span class="sxs-lookup"><span data-stu-id="52361-126">If multiple disks are attached to your VM, each disk that is smaller than 4 TiB will support caching.</span></span>
>
> <span data-ttu-id="52361-127">Az Azure-lemezek gyorsítótár-beállításának módosítása leválik, és újra csatolja a céllemez tartalmát.</span><span class="sxs-lookup"><span data-stu-id="52361-127">Changing the cache setting of an Azure disk detaches and re-attaches the target disk.</span></span> <span data-ttu-id="52361-128">Ha az operációs rendszer lemeze, a VM újraindul.</span><span class="sxs-lookup"><span data-stu-id="52361-128">If it is the operating system disk, the VM is restarted.</span></span> <span data-ttu-id="52361-129">Állítsa le az összes olyan alkalmazást/szolgáltatást, amelyet esetleg érinthet az ilyen zavarok, mielőtt módosítaná a lemezgyorsítótár beállítását.</span><span class="sxs-lookup"><span data-stu-id="52361-129">Stop all applications/services that might be affected by this disruption before changing the disk cache setting.</span></span> <span data-ttu-id="52361-130">Ezek az ajánlások nem követik az adatsérülést.</span><span class="sxs-lookup"><span data-stu-id="52361-130">Not following those recommendations could lead to data corruption.</span></span>

<span data-ttu-id="52361-131">Az állomás szintű gyorsítótár-beállításokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="52361-131">Specifies the host level caching settings of the disk.</span></span>
<span data-ttu-id="52361-132">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="52361-132">Valid values are:</span></span>

- <span data-ttu-id="52361-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="52361-133">None</span></span>
- <span data-ttu-id="52361-134">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="52361-134">ReadOnly</span></span>
- <span data-ttu-id="52361-135">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="52361-135">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: NoResize
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52361-136">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="52361-136">-InformationAction</span></span>
<span data-ttu-id="52361-137">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="52361-137">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="52361-138">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="52361-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="52361-139">Folytassa</span><span class="sxs-lookup"><span data-stu-id="52361-139">Continue</span></span>
- <span data-ttu-id="52361-140">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="52361-140">Ignore</span></span>
- <span data-ttu-id="52361-141">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="52361-141">Inquire</span></span>
- <span data-ttu-id="52361-142">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="52361-142">SilentlyContinue</span></span>
- <span data-ttu-id="52361-143">állj</span><span class="sxs-lookup"><span data-stu-id="52361-143">Stop</span></span>
- <span data-ttu-id="52361-144">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="52361-144">Suspend</span></span>

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

### <span data-ttu-id="52361-145">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="52361-145">-InformationVariable</span></span>
<span data-ttu-id="52361-146">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="52361-146">Specifies an information variable.</span></span>

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

### <span data-ttu-id="52361-147">-LUN</span><span class="sxs-lookup"><span data-stu-id="52361-147">-LUN</span></span>
<span data-ttu-id="52361-148">A virtuális gép adatmeghajtójának logikai egységét adja meg.</span><span class="sxs-lookup"><span data-stu-id="52361-148">Specifies the LUN for the data drive in the virtual machine.</span></span>
<span data-ttu-id="52361-149">Az érvényes értékek a következők: 0 – 15.</span><span class="sxs-lookup"><span data-stu-id="52361-149">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: NoResize
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52361-150">-Profil</span><span class="sxs-lookup"><span data-stu-id="52361-150">-Profile</span></span>
<span data-ttu-id="52361-151">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="52361-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="52361-152">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="52361-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="52361-153">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="52361-153">-ResizedSizeInGB</span></span>
<span data-ttu-id="52361-154">Az adatlemez új méretének meghatározása gigabájtban.</span><span class="sxs-lookup"><span data-stu-id="52361-154">Specifies the new size, in gigabytes, for the data disk.</span></span>
<span data-ttu-id="52361-155">Az új méretnek az aktuális méretnél nagyobbnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="52361-155">The new size must be larger than the current size.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52361-156">-VM</span><span class="sxs-lookup"><span data-stu-id="52361-156">-VM</span></span>
<span data-ttu-id="52361-157">Az adatlemezhez kapcsolt virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="52361-157">Specifies the virtual machine object that is attached to the data disk.</span></span>
<span data-ttu-id="52361-158">Virtuális gép objektum beszerzéséhez használja a **Get-AzureVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="52361-158">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="52361-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52361-159">CommonParameters</span></span>
<span data-ttu-id="52361-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="52361-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52361-161">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52361-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52361-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="52361-162">INPUTS</span></span>

## <span data-ttu-id="52361-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52361-163">OUTPUTS</span></span>

## <span data-ttu-id="52361-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="52361-164">NOTES</span></span>

## <span data-ttu-id="52361-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52361-165">RELATED LINKS</span></span>

[<span data-ttu-id="52361-166">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="52361-166">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="52361-167">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="52361-167">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="52361-168">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="52361-168">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="52361-169">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="52361-169">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="52361-170">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="52361-170">Update-AzureVM</span></span>](./Update-AzureVM.md)


