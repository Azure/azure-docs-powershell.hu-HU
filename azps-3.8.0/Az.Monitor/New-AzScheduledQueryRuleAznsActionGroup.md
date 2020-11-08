---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: 44f9eae56c822e5fe068679331bcdd3a0ad17d81
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002847"
---
# <span data-ttu-id="da596-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="da596-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="da596-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da596-102">SYNOPSIS</span></span>
<span data-ttu-id="da596-103">Azns típusú objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="da596-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="da596-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da596-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da596-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="da596-105">DESCRIPTION</span></span>
<span data-ttu-id="da596-106">Létrehoz egy Azns típusú objektumot.</span><span class="sxs-lookup"><span data-stu-id="da596-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="da596-107">Ezt az objektumot a naplózási riasztási szabályt létrehozó parancsnak kell átadnia.</span><span class="sxs-lookup"><span data-stu-id="da596-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="da596-108">Példák</span><span class="sxs-lookup"><span data-stu-id="da596-108">EXAMPLES</span></span>

### <span data-ttu-id="da596-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="da596-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="da596-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da596-110">PARAMETERS</span></span>

### <span data-ttu-id="da596-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="da596-111">-ActionGroup</span></span>
<span data-ttu-id="da596-112">Az értesítést küldő műveleti csoportok listája</span><span class="sxs-lookup"><span data-stu-id="da596-112">The list of action groups to send notification to</span></span>

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

### <span data-ttu-id="da596-113">-CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="da596-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="da596-114">A testre szabott webhook-tartalom</span><span class="sxs-lookup"><span data-stu-id="da596-114">The customized webhook payload</span></span>

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

### <span data-ttu-id="da596-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da596-115">-DefaultProfile</span></span>
<span data-ttu-id="da596-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da596-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da596-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="da596-117">-EmailSubject</span></span>
<span data-ttu-id="da596-118">Értesítés küldése e-mailben</span><span class="sxs-lookup"><span data-stu-id="da596-118">The email subject of alert notification</span></span>

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

### <span data-ttu-id="da596-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da596-119">CommonParameters</span></span>
<span data-ttu-id="da596-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da596-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da596-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="da596-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da596-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da596-122">INPUTS</span></span>

### <span data-ttu-id="da596-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="da596-123">None</span></span>

## <span data-ttu-id="da596-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da596-124">OUTPUTS</span></span>

### <span data-ttu-id="da596-125">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="da596-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="da596-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da596-126">NOTES</span></span>

## <span data-ttu-id="da596-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da596-127">RELATED LINKS</span></span>
