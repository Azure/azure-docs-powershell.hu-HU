---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06a78584437021df570bc5ff2b6ec19e332bffd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491320"
---
# <span data-ttu-id="cd9c4-101">Save-AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="cd9c4-101">Save-AzureRmProfile</span></span>

## <span data-ttu-id="cd9c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd9c4-102">SYNOPSIS</span></span>
<span data-ttu-id="cd9c4-103">Az aktuális hitelesítési adatokat menti a többi PowerShell-munkamenetben való használatra.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="cd9c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd9c4-104">SYNTAX</span></span>

```
Save-AzureRmProfile [[-Profile] <AzureRMProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd9c4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd9c4-105">DESCRIPTION</span></span>
<span data-ttu-id="cd9c4-106">Az Save-AzureRmProfile parancsmag az aktuális hitelesítési adatokat menti a többi PowerShell-munkamenetben való használatra.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-106">The Save-AzureRmProfile cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="cd9c4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cd9c4-107">EXAMPLES</span></span>

### <span data-ttu-id="cd9c4-108">1. példa: az aktuális munkamenet profiljának mentése</span><span class="sxs-lookup"><span data-stu-id="cd9c4-108">Example 1: Saving the current session's profile</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmProfile -Path C:\test.json
```

<span data-ttu-id="cd9c4-109">Ebben a példában az aktuális munkamenet Azure-profilját az adott JSON-fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-109">This example saves the current session's Azure profile to the JSON file provided.</span></span>

### <span data-ttu-id="cd9c4-110">2. példa: adott profil mentése</span><span class="sxs-lookup"><span data-stu-id="cd9c4-110">Example 2: Saving a given profile</span></span>
```
PS C:\> Save-AzureRmProfile -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="cd9c4-111">Ebben a példában az Azure-profilt átmenti a parancsmagra a JSON-fájlra.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-111">This example saves the Azure profile that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="cd9c4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd9c4-112">PARAMETERS</span></span>

### <span data-ttu-id="cd9c4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="cd9c4-113">-Force</span></span>
<span data-ttu-id="cd9c4-114">A megadott fájl felülírása ha létezik</span><span class="sxs-lookup"><span data-stu-id="cd9c4-114">Overwrite the given file if it exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9c4-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="cd9c4-115">-Path</span></span>
<span data-ttu-id="cd9c4-116">Annak a fájlnak az elérési útját adja meg, amelyre menteni szeretné a hitelesítési adatokat.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-116">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9c4-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="cd9c4-117">-Profile</span></span>
<span data-ttu-id="cd9c4-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cd9c4-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureRMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd9c4-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cd9c4-120">-Confirm</span></span>
<span data-ttu-id="cd9c4-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9c4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd9c4-122">-WhatIf</span></span>
<span data-ttu-id="cd9c4-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd9c4-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9c4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd9c4-125">CommonParameters</span></span>
<span data-ttu-id="cd9c4-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd9c4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd9c4-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd9c4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd9c4-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd9c4-128">INPUTS</span></span>

## <span data-ttu-id="cd9c4-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd9c4-129">OUTPUTS</span></span>

### <span data-ttu-id="cd9c4-130">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="cd9c4-130">PSAzureProfile</span></span>

## <span data-ttu-id="cd9c4-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd9c4-131">NOTES</span></span>

## <span data-ttu-id="cd9c4-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd9c4-132">RELATED LINKS</span></span>

[<span data-ttu-id="cd9c4-133">Select-AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="cd9c4-133">Select-AzureRMProfile</span></span>]()

