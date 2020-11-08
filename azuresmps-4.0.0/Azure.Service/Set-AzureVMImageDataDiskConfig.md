---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6C7CB0AE-C788-4E6F-AD48-E30B547A2269
online version: ''
schema: 2.0.0
ms.openlocfilehash: a7512ef446227742c2a3564c5f3e5f38f1e2ccce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015436"
---
# <span data-ttu-id="aed54-101">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="aed54-101">Set-AzureVMImageDataDiskConfig</span></span>

## <span data-ttu-id="aed54-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aed54-102">SYNOPSIS</span></span>
<span data-ttu-id="aed54-103">Az adatlemez tulajdonságainak megadása a virtuális gép képén</span><span class="sxs-lookup"><span data-stu-id="aed54-103">Sets the Data Disk properties on the virtual machine image.</span></span>

## <span data-ttu-id="aed54-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aed54-104">SYNTAX</span></span>

### <span data-ttu-id="aed54-105">UpdateAzureVMImageParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aed54-105">UpdateAzureVMImageParamSet (Default)</span></span>
```
Set-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-DataDiskName] <String>
 [-Lun] <Int32> [-HostCaching] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="aed54-106">AddAzureVMImageParamSet</span><span class="sxs-lookup"><span data-stu-id="aed54-106">AddAzureVMImageParamSet</span></span>
```
Set-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-Lun] <Int32>
 [-HostCaching] <String> [-MediaLink] <Uri> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="aed54-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="aed54-107">DESCRIPTION</span></span>
<span data-ttu-id="aed54-108">A **set-AzureVMImageDataDiskConfig** parancsmag az adatlemez tulajdonságait a virtuális gép képére állítja be.</span><span class="sxs-lookup"><span data-stu-id="aed54-108">The **Set-AzureVMImageDataDiskConfig** cmdlet sets the Data Disk properties on the virtual machine image.</span></span>

## <span data-ttu-id="aed54-109">Példák</span><span class="sxs-lookup"><span data-stu-id="aed54-109">EXAMPLES</span></span>

### <span data-ttu-id="aed54-110">1. példa: az adatlemez tulajdonságainak beállítása virtuális gép képe</span><span class="sxs-lookup"><span data-stu-id="aed54-110">Example 1: Set Data Disk properties on a virtual machine image</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="aed54-111">Ez a parancs beállítja a virtuális gép adatlemez-tulajdonságait, majd frissíti a virtuális gép képét.</span><span class="sxs-lookup"><span data-stu-id="aed54-111">This command sets data disk properties on a virtual machine then updates the virtual machine image.</span></span>

## <span data-ttu-id="aed54-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aed54-112">PARAMETERS</span></span>

### <span data-ttu-id="aed54-113">-DataDiskName</span><span class="sxs-lookup"><span data-stu-id="aed54-113">-DataDiskName</span></span>
<span data-ttu-id="aed54-114">Megadja annak az adatlemeznek a nevét, amelyet a parancsmag állít be.</span><span class="sxs-lookup"><span data-stu-id="aed54-114">Specifies the name of the data disk that this cmdlet configures.</span></span>

```yaml
Type: String
Parameter Sets: UpdateAzureVMImageParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aed54-115">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="aed54-115">-DiskConfig</span></span>
<span data-ttu-id="aed54-116">Itt adhatja meg azt a Disk Configuration objektumot, amely az operációs rendszer lemezét és az adatlemez-objektumokat ágyazza be.</span><span class="sxs-lookup"><span data-stu-id="aed54-116">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

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

### <span data-ttu-id="aed54-117">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="aed54-117">-HostCaching</span></span>
<span data-ttu-id="aed54-118">Az operációs rendszer merevlemezének az állomás-gyorsítótár attribútumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="aed54-118">Specifies the host cache attribute for the operating system disk.</span></span>

<span data-ttu-id="aed54-119">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="aed54-119">Valid values are:</span></span>

<span data-ttu-id="aed54-120">– ReadOnly--ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aed54-120">--ReadOnly --ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aed54-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="aed54-121">-InformationAction</span></span>
<span data-ttu-id="aed54-122">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="aed54-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="aed54-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="aed54-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aed54-124">Folytassa</span><span class="sxs-lookup"><span data-stu-id="aed54-124">Continue</span></span>
- <span data-ttu-id="aed54-125">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="aed54-125">Ignore</span></span>
- <span data-ttu-id="aed54-126">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="aed54-126">Inquire</span></span>
- <span data-ttu-id="aed54-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="aed54-127">SilentlyContinue</span></span>
- <span data-ttu-id="aed54-128">állj</span><span class="sxs-lookup"><span data-stu-id="aed54-128">Stop</span></span>
- <span data-ttu-id="aed54-129">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="aed54-129">Suspend</span></span>

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

### <span data-ttu-id="aed54-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="aed54-130">-InformationVariable</span></span>
<span data-ttu-id="aed54-131">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="aed54-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="aed54-132">-LUN</span><span class="sxs-lookup"><span data-stu-id="aed54-132">-Lun</span></span>
<span data-ttu-id="aed54-133">Azt a bővítőhelyet adja meg, ahol az adatmeghajtó a virtuális gépben van szerelve.</span><span class="sxs-lookup"><span data-stu-id="aed54-133">Specifies the slot where the data drive is mounted in the virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aed54-134">-MediaLink</span><span class="sxs-lookup"><span data-stu-id="aed54-134">-MediaLink</span></span>
<span data-ttu-id="aed54-135">Annak a helynek az URI azonosítóját adja meg, amelybe az új virtuális merevlemezt hozza létre az új adatlemez felvételekor.</span><span class="sxs-lookup"><span data-stu-id="aed54-135">Specifies the URI of the location where the new virtual hard drive is created when the new data disk is added.</span></span>

```yaml
Type: Uri
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aed54-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aed54-136">CommonParameters</span></span>
<span data-ttu-id="aed54-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aed54-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aed54-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aed54-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aed54-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aed54-139">INPUTS</span></span>

## <span data-ttu-id="aed54-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aed54-140">OUTPUTS</span></span>

### <span data-ttu-id="aed54-141">Microsoft. WindowsAzure. Command. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="aed54-141">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="aed54-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aed54-142">NOTES</span></span>

## <span data-ttu-id="aed54-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aed54-143">RELATED LINKS</span></span>

[<span data-ttu-id="aed54-144">Remove-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="aed54-144">Remove-AzureVMImageDataDiskConfig</span></span>](./Remove-AzureVMImageDataDiskConfig.md)


