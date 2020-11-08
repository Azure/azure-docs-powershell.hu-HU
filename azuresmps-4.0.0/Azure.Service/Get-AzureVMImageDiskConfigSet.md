---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: ACBE32E5-AA8C-43CA-9FF4-4B59906C6B85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 45d18179fba41d39456a11575fc2041ad4be8557
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016530"
---
# <span data-ttu-id="db10e-101">Get-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="db10e-101">Get-AzureVMImageDiskConfigSet</span></span>

## <span data-ttu-id="db10e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db10e-102">SYNOPSIS</span></span>
<span data-ttu-id="db10e-103">Beilleszt egy Disk Configuration set objektumot a szövegbeviteli kép környezetből.</span><span class="sxs-lookup"><span data-stu-id="db10e-103">Gets a disk configuration set object from the input image context.</span></span>

## <span data-ttu-id="db10e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db10e-104">SYNTAX</span></span>

```
Get-AzureVMImageDiskConfigSet [[-ImageContext] <OSImageContext>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="db10e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="db10e-105">DESCRIPTION</span></span>
<span data-ttu-id="db10e-106">A **Get-AzureVMImageDiskConfigSet** parancsmag a bemeneti kép környezetből kapja meg a lemezkvóta-objektumokat.</span><span class="sxs-lookup"><span data-stu-id="db10e-106">The **Get-AzureVMImageDiskConfigSet** cmdlet gets a disk configuration set object from the input image context.</span></span>

## <span data-ttu-id="db10e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="db10e-107">EXAMPLES</span></span>

### <span data-ttu-id="db10e-108">Példa 1: a Disk Configuration set objektum beszerzése virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="db10e-108">Example 1: Get a disk configuration set object from a virtual machine</span></span>
```
PS C:\> Get-AzureVMImage -ImageName $Img | Get-AzureVMImageDiskConfigSet
```

<span data-ttu-id="db10e-109">Ez a parancs a Disk Configuration set objektumot egy virtuális gépről kapja.</span><span class="sxs-lookup"><span data-stu-id="db10e-109">This command gets a disk configuration set object from a virtual machine.</span></span>

## <span data-ttu-id="db10e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db10e-110">PARAMETERS</span></span>

### <span data-ttu-id="db10e-111">-ImageContext</span><span class="sxs-lookup"><span data-stu-id="db10e-111">-ImageContext</span></span>
<span data-ttu-id="db10e-112">A virtuális gép képkörnyezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db10e-112">Specifies the virtual machine image context.</span></span>

```yaml
Type: OSImageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db10e-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="db10e-113">-InformationAction</span></span>
<span data-ttu-id="db10e-114">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="db10e-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="db10e-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="db10e-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="db10e-116">Folytassa</span><span class="sxs-lookup"><span data-stu-id="db10e-116">Continue</span></span>
- <span data-ttu-id="db10e-117">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="db10e-117">Ignore</span></span>
- <span data-ttu-id="db10e-118">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="db10e-118">Inquire</span></span>
- <span data-ttu-id="db10e-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="db10e-119">SilentlyContinue</span></span>
- <span data-ttu-id="db10e-120">állj</span><span class="sxs-lookup"><span data-stu-id="db10e-120">Stop</span></span>
- <span data-ttu-id="db10e-121">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="db10e-121">Suspend</span></span>

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

### <span data-ttu-id="db10e-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="db10e-122">-InformationVariable</span></span>
<span data-ttu-id="db10e-123">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="db10e-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="db10e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db10e-124">CommonParameters</span></span>
<span data-ttu-id="db10e-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db10e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db10e-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db10e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db10e-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db10e-127">INPUTS</span></span>

## <span data-ttu-id="db10e-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db10e-128">OUTPUTS</span></span>

### <span data-ttu-id="db10e-129">Microsoft. WindowsAzure. Command. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="db10e-129">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="db10e-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db10e-130">NOTES</span></span>

## <span data-ttu-id="db10e-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db10e-131">RELATED LINKS</span></span>

[<span data-ttu-id="db10e-132">Új – AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="db10e-132">New-AzureVMImageDiskConfigSet</span></span>](./New-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="db10e-133">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="db10e-133">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)


