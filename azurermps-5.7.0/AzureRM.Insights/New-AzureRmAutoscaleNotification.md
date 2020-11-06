---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
ms.openlocfilehash: ee95455b5081105ec4e28a4811e46ca92bfbc240
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496547"
---
# <span data-ttu-id="22c17-101">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="22c17-101">New-AzureRmAutoscaleNotification</span></span>

## <span data-ttu-id="22c17-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22c17-102">SYNOPSIS</span></span>
<span data-ttu-id="22c17-103">E-mail-értesítést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="22c17-103">Creates an Autoscale email notification.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22c17-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22c17-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator] 
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22c17-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="22c17-105">DESCRIPTION</span></span>
<span data-ttu-id="22c17-106">A **New-AzureRmAutoscaleNotification** parancsmag e-mail-értesítést hoz létre az automéretarányhoz.</span><span class="sxs-lookup"><span data-stu-id="22c17-106">The **New-AzureRmAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="22c17-107">Példák</span><span class="sxs-lookup"><span data-stu-id="22c17-107">EXAMPLES</span></span>

### <span data-ttu-id="22c17-108">1. példa: automéretarányos e-mail-értesítés létrehozása</span><span class="sxs-lookup"><span data-stu-id="22c17-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="22c17-109">Ez a parancs egy Autosacale-e-mail-értesítést hoz létre két megadott címhez.</span><span class="sxs-lookup"><span data-stu-id="22c17-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="22c17-110">2. példa: automéretarányos e-mail-értesítés létrehozása az előfizetés rendszergazdájának</span><span class="sxs-lookup"><span data-stu-id="22c17-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="22c17-111">Ez a parancs Autosacale-e-mail-értesítést hoz létre az előfizetés rendszergazdájához.</span><span class="sxs-lookup"><span data-stu-id="22c17-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="22c17-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22c17-112">PARAMETERS</span></span>

### <span data-ttu-id="22c17-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="22c17-113">-CustomEmail</span></span>
<span data-ttu-id="22c17-114">Az e-mail-címek vesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="22c17-114">Specifies a comma-separated list of email addresses.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: CustomEmails

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22c17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22c17-115">-DefaultProfile</span></span>
<span data-ttu-id="22c17-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="22c17-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c17-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="22c17-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="22c17-118">Jelzi, hogy ez a művelet e-mailben értesítést küld az előfizetés rendszergazdájától.</span><span class="sxs-lookup"><span data-stu-id="22c17-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22c17-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="22c17-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="22c17-120">Azt jelzi, hogy ez a művelet e-mail-értesítést küld az előfizetés közös rendszergazdáinak.</span><span class="sxs-lookup"><span data-stu-id="22c17-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: SendEmailToSubscriptionCoAdministrators

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22c17-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="22c17-121">-Webhook</span></span>
<span data-ttu-id="22c17-122">Az automéretarányos webhorgok vesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="22c17-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

```yaml
Type: WebhookNotification[]
Parameter Sets: (All)
Aliases: Webhooks

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22c17-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22c17-123">CommonParameters</span></span>
<span data-ttu-id="22c17-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22c17-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22c17-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22c17-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22c17-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22c17-126">INPUTS</span></span>

### <span data-ttu-id="22c17-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="22c17-127">None</span></span>
<span data-ttu-id="22c17-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="22c17-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="22c17-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22c17-129">OUTPUTS</span></span>

### <span data-ttu-id="22c17-130">Microsoft. Azure. Management. monitor. Management. models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="22c17-130">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="22c17-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22c17-131">NOTES</span></span>

## <span data-ttu-id="22c17-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22c17-132">RELATED LINKS</span></span>

[<span data-ttu-id="22c17-133">Új – AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="22c17-133">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


