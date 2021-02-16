---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/publish-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
ms.openlocfilehash: 4ef38ab40f90024124f7d5f09f1a55c16520dd6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168075"
---
# <span data-ttu-id="f3ac3-101">Publish-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="f3ac3-101">Publish-AzBotServiceApp</span></span>

## <span data-ttu-id="f3ac3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3ac3-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ac3-103">A paraméterek által megadott BotService értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="f3ac3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f3ac3-104">SYNTAX</span></span>

```
Publish-AzBotServiceApp -CodeDir <String> -Name <String> -ResourceGroupName <String> [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f3ac3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f3ac3-105">DESCRIPTION</span></span>
<span data-ttu-id="f3ac3-106">A paraméterek által megadott BotService értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="f3ac3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f3ac3-107">EXAMPLES</span></span>

### <span data-ttu-id="f3ac3-108">1. példa: A botservice közzététele az Azure-ban</span><span class="sxs-lookup"><span data-stu-id="f3ac3-108">Example 1: Publish your BotService to Azure</span></span>
```powershell
PS C:\> Publish-AzBotServiceApp -ResourceGroupName youriBotTest -CodeDir D:\zips\MyEchoBot -Name youriechobottest

```

<span data-ttu-id="f3ac3-109">A BotService szolgáltatás közzététele az Azure-ban kód alapján</span><span class="sxs-lookup"><span data-stu-id="f3ac3-109">Publish your BotService to Azure by code</span></span>

## <span data-ttu-id="f3ac3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3ac3-110">PARAMETERS</span></span>

### <span data-ttu-id="f3ac3-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="f3ac3-111">-CodeDir</span></span>
<span data-ttu-id="f3ac3-112">Ez a paraméter határozza meg a ZIP elérési útját.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-112">This parameter defines the Path of the ZIP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ac3-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f3ac3-113">-Name</span></span>
<span data-ttu-id="f3ac3-114">Ez a paraméter határozza meg a robot nevét.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-114">This parameter defines the name of the bot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ac3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3ac3-115">-ResourceGroupName</span></span>
<span data-ttu-id="f3ac3-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ac3-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3ac3-117">-Confirm</span></span>
<span data-ttu-id="f3ac3-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3ac3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3ac3-119">-WhatIf</span></span>
<span data-ttu-id="f3ac3-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3ac3-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3ac3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ac3-122">CommonParameters</span></span>
<span data-ttu-id="f3ac3-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ac3-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3ac3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ac3-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3ac3-125">INPUTS</span></span>

## <span data-ttu-id="f3ac3-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3ac3-126">OUTPUTS</span></span>

## <span data-ttu-id="f3ac3-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f3ac3-127">NOTES</span></span>

<span data-ttu-id="f3ac3-128">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f3ac3-128">ALIASES</span></span>

## <span data-ttu-id="f3ac3-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3ac3-129">RELATED LINKS</span></span>

