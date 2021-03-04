---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: f73ca19ffa2c68599a5244d41b39d90ebbd2835a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930442"
---
# <span data-ttu-id="22111-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="22111-101">Save-AzContext</span></span>

## <span data-ttu-id="22111-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22111-102">SYNOPSIS</span></span>
<span data-ttu-id="22111-103">Menti az aktuális hitelesítési adatokat más PowerShell-munkamenetekben való használatra.</span><span class="sxs-lookup"><span data-stu-id="22111-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="22111-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="22111-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22111-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="22111-105">DESCRIPTION</span></span>
<span data-ttu-id="22111-106">A Save-AzContext parancsmag menti az aktuális hitelesítési adatokat más PowerShell-munkamenetekben való használatra.</span><span class="sxs-lookup"><span data-stu-id="22111-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="22111-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="22111-107">EXAMPLES</span></span>

### <span data-ttu-id="22111-108">1. példa: Az aktuális munkamenet környezetének mentése</span><span class="sxs-lookup"><span data-stu-id="22111-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="22111-109">Ez a példa menti az aktuális munkamenet Azure-környezetét a megadott JSON-fájlba.</span><span class="sxs-lookup"><span data-stu-id="22111-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="22111-110">2. példa: Adott környezet mentése</span><span class="sxs-lookup"><span data-stu-id="22111-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="22111-111">Ez a példa menti a megadott JSON-fájlnak a parancsmagnak átadott Azure-környezetet.</span><span class="sxs-lookup"><span data-stu-id="22111-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="22111-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22111-112">PARAMETERS</span></span>

### <span data-ttu-id="22111-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22111-113">-DefaultProfile</span></span>
<span data-ttu-id="22111-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22111-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22111-115">-Force</span><span class="sxs-lookup"><span data-stu-id="22111-115">-Force</span></span>
<span data-ttu-id="22111-116">A megadott fájl felülírása( ha létezik)</span><span class="sxs-lookup"><span data-stu-id="22111-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="22111-117">-Path</span><span class="sxs-lookup"><span data-stu-id="22111-117">-Path</span></span>
<span data-ttu-id="22111-118">Annak a fájlnak az elérési útját adja meg, amelybe menteni kell a hitelesítési adatokat.</span><span class="sxs-lookup"><span data-stu-id="22111-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="22111-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="22111-119">-Profile</span></span>
<span data-ttu-id="22111-120">Azt az Azure-környezetet adja meg, amelyből a parancsmag felolvassa.</span><span class="sxs-lookup"><span data-stu-id="22111-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="22111-121">Ha nem ad meg kontextust, ez a parancsmag a helyi alapértelmezett környezetből olvassa be az olvasott értékeket.</span><span class="sxs-lookup"><span data-stu-id="22111-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="22111-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22111-122">-Confirm</span></span>
<span data-ttu-id="22111-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="22111-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22111-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22111-124">-WhatIf</span></span>
<span data-ttu-id="22111-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="22111-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22111-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22111-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22111-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22111-127">CommonParameters</span></span>
<span data-ttu-id="22111-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22111-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22111-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22111-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22111-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22111-130">INPUTS</span></span>

### <span data-ttu-id="22111-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="22111-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="22111-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22111-132">OUTPUTS</span></span>

### <span data-ttu-id="22111-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="22111-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="22111-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="22111-134">NOTES</span></span>

## <span data-ttu-id="22111-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22111-135">RELATED LINKS</span></span>
