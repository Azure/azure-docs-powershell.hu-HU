---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
ms.openlocfilehash: 3d14ef7dca35796baa3e3aecf0c3df98674bfb9b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162610"
---
# <span data-ttu-id="2b958-101">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2b958-101">New-AzApiManagementProduct</span></span>

## <span data-ttu-id="2b958-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b958-102">SYNOPSIS</span></span>
<span data-ttu-id="2b958-103">LÉTREHOZ egy API-kezelési terméket.</span><span class="sxs-lookup"><span data-stu-id="2b958-103">Creates an API Management product.</span></span>

## <span data-ttu-id="2b958-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2b958-104">SYNTAX</span></span>

```
New-AzApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b958-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2b958-105">DESCRIPTION</span></span>
<span data-ttu-id="2b958-106">A **New-AzApiManagementProduct** parancsmag létrehoz egy API Management terméket.</span><span class="sxs-lookup"><span data-stu-id="2b958-106">The **New-AzApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="2b958-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2b958-107">EXAMPLES</span></span>

### <span data-ttu-id="2b958-108">1. példa: Előfizetést nem igénylő termék létrehozása</span><span class="sxs-lookup"><span data-stu-id="2b958-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="2b958-109">Ez a parancs létrehoz egy API-kezelő terméket.</span><span class="sxs-lookup"><span data-stu-id="2b958-109">This command creates an API Management product.</span></span>
<span data-ttu-id="2b958-110">Nincs szükség előfizetésre.</span><span class="sxs-lookup"><span data-stu-id="2b958-110">No subscription is required.</span></span>

### <span data-ttu-id="2b958-111">2. példa: Előfizetést és jóváhagyást igénylő termék létrehozása</span><span class="sxs-lookup"><span data-stu-id="2b958-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="2b958-112">Ez a parancs létrehoz egy terméket.</span><span class="sxs-lookup"><span data-stu-id="2b958-112">This command creates a product.</span></span>
<span data-ttu-id="2b958-113">Előfizetésre és jóváhagyásra van szükség.</span><span class="sxs-lookup"><span data-stu-id="2b958-113">A subscription and approval are required.</span></span>
<span data-ttu-id="2b958-114">Ez a parancs 10 napra állítja az értesítési időszakot.</span><span class="sxs-lookup"><span data-stu-id="2b958-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="2b958-115">Az előfizetés időtartama egy évre van állítva.</span><span class="sxs-lookup"><span data-stu-id="2b958-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="2b958-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b958-116">PARAMETERS</span></span>

### <span data-ttu-id="2b958-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="2b958-117">-ApprovalRequired</span></span>
<span data-ttu-id="2b958-118">Azt jelzi, hogy a termék előfizetése jóváhagyást igényel-e.</span><span class="sxs-lookup"><span data-stu-id="2b958-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="2b958-119">Ez a paraméter alapértelmezés szerint **$False.**</span><span class="sxs-lookup"><span data-stu-id="2b958-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="2b958-120">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2b958-120">-Context</span></span>
<span data-ttu-id="2b958-121">Egy **PsApiManagementContext** objektum egy példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b958-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2b958-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b958-122">-DefaultProfile</span></span>
<span data-ttu-id="2b958-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b958-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b958-124">-Leírás</span><span class="sxs-lookup"><span data-stu-id="2b958-124">-Description</span></span>
<span data-ttu-id="2b958-125">Megadja a termékleírást.</span><span class="sxs-lookup"><span data-stu-id="2b958-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="2b958-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="2b958-126">-LegalTerms</span></span>
<span data-ttu-id="2b958-127">A termék jogi feltételeit határozza meg.</span><span class="sxs-lookup"><span data-stu-id="2b958-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="2b958-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="2b958-128">-ProductId</span></span>
<span data-ttu-id="2b958-129">Az új termék azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2b958-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="2b958-130">Ha nem adja meg ezt a paramétert, új termék jön létre.</span><span class="sxs-lookup"><span data-stu-id="2b958-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="2b958-131">-State</span><span class="sxs-lookup"><span data-stu-id="2b958-131">-State</span></span>
<span data-ttu-id="2b958-132">A termék állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="2b958-132">Specifies the product state.</span></span>
<span data-ttu-id="2b958-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="2b958-133">psdx_paramvalues</span></span>
- <span data-ttu-id="2b958-134">Nincs közzétolva</span><span class="sxs-lookup"><span data-stu-id="2b958-134">NotPublished</span></span>
- <span data-ttu-id="2b958-135">Közzétéve: Az alapértelmezett érték nincs közzétéve.</span><span class="sxs-lookup"><span data-stu-id="2b958-135">Published The default value is NotPublished.</span></span>

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

### <span data-ttu-id="2b958-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="2b958-136">-SubscriptionRequired</span></span>
<span data-ttu-id="2b958-137">Azt jelzi, hogy a terméknek előfizetésre van-e szüksége.</span><span class="sxs-lookup"><span data-stu-id="2b958-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="2b958-138">Az alapértelmezett érték a **$True.**</span><span class="sxs-lookup"><span data-stu-id="2b958-138">The default value is **$True**.</span></span>

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

### <span data-ttu-id="2b958-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="2b958-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="2b958-140">Az egyidejű előfizetések maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b958-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="2b958-141">Az alapértelmezett érték a Nincs.</span><span class="sxs-lookup"><span data-stu-id="2b958-141">The default value is None.</span></span>

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

### <span data-ttu-id="2b958-142">-Title</span><span class="sxs-lookup"><span data-stu-id="2b958-142">-Title</span></span>
<span data-ttu-id="2b958-143">A termék címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b958-143">Specifies the product title.</span></span>

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

### <span data-ttu-id="2b958-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b958-144">CommonParameters</span></span>
<span data-ttu-id="2b958-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b958-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b958-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b958-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b958-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b958-147">INPUTS</span></span>

### <span data-ttu-id="2b958-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2b958-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2b958-149">System.String</span><span class="sxs-lookup"><span data-stu-id="2b958-149">System.String</span></span>

### <span data-ttu-id="2b958-150">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2b958-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2b958-151">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2b958-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2b958-152">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="2b958-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2b958-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b958-153">OUTPUTS</span></span>

### <span data-ttu-id="2b958-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2b958-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="2b958-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2b958-155">NOTES</span></span>

## <span data-ttu-id="2b958-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b958-156">RELATED LINKS</span></span>

[<span data-ttu-id="2b958-157">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2b958-157">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="2b958-158">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2b958-158">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="2b958-159">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2b958-159">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


