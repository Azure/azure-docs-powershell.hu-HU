---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: 010698183dec206002c0966fb8f37d629d24794a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012983"
---
# <span data-ttu-id="d7aa1-101">New-AzAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="d7aa1-101">New-AzAutoscaleNotification</span></span>

## <span data-ttu-id="d7aa1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7aa1-102">SYNOPSIS</span></span>
<span data-ttu-id="d7aa1-103">E-mail-értesítést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d7aa1-103">Creates an Autoscale email notification.</span></span>

## <span data-ttu-id="d7aa1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7aa1-104">SYNTAX</span></span>

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7aa1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7aa1-105">DESCRIPTION</span></span>
<span data-ttu-id="d7aa1-106">A **New-AzAutoscaleNotification** parancsmag e-mail-értesítést hoz létre az automéretarányhoz.</span><span class="sxs-lookup"><span data-stu-id="d7aa1-106">The **New-AzAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="d7aa1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d7aa1-107">EXAMPLES</span></span>

### <span data-ttu-id="d7aa1-108">1. példa: automéretarányos e-mail-értesítés létrehozása</span><span class="sxs-lookup"><span data-stu-id="d7aa1-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="d7aa1-109">Ez a parancs egy Autosacale-e-mail-értesítést hoz létre két megadott címhez.</span><span class="sxs-lookup"><span data-stu-id="d7aa1-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="d7aa1-110">2. példa: automéretarányos e-mail-értesítés létrehozása az előfizetés rendszergazdájának</span><span class="sxs-lookup"><span data-stu-id="d7aa1-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="d7aa1-111">Ez a parancs Autosacale-e-mail-értesítést hoz létre az előfizetés rendszergazdájához.</span><span class="sxs-lookup"><span data-stu-id="d7aa1-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="d7aa1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7aa1-112">PARAMETERS</span></span>

### <span data-ttu-id="d7aa1-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="d7aa1-113">-CustomEmail</span></span>
<span data-ttu-id="d7aa1-114">Az e-mail-címek vesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7aa1-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="d7aa1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7aa1-115">-DefaultProfile</span></span>
<span data-ttu-id="d7aa1-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d7aa1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7aa1-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="d7aa1-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="d7aa1-118">Jelzi, hogy ez a művelet e-mailben értesítést küld az előfizetés rendszergazdájától.</span><span class="sxs-lookup"><span data-stu-id="d7aa1-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="d7aa1-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="d7aa1-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="d7aa1-120">Azt jelzi, hogy ez a művelet e-mail-értesítést küld az előfizetés közös rendszergazdáinak.</span><span class="sxs-lookup"><span data-stu-id="d7aa1-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="d7aa1-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="d7aa1-121">-Webhook</span></span>
<span data-ttu-id="d7aa1-122">Az automéretarányos webhorgok vesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7aa1-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="d7aa1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7aa1-123">CommonParameters</span></span>
<span data-ttu-id="d7aa1-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7aa1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7aa1-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d7aa1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7aa1-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7aa1-126">INPUTS</span></span>

### <span data-ttu-id="d7aa1-127">Microsoft. Azure. Management. monitor. Management. models. WebhookNotification []</span><span class="sxs-lookup"><span data-stu-id="d7aa1-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="d7aa1-128">System. string []</span><span class="sxs-lookup"><span data-stu-id="d7aa1-128">System.String[]</span></span>

### <span data-ttu-id="d7aa1-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d7aa1-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d7aa1-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7aa1-130">OUTPUTS</span></span>

### <span data-ttu-id="d7aa1-131">Microsoft. Azure. Management. monitor. Management. models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="d7aa1-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="d7aa1-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7aa1-132">NOTES</span></span>

## <span data-ttu-id="d7aa1-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7aa1-133">RELATED LINKS</span></span>

[<span data-ttu-id="d7aa1-134">Új – AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="d7aa1-134">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


