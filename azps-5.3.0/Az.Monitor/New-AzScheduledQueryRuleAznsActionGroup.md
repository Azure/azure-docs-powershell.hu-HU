---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: 44f9eae56c822e5fe068679331bcdd3a0ad17d81
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467565"
---
# <span data-ttu-id="b087e-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="b087e-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="b087e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b087e-102">SYNOPSIS</span></span>
<span data-ttu-id="b087e-103">Azns műveletcsoport típusú objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="b087e-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="b087e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b087e-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b087e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b087e-105">DESCRIPTION</span></span>
<span data-ttu-id="b087e-106">Azns műveletcsoport típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b087e-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="b087e-107">Ezt az objektumot a naplóriasztás szabályát figyelő parancsnak kell átadódni.</span><span class="sxs-lookup"><span data-stu-id="b087e-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="b087e-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b087e-108">EXAMPLES</span></span>

### <span data-ttu-id="b087e-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="b087e-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="b087e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b087e-110">PARAMETERS</span></span>

### <span data-ttu-id="b087e-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="b087e-111">-ActionGroup</span></span>
<span data-ttu-id="b087e-112">Az értesítéseket küldő műveletcsoportok listája</span><span class="sxs-lookup"><span data-stu-id="b087e-112">The list of action groups to send notification to</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b087e-113">-CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="b087e-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="b087e-114">A testre szabott webhook hasznos terhelés</span><span class="sxs-lookup"><span data-stu-id="b087e-114">The customized webhook payload</span></span>

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

### <span data-ttu-id="b087e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b087e-115">-DefaultProfile</span></span>
<span data-ttu-id="b087e-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b087e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b087e-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="b087e-117">-EmailSubject</span></span>
<span data-ttu-id="b087e-118">Az értesítés tárgyának e-mailben való elküldése</span><span class="sxs-lookup"><span data-stu-id="b087e-118">The email subject of alert notification</span></span>

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

### <span data-ttu-id="b087e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b087e-119">CommonParameters</span></span>
<span data-ttu-id="b087e-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b087e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b087e-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b087e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b087e-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b087e-122">INPUTS</span></span>

### <span data-ttu-id="b087e-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="b087e-123">None</span></span>

## <span data-ttu-id="b087e-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b087e-124">OUTPUTS</span></span>

### <span data-ttu-id="b087e-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="b087e-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="b087e-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b087e-126">NOTES</span></span>

## <span data-ttu-id="b087e-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b087e-127">RELATED LINKS</span></span>
