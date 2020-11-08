---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C9470E5-21D2-4AF5-9F11-F66F94B133C0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23f4511f8e0439c1581cc388843a37266092f4d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016454"
---
# <span data-ttu-id="3c019-101">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="3c019-101">Remove-AzureVMImage</span></span>

## <span data-ttu-id="3c019-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c019-102">SYNOPSIS</span></span>
<span data-ttu-id="3c019-103">Eltávolítja az operációs rendszer képét a képtárházból.</span><span class="sxs-lookup"><span data-stu-id="3c019-103">Removes an operating system image from the image repository.</span></span>

## <span data-ttu-id="3c019-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c019-104">SYNTAX</span></span>

```
Remove-AzureVMImage [-ImageName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3c019-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c019-105">DESCRIPTION</span></span>
<span data-ttu-id="3c019-106">A **Remove-AzureVMImage** parancsmag eltávolítja az operációs rendszer képét a képtárházból.</span><span class="sxs-lookup"><span data-stu-id="3c019-106">The **Remove-AzureVMImage** cmdlet removes an operating system image from the image repository.</span></span>
<span data-ttu-id="3c019-107">Ez a parancsmag alapértelmezés szerint nem törli a kapcsolódó fizikai képblobot a tárolási fiókból.</span><span class="sxs-lookup"><span data-stu-id="3c019-107">By default, this cmdlet does not delete the associated physical image blob from the storage account.</span></span>
<span data-ttu-id="3c019-108">Ha törölni szeretné a kapcsolódó virtuális merevlemezt (VHD), használja a **DeleteVHD** paramétert.</span><span class="sxs-lookup"><span data-stu-id="3c019-108">To delete the associated virtual hard drive (VHD), use the **DeleteVHD** parameter.</span></span>

## <span data-ttu-id="3c019-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3c019-109">EXAMPLES</span></span>

### <span data-ttu-id="3c019-110">1. példa: kép eltávolítása a képtárházból</span><span class="sxs-lookup"><span data-stu-id="3c019-110">Example 1: Remove an image from the image repository</span></span>
```
PS C:\> Remove-AzureVMImage -ImageName "Image001"
```

<span data-ttu-id="3c019-111">Ez a parancs eltávolítja a Kép001 nevű képet a képtárházból.</span><span class="sxs-lookup"><span data-stu-id="3c019-111">This command removes the image named Image001 from the image repository.</span></span>

### <span data-ttu-id="3c019-112">2. példa: képek eltávolítása a képtárházból és a VHD-ből</span><span class="sxs-lookup"><span data-stu-id="3c019-112">Example 2: Remove an image from the image repository and also the VHD</span></span>
```
PS C:\> Remove-AzureVMImage -ImageName " Image001" -DeleteVHD
```

<span data-ttu-id="3c019-113">Ez a parancs eltávolítja a Kép001 nevű képet a képtárházból, és törli a fizikai VHD-képet a tároló fiókból.</span><span class="sxs-lookup"><span data-stu-id="3c019-113">This command removes the image named Image001 from the image repository and also deletes the physical VHD image from the storage account.</span></span>

### <span data-ttu-id="3c019-114">3. példa: az előfizetés környezetének beállítása, majd az összes kép eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3c019-114">Example 3: Set a subscription context and then remove all the images</span></span>
```
PS C:\> $SubsId = &amp;lt;MySubscriptionID&amp;gt;
PS C:\> $Cert = Get-AzureCertificate cert:\LocalMachine\MY\&amp;lt;CertificateThumbprint&amp;gt;
PS C:\> Get-AzureVMImage `
| Where-Object {$_.Label -match "Beta" }`
| Foreach-Object {Remove-AzureVMImage -ImageName $_.name }
```

<span data-ttu-id="3c019-115">Ez a parancs beállítja az előfizetés környezetét, majd eltávolítja az összes képet a képtárházból, amelynek a címkéje tartalmazza a béta nevet.</span><span class="sxs-lookup"><span data-stu-id="3c019-115">This command sets the subscription context and then removes all the images from the image repository whose Label includes the name Beta.</span></span>

## <span data-ttu-id="3c019-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c019-116">PARAMETERS</span></span>

### <span data-ttu-id="3c019-117">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="3c019-117">-DeleteVHD</span></span>
<span data-ttu-id="3c019-118">Azt jelzi, hogy ez a parancsmag törli a fizikai VHD-képblobot a tárolási fiókból.</span><span class="sxs-lookup"><span data-stu-id="3c019-118">Indicates that this cmdlet deletes the physical VHD image blob from the storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c019-119">-ImageName</span><span class="sxs-lookup"><span data-stu-id="3c019-119">-ImageName</span></span>
<span data-ttu-id="3c019-120">A képtárházból eltávolítandó operációs rendszert vagy virtuális gép képét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c019-120">Specifies the operating system or virtual machine image to remove from the image repository.</span></span>

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

### <span data-ttu-id="3c019-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3c019-121">-InformationAction</span></span>
<span data-ttu-id="3c019-122">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="3c019-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3c019-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3c019-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3c019-124">Folytassa</span><span class="sxs-lookup"><span data-stu-id="3c019-124">Continue</span></span>
- <span data-ttu-id="3c019-125">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="3c019-125">Ignore</span></span>
- <span data-ttu-id="3c019-126">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="3c019-126">Inquire</span></span>
- <span data-ttu-id="3c019-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3c019-127">SilentlyContinue</span></span>
- <span data-ttu-id="3c019-128">állj</span><span class="sxs-lookup"><span data-stu-id="3c019-128">Stop</span></span>
- <span data-ttu-id="3c019-129">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="3c019-129">Suspend</span></span>

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

### <span data-ttu-id="3c019-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3c019-130">-InformationVariable</span></span>
<span data-ttu-id="3c019-131">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="3c019-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3c019-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="3c019-132">-Profile</span></span>
<span data-ttu-id="3c019-133">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3c019-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3c019-134">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3c019-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3c019-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c019-135">CommonParameters</span></span>
<span data-ttu-id="3c019-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c019-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c019-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c019-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c019-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c019-138">INPUTS</span></span>

## <span data-ttu-id="3c019-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c019-139">OUTPUTS</span></span>

## <span data-ttu-id="3c019-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c019-140">NOTES</span></span>

## <span data-ttu-id="3c019-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c019-141">RELATED LINKS</span></span>

[<span data-ttu-id="3c019-142">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="3c019-142">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="3c019-143">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="3c019-143">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="3c019-144">Mentés-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="3c019-144">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="3c019-145">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="3c019-145">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


