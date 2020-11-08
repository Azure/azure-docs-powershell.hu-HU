---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9CD39F1C-D858-4275-A6DE-10901DC962FE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4cb2557b411d46ce718f97ba7939efb4571ce025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015444"
---
# <span data-ttu-id="1e771-101">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="1e771-101">Set-AzureVMImageOSDiskConfig</span></span>

## <span data-ttu-id="1e771-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e771-102">SYNOPSIS</span></span>
<span data-ttu-id="1e771-103">Az operációs rendszer lemezének tulajdonságait állítja be egy virtuális gép képére.</span><span class="sxs-lookup"><span data-stu-id="1e771-103">Sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="1e771-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e771-104">SYNTAX</span></span>

### <span data-ttu-id="1e771-105">UpdateAzureVMImageParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1e771-105">UpdateAzureVMImageParamSet (Default)</span></span>
```
Set-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-HostCaching] <String>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1e771-106">AddAzureVMImageParamSet</span><span class="sxs-lookup"><span data-stu-id="1e771-106">AddAzureVMImageParamSet</span></span>
```
Set-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-HostCaching] <String>]
 [-MediaLink] <Uri> [-OSState] <String> [-OS] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1e771-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e771-107">DESCRIPTION</span></span>
<span data-ttu-id="1e771-108">A **set-AzureVMImageOSDiskConfig** parancsmag az operációs rendszer lemezének tulajdonságait állítja be egy virtuális gép képére.</span><span class="sxs-lookup"><span data-stu-id="1e771-108">The **Set-AzureVMImageOSDiskConfig** cmdlet sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="1e771-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1e771-109">EXAMPLES</span></span>

### <span data-ttu-id="1e771-110">1. példa: az operációs rendszer lemezének tulajdonságainak beállítása virtuális gép képe</span><span class="sxs-lookup"><span data-stu-id="1e771-110">Example 1: Set the operating system disk properties on a virtual machine image</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="1e771-111">Ebben a példában az operációs rendszer Disk tulajdonságát egy virtuális gép képe szerint állíthatja be.</span><span class="sxs-lookup"><span data-stu-id="1e771-111">This example sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="1e771-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e771-112">PARAMETERS</span></span>

### <span data-ttu-id="1e771-113">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="1e771-113">-DiskConfig</span></span>
<span data-ttu-id="1e771-114">Itt adhatja meg azt a Disk Configuration objektumot, amely az operációs rendszer lemezét és az adatlemez-objektumokat ágyazza be.</span><span class="sxs-lookup"><span data-stu-id="1e771-114">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e771-115">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="1e771-115">-HostCaching</span></span>
<span data-ttu-id="1e771-116">Az operációs rendszer merevlemezének az állomás-gyorsítótár attribútumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e771-116">Specifies the host cache attribute for the operating system disk.</span></span>

<span data-ttu-id="1e771-117">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="1e771-117">Valid values are:</span></span>

<span data-ttu-id="1e771-118">– ReadOnly--ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1e771-118">--ReadOnly --ReadWrite</span></span>

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

### <span data-ttu-id="1e771-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1e771-119">-InformationAction</span></span>
<span data-ttu-id="1e771-120">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="1e771-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1e771-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="1e771-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1e771-122">Folytassa</span><span class="sxs-lookup"><span data-stu-id="1e771-122">Continue</span></span>
- <span data-ttu-id="1e771-123">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="1e771-123">Ignore</span></span>
- <span data-ttu-id="1e771-124">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="1e771-124">Inquire</span></span>
- <span data-ttu-id="1e771-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1e771-125">SilentlyContinue</span></span>
- <span data-ttu-id="1e771-126">állj</span><span class="sxs-lookup"><span data-stu-id="1e771-126">Stop</span></span>
- <span data-ttu-id="1e771-127">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="1e771-127">Suspend</span></span>

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

### <span data-ttu-id="1e771-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1e771-128">-InformationVariable</span></span>
<span data-ttu-id="1e771-129">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="1e771-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1e771-130">-MediaLink</span><span class="sxs-lookup"><span data-stu-id="1e771-130">-MediaLink</span></span>
<span data-ttu-id="1e771-131">Annak a helynek az URI azonosítóját adja meg, amelybe az új virtuális merevlemezt hozza létre az új adatlemez felvételekor.</span><span class="sxs-lookup"><span data-stu-id="1e771-131">Specifies the URI of the location where the new virtual hard drive is created when the new data disk is added.</span></span>

```yaml
Type: Uri
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e771-132">-OS</span><span class="sxs-lookup"><span data-stu-id="1e771-132">-OS</span></span>
<span data-ttu-id="1e771-133">A lemez konfigurációjának operációs rendszerét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e771-133">Specifies the operating system of the disk configuration.</span></span>

<span data-ttu-id="1e771-134">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="1e771-134">Valid values are:</span></span>

- <span data-ttu-id="1e771-135">Windows</span><span class="sxs-lookup"><span data-stu-id="1e771-135">Windows</span></span>
- <span data-ttu-id="1e771-136">Linux</span><span class="sxs-lookup"><span data-stu-id="1e771-136">Linux</span></span>

```yaml
Type: String
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e771-137">-OSState</span><span class="sxs-lookup"><span data-stu-id="1e771-137">-OSState</span></span>
<span data-ttu-id="1e771-138">A virtuálisgép-képek operációs rendszerének állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e771-138">Specifies the operating system state for virtual machine image</span></span>

<span data-ttu-id="1e771-139">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="1e771-139">Valid values are:</span></span>

- <span data-ttu-id="1e771-140">Nemlineáris</span><span class="sxs-lookup"><span data-stu-id="1e771-140">Generalized</span></span>
- <span data-ttu-id="1e771-141">Speciális</span><span class="sxs-lookup"><span data-stu-id="1e771-141">Specialized</span></span>

<span data-ttu-id="1e771-142">A paraméter használata azt jelzi, hogy a virtuális gép képe az Azure-ra rögzíthető.</span><span class="sxs-lookup"><span data-stu-id="1e771-142">The use of this parameter indicates your intent to capture the virtual machine image to Azure.</span></span>

```yaml
Type: String
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e771-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e771-143">CommonParameters</span></span>
<span data-ttu-id="1e771-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e771-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e771-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e771-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e771-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e771-146">INPUTS</span></span>

## <span data-ttu-id="1e771-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e771-147">OUTPUTS</span></span>

### <span data-ttu-id="1e771-148">Microsoft. WindowsAzure. Command. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="1e771-148">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="1e771-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e771-149">NOTES</span></span>

## <span data-ttu-id="1e771-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e771-150">RELATED LINKS</span></span>

[<span data-ttu-id="1e771-151">Remove-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="1e771-151">Remove-AzureVMImageOSDiskConfig</span></span>](./Remove-AzureVMImageOSDiskConfig.md)


