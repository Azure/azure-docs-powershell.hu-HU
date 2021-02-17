---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 237742c633ffe7a2a113467c7a12725b4f3b8b89
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403068"
---
# <span data-ttu-id="107ec-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="107ec-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="107ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="107ec-102">SYNOPSIS</span></span>
<span data-ttu-id="107ec-103">Riasztási szabályt hoz létre webhook.</span><span class="sxs-lookup"><span data-stu-id="107ec-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="107ec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="107ec-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="107ec-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="107ec-105">DESCRIPTION</span></span>
<span data-ttu-id="107ec-106">A **New-AzAlertRuleWebhook** parancsmag létrehoz egy webhook riasztási szabályt.</span><span class="sxs-lookup"><span data-stu-id="107ec-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="107ec-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="107ec-107">EXAMPLES</span></span>

### <span data-ttu-id="107ec-108">1. példa: Értesítési szabály létrehozása webhook</span><span class="sxs-lookup"><span data-stu-id="107ec-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="107ec-109">Ez a parancs csak a szolgáltatás URI-ját megadásával hoz létre webhook riasztási szabályt.</span><span class="sxs-lookup"><span data-stu-id="107ec-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="107ec-110">2. példa: Webhook létrehozása egyetlen tulajdonsággal</span><span class="sxs-lookup"><span data-stu-id="107ec-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="107ec-111">Ez a parancs egy webhook riasztási szabályt hoz létre egy olyan Contoso.com, amely egyetlen tulajdonsággal rendelkezik, majd azt a $Actual változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="107ec-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="107ec-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="107ec-112">PARAMETERS</span></span>

### <span data-ttu-id="107ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="107ec-113">-DefaultProfile</span></span>
<span data-ttu-id="107ec-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="107ec-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="107ec-115">-Tulajdonság</span><span class="sxs-lookup"><span data-stu-id="107ec-115">-Property</span></span>
<span data-ttu-id="107ec-116">A @(tulajdonság1 = 'érték1',....) formátumban adja meg a tulajdonságok listáját.</span><span class="sxs-lookup"><span data-stu-id="107ec-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="107ec-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="107ec-117">-ServiceUri</span></span>
<span data-ttu-id="107ec-118">A szolgáltatás URI-ját adja meg.</span><span class="sxs-lookup"><span data-stu-id="107ec-118">Specifies the service URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="107ec-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="107ec-119">CommonParameters</span></span>
<span data-ttu-id="107ec-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="107ec-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="107ec-121">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="107ec-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="107ec-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="107ec-122">INPUTS</span></span>

### <span data-ttu-id="107ec-123">System.String</span><span class="sxs-lookup"><span data-stu-id="107ec-123">System.String</span></span>

### <span data-ttu-id="107ec-124">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="107ec-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="107ec-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="107ec-125">OUTPUTS</span></span>

### <span data-ttu-id="107ec-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="107ec-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="107ec-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="107ec-127">NOTES</span></span>

## <span data-ttu-id="107ec-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="107ec-128">RELATED LINKS</span></span>


[<span data-ttu-id="107ec-129">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="107ec-129">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="107ec-130">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="107ec-130">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="107ec-131">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="107ec-131">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="107ec-132">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="107ec-132">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


