---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
ms.openlocfilehash: 5c6200f6d68760cbd93460b38cb72a379845e622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679056"
---
# <span data-ttu-id="00852-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="00852-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="00852-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="00852-102">SYNOPSIS</span></span>
<span data-ttu-id="00852-103">Az aktuális hitelesítési adatokat menti a többi PowerShell-munkamenetben való használatra.</span><span class="sxs-lookup"><span data-stu-id="00852-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00852-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="00852-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00852-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="00852-105">DESCRIPTION</span></span>
<span data-ttu-id="00852-106">Az Save-AzureRmContext parancsmag az aktuális hitelesítési adatokat menti a többi PowerShell-munkamenetben való használatra.</span><span class="sxs-lookup"><span data-stu-id="00852-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="00852-107">Példák</span><span class="sxs-lookup"><span data-stu-id="00852-107">EXAMPLES</span></span>

### <span data-ttu-id="00852-108">1. példa: az aktuális munkamenet környezetének mentése</span><span class="sxs-lookup"><span data-stu-id="00852-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="00852-109">Ez a példa az aktuális munkamenet Azure-környezetét az adott JSON-fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="00852-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="00852-110">2. példa: adott környezet mentése</span><span class="sxs-lookup"><span data-stu-id="00852-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="00852-111">Ez a példa menti az Azure-környezetet, amelyet áthalad a parancsmagnak a JSON-fájlra.</span><span class="sxs-lookup"><span data-stu-id="00852-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="00852-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="00852-112">PARAMETERS</span></span>

### <span data-ttu-id="00852-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00852-113">-DefaultProfile</span></span>
<span data-ttu-id="00852-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00852-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00852-115">-Force</span><span class="sxs-lookup"><span data-stu-id="00852-115">-Force</span></span>
<span data-ttu-id="00852-116">A megadott fájl felülírása ha létezik</span><span class="sxs-lookup"><span data-stu-id="00852-116">Overwrite the given file if it exists</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00852-117">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="00852-117">-Path</span></span>
<span data-ttu-id="00852-118">Annak a fájlnak az elérési útját adja meg, amelyre menteni szeretné a hitelesítési adatokat.</span><span class="sxs-lookup"><span data-stu-id="00852-118">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00852-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="00852-119">-Profile</span></span>
<span data-ttu-id="00852-120">Azt az Azure-környezetet adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="00852-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="00852-121">Ha nem ad meg környezetet, a parancsmag a helyi alapértelmezett környezetből olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="00852-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00852-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="00852-122">-Confirm</span></span>
<span data-ttu-id="00852-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="00852-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00852-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00852-124">-WhatIf</span></span>
<span data-ttu-id="00852-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="00852-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00852-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="00852-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00852-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00852-127">CommonParameters</span></span>
<span data-ttu-id="00852-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="00852-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00852-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00852-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00852-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="00852-130">INPUTS</span></span>

### <span data-ttu-id="00852-131">Microsoft. Azure. commands. Common. Authentication. models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="00852-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>

## <span data-ttu-id="00852-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00852-132">OUTPUTS</span></span>

### <span data-ttu-id="00852-133">Microsoft. Azure. Command. profil. models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="00852-133">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="00852-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="00852-134">NOTES</span></span>

## <span data-ttu-id="00852-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00852-135">RELATED LINKS</span></span>

