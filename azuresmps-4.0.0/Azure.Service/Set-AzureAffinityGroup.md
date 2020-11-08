---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B2C7E454-F38F-4139-ADA2-D1C59C03CC50
online version: ''
schema: 2.0.0
ms.openlocfilehash: efa519c380ffa78f44e8ac6edebda284a4ce3cd0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016431"
---
# <span data-ttu-id="7282f-101">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="7282f-101">Set-AzureAffinityGroup</span></span>

## <span data-ttu-id="7282f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7282f-102">SYNOPSIS</span></span>
<span data-ttu-id="7282f-103">Egy affinitási csoport tulajdonságainak módosítása</span><span class="sxs-lookup"><span data-stu-id="7282f-103">Modifies properties of an affinity group.</span></span>

## <span data-ttu-id="7282f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7282f-104">SYNTAX</span></span>

```
Set-AzureAffinityGroup [-Name] <String> -Label <String> [-Description <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7282f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7282f-105">DESCRIPTION</span></span>
<span data-ttu-id="7282f-106">A **set-AzureAffinityGroup** parancsmag az Azure affinitás csoport tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="7282f-106">The **Set-AzureAffinityGroup** cmdlet modifies properties of an Azure affinity group.</span></span>
<span data-ttu-id="7282f-107">Módosíthatja a címkét és a leírást.</span><span class="sxs-lookup"><span data-stu-id="7282f-107">You can change the label and the description.</span></span>

## <span data-ttu-id="7282f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="7282f-108">EXAMPLES</span></span>

### <span data-ttu-id="7282f-109">Példa 1: affinitás csoport módosítása</span><span class="sxs-lookup"><span data-stu-id="7282f-109">Example 1: Modify an affinity group</span></span>
```
PS C:\> Set-AzureAffinityGroup -Name "South01" -Label "SouthUSProduction" -Description "Production applications for Southern US locations"
```

<span data-ttu-id="7282f-110">Ez a parancs módosítja a South01 nevű affinitási csoport címkéjét, a SouthUSProduction a parancs a leírást is módosítja.</span><span class="sxs-lookup"><span data-stu-id="7282f-110">This command modifies the label of the affinity group named South01 to be SouthUSProduction The command also modifies the description.</span></span>

## <span data-ttu-id="7282f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7282f-111">PARAMETERS</span></span>

### <span data-ttu-id="7282f-112">-Leírás</span><span class="sxs-lookup"><span data-stu-id="7282f-112">-Description</span></span>
<span data-ttu-id="7282f-113">A affinitás csoport leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="7282f-113">Specifies the description of the affinity group.</span></span>
<span data-ttu-id="7282f-114">A Leírás legfeljebb 1024 karakter hosszú lehet.</span><span class="sxs-lookup"><span data-stu-id="7282f-114">The description can be up to 1024 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7282f-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7282f-115">-InformationAction</span></span>
<span data-ttu-id="7282f-116">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="7282f-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7282f-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7282f-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7282f-118">Folytassa</span><span class="sxs-lookup"><span data-stu-id="7282f-118">Continue</span></span>
- <span data-ttu-id="7282f-119">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="7282f-119">Ignore</span></span>
- <span data-ttu-id="7282f-120">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="7282f-120">Inquire</span></span>
- <span data-ttu-id="7282f-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7282f-121">SilentlyContinue</span></span>
- <span data-ttu-id="7282f-122">állj</span><span class="sxs-lookup"><span data-stu-id="7282f-122">Stop</span></span>
- <span data-ttu-id="7282f-123">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="7282f-123">Suspend</span></span>

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

### <span data-ttu-id="7282f-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7282f-124">-InformationVariable</span></span>
<span data-ttu-id="7282f-125">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="7282f-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7282f-126">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="7282f-126">-Label</span></span>
<span data-ttu-id="7282f-127">Az affinitás csoport címkéjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7282f-127">Specifies a label for the affinity group.</span></span>
<span data-ttu-id="7282f-128">A címke legfeljebb 100 karakter hosszú lehet.</span><span class="sxs-lookup"><span data-stu-id="7282f-128">The label can be up to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7282f-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7282f-129">-Name</span></span>
<span data-ttu-id="7282f-130">A parancsmag által módosított affinitási csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7282f-130">Specifies the name of the affinity group that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7282f-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="7282f-131">-Profile</span></span>
<span data-ttu-id="7282f-132">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="7282f-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7282f-133">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="7282f-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7282f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7282f-134">CommonParameters</span></span>
<span data-ttu-id="7282f-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7282f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7282f-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7282f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7282f-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7282f-137">INPUTS</span></span>

## <span data-ttu-id="7282f-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7282f-138">OUTPUTS</span></span>

## <span data-ttu-id="7282f-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7282f-139">NOTES</span></span>

## <span data-ttu-id="7282f-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7282f-140">RELATED LINKS</span></span>

[<span data-ttu-id="7282f-141">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="7282f-141">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="7282f-142">Új – AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="7282f-142">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="7282f-143">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="7282f-143">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)


