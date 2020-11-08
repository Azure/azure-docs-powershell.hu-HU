---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
ms.openlocfilehash: 3d14ef7dca35796baa3e3aecf0c3df98674bfb9b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187097"
---
# <span data-ttu-id="08d29-101">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="08d29-101">New-AzApiManagementProduct</span></span>

## <span data-ttu-id="08d29-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08d29-102">SYNOPSIS</span></span>
<span data-ttu-id="08d29-103">API-kezelési terméket hoz létre.</span><span class="sxs-lookup"><span data-stu-id="08d29-103">Creates an API Management product.</span></span>

## <span data-ttu-id="08d29-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08d29-104">SYNTAX</span></span>

```
New-AzApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08d29-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="08d29-105">DESCRIPTION</span></span>
<span data-ttu-id="08d29-106">A **New-AzApiManagementProduct** PARANCSMAG egy API-kezelési terméket hoz létre.</span><span class="sxs-lookup"><span data-stu-id="08d29-106">The **New-AzApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="08d29-107">Példák</span><span class="sxs-lookup"><span data-stu-id="08d29-107">EXAMPLES</span></span>

### <span data-ttu-id="08d29-108">1. példa: előfizetést nem igénylő termékek létrehozása</span><span class="sxs-lookup"><span data-stu-id="08d29-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="08d29-109">Ez a parancs API-kezelési terméket hoz létre.</span><span class="sxs-lookup"><span data-stu-id="08d29-109">This command creates an API Management product.</span></span>
<span data-ttu-id="08d29-110">Nincs szükség előfizetésre.</span><span class="sxs-lookup"><span data-stu-id="08d29-110">No subscription is required.</span></span>

### <span data-ttu-id="08d29-111">2. példa: előfizetés és jóváhagyást igénylő termékek létrehozása</span><span class="sxs-lookup"><span data-stu-id="08d29-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="08d29-112">Ez a parancs létrehoz egy terméket.</span><span class="sxs-lookup"><span data-stu-id="08d29-112">This command creates a product.</span></span>
<span data-ttu-id="08d29-113">Előfizetés és jóváhagyás szükséges.</span><span class="sxs-lookup"><span data-stu-id="08d29-113">A subscription and approval are required.</span></span>
<span data-ttu-id="08d29-114">Ez a parancs 10 napra állítja be az értesítési időszakot.</span><span class="sxs-lookup"><span data-stu-id="08d29-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="08d29-115">Az előfizetési időtartam egy évre van állítva.</span><span class="sxs-lookup"><span data-stu-id="08d29-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="08d29-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08d29-116">PARAMETERS</span></span>

### <span data-ttu-id="08d29-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="08d29-117">-ApprovalRequired</span></span>
<span data-ttu-id="08d29-118">Azt jelzi, hogy a termékké való előfizetés jóváhagyást igényel-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="08d29-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="08d29-119">Alapértelmezés szerint ez a paraméter **$false**.</span><span class="sxs-lookup"><span data-stu-id="08d29-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="08d29-120">-Környezet</span><span class="sxs-lookup"><span data-stu-id="08d29-120">-Context</span></span>
<span data-ttu-id="08d29-121">Egy **PsApiManagementContext** -objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="08d29-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08d29-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08d29-122">-DefaultProfile</span></span>
<span data-ttu-id="08d29-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08d29-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08d29-124">-Leírás</span><span class="sxs-lookup"><span data-stu-id="08d29-124">-Description</span></span>
<span data-ttu-id="08d29-125">A termékleírást adja meg.</span><span class="sxs-lookup"><span data-stu-id="08d29-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="08d29-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="08d29-126">-LegalTerms</span></span>
<span data-ttu-id="08d29-127">A szorzat jogi használati feltételeit adja meg.</span><span class="sxs-lookup"><span data-stu-id="08d29-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="08d29-128">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="08d29-128">-ProductId</span></span>
<span data-ttu-id="08d29-129">Az új szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="08d29-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="08d29-130">Ha nem adja meg ezt a paramétert, egy új terméket hoz létre.</span><span class="sxs-lookup"><span data-stu-id="08d29-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="08d29-131">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="08d29-131">-State</span></span>
<span data-ttu-id="08d29-132">A termékek állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="08d29-132">Specifies the product state.</span></span>
<span data-ttu-id="08d29-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="08d29-133">psdx_paramvalues</span></span>
- <span data-ttu-id="08d29-134">NotPublished</span><span class="sxs-lookup"><span data-stu-id="08d29-134">NotPublished</span></span>
- <span data-ttu-id="08d29-135">Közzétette: az alapértelmezett érték a NotPublished.</span><span class="sxs-lookup"><span data-stu-id="08d29-135">Published The default value is NotPublished.</span></span>

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

### <span data-ttu-id="08d29-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="08d29-136">-SubscriptionRequired</span></span>
<span data-ttu-id="08d29-137">Azt jelzi, hogy a terméket előfizetést kell-e adni.</span><span class="sxs-lookup"><span data-stu-id="08d29-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="08d29-138">Az alapértelmezett érték **$true**.</span><span class="sxs-lookup"><span data-stu-id="08d29-138">The default value is **$True**.</span></span>

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

### <span data-ttu-id="08d29-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="08d29-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="08d29-140">Az egyidejű előfizetések maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="08d29-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="08d29-141">Az alapértelmezett érték a nincs.</span><span class="sxs-lookup"><span data-stu-id="08d29-141">The default value is None.</span></span>

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

### <span data-ttu-id="08d29-142">-Cím</span><span class="sxs-lookup"><span data-stu-id="08d29-142">-Title</span></span>
<span data-ttu-id="08d29-143">Megadja a terméknév címét.</span><span class="sxs-lookup"><span data-stu-id="08d29-143">Specifies the product title.</span></span>

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

### <span data-ttu-id="08d29-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08d29-144">CommonParameters</span></span>
<span data-ttu-id="08d29-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08d29-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08d29-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="08d29-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08d29-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08d29-147">INPUTS</span></span>

### <span data-ttu-id="08d29-148">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="08d29-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="08d29-149">System. String</span><span class="sxs-lookup"><span data-stu-id="08d29-149">System.String</span></span>

### <span data-ttu-id="08d29-150">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="08d29-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="08d29-151">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="08d29-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="08d29-152">System. nulla ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementProductState, Microsoft. Azure. PowerShell. parancsmagok. ApiManagement. ServiceManagement, Version = 1.0.0.0, = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="08d29-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="08d29-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08d29-153">OUTPUTS</span></span>

### <span data-ttu-id="08d29-154">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="08d29-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="08d29-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08d29-155">NOTES</span></span>

## <span data-ttu-id="08d29-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08d29-156">RELATED LINKS</span></span>

[<span data-ttu-id="08d29-157">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="08d29-157">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="08d29-158">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="08d29-158">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="08d29-159">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="08d29-159">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)

