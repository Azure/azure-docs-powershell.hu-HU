---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E712421A-FA69-46E7-A0DE-F2734D767F2D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8355e0a1d36a6c1dc5b2ca8172cde5bf94480bbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016532"
---
# <span data-ttu-id="ff6fb-101">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ff6fb-101">Get-AzureVMImage</span></span>

## <span data-ttu-id="ff6fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff6fb-102">SYNOPSIS</span></span>
<span data-ttu-id="ff6fb-103">A képtárházban egy operációs rendszer vagy egy virtuális gép tulajdonságainak egy vagy több elemét kapja.</span><span class="sxs-lookup"><span data-stu-id="ff6fb-103">Gets the properties on one or a list of operating systems or a virtual machine image in the image repository.</span></span>

## <span data-ttu-id="ff6fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff6fb-104">SYNTAX</span></span>

```
Get-AzureVMImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ff6fb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff6fb-105">DESCRIPTION</span></span>
<span data-ttu-id="ff6fb-106">A **Get-AzureVMImage** parancsmag egy vagy több operációs rendszer vagy egy virtuális gép egy vagy több, a képtárházban lévő képére vonatkozó tulajdonságot kap.</span><span class="sxs-lookup"><span data-stu-id="ff6fb-106">The **Get-AzureVMImage** cmdlet gets properties on one or a list of operating systems or a virtual machine image in the image repository.</span></span>
<span data-ttu-id="ff6fb-107">A parancsmag információt ad eredményül a tárházban lévő összes képhez, vagy ha a kép neve meg van határozva, akkor egy bizonyos képre.</span><span class="sxs-lookup"><span data-stu-id="ff6fb-107">The cmdlet returns information for all images in the repository, or about a specific image if its image name is provided.</span></span>

## <span data-ttu-id="ff6fb-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ff6fb-108">EXAMPLES</span></span>

### <span data-ttu-id="ff6fb-109">Példa 1: adott képobjektum beszerzése az aktuális képtárházból.</span><span class="sxs-lookup"><span data-stu-id="ff6fb-109">Example 1: Get a specific image object from the current image repository.</span></span>
```
PS C:\> Get-AzureVMImage -ImageName Image001
```

<span data-ttu-id="ff6fb-110">Ez a parancs a Kép001 nevű kép objektumot az aktuális képtárházból kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ff6fb-110">This command gets the image object named Image001 from the current image repository.</span></span>

### <span data-ttu-id="ff6fb-111">2. példa: az aktuális képtárház összes képének beolvasása</span><span class="sxs-lookup"><span data-stu-id="ff6fb-111">Example 2: Get all images from the current image repository</span></span>
```
PS C:\> Get-AzureVMImage
```

<span data-ttu-id="ff6fb-112">A parancs a jelenlegi képtárházból olvassa be az összes képet.</span><span class="sxs-lookup"><span data-stu-id="ff6fb-112">This command retrieves all the images from the current image repository.</span></span>

### <span data-ttu-id="ff6fb-113">3. példa: az előfizetés környezetének beállítása, majd az összes kép beolvasása</span><span class="sxs-lookup"><span data-stu-id="ff6fb-113">Example 3: Set the subscription context and then get all the images</span></span>
```
PS C:\> $SubsId = <MySubscriptionID>
C:\PS>$Cert = Get-AzureCertificate cert:\LocalMachine\MY\<CertificateThumbprint>
C:\PS>$MyOSImages = Get-AzureVMImage
```

<span data-ttu-id="ff6fb-114">Ez a parancs beállítja az előfizetés környezetét, majd beolvassa az összes képet a képtárházból.</span><span class="sxs-lookup"><span data-stu-id="ff6fb-114">This command sets the subscription context and then retrieves all the images from the image repository.</span></span>

## <span data-ttu-id="ff6fb-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff6fb-115">PARAMETERS</span></span>

### <span data-ttu-id="ff6fb-116">-ImageName</span><span class="sxs-lookup"><span data-stu-id="ff6fb-116">-ImageName</span></span>
<span data-ttu-id="ff6fb-117">Itt adhatja meg az operációs rendszer vagy a virtuális gép képét a képtárházban.</span><span class="sxs-lookup"><span data-stu-id="ff6fb-117">Specifies the name of the operating system or virtual machine image in the image repository.</span></span>
<span data-ttu-id="ff6fb-118">Ha nem adja meg ezt a paramétert, a program az összes képet visszaadja.</span><span class="sxs-lookup"><span data-stu-id="ff6fb-118">If you do not specify this parameter, all the images are returned.</span></span>

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

### <span data-ttu-id="ff6fb-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ff6fb-119">-InformationAction</span></span>
<span data-ttu-id="ff6fb-120">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="ff6fb-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ff6fb-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ff6fb-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ff6fb-122">Folytassa</span><span class="sxs-lookup"><span data-stu-id="ff6fb-122">Continue</span></span>
- <span data-ttu-id="ff6fb-123">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="ff6fb-123">Ignore</span></span>
- <span data-ttu-id="ff6fb-124">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="ff6fb-124">Inquire</span></span>
- <span data-ttu-id="ff6fb-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ff6fb-125">SilentlyContinue</span></span>
- <span data-ttu-id="ff6fb-126">állj</span><span class="sxs-lookup"><span data-stu-id="ff6fb-126">Stop</span></span>
- <span data-ttu-id="ff6fb-127">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="ff6fb-127">Suspend</span></span>

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

### <span data-ttu-id="ff6fb-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ff6fb-128">-InformationVariable</span></span>
<span data-ttu-id="ff6fb-129">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="ff6fb-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ff6fb-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="ff6fb-130">-Profile</span></span>
<span data-ttu-id="ff6fb-131">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ff6fb-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ff6fb-132">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ff6fb-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ff6fb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff6fb-133">CommonParameters</span></span>
<span data-ttu-id="ff6fb-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff6fb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff6fb-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff6fb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff6fb-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff6fb-136">INPUTS</span></span>

## <span data-ttu-id="ff6fb-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff6fb-137">OUTPUTS</span></span>

## <span data-ttu-id="ff6fb-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff6fb-138">NOTES</span></span>

## <span data-ttu-id="ff6fb-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff6fb-139">RELATED LINKS</span></span>

[<span data-ttu-id="ff6fb-140">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ff6fb-140">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="ff6fb-141">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ff6fb-141">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="ff6fb-142">Mentés-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ff6fb-142">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="ff6fb-143">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ff6fb-143">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


