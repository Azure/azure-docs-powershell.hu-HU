---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DBC4A0B8-A34A-47AC-930B-EFE23A95A216
online version: ''
schema: 2.0.0
ms.openlocfilehash: 178349299767eefb1d89c31a0199f53373bd2ae2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015995"
---
# <span data-ttu-id="cf064-101">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="cf064-101">New-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="cf064-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf064-102">SYNOPSIS</span></span>
<span data-ttu-id="cf064-103">Azure RemoteApp-sablon feltöltése vagy importálása</span><span class="sxs-lookup"><span data-stu-id="cf064-103">Uploads or imports an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="cf064-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf064-104">SYNTAX</span></span>

### <span data-ttu-id="cf064-105">UploadLocalVhd (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cf064-105">UploadLocalVhd (Default)</span></span>
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> [-Path] <String> [-Resume]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cf064-106">AzureVmUpload</span><span class="sxs-lookup"><span data-stu-id="cf064-106">AzureVmUpload</span></span>
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> -AzureVmImageName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cf064-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf064-107">DESCRIPTION</span></span>
<span data-ttu-id="cf064-108">A **New-AzureRemoteAppTemplateImage** parancsmag az Azure RemoteApp-sablon képét tölti fel vagy importálja.</span><span class="sxs-lookup"><span data-stu-id="cf064-108">The **New-AzureRemoteAppTemplateImage** cmdlet uploads or imports an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="cf064-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cf064-109">EXAMPLES</span></span>

### <span data-ttu-id="cf064-110">1. példa: egy VHD-fájl feltöltése sablon létrehozásához</span><span class="sxs-lookup"><span data-stu-id="cf064-110">Example 1: Upload a VHD file to create a template image</span></span>
```
PS C:\> New-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -Location "North Europe" -Path "C:\RemoteAppImages\ContosoApps.vhd"
```

<span data-ttu-id="cf064-111">Ez a parancs feltölti a C:\RemoteAppImages\ContosoApps.vhd, hogy az Észak-Európa adatközpontban hozzon létre egy ContosoApps nevű sablont.</span><span class="sxs-lookup"><span data-stu-id="cf064-111">This command uploads C:\RemoteAppImages\ContosoApps.vhd to create a template image named ContosoApps in the North Europe data center.</span></span>

## <span data-ttu-id="cf064-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf064-112">PARAMETERS</span></span>

### <span data-ttu-id="cf064-113">-AzureVmImageName</span><span class="sxs-lookup"><span data-stu-id="cf064-113">-AzureVmImageName</span></span>
<span data-ttu-id="cf064-114">A sablonként használt Azure Virtual Machine-gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf064-114">Specifies the name of an Azure virtual machine to use as a template image.</span></span>

```yaml
Type: String
Parameter Sets: AzureVmUpload
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf064-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="cf064-115">-ImageName</span></span>
<span data-ttu-id="cf064-116">Egy Azure RemoteApp-sablon nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf064-116">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf064-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="cf064-117">-Location</span></span>
<span data-ttu-id="cf064-118">A sablonnak az Azure-régióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf064-118">Specifies the Azure region of the template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf064-119">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="cf064-119">-Path</span></span>
<span data-ttu-id="cf064-120">A sablon képének elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf064-120">Specifies the file path of the template image.</span></span>

```yaml
Type: String
Parameter Sets: UploadLocalVhd
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf064-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="cf064-121">-Profile</span></span>
<span data-ttu-id="cf064-122">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="cf064-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cf064-123">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="cf064-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cf064-124">– Önéletrajz</span><span class="sxs-lookup"><span data-stu-id="cf064-124">-Resume</span></span>
<span data-ttu-id="cf064-125">Jelzi, hogy ez a parancsmag akkor indul el, ha egy sablon képe megszakad.</span><span class="sxs-lookup"><span data-stu-id="cf064-125">Indicates that this cmdlet resumes if the upload of a template image is interrupted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UploadLocalVhd
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf064-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf064-126">CommonParameters</span></span>
<span data-ttu-id="cf064-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf064-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf064-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf064-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf064-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf064-129">INPUTS</span></span>

## <span data-ttu-id="cf064-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf064-130">OUTPUTS</span></span>

## <span data-ttu-id="cf064-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf064-131">NOTES</span></span>

## <span data-ttu-id="cf064-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf064-132">RELATED LINKS</span></span>

[<span data-ttu-id="cf064-133">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="cf064-133">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="cf064-134">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="cf064-134">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="cf064-135">Rename-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="cf064-135">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


