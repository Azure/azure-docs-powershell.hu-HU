---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F420A47F-D036-4B31-AA59-97CFC9C79E75
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a53d0821832b29f0f1f6a0b2ab5f1353e3331a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016198"
---
# <span data-ttu-id="844ca-101">New-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="844ca-101">New-AzureVMImageDiskConfigSet</span></span>

## <span data-ttu-id="844ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="844ca-102">SYNOPSIS</span></span>
<span data-ttu-id="844ca-103">Létrehoz egy Disk Configuration set objektumot.</span><span class="sxs-lookup"><span data-stu-id="844ca-103">Creates a disk configuration set object.</span></span>

## <span data-ttu-id="844ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="844ca-104">SYNTAX</span></span>

```
New-AzureVMImageDiskConfigSet [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="844ca-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="844ca-105">DESCRIPTION</span></span>
<span data-ttu-id="844ca-106">A **New-AzureVMImageDiskConfigSet** parancsmag létrehoz egy olyan Disk Configuration set objektumot, amely a képfrissítési parancsmagra lett átadva.</span><span class="sxs-lookup"><span data-stu-id="844ca-106">The **New-AzureVMImageDiskConfigSet** cmdlet creates a disk configuration set object that is passed to the image update cmdlet.</span></span>
<span data-ttu-id="844ca-107">A OSDiskConfig és a DataDiskConfig objektumot ágyazza be.</span><span class="sxs-lookup"><span data-stu-id="844ca-107">It encapsulates the OSDiskConfig and the DataDiskConfig object.</span></span>
<span data-ttu-id="844ca-108">A **set-AzureVMImageOSDiskConfig** és a **set-AzureVMImageDataDiskConfig** parancsmagok segítségével beállíthatja az operációs rendszer lemez-és adatlemez-tulajdonságait a virtuális gép képére.</span><span class="sxs-lookup"><span data-stu-id="844ca-108">Use the **Set-AzureVMImageOSDiskConfig** and **Set-AzureVMImageDataDiskConfig** cmdlets to set the OS Disk and Data Disk properties for the virtual machine image.</span></span>

## <span data-ttu-id="844ca-109">Példák</span><span class="sxs-lookup"><span data-stu-id="844ca-109">EXAMPLES</span></span>

### <span data-ttu-id="844ca-110">Példa 1: Disk Configuration set objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="844ca-110">Example 1: Create a disk configuration set object</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="844ca-111">Ez a parancs létrehoz egy Disk Configuration set objektumot, és a találatokat az $Disk nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="844ca-111">This command creates a disk configuration set object and stores the results in the variable named $Disk.</span></span>
<span data-ttu-id="844ca-112">A lemez beállítása után a rendszer a OSDiskConfig és a DataDiskConfig beállítását használja.</span><span class="sxs-lookup"><span data-stu-id="844ca-112">After the disk configuration is created, it is used to set the OSDiskConfig and DataDiskConfig.</span></span>
<span data-ttu-id="844ca-113">Ezután a virtuális gép frissíti a konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="844ca-113">Then the virtual machine is updated with the configuration.</span></span>

## <span data-ttu-id="844ca-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="844ca-114">PARAMETERS</span></span>

### <span data-ttu-id="844ca-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="844ca-115">-InformationAction</span></span>
<span data-ttu-id="844ca-116">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="844ca-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="844ca-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="844ca-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="844ca-118">Folytassa</span><span class="sxs-lookup"><span data-stu-id="844ca-118">Continue</span></span>
- <span data-ttu-id="844ca-119">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="844ca-119">Ignore</span></span>
- <span data-ttu-id="844ca-120">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="844ca-120">Inquire</span></span>
- <span data-ttu-id="844ca-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="844ca-121">SilentlyContinue</span></span>
- <span data-ttu-id="844ca-122">állj</span><span class="sxs-lookup"><span data-stu-id="844ca-122">Stop</span></span>
- <span data-ttu-id="844ca-123">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="844ca-123">Suspend</span></span>

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

### <span data-ttu-id="844ca-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="844ca-124">-InformationVariable</span></span>
<span data-ttu-id="844ca-125">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="844ca-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="844ca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="844ca-126">CommonParameters</span></span>
<span data-ttu-id="844ca-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="844ca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="844ca-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="844ca-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="844ca-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="844ca-129">INPUTS</span></span>

## <span data-ttu-id="844ca-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="844ca-130">OUTPUTS</span></span>

### <span data-ttu-id="844ca-131">Microsoft. WindowsAzure. Command. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="844ca-131">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="844ca-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="844ca-132">NOTES</span></span>

## <span data-ttu-id="844ca-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="844ca-133">RELATED LINKS</span></span>

[<span data-ttu-id="844ca-134">Get-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="844ca-134">Get-AzureVMImageDiskConfigSet</span></span>](./Get-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="844ca-135">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="844ca-135">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)

[<span data-ttu-id="844ca-136">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="844ca-136">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


