---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
ms.openlocfilehash: a978fce4d44a061796597f2f3ae08c78c1021bdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498035"
---
# <span data-ttu-id="03bf8-101">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="03bf8-101">New-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="03bf8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="03bf8-103">API-kezelési terméket hoz létre.</span><span class="sxs-lookup"><span data-stu-id="03bf8-103">Creates an API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03bf8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03bf8-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03bf8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="03bf8-105">DESCRIPTION</span></span>
<span data-ttu-id="03bf8-106">A **New-AzureRmApiManagementProduct** PARANCSMAG egy API-kezelési terméket hoz létre.</span><span class="sxs-lookup"><span data-stu-id="03bf8-106">The **New-AzureRmApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="03bf8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="03bf8-107">EXAMPLES</span></span>

### <span data-ttu-id="03bf8-108">1. példa: előfizetést nem igénylő termékek létrehozása</span><span class="sxs-lookup"><span data-stu-id="03bf8-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>New-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="03bf8-109">Ez a parancs API-kezelési terméket hoz létre.</span><span class="sxs-lookup"><span data-stu-id="03bf8-109">This command creates an API Management product.</span></span>
<span data-ttu-id="03bf8-110">Nincs szükség előfizetésre.</span><span class="sxs-lookup"><span data-stu-id="03bf8-110">No subscription is required.</span></span>

### <span data-ttu-id="03bf8-111">2. példa: előfizetés és jóváhagyást igénylő termékek létrehozása</span><span class="sxs-lookup"><span data-stu-id="03bf8-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>New-AzureRmApiManagementProduct -Context $APImContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="03bf8-112">Ez a parancs létrehoz egy terméket.</span><span class="sxs-lookup"><span data-stu-id="03bf8-112">This command creates a product.</span></span>
<span data-ttu-id="03bf8-113">Előfizetés és jóváhagyás szükséges.</span><span class="sxs-lookup"><span data-stu-id="03bf8-113">A subscription and approval are required.</span></span>
<span data-ttu-id="03bf8-114">Ez a parancs 10 napra állítja be az értesítési időszakot.</span><span class="sxs-lookup"><span data-stu-id="03bf8-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="03bf8-115">Az előfizetési időtartam egy évre van állítva.</span><span class="sxs-lookup"><span data-stu-id="03bf8-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="03bf8-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03bf8-116">PARAMETERS</span></span>

### <span data-ttu-id="03bf8-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="03bf8-117">-ApprovalRequired</span></span>
<span data-ttu-id="03bf8-118">Azt jelzi, hogy a termékké való előfizetés jóváhagyást igényel-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="03bf8-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="03bf8-119">Alapértelmezés szerint ez a paraméter **$false**.</span><span class="sxs-lookup"><span data-stu-id="03bf8-119">By default, this parameter is **$False**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03bf8-120">-Környezet</span><span class="sxs-lookup"><span data-stu-id="03bf8-120">-Context</span></span>
<span data-ttu-id="03bf8-121">Egy **PsApiManagementContext** -objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="03bf8-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03bf8-122">-Leírás</span><span class="sxs-lookup"><span data-stu-id="03bf8-122">-Description</span></span>
<span data-ttu-id="03bf8-123">A termékleírást adja meg.</span><span class="sxs-lookup"><span data-stu-id="03bf8-123">Specifies the product description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03bf8-124">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="03bf8-124">-LegalTerms</span></span>
<span data-ttu-id="03bf8-125">A szorzat jogi használati feltételeit adja meg.</span><span class="sxs-lookup"><span data-stu-id="03bf8-125">Specifies the legal terms of use of the product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03bf8-126">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="03bf8-126">-ProductId</span></span>
<span data-ttu-id="03bf8-127">Az új szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="03bf8-127">Specifies the identifier of new product.</span></span>
<span data-ttu-id="03bf8-128">Ha nem adja meg ezt a paramétert, egy új terméket hoz létre.</span><span class="sxs-lookup"><span data-stu-id="03bf8-128">If you do not specify this parameter, a new product is generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03bf8-129">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="03bf8-129">-State</span></span>
<span data-ttu-id="03bf8-130">A termékek állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="03bf8-130">Specifies the product state.</span></span>
<span data-ttu-id="03bf8-131">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="03bf8-131">psdx_paramvalues</span></span>

- <span data-ttu-id="03bf8-132">NotPublished</span><span class="sxs-lookup"><span data-stu-id="03bf8-132">NotPublished</span></span>
- <span data-ttu-id="03bf8-133">Közzétett</span><span class="sxs-lookup"><span data-stu-id="03bf8-133">Published</span></span> 

<span data-ttu-id="03bf8-134">Az alapértelmezett érték a NotPublished.</span><span class="sxs-lookup"><span data-stu-id="03bf8-134">The default value is NotPublished.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState]
Parameter Sets: (All)
Aliases: 
Accepted values: NotPublished, Published

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03bf8-135">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="03bf8-135">-SubscriptionRequired</span></span>
<span data-ttu-id="03bf8-136">Azt jelzi, hogy a terméket előfizetést kell-e adni.</span><span class="sxs-lookup"><span data-stu-id="03bf8-136">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="03bf8-137">Az alapértelmezett érték **$true**.</span><span class="sxs-lookup"><span data-stu-id="03bf8-137">The default value is **$True**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03bf8-138">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="03bf8-138">-SubscriptionsLimit</span></span>
<span data-ttu-id="03bf8-139">Az egyidejű előfizetések maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="03bf8-139">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="03bf8-140">Az alapértelmezett érték 1.</span><span class="sxs-lookup"><span data-stu-id="03bf8-140">The default value is 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03bf8-141">-Cím</span><span class="sxs-lookup"><span data-stu-id="03bf8-141">-Title</span></span>
<span data-ttu-id="03bf8-142">Megadja a terméknév címét.</span><span class="sxs-lookup"><span data-stu-id="03bf8-142">Specifies the product title.</span></span>

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

### <span data-ttu-id="03bf8-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03bf8-143">-DefaultProfile</span></span>
<span data-ttu-id="03bf8-144">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03bf8-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03bf8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03bf8-145">CommonParameters</span></span>
<span data-ttu-id="03bf8-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03bf8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03bf8-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03bf8-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03bf8-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03bf8-148">INPUTS</span></span>

## <span data-ttu-id="03bf8-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03bf8-149">OUTPUTS</span></span>

### <span data-ttu-id="03bf8-150">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="03bf8-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="03bf8-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03bf8-151">NOTES</span></span>

## <span data-ttu-id="03bf8-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03bf8-152">RELATED LINKS</span></span>

[<span data-ttu-id="03bf8-153">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="03bf8-153">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="03bf8-154">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="03bf8-154">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="03bf8-155">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="03bf8-155">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


