---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 54C89A5F-BF94-468C-92E7-224808FDD0EC
online version: ''
schema: 2.0.0
ms.openlocfilehash: be84995e4826b79befc6282133d70f3ee4a79b4f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016227"
---
# <span data-ttu-id="e11bd-101">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="e11bd-101">New-AzureAffinityGroup</span></span>

## <span data-ttu-id="e11bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e11bd-102">SYNOPSIS</span></span>
<span data-ttu-id="e11bd-103">Affinitási csoportot hoz létre a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="e11bd-103">Creates an affinity group in the current subscription.</span></span>

## <span data-ttu-id="e11bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e11bd-104">SYNTAX</span></span>

```
New-AzureAffinityGroup [-Name] <String> [-Label <String>] [-Description <String>] -Location <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="e11bd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e11bd-105">DESCRIPTION</span></span>
<span data-ttu-id="e11bd-106">A **New-AzureAffinityGroup** parancsmag az Azure affinitás csoportot az aktuális Azure-előfizetésből hozza létre.</span><span class="sxs-lookup"><span data-stu-id="e11bd-106">The **New-AzureAffinityGroup** cmdlet creates an Azure affinity group in the current Azure subscription.</span></span>

<span data-ttu-id="e11bd-107">Az affinitás csoport a szolgáltatásokat és az erőforrásokat egy Azure Datacenter-adatközpontban helyezi el együtt.</span><span class="sxs-lookup"><span data-stu-id="e11bd-107">An affinity group puts your services and their resources together in an Azure datacenter.</span></span>
<span data-ttu-id="e11bd-108">Az affinitás csoport tagjai az optimális teljesítmény érdekében csoportosítják a tagokat.</span><span class="sxs-lookup"><span data-stu-id="e11bd-108">The affinity group groups members together for optimal performance.</span></span>
<span data-ttu-id="e11bd-109">Adjon meg affinitási csoportokat az előfizetési szinten.</span><span class="sxs-lookup"><span data-stu-id="e11bd-109">Define affinity groups at the subscription level.</span></span>
<span data-ttu-id="e11bd-110">Az affinitási csoportok az Ön által létrehozott minden további felhőalapú szolgáltatásban vagy tárolási fiókban elérhetők.</span><span class="sxs-lookup"><span data-stu-id="e11bd-110">Your affinity groups are available to any subsequent cloud services or storage accounts that you create.</span></span>
<span data-ttu-id="e11bd-111">Csak akkor vehet fel szolgáltatásokat az affinitás csoportba, amikor létrehozta.</span><span class="sxs-lookup"><span data-stu-id="e11bd-111">You can add services to an affinity group only when you create it.</span></span>

## <span data-ttu-id="e11bd-112">Példák</span><span class="sxs-lookup"><span data-stu-id="e11bd-112">EXAMPLES</span></span>

### <span data-ttu-id="e11bd-113">1. példa: affinitási csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="e11bd-113">Example 1: Create an affinity group</span></span>
```
PS C:\> New-AzureAffinityGroup -Name "South01" -Location "South Central US" -Label "South Region" -Description "Affinity group for production applications in southern region."
```

<span data-ttu-id="e11bd-114">Ez a parancs létrehoz egy South01 nevű affinitási csoportot a dél-közép-amerikai régióban.</span><span class="sxs-lookup"><span data-stu-id="e11bd-114">This command creates an affinity group named South01 in the South Central US region.</span></span>
<span data-ttu-id="e11bd-115">A parancs egy címkét és egy leírást ad meg.</span><span class="sxs-lookup"><span data-stu-id="e11bd-115">The command specifies a label and a description.</span></span>

## <span data-ttu-id="e11bd-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e11bd-116">PARAMETERS</span></span>

### <span data-ttu-id="e11bd-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="e11bd-117">-Description</span></span>
<span data-ttu-id="e11bd-118">A affinitás csoport leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="e11bd-118">Specifies a description for the affinity group.</span></span>
<span data-ttu-id="e11bd-119">Lehet, hogy a Leírás legfeljebb 1024 karakter hosszú lehet.</span><span class="sxs-lookup"><span data-stu-id="e11bd-119">The description may be up to 1024 characters long.</span></span>

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

### <span data-ttu-id="e11bd-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e11bd-120">-InformationAction</span></span>
<span data-ttu-id="e11bd-121">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="e11bd-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e11bd-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e11bd-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e11bd-123">Folytassa</span><span class="sxs-lookup"><span data-stu-id="e11bd-123">Continue</span></span>
- <span data-ttu-id="e11bd-124">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="e11bd-124">Ignore</span></span>
- <span data-ttu-id="e11bd-125">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="e11bd-125">Inquire</span></span>
- <span data-ttu-id="e11bd-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e11bd-126">SilentlyContinue</span></span>
- <span data-ttu-id="e11bd-127">állj</span><span class="sxs-lookup"><span data-stu-id="e11bd-127">Stop</span></span>
- <span data-ttu-id="e11bd-128">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="e11bd-128">Suspend</span></span>

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

### <span data-ttu-id="e11bd-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e11bd-129">-InformationVariable</span></span>
<span data-ttu-id="e11bd-130">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="e11bd-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e11bd-131">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="e11bd-131">-Label</span></span>
<span data-ttu-id="e11bd-132">Az affinitás csoport címkéjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e11bd-132">Specifies a label for the affinity group.</span></span>
<span data-ttu-id="e11bd-133">Előfordulhat, hogy a címke legfeljebb 100 karakter hosszú lehet.</span><span class="sxs-lookup"><span data-stu-id="e11bd-133">The label may be up to 100 characters long.</span></span>

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

### <span data-ttu-id="e11bd-134">-Hely</span><span class="sxs-lookup"><span data-stu-id="e11bd-134">-Location</span></span>
<span data-ttu-id="e11bd-135">Annak az Azure Datacenter-adatközpontnak a földrajzi helyét adja meg, ahol a parancsmag létrehozta az affinitás csoportot.</span><span class="sxs-lookup"><span data-stu-id="e11bd-135">Specifies the geographical location of the Azure datacenter where this cmdlet creates the affinity group.</span></span>

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

### <span data-ttu-id="e11bd-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e11bd-136">-Name</span></span>
<span data-ttu-id="e11bd-137">A affinitás csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e11bd-137">Specifies a name for the affinity group.</span></span>
<span data-ttu-id="e11bd-138">A névnek egyedinek kell lennie az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="e11bd-138">The name must be unique to the subscription.</span></span>

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

### <span data-ttu-id="e11bd-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="e11bd-139">-Profile</span></span>
<span data-ttu-id="e11bd-140">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="e11bd-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e11bd-141">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="e11bd-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e11bd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e11bd-142">CommonParameters</span></span>
<span data-ttu-id="e11bd-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e11bd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e11bd-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e11bd-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e11bd-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e11bd-145">INPUTS</span></span>

## <span data-ttu-id="e11bd-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e11bd-146">OUTPUTS</span></span>

## <span data-ttu-id="e11bd-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e11bd-147">NOTES</span></span>

## <span data-ttu-id="e11bd-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e11bd-148">RELATED LINKS</span></span>

[<span data-ttu-id="e11bd-149">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="e11bd-149">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="e11bd-150">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="e11bd-150">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)

[<span data-ttu-id="e11bd-151">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="e11bd-151">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


