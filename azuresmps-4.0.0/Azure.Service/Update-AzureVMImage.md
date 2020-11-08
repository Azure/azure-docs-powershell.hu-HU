---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5544F2E2-27EF-4079-8E13-6B85DF2018A2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a71ad8b25a17c1c2933cdcf305ba0b53f67bf0f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016583"
---
# <span data-ttu-id="497f3-101">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="497f3-101">Update-AzureVMImage</span></span>

## <span data-ttu-id="497f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="497f3-102">SYNOPSIS</span></span>
<span data-ttu-id="497f3-103">A képtárházban frissíti az operációs rendszer képének címkéjét.</span><span class="sxs-lookup"><span data-stu-id="497f3-103">Updates the label of an operating system image in the image repository.</span></span>

## <span data-ttu-id="497f3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="497f3-104">SYNTAX</span></span>

```
Update-AzureVMImage [-ImageName] <String> [-Label] <String> [[-Eula] <String>] [[-Description] <String>]
 [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>]
 [[-DiskConfig] <VirtualMachineImageDiskConfigSet>] [[-Language] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-DontShowInGui] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="497f3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="497f3-105">DESCRIPTION</span></span>
<span data-ttu-id="497f3-106">Az **Update-AzureVMImage** parancsmag a képtárházban lévő operációs rendszer képére frissíti a címkét.</span><span class="sxs-lookup"><span data-stu-id="497f3-106">The **Update-AzureVMImage** cmdlet updates the label on an operating system image in the image repository.</span></span>
<span data-ttu-id="497f3-107">Egy képobjektumot ad eredményül, amely a frissített képpel kapcsolatos információkat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="497f3-107">It returns an image object with information about the updated image.</span></span>

## <span data-ttu-id="497f3-108">Példák</span><span class="sxs-lookup"><span data-stu-id="497f3-108">EXAMPLES</span></span>

### <span data-ttu-id="497f3-109">Példa 1: kép frissítése a képfelirat módosításával</span><span class="sxs-lookup"><span data-stu-id="497f3-109">Example 1: Update an image by changing the image label</span></span>
```
PS C:\> Update-AzureVMImage -ImageName "Windows-Server-2008-SP2" -Label "DoNotUse"
```

<span data-ttu-id="497f3-110">Ez a parancs frissíti a Windows-Server-2008-SP2 lemezképfájlt, ha módosítja a képfeliratot a DoNotUse-ra.</span><span class="sxs-lookup"><span data-stu-id="497f3-110">This command updates the image named Windows-Server-2008-SP2 by changing the image label to DoNotUse.</span></span>

### <span data-ttu-id="497f3-111">2. példa: az összes operációs rendszer beszerzése címke szerint, majd a címke frissítése</span><span class="sxs-lookup"><span data-stu-id="497f3-111">Example 2: Get all operating systems by label and then update the label</span></span>
```
PS C:\> Get-AzureVMImage | Where-Object {$_.Label -eq "DoNotUse" } | Update-AzureVMImage -Label "Updated"
```

<span data-ttu-id="497f3-112">Ez a parancs beolvassa az összes operációs rendszer DoNotUse, és a címkét módosította.</span><span class="sxs-lookup"><span data-stu-id="497f3-112">This command gets all the operating system images labeled DoNotUse and changes the label to Updated.</span></span>

## <span data-ttu-id="497f3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="497f3-113">PARAMETERS</span></span>

### <span data-ttu-id="497f3-114">-Leírás</span><span class="sxs-lookup"><span data-stu-id="497f3-114">-Description</span></span>
<span data-ttu-id="497f3-115">Az operációs rendszer képének leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="497f3-115">Specifies the description of the operating system image.</span></span>

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

### <span data-ttu-id="497f3-116">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="497f3-116">-DiskConfig</span></span>
<span data-ttu-id="497f3-117">A **AzureVMImageDiskConfigSet** , a **set-AzureVMImageOSDiskConfig** és a **set-AzureVMImageDataDiskConfig** parancsmagok használatával létrehozott virtuális gép lemezképfájljának operációs rendszerének és adatlemezének konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="497f3-117">Specifies the operating system disk and data disk configuration for the virtual machine image created by using the **New-AzureVMImageDiskConfigSet** , **Set-AzureVMImageOSDiskConfig** , and **Set-AzureVMImageDataDiskConfig** cmdlets.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="497f3-118">-DontShowInGui</span><span class="sxs-lookup"><span data-stu-id="497f3-118">-DontShowInGui</span></span>
<span data-ttu-id="497f3-119">Jelzi, hogy ez a parancsmag nem jeleníti meg a képet a GUI-ban.</span><span class="sxs-lookup"><span data-stu-id="497f3-119">Indicates that this cmdlet does not show the image in the GUI.</span></span>

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

### <span data-ttu-id="497f3-120">-EULA</span><span class="sxs-lookup"><span data-stu-id="497f3-120">-Eula</span></span>
<span data-ttu-id="497f3-121">A végfelhasználói licencszerződést adja meg.</span><span class="sxs-lookup"><span data-stu-id="497f3-121">Specifies the End User License Agreement.</span></span>
<span data-ttu-id="497f3-122">Azt javasoljuk, hogy az érték egy URL-cím.</span><span class="sxs-lookup"><span data-stu-id="497f3-122">We recommend that the value is a URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="497f3-123">-IconName</span><span class="sxs-lookup"><span data-stu-id="497f3-123">-IconName</span></span>
<span data-ttu-id="497f3-124">Az operációs rendszer vagy a virtuális gép képének normál ikonjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="497f3-124">Specifies the standard icon name for the operating system or virtual machine image.</span></span>

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

### <span data-ttu-id="497f3-125">-ImageFamily</span><span class="sxs-lookup"><span data-stu-id="497f3-125">-ImageFamily</span></span>
<span data-ttu-id="497f3-126">Egy olyan értéket ad meg, amely az operációs rendszer vagy a virtuális gép képeinek csoportosítására használható.</span><span class="sxs-lookup"><span data-stu-id="497f3-126">Specifies a value that can be used to group operating system or virtual machine images.</span></span>

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

### <span data-ttu-id="497f3-127">-ImageName</span><span class="sxs-lookup"><span data-stu-id="497f3-127">-ImageName</span></span>
<span data-ttu-id="497f3-128">A képtárházban frissítendő kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="497f3-128">Specifies the name of the image to update in the image repository.</span></span>

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

### <span data-ttu-id="497f3-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="497f3-129">-InformationAction</span></span>
<span data-ttu-id="497f3-130">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="497f3-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="497f3-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="497f3-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="497f3-132">Folytassa</span><span class="sxs-lookup"><span data-stu-id="497f3-132">Continue</span></span>
- <span data-ttu-id="497f3-133">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="497f3-133">Ignore</span></span>
- <span data-ttu-id="497f3-134">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="497f3-134">Inquire</span></span>
- <span data-ttu-id="497f3-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="497f3-135">SilentlyContinue</span></span>
- <span data-ttu-id="497f3-136">állj</span><span class="sxs-lookup"><span data-stu-id="497f3-136">Stop</span></span>
- <span data-ttu-id="497f3-137">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="497f3-137">Suspend</span></span>

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

### <span data-ttu-id="497f3-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="497f3-138">-InformationVariable</span></span>
<span data-ttu-id="497f3-139">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="497f3-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="497f3-140">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="497f3-140">-Label</span></span>
<span data-ttu-id="497f3-141">A kép új feliratát adja meg.</span><span class="sxs-lookup"><span data-stu-id="497f3-141">Specifies the new label of the image.</span></span>

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

### <span data-ttu-id="497f3-142">-Nyelv</span><span class="sxs-lookup"><span data-stu-id="497f3-142">-Language</span></span>
<span data-ttu-id="497f3-143">Az operációs rendszer nyelvét adja meg a virtuális gép vagy az operációs rendszer képen.</span><span class="sxs-lookup"><span data-stu-id="497f3-143">Specifies the language for the operating system in the virtual machine or operating system image.</span></span>

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

### <span data-ttu-id="497f3-144">-PrivacyUri</span><span class="sxs-lookup"><span data-stu-id="497f3-144">-PrivacyUri</span></span>
<span data-ttu-id="497f3-145">Meghatározza az operációs rendszer képhez kapcsolódó adatvédelmi szabályokat tartalmazó dokumentumra mutató URI-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="497f3-145">Specifies the URI that points to a document that contains the privacy policy related to the operating system image.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="497f3-146">-Profil</span><span class="sxs-lookup"><span data-stu-id="497f3-146">-Profile</span></span>
<span data-ttu-id="497f3-147">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="497f3-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="497f3-148">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="497f3-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="497f3-149">-PublishedDate</span><span class="sxs-lookup"><span data-stu-id="497f3-149">-PublishedDate</span></span>
<span data-ttu-id="497f3-150">Azt a dátumot adja meg, amikor az operációs rendszer képet felvette a képtárházba.</span><span class="sxs-lookup"><span data-stu-id="497f3-150">Specifies the date when the operating system image was added to the image repository.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="497f3-151">-RecommendedVMSize</span><span class="sxs-lookup"><span data-stu-id="497f3-151">-RecommendedVMSize</span></span>
<span data-ttu-id="497f3-152">A virtuális gép méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="497f3-152">Specifies the size of the virtual machine.</span></span>

<span data-ttu-id="497f3-153">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="497f3-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="497f3-154">Közepes</span><span class="sxs-lookup"><span data-stu-id="497f3-154">Medium</span></span>
- <span data-ttu-id="497f3-155">Nagy</span><span class="sxs-lookup"><span data-stu-id="497f3-155">Large</span></span>
- <span data-ttu-id="497f3-156">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="497f3-156">ExtraLarge</span></span>
- <span data-ttu-id="497f3-157">A5</span><span class="sxs-lookup"><span data-stu-id="497f3-157">A5</span></span>
- <span data-ttu-id="497f3-158">A6</span><span class="sxs-lookup"><span data-stu-id="497f3-158">A6</span></span>
- <span data-ttu-id="497f3-159">A7</span><span class="sxs-lookup"><span data-stu-id="497f3-159">A7</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="497f3-160">-SmallIconName</span><span class="sxs-lookup"><span data-stu-id="497f3-160">-SmallIconName</span></span>
<span data-ttu-id="497f3-161">Megadja az operációs rendszer vagy a virtuálisgép-kép kis ikonjának nevét.</span><span class="sxs-lookup"><span data-stu-id="497f3-161">Specifies the small icon name for the operating system or virtual machine image.</span></span>

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

### <span data-ttu-id="497f3-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="497f3-162">CommonParameters</span></span>
<span data-ttu-id="497f3-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="497f3-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="497f3-164">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="497f3-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="497f3-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="497f3-165">INPUTS</span></span>

## <span data-ttu-id="497f3-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="497f3-166">OUTPUTS</span></span>

### <span data-ttu-id="497f3-167">OSImageContext</span><span class="sxs-lookup"><span data-stu-id="497f3-167">OSImageContext</span></span>

## <span data-ttu-id="497f3-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="497f3-168">NOTES</span></span>

## <span data-ttu-id="497f3-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="497f3-169">RELATED LINKS</span></span>

[<span data-ttu-id="497f3-170">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="497f3-170">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="497f3-171">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="497f3-171">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="497f3-172">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="497f3-172">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="497f3-173">Mentés-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="497f3-173">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="497f3-174">Új – AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="497f3-174">New-AzureVMImageDiskConfigSet</span></span>](./New-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="497f3-175">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="497f3-175">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)

[<span data-ttu-id="497f3-176">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="497f3-176">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


