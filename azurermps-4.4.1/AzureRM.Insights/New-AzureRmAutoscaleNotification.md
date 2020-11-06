---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
ms.openlocfilehash: f6791d2cc962f0bb0db038ad8c5391425c09bfbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504155"
---
# <span data-ttu-id="3d893-101">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="3d893-101">New-AzureRmAutoscaleNotification</span></span>

## <span data-ttu-id="3d893-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d893-102">SYNOPSIS</span></span>
<span data-ttu-id="3d893-103">E-mail-értesítést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3d893-103">Creates an Autoscale email notification.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d893-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d893-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleNotification [[-Webhooks] <WebhookNotification[]>] [[-CustomEmails] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d893-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d893-105">DESCRIPTION</span></span>
<span data-ttu-id="3d893-106">A **New-AzureRmAutoscaleNotification** parancsmag e-mail-értesítést hoz létre az automéretarányhoz.</span><span class="sxs-lookup"><span data-stu-id="3d893-106">The **New-AzureRmAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="3d893-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3d893-107">EXAMPLES</span></span>

### <span data-ttu-id="3d893-108">1. példa: automéretarányos e-mail-értesítés létrehozása</span><span class="sxs-lookup"><span data-stu-id="3d893-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="3d893-109">Ez a parancs egy Autosacale-e-mail-értesítést hoz létre két megadott címhez.</span><span class="sxs-lookup"><span data-stu-id="3d893-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="3d893-110">2. példa: automéretarányos e-mail-értesítés létrehozása az előfizetés rendszergazdájának</span><span class="sxs-lookup"><span data-stu-id="3d893-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="3d893-111">Ez a parancs Autosacale-e-mail-értesítést hoz létre az előfizetés rendszergazdájához.</span><span class="sxs-lookup"><span data-stu-id="3d893-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="3d893-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d893-112">PARAMETERS</span></span>

### <span data-ttu-id="3d893-113">-CustomEmails</span><span class="sxs-lookup"><span data-stu-id="3d893-113">-CustomEmails</span></span>
<span data-ttu-id="3d893-114">Az e-mail-címek vesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d893-114">Specifies a comma-separated list of email addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d893-115">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="3d893-115">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="3d893-116">Jelzi, hogy ez a művelet e-mailben értesítést küld az előfizetés rendszergazdájától.</span><span class="sxs-lookup"><span data-stu-id="3d893-116">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="3d893-117">-SendEmailToSubscriptionCoAdministrators</span><span class="sxs-lookup"><span data-stu-id="3d893-117">-SendEmailToSubscriptionCoAdministrators</span></span>
<span data-ttu-id="3d893-118">Azt jelzi, hogy ez a művelet e-mail-értesítést küld az előfizetés közös rendszergazdáinak.</span><span class="sxs-lookup"><span data-stu-id="3d893-118">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="3d893-119">-Webkampók</span><span class="sxs-lookup"><span data-stu-id="3d893-119">-Webhooks</span></span>
<span data-ttu-id="3d893-120">Az automéretarányos webhorgok vesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d893-120">Specifies a comma-separated list of Autoscale webhooks.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d893-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d893-121">-DefaultProfile</span></span>
<span data-ttu-id="3d893-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3d893-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d893-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d893-123">CommonParameters</span></span>
<span data-ttu-id="3d893-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d893-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d893-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d893-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d893-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d893-126">INPUTS</span></span>

## <span data-ttu-id="3d893-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d893-127">OUTPUTS</span></span>

### <span data-ttu-id="3d893-128">Microsoft. Azure. Management. monitor. Management. models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="3d893-128">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="3d893-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d893-129">NOTES</span></span>

## <span data-ttu-id="3d893-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d893-130">RELATED LINKS</span></span>

[<span data-ttu-id="3d893-131">Új – AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="3d893-131">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


