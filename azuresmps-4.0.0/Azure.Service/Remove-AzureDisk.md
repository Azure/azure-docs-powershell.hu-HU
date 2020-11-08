---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 75A50C59-28D1-4D29-A420-D24BF479F79E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29e5e7e0bc2fcc0ce93186cf966f18d6c9c3e372
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016157"
---
# <span data-ttu-id="7cf14-101">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="7cf14-101">Remove-AzureDisk</span></span>

## <span data-ttu-id="7cf14-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7cf14-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf14-103">Lemez eltávolítása az Azure Disk repositoryból.</span><span class="sxs-lookup"><span data-stu-id="7cf14-103">Removes a disk from the Azure disk repository.</span></span>

## <span data-ttu-id="7cf14-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7cf14-104">SYNTAX</span></span>

```
Remove-AzureDisk [-DiskName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7cf14-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7cf14-105">DESCRIPTION</span></span>
<span data-ttu-id="7cf14-106">A **Remove-AzureDisk** parancsmag a jelenlegi előfizetésben az Azure Disk repositoryból távolítja el a lemezt.</span><span class="sxs-lookup"><span data-stu-id="7cf14-106">The **Remove-AzureDisk** cmdlet removes a disk from the Azure disk repository in the current subscription.</span></span>
<span data-ttu-id="7cf14-107">Ez a parancsmag alapértelmezés szerint nem törli a blob-tárolóból származó virtuális merevlemezt (VHD-fájlt).</span><span class="sxs-lookup"><span data-stu-id="7cf14-107">By default, this cmdlet does not delete the virtual hard disk (VHD) file from blob storage.</span></span>
<span data-ttu-id="7cf14-108">A VHD törléséhez adja meg a *DeleteVHD* paramétert.</span><span class="sxs-lookup"><span data-stu-id="7cf14-108">To delete the VHD, specify the *DeleteVHD* parameter.</span></span>

## <span data-ttu-id="7cf14-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7cf14-109">EXAMPLES</span></span>

### <span data-ttu-id="7cf14-110">1. példa: lemez eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7cf14-110">Example 1: Remove a disk</span></span>
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk"
```

<span data-ttu-id="7cf14-111">Ez a parancs eltávolítja a ContosoDataDisk Disk nevű lemezt a repositoryból.</span><span class="sxs-lookup"><span data-stu-id="7cf14-111">This command removes the disk named ContosoDataDisk disk from the disk repository.</span></span>
<span data-ttu-id="7cf14-112">A parancs nem törli a VHD-t.</span><span class="sxs-lookup"><span data-stu-id="7cf14-112">The command does not delete the VHD.</span></span>

### <span data-ttu-id="7cf14-113">2. példa: lemez eltávolítása és törlése</span><span class="sxs-lookup"><span data-stu-id="7cf14-113">Example 2: Remove and delete a disk</span></span>
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk" -DeleteVHD
```

<span data-ttu-id="7cf14-114">Ez a parancs eltávolítja a ContosoDataDisk Disk nevű lemezt a repositoryból.</span><span class="sxs-lookup"><span data-stu-id="7cf14-114">This command removes the disk named ContosoDataDisk disk from the disk repository.</span></span>
<span data-ttu-id="7cf14-115">Ez a parancs a DeleteVHD paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="7cf14-115">This command specifies the DeleteVHD parameter.</span></span>
<span data-ttu-id="7cf14-116">Ezért a parancs a VHD-fájlból törli a VHD-t.</span><span class="sxs-lookup"><span data-stu-id="7cf14-116">Therefore, the command deletes the VHD from Azure Storage.</span></span>

## <span data-ttu-id="7cf14-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7cf14-117">PARAMETERS</span></span>

### <span data-ttu-id="7cf14-118">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="7cf14-118">-DeleteVHD</span></span>
<span data-ttu-id="7cf14-119">Azt jelzi, hogy ez a parancsmag eltávolítja a VHD-t a blob-tárolóból.</span><span class="sxs-lookup"><span data-stu-id="7cf14-119">Indicates that this cmdlet removes the VHD from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf14-120">-DiskName</span><span class="sxs-lookup"><span data-stu-id="7cf14-120">-DiskName</span></span>
<span data-ttu-id="7cf14-121">Itt adhatja meg annak az adatlemeznek a nevét, amely a parancsmag által eltávolított tárolóban van.</span><span class="sxs-lookup"><span data-stu-id="7cf14-121">Specifies the name of the data disk in the disk repository that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7cf14-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7cf14-122">-InformationAction</span></span>
<span data-ttu-id="7cf14-123">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="7cf14-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7cf14-124">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7cf14-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7cf14-125">Folytassa</span><span class="sxs-lookup"><span data-stu-id="7cf14-125">Continue</span></span>
- <span data-ttu-id="7cf14-126">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="7cf14-126">Ignore</span></span>
- <span data-ttu-id="7cf14-127">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="7cf14-127">Inquire</span></span>
- <span data-ttu-id="7cf14-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7cf14-128">SilentlyContinue</span></span>
- <span data-ttu-id="7cf14-129">állj</span><span class="sxs-lookup"><span data-stu-id="7cf14-129">Stop</span></span>
- <span data-ttu-id="7cf14-130">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="7cf14-130">Suspend</span></span>

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

### <span data-ttu-id="7cf14-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7cf14-131">-InformationVariable</span></span>
<span data-ttu-id="7cf14-132">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="7cf14-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7cf14-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="7cf14-133">-Profile</span></span>
<span data-ttu-id="7cf14-134">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="7cf14-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7cf14-135">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="7cf14-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7cf14-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf14-136">CommonParameters</span></span>
<span data-ttu-id="7cf14-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7cf14-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf14-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cf14-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf14-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cf14-139">INPUTS</span></span>

## <span data-ttu-id="7cf14-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cf14-140">OUTPUTS</span></span>

## <span data-ttu-id="7cf14-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7cf14-141">NOTES</span></span>

## <span data-ttu-id="7cf14-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cf14-142">RELATED LINKS</span></span>

[<span data-ttu-id="7cf14-143">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="7cf14-143">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="7cf14-144">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="7cf14-144">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="7cf14-145">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="7cf14-145">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


