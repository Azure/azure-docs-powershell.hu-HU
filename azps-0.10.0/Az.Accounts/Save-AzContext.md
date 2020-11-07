---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 07e565031a5c29ae1be78246cad95326952007e6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841029"
---
# <span data-ttu-id="a0cb5-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="a0cb5-101">Save-AzContext</span></span>

## <span data-ttu-id="a0cb5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="a0cb5-103">Az aktuális hitelesítési adatokat menti a többi PowerShell-munkamenetben való használatra.</span><span class="sxs-lookup"><span data-stu-id="a0cb5-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="a0cb5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0cb5-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0cb5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0cb5-105">DESCRIPTION</span></span>
<span data-ttu-id="a0cb5-106">Az Save-AzContext parancsmag az aktuális hitelesítési adatokat menti a többi PowerShell-munkamenetben való használatra.</span><span class="sxs-lookup"><span data-stu-id="a0cb5-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="a0cb5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a0cb5-107">EXAMPLES</span></span>

### <span data-ttu-id="a0cb5-108">1. példa: az aktuális munkamenet környezetének mentése</span><span class="sxs-lookup"><span data-stu-id="a0cb5-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="a0cb5-109">Ez a példa az aktuális munkamenet Azure-környezetét az adott JSON-fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="a0cb5-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="a0cb5-110">2. példa: adott környezet mentése</span><span class="sxs-lookup"><span data-stu-id="a0cb5-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="a0cb5-111">Ez a példa menti az Azure-környezetet, amelyet áthalad a parancsmagnak a JSON-fájlra.</span><span class="sxs-lookup"><span data-stu-id="a0cb5-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="a0cb5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0cb5-112">PARAMETERS</span></span>

### <span data-ttu-id="a0cb5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0cb5-113">-DefaultProfile</span></span>
<span data-ttu-id="a0cb5-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0cb5-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cb5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a0cb5-115">-Force</span></span>
<span data-ttu-id="a0cb5-116">A megadott fájl felülírása ha létezik</span><span class="sxs-lookup"><span data-stu-id="a0cb5-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="a0cb5-117">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="a0cb5-117">-Path</span></span>
<span data-ttu-id="a0cb5-118">Annak a fájlnak az elérési útját adja meg, amelyre menteni szeretné a hitelesítési adatokat.</span><span class="sxs-lookup"><span data-stu-id="a0cb5-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="a0cb5-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="a0cb5-119">-Profile</span></span>
<span data-ttu-id="a0cb5-120">Azt az Azure-környezetet adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="a0cb5-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="a0cb5-121">Ha nem ad meg környezetet, a parancsmag a helyi alapértelmezett környezetből olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="a0cb5-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="a0cb5-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a0cb5-122">-Confirm</span></span>
<span data-ttu-id="a0cb5-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a0cb5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0cb5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0cb5-124">-WhatIf</span></span>
<span data-ttu-id="a0cb5-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a0cb5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0cb5-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a0cb5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0cb5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0cb5-127">CommonParameters</span></span>
<span data-ttu-id="a0cb5-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0cb5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0cb5-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a0cb5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0cb5-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0cb5-130">INPUTS</span></span>

### <span data-ttu-id="a0cb5-131">Microsoft. Azure. commands. Common. Authentication. models. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="a0cb5-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="a0cb5-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0cb5-132">OUTPUTS</span></span>

### <span data-ttu-id="a0cb5-133">Microsoft. Azure. Command. profil. models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="a0cb5-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="a0cb5-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0cb5-134">NOTES</span></span>

## <span data-ttu-id="a0cb5-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0cb5-135">RELATED LINKS</span></span>
