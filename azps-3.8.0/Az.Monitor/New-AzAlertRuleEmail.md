---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 7d9ed01346c04974fb43d7e3b233badb7a185dc2
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411364"
---
# <span data-ttu-id="374aa-101">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="374aa-101">New-AzAlertRuleEmail</span></span>

## <span data-ttu-id="374aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="374aa-102">SYNOPSIS</span></span>
<span data-ttu-id="374aa-103">E-mail műveletet hoz létre egy riasztási szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="374aa-103">Creates an email action for an alert rule.</span></span>

## <span data-ttu-id="374aa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="374aa-104">SYNTAX</span></span>

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="374aa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="374aa-105">DESCRIPTION</span></span>
<span data-ttu-id="374aa-106">A **New-AzAlertRuleEmail** parancsmag létrehoz egy e-mail műveletet egy riasztási szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="374aa-106">The **New-AzAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="374aa-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="374aa-107">EXAMPLES</span></span>

### <span data-ttu-id="374aa-108">1. példa: Értesítési szabály e-mail-művelet létrehozása szolgáltatástulajdonosoknak</span><span class="sxs-lookup"><span data-stu-id="374aa-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="374aa-109">Ez a parancs egy riasztási szabály e-mail-műveletet hoz létre, és elküldi azt a szolgáltatástulajdonosoknak, ha riasztási szabály van beszabályzva.</span><span class="sxs-lookup"><span data-stu-id="374aa-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="374aa-110">2. példa: Értesítési szabály e-mail-művelet létrehozása nem szolgáltatástulajdonosoknak</span><span class="sxs-lookup"><span data-stu-id="374aa-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="374aa-111">Ez a parancs egy riasztási szabály e-mail-műveletet hoz létre a megadott e-mail-címekhez, de nem a szolgáltatástulajdonosokhoz.</span><span class="sxs-lookup"><span data-stu-id="374aa-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="374aa-112">3. példa: Értesítési szabály e-mail-művelet létrehozása szolgáltatástulajdonosoknak és nem szolgáltatástulajdonosoknak</span><span class="sxs-lookup"><span data-stu-id="374aa-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="374aa-113">Ez a parancs egy riasztási szabály e-mail-műveletet hoz létre a megadott címhez és a szolgáltatástulajdonosokhoz.</span><span class="sxs-lookup"><span data-stu-id="374aa-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="374aa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="374aa-114">PARAMETERS</span></span>

### <span data-ttu-id="374aa-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="374aa-115">-CustomEmail</span></span>
<span data-ttu-id="374aa-116">Vesszővel elválasztott e-mail-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="374aa-116">Specifies a list of comma-separated e-mail addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="374aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="374aa-117">-DefaultProfile</span></span>
<span data-ttu-id="374aa-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="374aa-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="374aa-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="374aa-119">-SendToServiceOwner</span></span>
<span data-ttu-id="374aa-120">Azt jelzi, hogy ez a művelet e-mailt küld a szolgáltatástulajdonosoknak, amikor a szabály ki van tűzve.</span><span class="sxs-lookup"><span data-stu-id="374aa-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="374aa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="374aa-121">CommonParameters</span></span>
<span data-ttu-id="374aa-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="374aa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="374aa-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="374aa-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="374aa-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="374aa-124">INPUTS</span></span>

### <span data-ttu-id="374aa-125">System.String[]</span><span class="sxs-lookup"><span data-stu-id="374aa-125">System.String[]</span></span>

### <span data-ttu-id="374aa-126">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="374aa-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="374aa-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="374aa-127">OUTPUTS</span></span>

### <span data-ttu-id="374aa-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="374aa-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="374aa-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="374aa-129">NOTES</span></span>

## <span data-ttu-id="374aa-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="374aa-130">RELATED LINKS</span></span>


[<span data-ttu-id="374aa-131">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="374aa-131">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="374aa-132">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="374aa-132">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="374aa-133">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="374aa-133">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


