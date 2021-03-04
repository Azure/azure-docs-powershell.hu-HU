---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/publish-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
ms.openlocfilehash: 551428a1c5d1737d32aeddf2dd5653586d1dbfbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925154"
---
# <span data-ttu-id="bbce6-101">Publish-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="bbce6-101">Publish-AzBotServiceApp</span></span>

## <span data-ttu-id="bbce6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbce6-102">SYNOPSIS</span></span>
<span data-ttu-id="bbce6-103">A paraméterek által megadott BotService értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="bbce6-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="bbce6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bbce6-104">SYNTAX</span></span>

```
Publish-AzBotServiceApp -CodeDir <String> -Name <String> -ResourceGroupName <String> [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="bbce6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bbce6-105">DESCRIPTION</span></span>
<span data-ttu-id="bbce6-106">A paraméterek által megadott BotService értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="bbce6-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="bbce6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bbce6-107">EXAMPLES</span></span>

### <span data-ttu-id="bbce6-108">1. példa: A botservice közzététele az Azure-ban</span><span class="sxs-lookup"><span data-stu-id="bbce6-108">Example 1: Publish your BotService to Azure</span></span>
```powershell
PS C:\> Publish-AzBotServiceApp -ResourceGroupName youriBotTest -CodeDir D:\zips\MyEchoBot -Name youriechobottest

```

<span data-ttu-id="bbce6-109">A BotService szolgáltatás közzététele az Azure-ban kód alapján</span><span class="sxs-lookup"><span data-stu-id="bbce6-109">Publish your BotService to Azure by code</span></span>

## <span data-ttu-id="bbce6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbce6-110">PARAMETERS</span></span>

### <span data-ttu-id="bbce6-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="bbce6-111">-CodeDir</span></span>
<span data-ttu-id="bbce6-112">Ez a paraméter határozza meg a ZIP elérési útját.</span><span class="sxs-lookup"><span data-stu-id="bbce6-112">This parameter defines the Path of the ZIP</span></span>

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

### <span data-ttu-id="bbce6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="bbce6-113">-Name</span></span>
<span data-ttu-id="bbce6-114">Ez a paraméter határozza meg a robot nevét.</span><span class="sxs-lookup"><span data-stu-id="bbce6-114">This parameter defines the name of the bot.</span></span>

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

### <span data-ttu-id="bbce6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbce6-115">-ResourceGroupName</span></span>
<span data-ttu-id="bbce6-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bbce6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbce6-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbce6-117">-Confirm</span></span>
<span data-ttu-id="bbce6-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bbce6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbce6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbce6-119">-WhatIf</span></span>
<span data-ttu-id="bbce6-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bbce6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbce6-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bbce6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbce6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbce6-122">CommonParameters</span></span>
<span data-ttu-id="bbce6-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbce6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbce6-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bbce6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbce6-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bbce6-125">INPUTS</span></span>

## <span data-ttu-id="bbce6-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbce6-126">OUTPUTS</span></span>

## <span data-ttu-id="bbce6-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bbce6-127">NOTES</span></span>

<span data-ttu-id="bbce6-128">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="bbce6-128">ALIASES</span></span>

## <span data-ttu-id="bbce6-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bbce6-129">RELATED LINKS</span></span>

