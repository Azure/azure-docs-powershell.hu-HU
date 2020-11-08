---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: 44f9eae56c822e5fe068679331bcdd3a0ad17d81
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181797"
---
# <span data-ttu-id="13d93-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="13d93-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="13d93-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13d93-102">SYNOPSIS</span></span>
<span data-ttu-id="13d93-103">Azns típusú objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="13d93-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="13d93-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13d93-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13d93-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="13d93-105">DESCRIPTION</span></span>
<span data-ttu-id="13d93-106">Létrehoz egy Azns típusú objektumot.</span><span class="sxs-lookup"><span data-stu-id="13d93-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="13d93-107">Ezt az objektumot a naplózási riasztási szabályt létrehozó parancsnak kell átadnia.</span><span class="sxs-lookup"><span data-stu-id="13d93-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="13d93-108">Példák</span><span class="sxs-lookup"><span data-stu-id="13d93-108">EXAMPLES</span></span>

### <span data-ttu-id="13d93-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="13d93-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="13d93-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13d93-110">PARAMETERS</span></span>

### <span data-ttu-id="13d93-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="13d93-111">-ActionGroup</span></span>
<span data-ttu-id="13d93-112">Az értesítést küldő műveleti csoportok listája</span><span class="sxs-lookup"><span data-stu-id="13d93-112">The list of action groups to send notification to</span></span>

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

### <span data-ttu-id="13d93-113">-CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="13d93-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="13d93-114">A testre szabott webhook-tartalom</span><span class="sxs-lookup"><span data-stu-id="13d93-114">The customized webhook payload</span></span>

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

### <span data-ttu-id="13d93-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13d93-115">-DefaultProfile</span></span>
<span data-ttu-id="13d93-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13d93-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13d93-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="13d93-117">-EmailSubject</span></span>
<span data-ttu-id="13d93-118">Értesítés küldése e-mailben</span><span class="sxs-lookup"><span data-stu-id="13d93-118">The email subject of alert notification</span></span>

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

### <span data-ttu-id="13d93-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d93-119">CommonParameters</span></span>
<span data-ttu-id="13d93-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13d93-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d93-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="13d93-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d93-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13d93-122">INPUTS</span></span>

### <span data-ttu-id="13d93-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="13d93-123">None</span></span>

## <span data-ttu-id="13d93-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13d93-124">OUTPUTS</span></span>

### <span data-ttu-id="13d93-125">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="13d93-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="13d93-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13d93-126">NOTES</span></span>

## <span data-ttu-id="13d93-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13d93-127">RELATED LINKS</span></span>
