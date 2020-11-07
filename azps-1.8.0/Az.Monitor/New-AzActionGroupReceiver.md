---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: 35f540d26464b7cdc4b08916f1397b71ee7cca18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835065"
---
# <span data-ttu-id="6be48-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="6be48-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="6be48-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6be48-102">SYNOPSIS</span></span>
<span data-ttu-id="6be48-103">Új akciócsoport-vevőkészülék létrehozása.</span><span class="sxs-lookup"><span data-stu-id="6be48-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="6be48-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6be48-104">SYNTAX</span></span>

### <span data-ttu-id="6be48-105">NewEmailReceiver (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6be48-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6be48-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="6be48-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6be48-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="6be48-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6be48-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6be48-108">DESCRIPTION</span></span>
<span data-ttu-id="6be48-109">A **New-AzActionGroupReceiver** parancsmag új műveleti csoportba foglalt vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="6be48-109">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="6be48-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6be48-110">EXAMPLES</span></span>

### <span data-ttu-id="6be48-111">Példa 1: új e-mail-vevőkészülék létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="6be48-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="6be48-112">A parancs új e-mail-vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="6be48-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="6be48-113">2. példa: új SMS-vevőkészülék létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="6be48-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="6be48-114">A parancs új SMS-vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="6be48-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="6be48-115">3. példa: új webhook-vevőkészülék létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="6be48-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="6be48-116">A parancs új webhook-vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="6be48-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="6be48-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6be48-117">PARAMETERS</span></span>

### <span data-ttu-id="6be48-118">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="6be48-118">-CountryCode</span></span>
<span data-ttu-id="6be48-119">Az SMS-vevőkészülék országkódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="6be48-119">Specifies the country code for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6be48-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6be48-120">-DefaultProfile</span></span>
<span data-ttu-id="6be48-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6be48-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6be48-122">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="6be48-122">-EmailAddress</span></span>
<span data-ttu-id="6be48-123">Az E-mail címzett címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6be48-123">Specifies the address for the Email receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewEmailReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6be48-124">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="6be48-124">-EmailReceiver</span></span>
<span data-ttu-id="6be48-125">E-mail-címzett létrehozásának megadása</span><span class="sxs-lookup"><span data-stu-id="6be48-125">Specifies to create an Email receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewEmailReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6be48-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6be48-126">-Name</span></span>
<span data-ttu-id="6be48-127">A címzett nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6be48-127">Specifies the name for the receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6be48-128">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="6be48-128">-PhoneNumber</span></span>
<span data-ttu-id="6be48-129">Az SMS-vevőkészülék telefonszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6be48-129">Specifies the phone number for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6be48-130">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="6be48-130">-ServiceUri</span></span>
<span data-ttu-id="6be48-131">A webhook-vevőkészülék URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6be48-131">Specifies the URI for the webhook receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6be48-132">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="6be48-132">-SmsReceiver</span></span>
<span data-ttu-id="6be48-133">Az SMS-vevőkészülék létrehozásának megadása</span><span class="sxs-lookup"><span data-stu-id="6be48-133">Specifies to create a SMS receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6be48-134">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="6be48-134">-WebhookReceiver</span></span>
<span data-ttu-id="6be48-135">A webhook-vevőkészülék létrehozásának meghatározása</span><span class="sxs-lookup"><span data-stu-id="6be48-135">Specifies to create a webhook receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6be48-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6be48-136">CommonParameters</span></span>
<span data-ttu-id="6be48-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6be48-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6be48-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6be48-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6be48-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6be48-139">INPUTS</span></span>

### <span data-ttu-id="6be48-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6be48-140">System.String</span></span>

### <span data-ttu-id="6be48-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6be48-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6be48-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6be48-142">OUTPUTS</span></span>

### <span data-ttu-id="6be48-143">Microsoft. Azure. commands. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="6be48-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="6be48-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6be48-144">NOTES</span></span>

## <span data-ttu-id="6be48-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6be48-145">RELATED LINKS</span></span>

<span data-ttu-id="6be48-146">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="6be48-146">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
