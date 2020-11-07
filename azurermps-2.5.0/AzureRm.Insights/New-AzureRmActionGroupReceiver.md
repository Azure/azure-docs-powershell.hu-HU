---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroupreceiver
schema: 2.0.0
ms.openlocfilehash: 0f452818db1af3f3a69db58f82b89e6cfa8ee461
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848286"
---
# <span data-ttu-id="7494c-101">New-AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="7494c-101">New-AzureRmActionGroupReceiver</span></span>

## <span data-ttu-id="7494c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7494c-102">SYNOPSIS</span></span>
<span data-ttu-id="7494c-103">Új akciócsoport-vevőkészülék létrehozása.</span><span class="sxs-lookup"><span data-stu-id="7494c-103">Creates an new action group receiver.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7494c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7494c-104">SYNTAX</span></span>

### <span data-ttu-id="7494c-105">NewEmailReceiver (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7494c-105">NewEmailReceiver (Default)</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7494c-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="7494c-106">NewSmsReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7494c-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="7494c-107">NewWebhookReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7494c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7494c-108">DESCRIPTION</span></span>
<span data-ttu-id="7494c-109">A **New-AzureRmActionGroupReceiver** parancsmag új műveleti csoportba foglalt vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="7494c-109">The **New-AzureRmActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="7494c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7494c-110">EXAMPLES</span></span>

### <span data-ttu-id="7494c-111">Példa 1: új e-mail-vevőkészülék létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="7494c-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzureRmActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="7494c-112">A parancs új e-mail-vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="7494c-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="7494c-113">2. példa: új SMS-vevőkészülék létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="7494c-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzureRmActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="7494c-114">A parancs új SMS-vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="7494c-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="7494c-115">3. példa: új webhook-vevőkészülék létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="7494c-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzureRmActionGroupReceiver -Name 'webhookReceiver1' -SMSReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="7494c-116">A parancs új webhook-vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="7494c-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="7494c-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7494c-117">PARAMETERS</span></span>

### <span data-ttu-id="7494c-118">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="7494c-118">-CountryCode</span></span>
<span data-ttu-id="7494c-119">Az SMS-vevőkészülék országkódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="7494c-119">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="7494c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7494c-120">-DefaultProfile</span></span>
<span data-ttu-id="7494c-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7494c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7494c-122">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="7494c-122">-EmailAddress</span></span>
<span data-ttu-id="7494c-123">Az E-mail címzett címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7494c-123">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="7494c-124">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="7494c-124">-EmailReceiver</span></span>
<span data-ttu-id="7494c-125">E-mail-címzett létrehozásának megadása</span><span class="sxs-lookup"><span data-stu-id="7494c-125">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="7494c-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7494c-126">-Name</span></span>
<span data-ttu-id="7494c-127">A címzett nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7494c-127">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="7494c-128">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="7494c-128">-PhoneNumber</span></span>
<span data-ttu-id="7494c-129">Az SMS-vevőkészülék telefonszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7494c-129">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="7494c-130">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="7494c-130">-ServiceUri</span></span>
<span data-ttu-id="7494c-131">A webhook-vevőkészülék URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7494c-131">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="7494c-132">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="7494c-132">-SmsReceiver</span></span>
<span data-ttu-id="7494c-133">Az SMS-vevőkészülék létrehozásának megadása</span><span class="sxs-lookup"><span data-stu-id="7494c-133">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="7494c-134">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="7494c-134">-WebhookReceiver</span></span>
<span data-ttu-id="7494c-135">A webhook-vevőkészülék létrehozásának meghatározása</span><span class="sxs-lookup"><span data-stu-id="7494c-135">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="7494c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7494c-136">CommonParameters</span></span>
<span data-ttu-id="7494c-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7494c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7494c-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7494c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7494c-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7494c-139">INPUTS</span></span>

### <span data-ttu-id="7494c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7494c-140">System.String</span></span>

### <span data-ttu-id="7494c-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7494c-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7494c-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7494c-142">OUTPUTS</span></span>

### <span data-ttu-id="7494c-143">Microsoft. Azure. commands. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="7494c-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="7494c-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7494c-144">NOTES</span></span>

## <span data-ttu-id="7494c-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7494c-145">RELATED LINKS</span></span>

<span data-ttu-id="7494c-146">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="7494c-146">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span></span>