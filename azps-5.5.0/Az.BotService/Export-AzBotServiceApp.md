---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/export-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
ms.openlocfilehash: dd922730f03b715924a69219c0b1f1ccb11534de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168090"
---
# <span data-ttu-id="3ab7c-101">Export-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="3ab7c-101">Export-AzBotServiceApp</span></span>

## <span data-ttu-id="3ab7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ab7c-102">SYNOPSIS</span></span>
<span data-ttu-id="3ab7c-103">A paraméterek által megadott BotService értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="3ab7c-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="3ab7c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3ab7c-104">SYNTAX</span></span>

```
Export-AzBotServiceApp [-Name <String>] [-ResourceGroupName <String>] [-SavePath <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3ab7c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3ab7c-105">DESCRIPTION</span></span>
<span data-ttu-id="3ab7c-106">A paraméterek által megadott BotService értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="3ab7c-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="3ab7c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3ab7c-107">EXAMPLES</span></span>

### <span data-ttu-id="3ab7c-108">1. példa: A BotService app mappa letöltése</span><span class="sxs-lookup"><span data-stu-id="3ab7c-108">Example 1: DownLoad the BotService App folder</span></span>
```powershell
PS C:\> Export-AzBotServiceApp -ResourceGroupName youriBotTest -name youriechobottest

Parameter $SavePath not provided, defaulting to current working directory.

    Directory: D:\powershell\BotService\azure-powershell\src\BotService

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          2020/12/15    13:45                youriechobottest
```

<span data-ttu-id="3ab7c-109">A BotService app mappa letöltése</span><span class="sxs-lookup"><span data-stu-id="3ab7c-109">DownLoad the BotService App folder</span></span>

## <span data-ttu-id="3ab7c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ab7c-110">PARAMETERS</span></span>

### <span data-ttu-id="3ab7c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ab7c-111">-DefaultProfile</span></span>
<span data-ttu-id="3ab7c-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ab7c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ab7c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3ab7c-113">-Name</span></span>
<span data-ttu-id="3ab7c-114">A roboterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="3ab7c-114">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab7c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ab7c-115">-ResourceGroupName</span></span>
<span data-ttu-id="3ab7c-116">A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="3ab7c-116">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="3ab7c-117">-SavePath</span><span class="sxs-lookup"><span data-stu-id="3ab7c-117">-SavePath</span></span>


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

### <span data-ttu-id="3ab7c-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ab7c-118">-SubscriptionId</span></span>
<span data-ttu-id="3ab7c-119">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3ab7c-119">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="3ab7c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ab7c-120">CommonParameters</span></span>
<span data-ttu-id="3ab7c-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ab7c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ab7c-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ab7c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ab7c-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ab7c-123">INPUTS</span></span>

## <span data-ttu-id="3ab7c-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ab7c-124">OUTPUTS</span></span>

### <span data-ttu-id="3ab7c-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="3ab7c-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="3ab7c-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3ab7c-126">NOTES</span></span>

<span data-ttu-id="3ab7c-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3ab7c-127">ALIASES</span></span>

## <span data-ttu-id="3ab7c-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ab7c-128">RELATED LINKS</span></span>

