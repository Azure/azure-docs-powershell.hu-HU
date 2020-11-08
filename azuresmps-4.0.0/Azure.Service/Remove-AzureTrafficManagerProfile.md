---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: B96A64DD-9005-4B04-A720-6FCF33797E8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1fa73aa4e38c8d222da6e73508e9a18a15c1e3f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016091"
---
# <span data-ttu-id="d95bb-101">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d95bb-101">Remove-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="d95bb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d95bb-102">SYNOPSIS</span></span>
<span data-ttu-id="d95bb-103">A forgalomirányító-profil eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="d95bb-103">Removes a Traffic Manager profile.</span></span>

## <span data-ttu-id="d95bb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d95bb-104">SYNTAX</span></span>

```
Remove-AzureTrafficManagerProfile -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d95bb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d95bb-105">DESCRIPTION</span></span>
<span data-ttu-id="d95bb-106">A **Remove-AzureTrafficManagerProfile** parancsmag eltávolítja a Microsoft Azure Traffic Manager-profilt a jelenlegi előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="d95bb-106">The **Remove-AzureTrafficManagerProfile** cmdlet removes a Microsoft Azure Traffic Manager profile from the current subscription.</span></span>

## <span data-ttu-id="d95bb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d95bb-107">EXAMPLES</span></span>

### <span data-ttu-id="d95bb-108">1. példa: forgalomirányító-profil eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d95bb-108">Example 1: Remove a Traffic Manager profile</span></span>
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="d95bb-109">Ez a parancs eltávolítja a MyProfile nevű Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="d95bb-109">This command removes the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="d95bb-110">2. példa: a Traffic Manager-profil eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d95bb-110">Example 2: Remove a Traffic Manager profile</span></span>
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile" -Force -PassThru
```

<span data-ttu-id="d95bb-111">Ez a parancs eltávolítja a MyProfile nevű forgalomirányító-profilt, és nem kér megerősítést, és az eredményt visszaszámítja.</span><span class="sxs-lookup"><span data-stu-id="d95bb-111">This command removes the Traffic Manager profile named MyProfile without prompting you for confirmation, and returns the results.</span></span>

## <span data-ttu-id="d95bb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d95bb-112">PARAMETERS</span></span>

### <span data-ttu-id="d95bb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d95bb-113">-Force</span></span>
<span data-ttu-id="d95bb-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="d95bb-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d95bb-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d95bb-115">-Name</span></span>
<span data-ttu-id="d95bb-116">A törlendő forgalomirányítási profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d95bb-116">Specifies the name of the Traffic Manager profile to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d95bb-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d95bb-117">-PassThru</span></span>
<span data-ttu-id="d95bb-118">Ha a művelet sikeres, akkor az $True értékét számítja ki. egyéb esetben $False.</span><span class="sxs-lookup"><span data-stu-id="d95bb-118">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="d95bb-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="d95bb-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d95bb-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="d95bb-120">-Profile</span></span>
<span data-ttu-id="d95bb-121">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d95bb-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d95bb-122">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d95bb-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d95bb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d95bb-123">CommonParameters</span></span>
<span data-ttu-id="d95bb-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d95bb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d95bb-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d95bb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d95bb-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d95bb-126">INPUTS</span></span>

## <span data-ttu-id="d95bb-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d95bb-127">OUTPUTS</span></span>

### <span data-ttu-id="d95bb-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d95bb-128">System.Boolean</span></span>
<span data-ttu-id="d95bb-129">Ez a parancsmag $True vagy $Falset hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d95bb-129">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="d95bb-130">Ha a művelet sikeres, és a *PassThru* paramétert adja meg, ez a parancsmag az $True értékét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d95bb-130">If the operation is successful and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="d95bb-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d95bb-131">NOTES</span></span>

## <span data-ttu-id="d95bb-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d95bb-132">RELATED LINKS</span></span>

[<span data-ttu-id="d95bb-133">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d95bb-133">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="d95bb-134">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d95bb-134">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="d95bb-135">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d95bb-135">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="d95bb-136">Új – AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d95bb-136">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="d95bb-137">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d95bb-137">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


