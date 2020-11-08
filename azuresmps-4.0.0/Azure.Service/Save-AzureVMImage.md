---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A1CE31E-0158-441E-BC2D-B5D21C9D9421
online version: ''
schema: 2.0.0
ms.openlocfilehash: a956aa7eaf383b0cf5cdb20b39d2f6b54e292f92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015451"
---
# <span data-ttu-id="c042f-101">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="c042f-101">Save-AzureVMImage</span></span>

## <span data-ttu-id="c042f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c042f-102">SYNOPSIS</span></span>
<span data-ttu-id="c042f-103">A leállított Azure virtuális gép képét rögzíti és menti.</span><span class="sxs-lookup"><span data-stu-id="c042f-103">Captures and saves the image of a stopped Azure virtual machine.</span></span>

## <span data-ttu-id="c042f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c042f-104">SYNTAX</span></span>

```
Save-AzureVMImage [-ServiceName] <String> [-Name] <String> [-ImageName] <String> [[-ImageLabel] <String>]
 [[-OSState] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c042f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c042f-105">DESCRIPTION</span></span>
<span data-ttu-id="c042f-106">A **Save-AzureVMImage** parancsmag rögzíti és menti a leállított Azure virtuális gép képét.</span><span class="sxs-lookup"><span data-stu-id="c042f-106">The **Save-AzureVMImage** cmdlet captures and saves the image of a stopped Azure virtual machine.</span></span>
<span data-ttu-id="c042f-107">Windows Virtual Machines esetén a Sysprep eszközt futtatva készítse elő a képet a rögzítés előtt.</span><span class="sxs-lookup"><span data-stu-id="c042f-107">For Windows virtual machines, run the Sysprep tool to prepare the image before it is captured.</span></span>
<span data-ttu-id="c042f-108">A kép rögzítése után a virtuális gép törlődik.</span><span class="sxs-lookup"><span data-stu-id="c042f-108">After the image is captured, the virtual machine is deleted.</span></span>

## <span data-ttu-id="c042f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c042f-109">EXAMPLES</span></span>

### <span data-ttu-id="c042f-110">1. példa: meglévő virtuális gép mentése és törlése egy központi példányból</span><span class="sxs-lookup"><span data-stu-id="c042f-110">Example 1: Save an existing virtual machine and then delete it from a deployment</span></span>
```
PS C:\> Save-AzureVMImage -ServiceName "MyService" -Name "MyVM" -NewImageName "MyBaseImage" -NewImageLabel "MyBaseVM"
```

<span data-ttu-id="c042f-111">Ez a parancs egy meglévő virtuális gépet rögzít, és törli azt a telepítőből.</span><span class="sxs-lookup"><span data-stu-id="c042f-111">This command captures an existing virtual machine and deletes it from the deployment.</span></span>

## <span data-ttu-id="c042f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c042f-112">PARAMETERS</span></span>

### <span data-ttu-id="c042f-113">-ImageLabel</span><span class="sxs-lookup"><span data-stu-id="c042f-113">-ImageLabel</span></span>
<span data-ttu-id="c042f-114">A virtuális gép képének címkéjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c042f-114">Specifies the label of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewImageLabel

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c042f-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="c042f-115">-ImageName</span></span>
<span data-ttu-id="c042f-116">A virtuális gép képének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c042f-116">Specifies the name of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewImageName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c042f-117">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c042f-117">-InformationAction</span></span>
<span data-ttu-id="c042f-118">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="c042f-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c042f-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c042f-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c042f-120">Folytassa</span><span class="sxs-lookup"><span data-stu-id="c042f-120">Continue</span></span>
- <span data-ttu-id="c042f-121">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="c042f-121">Ignore</span></span>
- <span data-ttu-id="c042f-122">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="c042f-122">Inquire</span></span>
- <span data-ttu-id="c042f-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c042f-123">SilentlyContinue</span></span>
- <span data-ttu-id="c042f-124">állj</span><span class="sxs-lookup"><span data-stu-id="c042f-124">Stop</span></span>
- <span data-ttu-id="c042f-125">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="c042f-125">Suspend</span></span>

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

### <span data-ttu-id="c042f-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c042f-126">-InformationVariable</span></span>
<span data-ttu-id="c042f-127">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="c042f-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c042f-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c042f-128">-Name</span></span>
<span data-ttu-id="c042f-129">A forrás virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c042f-129">Specifies the name of the source virtual machine.</span></span>

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

### <span data-ttu-id="c042f-130">-OSState</span><span class="sxs-lookup"><span data-stu-id="c042f-130">-OSState</span></span>
<span data-ttu-id="c042f-131">A virtuálisgép-kép operációs rendszerének állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c042f-131">Specifies the operation system state for the virtual machine image.</span></span>
<span data-ttu-id="c042f-132">Ezt a paramétert akkor érdemes használni, ha egy virtuális gép képét az Azure-ra szeretné menteni.</span><span class="sxs-lookup"><span data-stu-id="c042f-132">Use this parameter if you intend to capture a virtual machine image to Azure.</span></span>

<span data-ttu-id="c042f-133">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="c042f-133">Valid values are:</span></span>

- <span data-ttu-id="c042f-134">Nemlineáris</span><span class="sxs-lookup"><span data-stu-id="c042f-134">Generalized</span></span>
- <span data-ttu-id="c042f-135">Speciális</span><span class="sxs-lookup"><span data-stu-id="c042f-135">Specialized</span></span>

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

### <span data-ttu-id="c042f-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="c042f-136">-Profile</span></span>
<span data-ttu-id="c042f-137">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="c042f-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c042f-138">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="c042f-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c042f-139">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="c042f-139">-ServiceName</span></span>
<span data-ttu-id="c042f-140">Az Azure-szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c042f-140">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="c042f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c042f-141">CommonParameters</span></span>
<span data-ttu-id="c042f-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c042f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c042f-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c042f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c042f-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c042f-144">INPUTS</span></span>

## <span data-ttu-id="c042f-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c042f-145">OUTPUTS</span></span>

## <span data-ttu-id="c042f-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c042f-146">NOTES</span></span>

## <span data-ttu-id="c042f-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c042f-147">RELATED LINKS</span></span>

[<span data-ttu-id="c042f-148">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="c042f-148">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="c042f-149">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="c042f-149">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="c042f-150">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="c042f-150">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="c042f-151">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="c042f-151">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


