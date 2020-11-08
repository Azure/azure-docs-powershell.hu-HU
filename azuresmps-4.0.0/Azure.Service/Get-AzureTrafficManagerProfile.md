---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 28136DC3-520B-4134-8736-93D86EEABAE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf9fd7b67b63ce2bddb762c7006722b6035ffe87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015536"
---
# <span data-ttu-id="048ae-101">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="048ae-101">Get-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="048ae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="048ae-102">SYNOPSIS</span></span>
<span data-ttu-id="048ae-103">A forgalomirányító-profil részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="048ae-103">Gets the details of a Traffic Manager profile.</span></span>

## <span data-ttu-id="048ae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="048ae-104">SYNTAX</span></span>

```
Get-AzureTrafficManagerProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="048ae-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="048ae-105">DESCRIPTION</span></span>
<span data-ttu-id="048ae-106">A **Get-AzureTrafficManagerProfile** parancsmag a Microsoft Azure Traffic Manager-profil adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="048ae-106">The **Get-AzureTrafficManagerProfile** cmdlet gets the details of a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="048ae-107">Ha nem adja meg a *Name* paramétert, a parancsmag a forgalomirányítási profilokat az aktuális előfizetésben jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="048ae-107">If you do not specify the *Name* parameter, the cmdlet lists the Traffic Manager profiles in the current subscription.</span></span>

## <span data-ttu-id="048ae-108">Példák</span><span class="sxs-lookup"><span data-stu-id="048ae-108">EXAMPLES</span></span>

### <span data-ttu-id="048ae-109">Példa 1: a forgalomirányító-profilok listájának beszerzése az előfizetésben</span><span class="sxs-lookup"><span data-stu-id="048ae-109">Example 1: Get the list of Traffic Manager profiles in a subscription</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile
```

<span data-ttu-id="048ae-110">Ez a parancs beolvassa a forgalomirányító-profilok listáját az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="048ae-110">This command gets the list of Traffic Manager profiles in your subscription.</span></span>

### <span data-ttu-id="048ae-111">2. példa: adatforgalmi vezető profil beszerzése</span><span class="sxs-lookup"><span data-stu-id="048ae-111">Example 2: Get a Traffic Manager profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="048ae-112">Ez a parancs a MyProfile nevű forgalomirányítási profilt kapja.</span><span class="sxs-lookup"><span data-stu-id="048ae-112">This command gets the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="048ae-113">3. példa: végpont felvétele a forgalomirányító profiljába</span><span class="sxs-lookup"><span data-stu-id="048ae-113">Example 3: Add an endpoint to a Traffic Manager profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Add-AzureTrafficManagerEndpoint -DomainName "Myapp2.cloudapp.net" -TrafficManagerProfile $MyTrafficManagerProfile -Type "CloudService" -Status "Enabled" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="048ae-114">A parancs hozzáadja a végpontot egy forgalomirányító-profilhoz, majd menti a profilt.</span><span class="sxs-lookup"><span data-stu-id="048ae-114">This command adds an endpoint to a Traffic Manager profile, and then saves the profile.</span></span>

## <span data-ttu-id="048ae-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="048ae-115">PARAMETERS</span></span>

### <span data-ttu-id="048ae-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="048ae-116">-Name</span></span>
<span data-ttu-id="048ae-117">A beolvasott forgalomirányítási profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="048ae-117">Specifies the name of the Traffic Manager profile to get.</span></span>

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

### <span data-ttu-id="048ae-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="048ae-118">-Profile</span></span>
<span data-ttu-id="048ae-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="048ae-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="048ae-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="048ae-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="048ae-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="048ae-121">CommonParameters</span></span>
<span data-ttu-id="048ae-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="048ae-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="048ae-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="048ae-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="048ae-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="048ae-124">INPUTS</span></span>

## <span data-ttu-id="048ae-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="048ae-125">OUTPUTS</span></span>

### <span data-ttu-id="048ae-126">Microsoft. WindowsAzure. Command. Utilities. TrafficManager. models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="048ae-126">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="048ae-127">Ez a parancsmag a forgalomirányító-profil objektumát vagy objektumait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="048ae-127">This cmdlet generates a Traffic Manager profile object or objects.</span></span>

## <span data-ttu-id="048ae-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="048ae-128">NOTES</span></span>

## <span data-ttu-id="048ae-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="048ae-129">RELATED LINKS</span></span>

[<span data-ttu-id="048ae-130">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="048ae-130">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="048ae-131">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="048ae-131">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="048ae-132">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="048ae-132">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="048ae-133">Új – AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="048ae-133">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="048ae-134">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="048ae-134">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="048ae-135">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="048ae-135">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


