---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: 44f9eae56c822e5fe068679331bcdd3a0ad17d81
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152155"
---
# <span data-ttu-id="8002c-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="8002c-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="8002c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8002c-102">SYNOPSIS</span></span>
<span data-ttu-id="8002c-103">Azns műveletcsoport típusú objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="8002c-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="8002c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8002c-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8002c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8002c-105">DESCRIPTION</span></span>
<span data-ttu-id="8002c-106">Azns műveletcsoport típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8002c-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="8002c-107">Ezt az objektumot a naplóriasztás szabályát figyelő parancsnak kell átadódni.</span><span class="sxs-lookup"><span data-stu-id="8002c-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="8002c-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8002c-108">EXAMPLES</span></span>

### <span data-ttu-id="8002c-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="8002c-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="8002c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8002c-110">PARAMETERS</span></span>

### <span data-ttu-id="8002c-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="8002c-111">-ActionGroup</span></span>
<span data-ttu-id="8002c-112">Az értesítéseket küldő műveletcsoportok listája</span><span class="sxs-lookup"><span data-stu-id="8002c-112">The list of action groups to send notification to</span></span>

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

### <span data-ttu-id="8002c-113">-CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="8002c-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="8002c-114">A testre szabott webhook hasznos terhelés</span><span class="sxs-lookup"><span data-stu-id="8002c-114">The customized webhook payload</span></span>

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

### <span data-ttu-id="8002c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8002c-115">-DefaultProfile</span></span>
<span data-ttu-id="8002c-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8002c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8002c-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="8002c-117">-EmailSubject</span></span>
<span data-ttu-id="8002c-118">A riasztási értesítés tárgya e-mailben</span><span class="sxs-lookup"><span data-stu-id="8002c-118">The email subject of alert notification</span></span>

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

### <span data-ttu-id="8002c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8002c-119">CommonParameters</span></span>
<span data-ttu-id="8002c-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8002c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8002c-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8002c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8002c-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8002c-122">INPUTS</span></span>

### <span data-ttu-id="8002c-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="8002c-123">None</span></span>

## <span data-ttu-id="8002c-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8002c-124">OUTPUTS</span></span>

### <span data-ttu-id="8002c-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="8002c-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="8002c-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8002c-126">NOTES</span></span>

## <span data-ttu-id="8002c-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8002c-127">RELATED LINKS</span></span>
