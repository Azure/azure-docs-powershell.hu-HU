---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 849714BC-8B19-453E-B790-A9C38F9D48CB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ef8bd3b1fef6a3af01193a104f6917c4131064f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015425"
---
# <span data-ttu-id="b6fdc-101">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="b6fdc-101">Update-AzureDisk</span></span>

## <span data-ttu-id="b6fdc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6fdc-102">SYNOPSIS</span></span>
<span data-ttu-id="b6fdc-103">Az Azure Disk repositoryban módosítja a lemez feliratát.</span><span class="sxs-lookup"><span data-stu-id="b6fdc-103">Changes the label of a disk in the Azure disk repository.</span></span>

## <span data-ttu-id="b6fdc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6fdc-104">SYNTAX</span></span>

### <span data-ttu-id="b6fdc-105">Átméretezése</span><span class="sxs-lookup"><span data-stu-id="b6fdc-105">Resize</span></span>
```
Update-AzureDisk [-DiskName] <String> [[-Label] <String>] [-ResizedSizeInGB] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6fdc-106">Átméretezés</span><span class="sxs-lookup"><span data-stu-id="b6fdc-106">NoResize</span></span>
```
Update-AzureDisk [-DiskName] <String> [-Label] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b6fdc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6fdc-107">DESCRIPTION</span></span>
<span data-ttu-id="b6fdc-108">Az **Update-AzureDisk** parancsmag az aktuális Azure-előfizetés lemezéhez társított címkét módosítja.</span><span class="sxs-lookup"><span data-stu-id="b6fdc-108">The **Update-AzureDisk** cmdlet changes the label that is associated with a disk in the disk repository of the current Azure subscription.</span></span>

## <span data-ttu-id="b6fdc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b6fdc-109">EXAMPLES</span></span>

### <span data-ttu-id="b6fdc-110">Példa 1: a lemez címkéjének módosítása</span><span class="sxs-lookup"><span data-stu-id="b6fdc-110">Example 1: Change the label of a disk</span></span>
```
PS C:\> Update-AzureDisk ?DiskName "ContosoOSDisk" -Label "DoNotUse"
```

<span data-ttu-id="b6fdc-111">Ez a parancs megváltoztatja a ContosoOSDisk nevű lemez DoNotUse.</span><span class="sxs-lookup"><span data-stu-id="b6fdc-111">This command changes the label of the disk named ContosoOSDisk to DoNotUse.</span></span>

## <span data-ttu-id="b6fdc-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6fdc-112">PARAMETERS</span></span>

### <span data-ttu-id="b6fdc-113">-DiskName</span><span class="sxs-lookup"><span data-stu-id="b6fdc-113">-DiskName</span></span>
<span data-ttu-id="b6fdc-114">Annak a lemeznek a neve, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="b6fdc-114">Specifies the name of the disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b6fdc-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b6fdc-115">-InformationAction</span></span>
<span data-ttu-id="b6fdc-116">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="b6fdc-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b6fdc-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b6fdc-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b6fdc-118">Folytassa</span><span class="sxs-lookup"><span data-stu-id="b6fdc-118">Continue</span></span>
- <span data-ttu-id="b6fdc-119">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="b6fdc-119">Ignore</span></span>
- <span data-ttu-id="b6fdc-120">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="b6fdc-120">Inquire</span></span>
- <span data-ttu-id="b6fdc-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b6fdc-121">SilentlyContinue</span></span>
- <span data-ttu-id="b6fdc-122">állj</span><span class="sxs-lookup"><span data-stu-id="b6fdc-122">Stop</span></span>
- <span data-ttu-id="b6fdc-123">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="b6fdc-123">Suspend</span></span>

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

### <span data-ttu-id="b6fdc-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b6fdc-124">-InformationVariable</span></span>
<span data-ttu-id="b6fdc-125">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="b6fdc-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b6fdc-126">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="b6fdc-126">-Label</span></span>
<span data-ttu-id="b6fdc-127">A lemez új címkéjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6fdc-127">Specifies the new label for the disk.</span></span>

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoResize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6fdc-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="b6fdc-128">-Profile</span></span>
<span data-ttu-id="b6fdc-129">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b6fdc-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b6fdc-130">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b6fdc-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b6fdc-131">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="b6fdc-131">-ResizedSizeInGB</span></span>
<span data-ttu-id="b6fdc-132">A lemez új méretét adja meg gigabájtban.</span><span class="sxs-lookup"><span data-stu-id="b6fdc-132">Specifies the new size, in gigabytes, for the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6fdc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6fdc-133">CommonParameters</span></span>
<span data-ttu-id="b6fdc-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6fdc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6fdc-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6fdc-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6fdc-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6fdc-136">INPUTS</span></span>

## <span data-ttu-id="b6fdc-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6fdc-137">OUTPUTS</span></span>

### <span data-ttu-id="b6fdc-138">DiskContext</span><span class="sxs-lookup"><span data-stu-id="b6fdc-138">DiskContext</span></span>

## <span data-ttu-id="b6fdc-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6fdc-139">NOTES</span></span>

## <span data-ttu-id="b6fdc-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6fdc-140">RELATED LINKS</span></span>

[<span data-ttu-id="b6fdc-141">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="b6fdc-141">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="b6fdc-142">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="b6fdc-142">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="b6fdc-143">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="b6fdc-143">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)


