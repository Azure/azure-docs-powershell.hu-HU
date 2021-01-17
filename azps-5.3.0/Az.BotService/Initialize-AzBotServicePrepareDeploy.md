---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/initialize-azbotservicepreparedeploy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
ms.openlocfilehash: 97f13dc7c9a74fef3775d0aed0db9d7acfa4da43
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480971"
---
# <span data-ttu-id="dc7d0-101">Initialize-AzBotServicePrepareDeploy</span><span class="sxs-lookup"><span data-stu-id="dc7d0-101">Initialize-AzBotServicePrepareDeploy</span></span>

## <span data-ttu-id="dc7d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc7d0-102">SYNOPSIS</span></span>
<span data-ttu-id="dc7d0-103">A paraméterek által megadott BotService értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="dc7d0-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="dc7d0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dc7d0-104">SYNTAX</span></span>

```
Initialize-AzBotServicePrepareDeploy [-CodeDir <String>] [-Language <String>] [-ProjFileName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dc7d0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dc7d0-105">DESCRIPTION</span></span>
<span data-ttu-id="dc7d0-106">A paraméterek által megadott BotService értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="dc7d0-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="dc7d0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dc7d0-107">EXAMPLES</span></span>

### <span data-ttu-id="dc7d0-108">1. példa: A Project Fájlmappa inicializálása</span><span class="sxs-lookup"><span data-stu-id="dc7d0-108">Example 1: Initialize the Project FileFolder</span></span>
```powershell
PS C:\> Initialize-AzBotServicePrepareDeploy -CodeDir D:\zips\MyEchoBot -ProjFileName MyEchoBot.csproj

```

<span data-ttu-id="dc7d0-109">Inicializálás: Erőforrás előkészítése használatra, és alapértelmezett állapot beállítása</span><span class="sxs-lookup"><span data-stu-id="dc7d0-109">Initialize Prepares a resource for use, and sets it to a default state</span></span>

## <span data-ttu-id="dc7d0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc7d0-110">PARAMETERS</span></span>

### <span data-ttu-id="dc7d0-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="dc7d0-111">-CodeDir</span></span>
<span data-ttu-id="dc7d0-112">A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="dc7d0-112">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc7d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc7d0-113">-DefaultProfile</span></span>
<span data-ttu-id="dc7d0-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc7d0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc7d0-115">-Language</span><span class="sxs-lookup"><span data-stu-id="dc7d0-115">-Language</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc7d0-116">-ProjFileName</span><span class="sxs-lookup"><span data-stu-id="dc7d0-116">-ProjFileName</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc7d0-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc7d0-117">-SubscriptionId</span></span>
<span data-ttu-id="dc7d0-118">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dc7d0-118">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc7d0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc7d0-119">CommonParameters</span></span>
<span data-ttu-id="dc7d0-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc7d0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc7d0-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc7d0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc7d0-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc7d0-122">INPUTS</span></span>

## <span data-ttu-id="dc7d0-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc7d0-123">OUTPUTS</span></span>

### <span data-ttu-id="dc7d0-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="dc7d0-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="dc7d0-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dc7d0-125">NOTES</span></span>

<span data-ttu-id="dc7d0-126">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="dc7d0-126">ALIASES</span></span>

## <span data-ttu-id="dc7d0-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc7d0-127">RELATED LINKS</span></span>

