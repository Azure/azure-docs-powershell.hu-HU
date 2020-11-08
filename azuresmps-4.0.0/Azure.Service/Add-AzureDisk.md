---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 16A34F31-1C61-4911-8C1F-9F82683524A1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 775d2deff8a83e758d48fb9328bf4156b142d20c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016393"
---
# <span data-ttu-id="61ee5-101">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="61ee5-101">Add-AzureDisk</span></span>

## <span data-ttu-id="61ee5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="61ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="61ee5-103">Lemez hozzáadása az Azure Disk repositoryhoz.</span><span class="sxs-lookup"><span data-stu-id="61ee5-103">Adds a disk to the Azure disk repository.</span></span>

## <span data-ttu-id="61ee5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="61ee5-104">SYNTAX</span></span>

```
Add-AzureDisk [-DiskName] <String> [-MediaLocation] <String> [-Label <String>] [-OS <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="61ee5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="61ee5-105">DESCRIPTION</span></span>
<span data-ttu-id="61ee5-106">Az **Add-AzureDisk** parancsmag a jelenlegi előfizetésben az Azure Disk repositoryba helyezi a lemezt.</span><span class="sxs-lookup"><span data-stu-id="61ee5-106">The **Add-AzureDisk** cmdlet adds a disk to the Azure disk repository in the current subscription.</span></span>
<span data-ttu-id="61ee5-107">Ez a parancsmag rendszerlemez vagy adatlemez hozzáadására használható.</span><span class="sxs-lookup"><span data-stu-id="61ee5-107">This cmdlet can add a system disk or a data disk.</span></span>
<span data-ttu-id="61ee5-108">Rendszerlemez hozzáadásához *az operációs rendszer paraméter segítségével* adja meg az operációs rendszer típusát.</span><span class="sxs-lookup"><span data-stu-id="61ee5-108">To add a system disk, specify an operating system type by using the *OS* parameter.</span></span>

## <span data-ttu-id="61ee5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="61ee5-109">EXAMPLES</span></span>

### <span data-ttu-id="61ee5-110">1. példa: a Windows operációs rendszert használó indítólemez hozzáadása</span><span class="sxs-lookup"><span data-stu-id="61ee5-110">Example 1: Add a startup disk that uses the Windows operating system</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyWinDisk" -MediaLocation "http://contosostorage.blob.core.azure.com/vhds/winserver-system.vhd" -Label "StartupDisk" -OS "Windows"
```

<span data-ttu-id="61ee5-111">Ez a parancs rendszerlemezt ad hozzá a merevlemez-tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="61ee5-111">This command adds a system disk to your disk repository.</span></span>
<span data-ttu-id="61ee5-112">A rendszerlemez a Windows operációs rendszert használja.</span><span class="sxs-lookup"><span data-stu-id="61ee5-112">The system disk uses the Windows operating system.</span></span>

### <span data-ttu-id="61ee5-113">2. példa: adatlemez hozzáadása</span><span class="sxs-lookup"><span data-stu-id="61ee5-113">Example 2: Add a data disk</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyDataDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/winserver-data.vhd" -Label "DataDisk"
```

<span data-ttu-id="61ee5-114">Ez a parancs adatlemezt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="61ee5-114">This command adds a data disk.</span></span>

### <span data-ttu-id="61ee5-115">3. példa: Linux rendszerlemez hozzáadása</span><span class="sxs-lookup"><span data-stu-id="61ee5-115">Example 3: Add a Linux system disk</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyLinuxDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/linuxsys.vhd" -OS "Linux"
```

<span data-ttu-id="61ee5-116">Ez a parancs egy Linux rendszerű rendszerlemezt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="61ee5-116">This command adds a Linux system disk.</span></span>

## <span data-ttu-id="61ee5-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="61ee5-117">PARAMETERS</span></span>

### <span data-ttu-id="61ee5-118">-DiskName</span><span class="sxs-lookup"><span data-stu-id="61ee5-118">-DiskName</span></span>
<span data-ttu-id="61ee5-119">Annak a lemeznek a neve, amely a parancsmagot adja.</span><span class="sxs-lookup"><span data-stu-id="61ee5-119">Specifies the name of the disk that this cmdlet adds.</span></span>

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

### <span data-ttu-id="61ee5-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="61ee5-120">-InformationAction</span></span>
<span data-ttu-id="61ee5-121">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="61ee5-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="61ee5-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="61ee5-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="61ee5-123">Folytassa</span><span class="sxs-lookup"><span data-stu-id="61ee5-123">Continue</span></span>
- <span data-ttu-id="61ee5-124">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="61ee5-124">Ignore</span></span>
- <span data-ttu-id="61ee5-125">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="61ee5-125">Inquire</span></span>
- <span data-ttu-id="61ee5-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="61ee5-126">SilentlyContinue</span></span>
- <span data-ttu-id="61ee5-127">állj</span><span class="sxs-lookup"><span data-stu-id="61ee5-127">Stop</span></span>
- <span data-ttu-id="61ee5-128">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="61ee5-128">Suspend</span></span>

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

### <span data-ttu-id="61ee5-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="61ee5-129">-InformationVariable</span></span>
<span data-ttu-id="61ee5-130">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="61ee5-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="61ee5-131">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="61ee5-131">-Label</span></span>
<span data-ttu-id="61ee5-132">Megadja a parancsmag által hozzáadott lemez címkéjét.</span><span class="sxs-lookup"><span data-stu-id="61ee5-132">Specifies a disk label for the disk that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61ee5-133">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="61ee5-133">-MediaLocation</span></span>
<span data-ttu-id="61ee5-134">A lemez fizikai helyét az Azure Storage szolgáltatásban adja meg.</span><span class="sxs-lookup"><span data-stu-id="61ee5-134">Specifies the physical location of the disk in Azure Storage.</span></span>
<span data-ttu-id="61ee5-135">Ez az érték az aktuális előfizetés és a tároló fiók blob lapjára hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="61ee5-135">This value refers to a blob page in the current subscription and storage account.</span></span>

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

### <span data-ttu-id="61ee5-136">-OS</span><span class="sxs-lookup"><span data-stu-id="61ee5-136">-OS</span></span>
<span data-ttu-id="61ee5-137">A rendszerlemez operációs rendszerének típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="61ee5-137">Specifies the operating system type for a system disk.</span></span>
<span data-ttu-id="61ee5-138">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="61ee5-138">Valid values are:</span></span> 

- <span data-ttu-id="61ee5-139">Windows</span><span class="sxs-lookup"><span data-stu-id="61ee5-139">Windows</span></span> 
- <span data-ttu-id="61ee5-140">Linux</span><span class="sxs-lookup"><span data-stu-id="61ee5-140">Linux</span></span> 

<span data-ttu-id="61ee5-141">Ha nem adja meg ezt a paramétert, a parancsmag adatlemezként hozzáadja a lemezt.</span><span class="sxs-lookup"><span data-stu-id="61ee5-141">If you do not specify this parameter, the cmdlet adds the disk as a data disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61ee5-142">-Profil</span><span class="sxs-lookup"><span data-stu-id="61ee5-142">-Profile</span></span>
<span data-ttu-id="61ee5-143">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="61ee5-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="61ee5-144">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="61ee5-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="61ee5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ee5-145">CommonParameters</span></span>
<span data-ttu-id="61ee5-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="61ee5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ee5-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61ee5-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ee5-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="61ee5-148">INPUTS</span></span>

## <span data-ttu-id="61ee5-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61ee5-149">OUTPUTS</span></span>

### <span data-ttu-id="61ee5-150">DiskContext</span><span class="sxs-lookup"><span data-stu-id="61ee5-150">DiskContext</span></span>

## <span data-ttu-id="61ee5-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="61ee5-151">NOTES</span></span>

## <span data-ttu-id="61ee5-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61ee5-152">RELATED LINKS</span></span>

[<span data-ttu-id="61ee5-153">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="61ee5-153">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="61ee5-154">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="61ee5-154">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)

[<span data-ttu-id="61ee5-155">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="61ee5-155">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


