---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: f3afbd9b96de51f754dd87dfa42ed6f71e5b3577
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490452"
---
# <span data-ttu-id="ccb82-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="ccb82-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="ccb82-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ccb82-102">SYNOPSIS</span></span>
<span data-ttu-id="ccb82-103">Az aktuális hitelesítési adatokat menti a többi PowerShell-munkamenetben való használatra.</span><span class="sxs-lookup"><span data-stu-id="ccb82-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="ccb82-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ccb82-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="ccb82-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ccb82-105">DESCRIPTION</span></span>
<span data-ttu-id="ccb82-106">Az Save-AzureRmContext parancsmag az aktuális hitelesítési adatokat menti a többi PowerShell-munkamenetben való használatra.</span><span class="sxs-lookup"><span data-stu-id="ccb82-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="ccb82-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ccb82-107">EXAMPLES</span></span>

### <span data-ttu-id="ccb82-108">1. példa: az aktuális munkamenet környezetének mentése</span><span class="sxs-lookup"><span data-stu-id="ccb82-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="ccb82-109">Ez a példa az aktuális munkamenet Azure-környezetét az adott JSON-fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="ccb82-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="ccb82-110">2. példa: adott környezet mentése</span><span class="sxs-lookup"><span data-stu-id="ccb82-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="ccb82-111">Ez a példa menti az Azure-környezetet, amelyet áthalad a parancsmagnak a JSON-fájlra.</span><span class="sxs-lookup"><span data-stu-id="ccb82-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="ccb82-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ccb82-112">PARAMETERS</span></span>

### <span data-ttu-id="ccb82-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ccb82-113">-Force</span></span>
<span data-ttu-id="ccb82-114">A megadott fájl felülírása ha létezik</span><span class="sxs-lookup"><span data-stu-id="ccb82-114">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="ccb82-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="ccb82-115">-Path</span></span>
<span data-ttu-id="ccb82-116">Annak a fájlnak az elérési útját adja meg, amelyre menteni szeretné a hitelesítési adatokat.</span><span class="sxs-lookup"><span data-stu-id="ccb82-116">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb82-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="ccb82-117">-Profile</span></span>
<span data-ttu-id="ccb82-118">Azt az Azure-környezetet adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ccb82-118">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="ccb82-119">Ha nem ad meg környezetet, a parancsmag a helyi alapértelmezett környezetből olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ccb82-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccb82-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ccb82-120">-Confirm</span></span>
<span data-ttu-id="ccb82-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ccb82-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccb82-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccb82-122">-WhatIf</span></span>
<span data-ttu-id="ccb82-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ccb82-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccb82-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ccb82-124">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="ccb82-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccb82-125">INPUTS</span></span>

### <span data-ttu-id="ccb82-126">Microsoft. Azure. commands. Common. Authentication. models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="ccb82-126">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>

## <span data-ttu-id="ccb82-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccb82-127">OUTPUTS</span></span>

### <span data-ttu-id="ccb82-128">Microsoft. Azure. Command. profil. models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="ccb82-128">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="ccb82-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ccb82-129">NOTES</span></span>

## <span data-ttu-id="ccb82-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ccb82-130">RELATED LINKS</span></span>

