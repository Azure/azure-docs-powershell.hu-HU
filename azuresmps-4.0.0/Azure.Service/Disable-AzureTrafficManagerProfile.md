---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: ECE9C2A6-7DA2-4477-B877-9970FBE26D7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f378cbf8926a650699ec50a2a0a42873dcb7528
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015693"
---
# <span data-ttu-id="1bb60-101">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1bb60-101">Disable-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="1bb60-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1bb60-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb60-103">Letiltja a Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="1bb60-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="1bb60-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1bb60-104">SYNTAX</span></span>

```
Disable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1bb60-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1bb60-105">DESCRIPTION</span></span>
<span data-ttu-id="1bb60-106">A **disable-AzureTrafficManagerProfile** parancsmag letiltja a Microsoft Azure Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="1bb60-106">The **Disable-AzureTrafficManagerProfile** cmdlet disables a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="1bb60-107">A *PassThru* paraméterrel megtekintheti, hogy a művelet sikerül-e.</span><span class="sxs-lookup"><span data-stu-id="1bb60-107">You can use the *PassThru* parameter to display whether the operation succeeds.</span></span>

## <span data-ttu-id="1bb60-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1bb60-108">EXAMPLES</span></span>

### <span data-ttu-id="1bb60-109">1. példa: a Traffic Manager-profil letiltása és az eredmények megjelenítése</span><span class="sxs-lookup"><span data-stu-id="1bb60-109">Example 1: Disable a Traffic Manager profile and display the results</span></span>
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

<span data-ttu-id="1bb60-110">Ez a parancs letiltja a MyProfile nevű Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="1bb60-110">This command disables the Traffic Manager profile named MyProfile.</span></span>
<span data-ttu-id="1bb60-111">A parancs a *PassThru* paramétert adja meg, hogy a parancs sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="1bb60-111">The command specifies the *PassThru* parameter to display whether the command succeeded.</span></span>

### <span data-ttu-id="1bb60-112">2. példa: a forgalomirányító-profil letiltása és találatok megjelenítése</span><span class="sxs-lookup"><span data-stu-id="1bb60-112">Example 2: Disable a Traffic Manager profile and display no results</span></span>
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="1bb60-113">Ez a parancs letiltja a MyProfile nevű Traffic Manager profilt, de nem jeleníti meg, hogy a parancs sikerült-e.</span><span class="sxs-lookup"><span data-stu-id="1bb60-113">This command disables the Traffic Manager profile named MyProfile but does not display whether the command succeeded.</span></span>

## <span data-ttu-id="1bb60-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1bb60-114">PARAMETERS</span></span>

### <span data-ttu-id="1bb60-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1bb60-115">-Name</span></span>
<span data-ttu-id="1bb60-116">A letiltani kívánt forgalomirányító-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1bb60-116">Specifies the name of the Traffic Manager profile to disable.</span></span>

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

### <span data-ttu-id="1bb60-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bb60-117">-PassThru</span></span>
<span data-ttu-id="1bb60-118">Ha a művelet sikeres, akkor az $True értékét számítja ki. egyéb esetben $False.</span><span class="sxs-lookup"><span data-stu-id="1bb60-118">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="1bb60-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="1bb60-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1bb60-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="1bb60-120">-Profile</span></span>
<span data-ttu-id="1bb60-121">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="1bb60-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1bb60-122">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="1bb60-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1bb60-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb60-123">CommonParameters</span></span>
<span data-ttu-id="1bb60-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1bb60-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb60-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bb60-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb60-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1bb60-126">INPUTS</span></span>

## <span data-ttu-id="1bb60-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1bb60-127">OUTPUTS</span></span>

### <span data-ttu-id="1bb60-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1bb60-128">System.Boolean</span></span>
<span data-ttu-id="1bb60-129">Ez a parancsmag $True vagy $Falset hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1bb60-129">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="1bb60-130">Ha a művelet sikeres, és a *PassThru* paramétert adja meg, ez a parancsmag az $True értékét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="1bb60-130">If the operation is successful and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="1bb60-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1bb60-131">NOTES</span></span>

## <span data-ttu-id="1bb60-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1bb60-132">RELATED LINKS</span></span>

[<span data-ttu-id="1bb60-133">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1bb60-133">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="1bb60-134">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1bb60-134">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="1bb60-135">Új – AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1bb60-135">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="1bb60-136">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1bb60-136">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="1bb60-137">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1bb60-137">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


