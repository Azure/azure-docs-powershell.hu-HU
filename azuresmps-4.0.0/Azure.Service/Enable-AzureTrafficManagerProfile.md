---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 51A1B699-03F6-4BB9-9186-FDFFB094F16A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 72420272e04519fa888660f8ccb6d432ecb0ee5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016375"
---
# <span data-ttu-id="176c9-101">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="176c9-101">Enable-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="176c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="176c9-102">SYNOPSIS</span></span>
<span data-ttu-id="176c9-103">Lehetővé teszi a forgalomirányítási profilok betöltését.</span><span class="sxs-lookup"><span data-stu-id="176c9-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="176c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="176c9-104">SYNTAX</span></span>

```
Enable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="176c9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="176c9-105">DESCRIPTION</span></span>
<span data-ttu-id="176c9-106">Az **enable-AzureTrafficManagerProfile** parancsmag lehetővé teszi a Microsoft Azure Traffic Manager-profil használatát.</span><span class="sxs-lookup"><span data-stu-id="176c9-106">The **Enable-AzureTrafficManagerProfile** cmdlet enables a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="176c9-107">Adja meg a *PassThru* paramétert annak megjelenítéséhez, hogy a művelet sikerül-e.</span><span class="sxs-lookup"><span data-stu-id="176c9-107">Specify the *PassThru* parameter to display whether the operation succeeds.</span></span>

## <span data-ttu-id="176c9-108">Példák</span><span class="sxs-lookup"><span data-stu-id="176c9-108">EXAMPLES</span></span>

### <span data-ttu-id="176c9-109">1. példa: forgalomirányító-profil engedélyezése</span><span class="sxs-lookup"><span data-stu-id="176c9-109">Example 1: Enable a Traffic Manager profile</span></span>
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="176c9-110">Ez a parancs engedélyezi a MyProfile nevű Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="176c9-110">This command enables the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="176c9-111">2. példa: a forgalomirányítási profil engedélyezése és a találatok megjelenítése</span><span class="sxs-lookup"><span data-stu-id="176c9-111">Example 2: Enable a Traffic Manager profile and display the results</span></span>
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

<span data-ttu-id="176c9-112">Ez a parancs engedélyezi a MyProfile nevű Traffic Manager-profilt, és megjeleníti, hogy a parancs sikerült-e.</span><span class="sxs-lookup"><span data-stu-id="176c9-112">This command enables the Traffic Manager profile named MyProfile and displays whether the command succeeded.</span></span>

## <span data-ttu-id="176c9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="176c9-113">PARAMETERS</span></span>

### <span data-ttu-id="176c9-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="176c9-114">-Name</span></span>
<span data-ttu-id="176c9-115">Az engedélyezni kívánt forgalomirányító-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="176c9-115">Specifies the name of the Traffic Manager profile to enable.</span></span>

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

### <span data-ttu-id="176c9-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="176c9-116">-PassThru</span></span>
<span data-ttu-id="176c9-117">Ha a művelet sikeres, akkor az $True értékét számítja ki. egyéb esetben $False.</span><span class="sxs-lookup"><span data-stu-id="176c9-117">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="176c9-118">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="176c9-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="176c9-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="176c9-119">-Profile</span></span>
<span data-ttu-id="176c9-120">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="176c9-120">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="176c9-121">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="176c9-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="176c9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176c9-122">CommonParameters</span></span>
<span data-ttu-id="176c9-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="176c9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176c9-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="176c9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176c9-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="176c9-125">INPUTS</span></span>

## <span data-ttu-id="176c9-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="176c9-126">OUTPUTS</span></span>

### <span data-ttu-id="176c9-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="176c9-127">System.Boolean</span></span>
<span data-ttu-id="176c9-128">Ez a parancsmag $True vagy $Falset hoz létre.</span><span class="sxs-lookup"><span data-stu-id="176c9-128">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="176c9-129">Ha a művelet sikeres, és a *PassThru* paraméter megadása esetén a parancsmag az $True értékét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="176c9-129">If the operation succeeds and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="176c9-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="176c9-130">NOTES</span></span>

## <span data-ttu-id="176c9-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="176c9-131">RELATED LINKS</span></span>

[<span data-ttu-id="176c9-132">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="176c9-132">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="176c9-133">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="176c9-133">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="176c9-134">Új – AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="176c9-134">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="176c9-135">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="176c9-135">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="176c9-136">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="176c9-136">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


