---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: 010698183dec206002c0966fb8f37d629d24794a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338130"
---
# <span data-ttu-id="19a54-101">New-AzAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="19a54-101">New-AzAutoscaleNotification</span></span>

## <span data-ttu-id="19a54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19a54-102">SYNOPSIS</span></span>
<span data-ttu-id="19a54-103">Automatikus méretezésű e-mail-értesítést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="19a54-103">Creates an Autoscale email notification.</span></span>

## <span data-ttu-id="19a54-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="19a54-104">SYNTAX</span></span>

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19a54-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="19a54-105">DESCRIPTION</span></span>
<span data-ttu-id="19a54-106">A **New-AzAutoscaleNotification parancsmag** létrehoz egy e-mail értesítést az automatikus méretezésről.</span><span class="sxs-lookup"><span data-stu-id="19a54-106">The **New-AzAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="19a54-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="19a54-107">EXAMPLES</span></span>

### <span data-ttu-id="19a54-108">1. példa: Automatikus e-mail-értesítés létrehozása</span><span class="sxs-lookup"><span data-stu-id="19a54-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="19a54-109">Ez a parancs létrehoz egy Autosacale e-mail értesítést két megadott címhez.</span><span class="sxs-lookup"><span data-stu-id="19a54-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="19a54-110">2. példa: Automatikus méretezésű e-mail értesítés létrehozása az előfizetés rendszergazdájához</span><span class="sxs-lookup"><span data-stu-id="19a54-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="19a54-111">Ez a parancs létrehoz egy Autosacale e-mail értesítést az előfizetés rendszergazdájának.</span><span class="sxs-lookup"><span data-stu-id="19a54-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="19a54-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19a54-112">PARAMETERS</span></span>

### <span data-ttu-id="19a54-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="19a54-113">-CustomEmail</span></span>
<span data-ttu-id="19a54-114">Az e-mail-címek vesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="19a54-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="19a54-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19a54-115">-DefaultProfile</span></span>
<span data-ttu-id="19a54-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="19a54-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19a54-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="19a54-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="19a54-118">Azt jelzi, hogy a művelet e-mailben értesítést küld az előfizetés rendszergazdájának.</span><span class="sxs-lookup"><span data-stu-id="19a54-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="19a54-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="19a54-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="19a54-120">Azt jelzi, hogy a művelet e-mailben értesítést küld az előfizetés társ-rendszergazdáinak.</span><span class="sxs-lookup"><span data-stu-id="19a54-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="19a54-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="19a54-121">-Webhook</span></span>
<span data-ttu-id="19a54-122">Az automatikus méretezésű webhookok vesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="19a54-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="19a54-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19a54-123">CommonParameters</span></span>
<span data-ttu-id="19a54-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19a54-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19a54-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19a54-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19a54-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19a54-126">INPUTS</span></span>

### <span data-ttu-id="19a54-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span><span class="sxs-lookup"><span data-stu-id="19a54-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="19a54-128">System.String[]</span><span class="sxs-lookup"><span data-stu-id="19a54-128">System.String[]</span></span>

### <span data-ttu-id="19a54-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="19a54-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="19a54-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19a54-130">OUTPUTS</span></span>

### <span data-ttu-id="19a54-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="19a54-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="19a54-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="19a54-132">NOTES</span></span>

## <span data-ttu-id="19a54-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19a54-133">RELATED LINKS</span></span>

[<span data-ttu-id="19a54-134">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="19a54-134">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


