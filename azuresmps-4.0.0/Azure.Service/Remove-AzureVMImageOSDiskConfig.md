---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1E1F98E9-FC45-4BEF-90F6-A21D7DB7C82F
online version: ''
schema: 2.0.0
ms.openlocfilehash: eac6db4400e5c51f295e0bbf549117ffdbc97644
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016445"
---
# <span data-ttu-id="03cb7-101">Remove-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="03cb7-101">Remove-AzureVMImageOSDiskConfig</span></span>

## <span data-ttu-id="03cb7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="03cb7-103">Eltávolítja az operációs rendszer lemezének konfigurációját a DiskConfigSet objektumból.</span><span class="sxs-lookup"><span data-stu-id="03cb7-103">Removes the operating system disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="03cb7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03cb7-104">SYNTAX</span></span>

```
Remove-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="03cb7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="03cb7-105">DESCRIPTION</span></span>
<span data-ttu-id="03cb7-106">A **Remove-AzureVMImageOSDiskConfig** parancsmag eltávolítja az operációs rendszer lemezének konfigurációját a DiskConfigSet objektumból.</span><span class="sxs-lookup"><span data-stu-id="03cb7-106">The **Remove-AzureVMImageOSDiskConfig** cmdlet removes the operating system disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="03cb7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="03cb7-107">EXAMPLES</span></span>

### <span data-ttu-id="03cb7-108">1. példa: az operációs rendszer lemez-konfigurációjának eltávolítása a DiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="03cb7-108">Example 1: Remove the operating system disk configuration from a DiskConfigSet</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> Remove-AzureVMImageOSDiskConfig -DiskConfig $Disk
```

<span data-ttu-id="03cb7-109">Ez a parancs eltávolítja az operációs rendszer lemezének konfigurációját a DiskConfigSet objektumból.</span><span class="sxs-lookup"><span data-stu-id="03cb7-109">This command removes the operating system disk configuration from the DiskConfigSet object</span></span>

## <span data-ttu-id="03cb7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03cb7-110">PARAMETERS</span></span>

### <span data-ttu-id="03cb7-111">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="03cb7-111">-DiskConfig</span></span>
<span data-ttu-id="03cb7-112">Itt adhatja meg azt a Disk Configuration objektumot, amely az operációs rendszer lemezét és az adatlemez-objektumokat ágyazza be.</span><span class="sxs-lookup"><span data-stu-id="03cb7-112">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

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

### <span data-ttu-id="03cb7-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="03cb7-113">-InformationAction</span></span>
<span data-ttu-id="03cb7-114">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="03cb7-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="03cb7-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="03cb7-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="03cb7-116">Folytassa</span><span class="sxs-lookup"><span data-stu-id="03cb7-116">Continue</span></span>
- <span data-ttu-id="03cb7-117">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="03cb7-117">Ignore</span></span>
- <span data-ttu-id="03cb7-118">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="03cb7-118">Inquire</span></span>
- <span data-ttu-id="03cb7-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="03cb7-119">SilentlyContinue</span></span>
- <span data-ttu-id="03cb7-120">állj</span><span class="sxs-lookup"><span data-stu-id="03cb7-120">Stop</span></span>
- <span data-ttu-id="03cb7-121">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="03cb7-121">Suspend</span></span>

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

### <span data-ttu-id="03cb7-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="03cb7-122">-InformationVariable</span></span>
<span data-ttu-id="03cb7-123">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="03cb7-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="03cb7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03cb7-124">CommonParameters</span></span>
<span data-ttu-id="03cb7-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03cb7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03cb7-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03cb7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03cb7-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03cb7-127">INPUTS</span></span>

## <span data-ttu-id="03cb7-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03cb7-128">OUTPUTS</span></span>

### <span data-ttu-id="03cb7-129">Microsoft. WindowsAzure. Command. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="03cb7-129">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="03cb7-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03cb7-130">NOTES</span></span>

## <span data-ttu-id="03cb7-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03cb7-131">RELATED LINKS</span></span>

[<span data-ttu-id="03cb7-132">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="03cb7-132">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)


