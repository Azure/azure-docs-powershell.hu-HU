---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertruleemail
schema: 2.0.0
ms.openlocfilehash: 20134cc0f2eef927361439fb431bc4ab9308a9a1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850826"
---
# <span data-ttu-id="10c5e-101">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="10c5e-101">New-AzureRmAlertRuleEmail</span></span>

## <span data-ttu-id="10c5e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="10c5e-103">E-mail-művelet létrehozása egy figyelmeztetési szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="10c5e-103">Creates an email action for an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10c5e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10c5e-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10c5e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="10c5e-105">DESCRIPTION</span></span>
<span data-ttu-id="10c5e-106">A **New-AzureRmAlertRuleEmail** parancsmag e-mail-műveleteket hoz létre egy figyelmeztetési szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="10c5e-106">The **New-AzureRmAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="10c5e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="10c5e-107">EXAMPLES</span></span>

### <span data-ttu-id="10c5e-108">Példa 1: figyelmeztetési szabály létrehozása e-mail-művelet a szolgáltatás tulajdonosainak</span><span class="sxs-lookup"><span data-stu-id="10c5e-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="10c5e-109">Ez a parancs figyelmeztetési szabályt hoz létre a szolgáltatás tulajdonosainak küldött e-mail-műveletről, ha riasztási szabály van kirúgva.</span><span class="sxs-lookup"><span data-stu-id="10c5e-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="10c5e-110">2. példa: figyelmeztetési szabály létrehozása e-mail-művelet a nem szolgáltató tulajdonosok számára</span><span class="sxs-lookup"><span data-stu-id="10c5e-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="10c5e-111">Ez a parancs figyelmeztetési szabályt hoz létre a megadott e-mail-címekhez, de a szolgáltatás tulajdonosainak nem.</span><span class="sxs-lookup"><span data-stu-id="10c5e-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="10c5e-112">3. példa: figyelmeztetési szabály létrehozása e-mail-művelet a szolgáltatás tulajdonosai és a nem szolgáltató tulajdonosok számára</span><span class="sxs-lookup"><span data-stu-id="10c5e-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="10c5e-113">Ez a parancs figyelmeztetési szabályt hoz létre a megadott címhez és a szolgáltatás tulajdonosainak szóló e-mail-művelethez.</span><span class="sxs-lookup"><span data-stu-id="10c5e-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="10c5e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10c5e-114">PARAMETERS</span></span>

### <span data-ttu-id="10c5e-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="10c5e-115">-CustomEmail</span></span>
<span data-ttu-id="10c5e-116">A pontosvesszővel tagolt e-mail-címek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="10c5e-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="10c5e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10c5e-117">-DefaultProfile</span></span>
<span data-ttu-id="10c5e-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="10c5e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c5e-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="10c5e-119">-SendToServiceOwner</span></span>
<span data-ttu-id="10c5e-120">Jelzi, hogy a művelet elküld egy e-mailt a szolgáltatás tulajdonosainak, amikor a szabály tüzeket hoz meg.</span><span class="sxs-lookup"><span data-stu-id="10c5e-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="10c5e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10c5e-121">CommonParameters</span></span>
<span data-ttu-id="10c5e-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10c5e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10c5e-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10c5e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10c5e-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10c5e-124">INPUTS</span></span>

### <span data-ttu-id="10c5e-125">System. string []</span><span class="sxs-lookup"><span data-stu-id="10c5e-125">System.String[]</span></span>

### <span data-ttu-id="10c5e-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="10c5e-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="10c5e-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10c5e-127">OUTPUTS</span></span>

### <span data-ttu-id="10c5e-128">Microsoft. Azure. Management. monitor. Management. models. RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="10c5e-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="10c5e-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10c5e-129">NOTES</span></span>

## <span data-ttu-id="10c5e-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10c5e-130">RELATED LINKS</span></span>



[<span data-ttu-id="10c5e-131">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="10c5e-131">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="10c5e-132">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="10c5e-132">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="10c5e-133">Új – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="10c5e-133">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


