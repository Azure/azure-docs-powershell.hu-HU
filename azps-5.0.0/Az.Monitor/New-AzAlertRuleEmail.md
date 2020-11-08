---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 592329ff0793fc99f8e5b0e7031a2248342102f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195741"
---
# <span data-ttu-id="67b1d-101">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="67b1d-101">New-AzAlertRuleEmail</span></span>

## <span data-ttu-id="67b1d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67b1d-102">SYNOPSIS</span></span>
<span data-ttu-id="67b1d-103">E-mail-művelet létrehozása egy figyelmeztetési szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="67b1d-103">Creates an email action for an alert rule.</span></span>

## <span data-ttu-id="67b1d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67b1d-104">SYNTAX</span></span>

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67b1d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="67b1d-105">DESCRIPTION</span></span>
<span data-ttu-id="67b1d-106">A **New-AzAlertRuleEmail** parancsmag e-mail-műveleteket hoz létre egy figyelmeztetési szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="67b1d-106">The **New-AzAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="67b1d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="67b1d-107">EXAMPLES</span></span>

### <span data-ttu-id="67b1d-108">Példa 1: figyelmeztetési szabály létrehozása e-mail-művelet a szolgáltatás tulajdonosainak</span><span class="sxs-lookup"><span data-stu-id="67b1d-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="67b1d-109">Ez a parancs figyelmeztetési szabályt hoz létre a szolgáltatás tulajdonosainak küldött e-mail-műveletről, ha riasztási szabály van kirúgva.</span><span class="sxs-lookup"><span data-stu-id="67b1d-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="67b1d-110">2. példa: figyelmeztetési szabály létrehozása e-mail-művelet a nem szolgáltató tulajdonosok számára</span><span class="sxs-lookup"><span data-stu-id="67b1d-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="67b1d-111">Ez a parancs figyelmeztetési szabályt hoz létre a megadott e-mail-címekhez, de a szolgáltatás tulajdonosainak nem.</span><span class="sxs-lookup"><span data-stu-id="67b1d-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="67b1d-112">3. példa: figyelmeztetési szabály létrehozása e-mail-művelet a szolgáltatás tulajdonosai és a nem szolgáltató tulajdonosok számára</span><span class="sxs-lookup"><span data-stu-id="67b1d-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="67b1d-113">Ez a parancs figyelmeztetési szabályt hoz létre a megadott címhez és a szolgáltatás tulajdonosainak szóló e-mail-művelethez.</span><span class="sxs-lookup"><span data-stu-id="67b1d-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="67b1d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67b1d-114">PARAMETERS</span></span>

### <span data-ttu-id="67b1d-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="67b1d-115">-CustomEmail</span></span>
<span data-ttu-id="67b1d-116">A pontosvesszővel tagolt e-mail-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="67b1d-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="67b1d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67b1d-117">-DefaultProfile</span></span>
<span data-ttu-id="67b1d-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="67b1d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67b1d-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="67b1d-119">-SendToServiceOwner</span></span>
<span data-ttu-id="67b1d-120">Jelzi, hogy a művelet elküld egy e-mailt a szolgáltatás tulajdonosainak, amikor a szabály tüzeket hoz meg.</span><span class="sxs-lookup"><span data-stu-id="67b1d-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="67b1d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67b1d-121">CommonParameters</span></span>
<span data-ttu-id="67b1d-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67b1d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67b1d-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="67b1d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67b1d-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67b1d-124">INPUTS</span></span>

### <span data-ttu-id="67b1d-125">System. string []</span><span class="sxs-lookup"><span data-stu-id="67b1d-125">System.String[]</span></span>

### <span data-ttu-id="67b1d-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="67b1d-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="67b1d-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67b1d-127">OUTPUTS</span></span>

### <span data-ttu-id="67b1d-128">Microsoft. Azure. Management. monitor. Management. models. RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="67b1d-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="67b1d-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67b1d-129">NOTES</span></span>

## <span data-ttu-id="67b1d-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67b1d-130">RELATED LINKS</span></span>

[<span data-ttu-id="67b1d-131">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="67b1d-131">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="67b1d-132">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="67b1d-132">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="67b1d-133">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="67b1d-133">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="67b1d-134">Új – AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="67b1d-134">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


