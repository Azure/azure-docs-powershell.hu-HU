---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95DCD2EC-8327-4A46-B624-289D0A28F7EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4614910b8c0ccd36bb8ef75ee98f662cf69a276a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016354"
---
# <span data-ttu-id="a2b62-101">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a2b62-101">Get-AzureDisk</span></span>

## <span data-ttu-id="a2b62-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2b62-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b62-103">Információt kap az Azure Disk repositoryban lévő lemezekről.</span><span class="sxs-lookup"><span data-stu-id="a2b62-103">Gets information about disks in the Azure disk repository.</span></span>

## <span data-ttu-id="a2b62-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2b62-104">SYNTAX</span></span>

```
Get-AzureDisk [[-DiskName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a2b62-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2b62-105">DESCRIPTION</span></span>
<span data-ttu-id="a2b62-106">A **Get-AzureDisk** parancsmag a jelenlegi előfizetés Azure Disk repositoryjában tárolt lemezekről tartalmaz információkat.</span><span class="sxs-lookup"><span data-stu-id="a2b62-106">The **Get-AzureDisk** cmdlet gets information about the disks that are stored in the Azure disk repository for the current subscription.</span></span>
<span data-ttu-id="a2b62-107">Ez a parancsmag a tárház összes lemezére vonatkozó információk listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="a2b62-107">This cmdlet returns a list of information for all disks in the repository.</span></span>
<span data-ttu-id="a2b62-108">Ha meg szeretné tekinteni egy adott lemez adatait, adja meg a lemez nevét.</span><span class="sxs-lookup"><span data-stu-id="a2b62-108">To view information for a specific disk, specify the name of the disk.</span></span>

## <span data-ttu-id="a2b62-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a2b62-109">EXAMPLES</span></span>

### <span data-ttu-id="a2b62-110">1. példa: adatok beszerzése lemezről</span><span class="sxs-lookup"><span data-stu-id="a2b62-110">Example 1: Get information about a disk</span></span>
```
PS C:\> Get-AzureDisk -DiskName "ContosoDataDisk"
```

<span data-ttu-id="a2b62-111">Ez a parancs információkat kap a ContosoDataDisk nevű lemezről az adattárból.</span><span class="sxs-lookup"><span data-stu-id="a2b62-111">This command gets information data about the disk named ContosoDataDisk from the disk repository.</span></span>

### <span data-ttu-id="a2b62-112">2. példa: információk kérése az összes lemezről</span><span class="sxs-lookup"><span data-stu-id="a2b62-112">Example 2: Get information about all disks</span></span>
```
PS C:\> Get-AzureDisk
```

<span data-ttu-id="a2b62-113">Ez a parancs információt kap az összes lemezről a tárházban.</span><span class="sxs-lookup"><span data-stu-id="a2b62-113">This command gets information about all the disks in the disk repository.</span></span>

### <span data-ttu-id="a2b62-114">3. példa: adatok beszerzése lemezről</span><span class="sxs-lookup"><span data-stu-id="a2b62-114">Example 3: Get information about a disk</span></span>
```
PS C:\> Get-AzureDisk | Where-Object {$_.AttachedTo -eq $Null } | Format-Table -AutoSize -Property "DiskName","DiskSizeInGB","MediaLink"
```

<span data-ttu-id="a2b62-115">Ez a parancs a lemezkezelő minden olyan lemezére vonatkozó adatot kap, amely jelenleg nem csatlakozik egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="a2b62-115">This command gets data for all of the disks in the disk repository that are not currently attached to a virtual machine.</span></span>
<span data-ttu-id="a2b62-116">A parancs minden lemezről információt kap, és az egyes objektumokat átadja a **Where-Object** parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="a2b62-116">The command gets information about all of the disks, and passes each object to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="a2b62-117">Ez a parancsmag olyan lemezekre esik, amelyek nem rendelkeznek $Null értékkel a **AttachedTo** tulajdonságban.</span><span class="sxs-lookup"><span data-stu-id="a2b62-117">That cmdlet drops any disk that does not have a value of $Null for the **AttachedTo** property.</span></span>
<span data-ttu-id="a2b62-118">A parancs táblázatként formázza a listát a **Format-Table** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="a2b62-118">The command formats the list as a table by using the **Format-Table** cmdlet.</span></span>

## <span data-ttu-id="a2b62-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2b62-119">PARAMETERS</span></span>

### <span data-ttu-id="a2b62-120">-DiskName</span><span class="sxs-lookup"><span data-stu-id="a2b62-120">-DiskName</span></span>
<span data-ttu-id="a2b62-121">Megadja annak a lemeznek a nevét, amelyről a parancsmag információt kap.</span><span class="sxs-lookup"><span data-stu-id="a2b62-121">Specifies the name of the disk in the disk repository about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="a2b62-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a2b62-122">-InformationAction</span></span>
<span data-ttu-id="a2b62-123">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="a2b62-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a2b62-124">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a2b62-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a2b62-125">Folytassa</span><span class="sxs-lookup"><span data-stu-id="a2b62-125">Continue</span></span>
- <span data-ttu-id="a2b62-126">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="a2b62-126">Ignore</span></span>
- <span data-ttu-id="a2b62-127">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="a2b62-127">Inquire</span></span>
- <span data-ttu-id="a2b62-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a2b62-128">SilentlyContinue</span></span>
- <span data-ttu-id="a2b62-129">állj</span><span class="sxs-lookup"><span data-stu-id="a2b62-129">Stop</span></span>
- <span data-ttu-id="a2b62-130">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="a2b62-130">Suspend</span></span>

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

### <span data-ttu-id="a2b62-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a2b62-131">-InformationVariable</span></span>
<span data-ttu-id="a2b62-132">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="a2b62-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a2b62-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="a2b62-133">-Profile</span></span>
<span data-ttu-id="a2b62-134">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="a2b62-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a2b62-135">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="a2b62-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a2b62-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b62-136">CommonParameters</span></span>
<span data-ttu-id="a2b62-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2b62-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b62-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2b62-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b62-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2b62-139">INPUTS</span></span>

## <span data-ttu-id="a2b62-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2b62-140">OUTPUTS</span></span>

## <span data-ttu-id="a2b62-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2b62-141">NOTES</span></span>

## <span data-ttu-id="a2b62-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2b62-142">RELATED LINKS</span></span>

[<span data-ttu-id="a2b62-143">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a2b62-143">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="a2b62-144">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a2b62-144">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)

[<span data-ttu-id="a2b62-145">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a2b62-145">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


