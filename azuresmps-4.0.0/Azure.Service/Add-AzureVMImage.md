---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DECCEE-86C8-4662-9ED0-D1BDB4E687C2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68efd1c750646abffa90eb8318d0df189a4c9eb9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015715"
---
# <span data-ttu-id="0f97d-101">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="0f97d-101">Add-AzureVMImage</span></span>

## <span data-ttu-id="0f97d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f97d-102">SYNOPSIS</span></span>
<span data-ttu-id="0f97d-103">Új operációs rendszer vagy egy új virtuálisgép-kép felvétele a képtárházba.</span><span class="sxs-lookup"><span data-stu-id="0f97d-103">Adds a new operating system image or a new virtual machine image to the image repository.</span></span>

## <span data-ttu-id="0f97d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f97d-104">SYNTAX</span></span>

### <span data-ttu-id="0f97d-105">OSImage (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0f97d-105">OSImage (Default)</span></span>
```
Add-AzureVMImage [-ImageName] <String> [-MediaLocation] <String> [-OS] <String> [[-Label] <String>]
 [[-Eula] <String>] [[-Description] <String>] [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>]
 [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>] [[-IconName] <String>] [[-SmallIconName] <String>]
 [-ShowInGui] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0f97d-106">VMImage</span><span class="sxs-lookup"><span data-stu-id="0f97d-106">VMImage</span></span>
```
Add-AzureVMImage [-ImageName] <String> [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-OS] <String>]
 [[-Label] <String>] [[-Eula] <String>] [[-Description] <String>] [[-ImageFamily] <String>]
 [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-ShowInGui] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0f97d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f97d-107">DESCRIPTION</span></span>
<span data-ttu-id="0f97d-108">Az **Add-AzureVMImage** parancsmag új operációs rendszert vagy új virtuális gépet ad hozzá a képtárházhoz.</span><span class="sxs-lookup"><span data-stu-id="0f97d-108">The **Add-AzureVMImage** cmdlet adds a new operating system image or a new virtual machine image to the image repository.</span></span>
<span data-ttu-id="0f97d-109">A kép egy általános operációs rendszer, amelyet a Windows Sysprep vagy a Linux esetén a megfelelő eszköz segítségével használhat a terjesztéshez.</span><span class="sxs-lookup"><span data-stu-id="0f97d-109">The image is a generalized operating system image, using either Sysprep for Windows or, for Linux, using the appropriate tool for the distribution.</span></span>

## <span data-ttu-id="0f97d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0f97d-110">EXAMPLES</span></span>

### <span data-ttu-id="0f97d-111">1. példa: operációs rendszer lemezképének felvétele a tárházba</span><span class="sxs-lookup"><span data-stu-id="0f97d-111">Example 1: Add an operating system image to the repository</span></span>
```
PS C:\> $S = New-AzureVMImageDiskConfigSet
PS C:\> Set-AzureVMImageOSDiskConfig -DiskConfig $S -HostCaching ReadWrite -OSState "Generalized" -OS "Windows" -MediaLink $Link
PS C:\> Set-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test1" -HostCaching ReadWrite -Lun 0 -MediaLink $Link1
PS C:\> Set-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test4" -HostCaching ReadWrite -Lun 0 -MediaLink $Link
PS C:\> Remove-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test4"
PS C:\> $IMGName = "TestCREATEvmimage2";
PS C:\> Add-AzureVMImage -ImageName $IMGName -Label "Test1" -Description "Test1" -DiskConfig $S -Eula "http://www.contoso.com" -ImageFamily Windows -PublishedDate (Get-Date) -PrivacyUri "http://www.test.com" -RecommendedVMSize Small -IconName "Icon01" -SmallIconName "SmallIcon01" -ShowInGui
```

<span data-ttu-id="0f97d-112">Ez a példa egy operációs rendszer képét egészíti ki a tárházban.</span><span class="sxs-lookup"><span data-stu-id="0f97d-112">This example adds an operating system image to the repository.</span></span>

## <span data-ttu-id="0f97d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f97d-113">PARAMETERS</span></span>

### <span data-ttu-id="0f97d-114">-Leírás</span><span class="sxs-lookup"><span data-stu-id="0f97d-114">-Description</span></span>
<span data-ttu-id="0f97d-115">Az operációs rendszer képének leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f97d-115">Specifies the description of the operating system image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f97d-116">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="0f97d-116">-DiskConfig</span></span>
<span data-ttu-id="0f97d-117">Megadja az operációs rendszer merevlemezének konfigurációját a virtuális gép képhez.</span><span class="sxs-lookup"><span data-stu-id="0f97d-117">Specifies the operating system disk configuration for the virtual machine image.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: VMImage
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f97d-118">-EULA</span><span class="sxs-lookup"><span data-stu-id="0f97d-118">-Eula</span></span>
<span data-ttu-id="0f97d-119">A végfelhasználói licencszerződést adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f97d-119">Specifies the End User License Agreement.</span></span>
<span data-ttu-id="0f97d-120">Ajánlott az érték URL-címét használni.</span><span class="sxs-lookup"><span data-stu-id="0f97d-120">It is recommended that you use an URL for this value.</span></span>

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

### <span data-ttu-id="0f97d-121">-IconName</span><span class="sxs-lookup"><span data-stu-id="0f97d-121">-IconName</span></span>
<span data-ttu-id="0f97d-122">Itt adhatja meg annak az ikonnak a nevét, amely akkor jelenik meg, ha a képet felveszi a tárházba.</span><span class="sxs-lookup"><span data-stu-id="0f97d-122">Specifies the name of the icon that is used when the image is added to the repository.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IconUri

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f97d-123">-ImageFamily</span><span class="sxs-lookup"><span data-stu-id="0f97d-123">-ImageFamily</span></span>
<span data-ttu-id="0f97d-124">Az operációs rendszer képeinek csoportosítására szolgáló értéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f97d-124">Specifies a value that is used to group operating system images.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f97d-125">-ImageName</span><span class="sxs-lookup"><span data-stu-id="0f97d-125">-ImageName</span></span>
<span data-ttu-id="0f97d-126">A képtárházba felvett kép nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="0f97d-126">Specifies the name of the image being added to the image repository.</span></span>

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

### <span data-ttu-id="0f97d-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0f97d-127">-InformationAction</span></span>
<span data-ttu-id="0f97d-128">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="0f97d-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0f97d-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0f97d-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0f97d-130">Folytassa</span><span class="sxs-lookup"><span data-stu-id="0f97d-130">Continue</span></span>
- <span data-ttu-id="0f97d-131">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="0f97d-131">Ignore</span></span>
- <span data-ttu-id="0f97d-132">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="0f97d-132">Inquire</span></span>
- <span data-ttu-id="0f97d-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0f97d-133">SilentlyContinue</span></span>
- <span data-ttu-id="0f97d-134">állj</span><span class="sxs-lookup"><span data-stu-id="0f97d-134">Stop</span></span>
- <span data-ttu-id="0f97d-135">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="0f97d-135">Suspend</span></span>

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

### <span data-ttu-id="0f97d-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0f97d-136">-InformationVariable</span></span>
<span data-ttu-id="0f97d-137">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="0f97d-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0f97d-138">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="0f97d-138">-Label</span></span>
<span data-ttu-id="0f97d-139">A kép megadására szolgáló címkét ad meg.</span><span class="sxs-lookup"><span data-stu-id="0f97d-139">Specifies a label to give the image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f97d-140">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="0f97d-140">-MediaLocation</span></span>
<span data-ttu-id="0f97d-141">Annak a fizikai blob-lapnak a helyét adja meg, amelyen a kép található.</span><span class="sxs-lookup"><span data-stu-id="0f97d-141">Specifies the location of the physical blob page where the image resides.</span></span>
<span data-ttu-id="0f97d-142">Ez a cikk az aktuális előfizetés tárterületének blob lapjára mutató hivatkozást tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="0f97d-142">This is a link to a blob page in the current subscription's storage.</span></span>

```yaml
Type: String
Parameter Sets: OSImage
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f97d-143">-OS</span><span class="sxs-lookup"><span data-stu-id="0f97d-143">-OS</span></span>
<span data-ttu-id="0f97d-144">A kép operációs rendszerének verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f97d-144">Specifies the operating system version of the image.</span></span>

```yaml
Type: String
Parameter Sets: OSImage
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: VMImage
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f97d-145">-PrivacyUri</span><span class="sxs-lookup"><span data-stu-id="0f97d-145">-PrivacyUri</span></span>
<span data-ttu-id="0f97d-146">Annak az URL-címnek az URL-címe, amely az operációs rendszer képhez kapcsolódó adatvédelmi házirendet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0f97d-146">Specifies the URL that points to a document that contains the privacy policy related to the operating system image.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f97d-147">-Profil</span><span class="sxs-lookup"><span data-stu-id="0f97d-147">-Profile</span></span>
<span data-ttu-id="0f97d-148">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="0f97d-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0f97d-149">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="0f97d-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0f97d-150">-PublishedDate</span><span class="sxs-lookup"><span data-stu-id="0f97d-150">-PublishedDate</span></span>
<span data-ttu-id="0f97d-151">Azt a dátumot adja meg, amikor az operációs rendszer képet felvette a képtárházba.</span><span class="sxs-lookup"><span data-stu-id="0f97d-151">Specifies the date when the operating system image was added to the image repository.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f97d-152">-RecommendedVMSize</span><span class="sxs-lookup"><span data-stu-id="0f97d-152">-RecommendedVMSize</span></span>
<span data-ttu-id="0f97d-153">Az operációs rendszer képből létrehozott virtuális gép által használt méretet adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f97d-153">Specifies the size to use for the virtual machine that is created from the operating system image.</span></span>

<span data-ttu-id="0f97d-154">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0f97d-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0f97d-155">Közepes</span><span class="sxs-lookup"><span data-stu-id="0f97d-155">Medium</span></span>
- <span data-ttu-id="0f97d-156">Nagy</span><span class="sxs-lookup"><span data-stu-id="0f97d-156">Large</span></span>
- <span data-ttu-id="0f97d-157">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="0f97d-157">ExtraLarge</span></span>
- <span data-ttu-id="0f97d-158">A5</span><span class="sxs-lookup"><span data-stu-id="0f97d-158">A5</span></span>
- <span data-ttu-id="0f97d-159">A6</span><span class="sxs-lookup"><span data-stu-id="0f97d-159">A6</span></span>
- <span data-ttu-id="0f97d-160">A7</span><span class="sxs-lookup"><span data-stu-id="0f97d-160">A7</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f97d-161">-ShowInGui</span><span class="sxs-lookup"><span data-stu-id="0f97d-161">-ShowInGui</span></span>
<span data-ttu-id="0f97d-162">Jelzi, hogy ez a parancsmag a képet a GUI-ban jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="0f97d-162">Indicates that this cmdlet shows the image in the GUI.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f97d-163">-SmallIconName</span><span class="sxs-lookup"><span data-stu-id="0f97d-163">-SmallIconName</span></span>
<span data-ttu-id="0f97d-164">Annak a kis ikonnak a neve, amely akkor jelenik meg, ha a képet felveszi a tárházba.</span><span class="sxs-lookup"><span data-stu-id="0f97d-164">Specifies the name of the small icon that is used when the image is added to the repository.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SmallIconUri

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f97d-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f97d-165">CommonParameters</span></span>
<span data-ttu-id="0f97d-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f97d-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f97d-167">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f97d-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f97d-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f97d-168">INPUTS</span></span>

## <span data-ttu-id="0f97d-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f97d-169">OUTPUTS</span></span>

### <span data-ttu-id="0f97d-170">OSImageContext</span><span class="sxs-lookup"><span data-stu-id="0f97d-170">OSImageContext</span></span>

## <span data-ttu-id="0f97d-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f97d-171">NOTES</span></span>

## <span data-ttu-id="0f97d-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f97d-172">RELATED LINKS</span></span>

[<span data-ttu-id="0f97d-173">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="0f97d-173">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="0f97d-174">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="0f97d-174">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="0f97d-175">Mentés-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="0f97d-175">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="0f97d-176">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="0f97d-176">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


