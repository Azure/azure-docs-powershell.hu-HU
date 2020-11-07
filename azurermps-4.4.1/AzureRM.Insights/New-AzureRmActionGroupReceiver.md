---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroupReceiver.md
ms.openlocfilehash: cd08e0106fe78ddae04ac4543210b310fe3aa579
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679083"
---
# <span data-ttu-id="b10c6-101">New-AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="b10c6-101">New-AzureRmActionGroupReceiver</span></span>

## <span data-ttu-id="b10c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b10c6-102">SYNOPSIS</span></span>
<span data-ttu-id="b10c6-103">Új akciócsoport-vevőkészülék létrehozása.</span><span class="sxs-lookup"><span data-stu-id="b10c6-103">Creates an new action group receiver.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b10c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b10c6-104">SYNTAX</span></span>

### <span data-ttu-id="b10c6-105">NewEmailReceiver (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b10c6-105">NewEmailReceiver (Default)</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b10c6-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="b10c6-106">NewSmsReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b10c6-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="b10c6-107">NewWebhookReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b10c6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b10c6-108">DESCRIPTION</span></span>
<span data-ttu-id="b10c6-109">A **New-AzureRmActionGroupReceiver** parancsmag új műveleti csoportba foglalt vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="b10c6-109">The **New-AzureRmActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="b10c6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b10c6-110">EXAMPLES</span></span>

### <span data-ttu-id="b10c6-111">Példa 1: új e-mail-vevőkészülék létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="b10c6-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzureRmActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="b10c6-112">A parancs új e-mail-vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="b10c6-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="b10c6-113">2. példa: új SMS-vevőkészülék létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="b10c6-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzureRmActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="b10c6-114">A parancs új SMS-vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="b10c6-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="b10c6-115">3. példa: új webhook-vevőkészülék létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="b10c6-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzureRmActionGroupReceiver -Name 'webhookReceiver1' -SMSReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="b10c6-116">A parancs új webhook-vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="b10c6-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="b10c6-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b10c6-117">PARAMETERS</span></span>

### <span data-ttu-id="b10c6-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b10c6-118">-Name</span></span>
<span data-ttu-id="b10c6-119">A címzett nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b10c6-119">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="b10c6-120">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="b10c6-120">-EmailAddress</span></span>
<span data-ttu-id="b10c6-121">Az E-mail címzett címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b10c6-121">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="b10c6-122">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="b10c6-122">-CountryCode</span></span>
<span data-ttu-id="b10c6-123">Az SMS-vevőkészülék országkódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b10c6-123">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="b10c6-124">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="b10c6-124">-PhoneNumber</span></span>
<span data-ttu-id="b10c6-125">Az SMS-vevőkészülék telefonszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b10c6-125">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="b10c6-126">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="b10c6-126">-ServiceUri</span></span>
<span data-ttu-id="b10c6-127">A webhook-vevőkészülék URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b10c6-127">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="b10c6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b10c6-128">-DefaultProfile</span></span>
<span data-ttu-id="b10c6-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b10c6-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b10c6-130">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="b10c6-130">-EmailReceiver</span></span>
<span data-ttu-id="b10c6-131">E-mail-címzett létrehozásának megadása</span><span class="sxs-lookup"><span data-stu-id="b10c6-131">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="b10c6-132">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="b10c6-132">-SmsReceiver</span></span>
<span data-ttu-id="b10c6-133">Az SMS-vevőkészülék létrehozásának megadása</span><span class="sxs-lookup"><span data-stu-id="b10c6-133">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="b10c6-134">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="b10c6-134">-WebhookReceiver</span></span>
<span data-ttu-id="b10c6-135">A webhook-vevőkészülék létrehozásának meghatározása</span><span class="sxs-lookup"><span data-stu-id="b10c6-135">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="b10c6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b10c6-136">CommonParameters</span></span>
<span data-ttu-id="b10c6-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b10c6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b10c6-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b10c6-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b10c6-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b10c6-139">INPUTS</span></span>

## <span data-ttu-id="b10c6-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b10c6-140">OUTPUTS</span></span>

### <span data-ttu-id="b10c6-141">Microsoft. Azure. commands. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="b10c6-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="b10c6-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b10c6-142">NOTES</span></span>

## <span data-ttu-id="b10c6-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b10c6-143">RELATED LINKS</span></span>

<span data-ttu-id="b10c6-144">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="b10c6-144">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span></span>
