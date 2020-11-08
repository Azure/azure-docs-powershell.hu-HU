---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5CAF2D29-F4AE-4322-AA4F-61267723B955
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2e19ad4b56e5141458f1fe9305a0c33691d024d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015497"
---
# <span data-ttu-id="a9e98-101">Remove-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="a9e98-101">Remove-AzureVMImageDataDiskConfig</span></span>

## <span data-ttu-id="a9e98-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9e98-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e98-103">Az adatlemez-konfiguráció eltávolítása a DiskConfigSet objektumból.</span><span class="sxs-lookup"><span data-stu-id="a9e98-103">Removes the data disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="a9e98-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9e98-104">SYNTAX</span></span>

### <span data-ttu-id="a9e98-105">RemoveByDiskName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a9e98-105">RemoveByDiskName (Default)</span></span>
```
Remove-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-DataDiskName] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a9e98-106">RemoveByDiskLun</span><span class="sxs-lookup"><span data-stu-id="a9e98-106">RemoveByDiskLun</span></span>
```
Remove-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-Lun] <Int32>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a9e98-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9e98-107">DESCRIPTION</span></span>
<span data-ttu-id="a9e98-108">A **Remove-AzureVMImageDataDiskConfig** parancsmag eltávolítja az adatlemez-konfigurációt az **DiskConfigSet** objektumból.</span><span class="sxs-lookup"><span data-stu-id="a9e98-108">The **Remove-AzureVMImageDataDiskConfig** cmdlet removes the data disk configuration from the **DiskConfigSet** object.</span></span>

## <span data-ttu-id="a9e98-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a9e98-109">EXAMPLES</span></span>

### <span data-ttu-id="a9e98-110">1. példa: az adatlemez-konfiguráció eltávolítása a DiskConfigSet objektumról</span><span class="sxs-lookup"><span data-stu-id="a9e98-110">Example 1: Remove the data disk configuration from the DiskConfigSet object</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> Remove-AzureVMImageDataDiskConfig -DiskConfig $Disk
```

<span data-ttu-id="a9e98-111">Ez a példa létrehoz egy **DiskConfigSet** , Beállítja azt, majd eltávolítja az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="a9e98-111">This example creates a **DiskConfigSet** , configures it, then removes the data disk.</span></span>

## <span data-ttu-id="a9e98-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9e98-112">PARAMETERS</span></span>

### <span data-ttu-id="a9e98-113">-DataDiskName</span><span class="sxs-lookup"><span data-stu-id="a9e98-113">-DataDiskName</span></span>
<span data-ttu-id="a9e98-114">A parancsmag által eltávolított adatlemez nevének meghatározása.</span><span class="sxs-lookup"><span data-stu-id="a9e98-114">Specifies the name of the data disk that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDiskName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e98-115">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="a9e98-115">-DiskConfig</span></span>
<span data-ttu-id="a9e98-116">Itt adhatja meg azt a Disk Configuration objektumot, amely az operációs rendszer lemezét és az adatlemez-objektumokat ágyazza be.</span><span class="sxs-lookup"><span data-stu-id="a9e98-116">Specifies the disk configuration object that encapsulates the operating system disk and data disk objects.</span></span>

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

### <span data-ttu-id="a9e98-117">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a9e98-117">-InformationAction</span></span>
<span data-ttu-id="a9e98-118">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="a9e98-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a9e98-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a9e98-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a9e98-120">Folytassa</span><span class="sxs-lookup"><span data-stu-id="a9e98-120">Continue</span></span>
- <span data-ttu-id="a9e98-121">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="a9e98-121">Ignore</span></span>
- <span data-ttu-id="a9e98-122">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="a9e98-122">Inquire</span></span>
- <span data-ttu-id="a9e98-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a9e98-123">SilentlyContinue</span></span>
- <span data-ttu-id="a9e98-124">állj</span><span class="sxs-lookup"><span data-stu-id="a9e98-124">Stop</span></span>
- <span data-ttu-id="a9e98-125">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="a9e98-125">Suspend</span></span>

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

### <span data-ttu-id="a9e98-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a9e98-126">-InformationVariable</span></span>
<span data-ttu-id="a9e98-127">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="a9e98-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a9e98-128">-LUN</span><span class="sxs-lookup"><span data-stu-id="a9e98-128">-Lun</span></span>
<span data-ttu-id="a9e98-129">Azt a bővítőhelyet adja meg, ahol az adatmeghajtó a virtuális gépben van szerelve.</span><span class="sxs-lookup"><span data-stu-id="a9e98-129">Specifies the slot where the data drive is mounted in the virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: RemoveByDiskLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e98-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e98-130">CommonParameters</span></span>
<span data-ttu-id="a9e98-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9e98-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e98-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9e98-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e98-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9e98-133">INPUTS</span></span>

## <span data-ttu-id="a9e98-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9e98-134">OUTPUTS</span></span>

### <span data-ttu-id="a9e98-135">Microsoft. WindowsAzure. Command. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="a9e98-135">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="a9e98-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9e98-136">NOTES</span></span>

## <span data-ttu-id="a9e98-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9e98-137">RELATED LINKS</span></span>

[<span data-ttu-id="a9e98-138">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="a9e98-138">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


