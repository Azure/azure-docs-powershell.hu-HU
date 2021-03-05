---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/initialize-azbotservicepreparedeploy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
ms.openlocfilehash: 118fce3e75ee7ba66fa30e6e07cfce16e5dadcff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009302"
---
# <span data-ttu-id="4ad7a-101">Initialize-AzBotServicePrepareDeploy</span><span class="sxs-lookup"><span data-stu-id="4ad7a-101">Initialize-AzBotServicePrepareDeploy</span></span>

## <span data-ttu-id="4ad7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ad7a-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad7a-103">A paraméterek által megadott BotService értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="4ad7a-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="4ad7a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4ad7a-104">SYNTAX</span></span>

```
Initialize-AzBotServicePrepareDeploy [-CodeDir <String>] [-Language <String>] [-ProjFileName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4ad7a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4ad7a-105">DESCRIPTION</span></span>
<span data-ttu-id="4ad7a-106">A paraméterek által megadott BotService értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="4ad7a-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="4ad7a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4ad7a-107">EXAMPLES</span></span>

### <span data-ttu-id="4ad7a-108">1. példa: A Project Fájlmappa inicializálása</span><span class="sxs-lookup"><span data-stu-id="4ad7a-108">Example 1: Initialize the Project FileFolder</span></span>
```powershell
PS C:\> Initialize-AzBotServicePrepareDeploy -CodeDir D:\zips\MyEchoBot -ProjFileName MyEchoBot.csproj

```

<span data-ttu-id="4ad7a-109">Inicializálás: Erőforrás előkészítése használatra, és alapértelmezett állapot beállítása</span><span class="sxs-lookup"><span data-stu-id="4ad7a-109">Initialize Prepares a resource for use, and sets it to a default state</span></span>

## <span data-ttu-id="4ad7a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ad7a-110">PARAMETERS</span></span>

### <span data-ttu-id="4ad7a-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="4ad7a-111">-CodeDir</span></span>
<span data-ttu-id="4ad7a-112">A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="4ad7a-112">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="4ad7a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ad7a-113">-DefaultProfile</span></span>
<span data-ttu-id="4ad7a-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ad7a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ad7a-115">-Language</span><span class="sxs-lookup"><span data-stu-id="4ad7a-115">-Language</span></span>


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

### <span data-ttu-id="4ad7a-116">-ProjFileName</span><span class="sxs-lookup"><span data-stu-id="4ad7a-116">-ProjFileName</span></span>


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

### <span data-ttu-id="4ad7a-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ad7a-117">-SubscriptionId</span></span>
<span data-ttu-id="4ad7a-118">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4ad7a-118">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="4ad7a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad7a-119">CommonParameters</span></span>
<span data-ttu-id="4ad7a-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ad7a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad7a-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ad7a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad7a-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ad7a-122">INPUTS</span></span>

## <span data-ttu-id="4ad7a-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ad7a-123">OUTPUTS</span></span>

### <span data-ttu-id="4ad7a-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="4ad7a-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="4ad7a-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4ad7a-125">NOTES</span></span>

<span data-ttu-id="4ad7a-126">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="4ad7a-126">ALIASES</span></span>

## <span data-ttu-id="4ad7a-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ad7a-127">RELATED LINKS</span></span>

