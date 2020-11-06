---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
ms.openlocfilehash: dac6e48faba1590897161ab59fed05f1f0b331df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498016"
---
# <span data-ttu-id="fe934-101">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="fe934-101">Set-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="fe934-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe934-102">SYNOPSIS</span></span>
<span data-ttu-id="fe934-103">Az API-kezelési termékek adatainak megadása</span><span class="sxs-lookup"><span data-stu-id="fe934-103">Sets the API Management product details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe934-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe934-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe934-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe934-105">DESCRIPTION</span></span>
<span data-ttu-id="fe934-106">A **set-AzureRmApiManagementProduct** PARANCSMAG az API-kezelési termékek adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="fe934-106">The **Set-AzureRmApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="fe934-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fe934-107">EXAMPLES</span></span>

### <span data-ttu-id="fe934-108">1. példa: a termékek részleteinek frissítése</span><span class="sxs-lookup"><span data-stu-id="fe934-108">Example 1: Update the product details</span></span>
```
PS C:\>Set-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="fe934-109">Ez a parancs frissíti az API-kezelési termékek adatait, előfizetést kér, majd közzéteszi a közzétételt.</span><span class="sxs-lookup"><span data-stu-id="fe934-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="fe934-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe934-110">PARAMETERS</span></span>

### <span data-ttu-id="fe934-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="fe934-111">-ApprovalRequired</span></span>
<span data-ttu-id="fe934-112">Azt jelzi, hogy a termékké való előfizetés jóváhagyást igényel-e.</span><span class="sxs-lookup"><span data-stu-id="fe934-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="fe934-113">Az alapértelmezett érték **$false**.</span><span class="sxs-lookup"><span data-stu-id="fe934-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="fe934-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="fe934-114">-Context</span></span>
<span data-ttu-id="fe934-115">A **PsApiManagementContext** objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe934-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fe934-116">-Leírás</span><span class="sxs-lookup"><span data-stu-id="fe934-116">-Description</span></span>
<span data-ttu-id="fe934-117">A termékleírást adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe934-117">Specifies the product description.</span></span>

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

### <span data-ttu-id="fe934-118">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="fe934-118">-LegalTerms</span></span>
<span data-ttu-id="fe934-119">A szorzat jogi használati feltételeit adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe934-119">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="fe934-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe934-120">-PassThru</span></span>
<span data-ttu-id="fe934-121">passthru</span><span class="sxs-lookup"><span data-stu-id="fe934-121">passthru</span></span>

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

### <span data-ttu-id="fe934-122">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="fe934-122">-ProductId</span></span>
<span data-ttu-id="fe934-123">A meglévő szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe934-123">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="fe934-124">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="fe934-124">-State</span></span>
<span data-ttu-id="fe934-125">A termékek állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe934-125">Specifies the product state.</span></span>
<span data-ttu-id="fe934-126">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="fe934-126">psdx_paramvalues</span></span>

- <span data-ttu-id="fe934-127">NotPublished</span><span class="sxs-lookup"><span data-stu-id="fe934-127">NotPublished</span></span>
- <span data-ttu-id="fe934-128">Közzétett</span><span class="sxs-lookup"><span data-stu-id="fe934-128">Published</span></span>

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

### <span data-ttu-id="fe934-129">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="fe934-129">-SubscriptionRequired</span></span>
<span data-ttu-id="fe934-130">Azt jelzi, hogy a terméket előfizetést kell-e adni.</span><span class="sxs-lookup"><span data-stu-id="fe934-130">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="fe934-131">A paraméter alapértelmezett értéke **$true**.</span><span class="sxs-lookup"><span data-stu-id="fe934-131">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="fe934-132">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="fe934-132">-SubscriptionsLimit</span></span>
<span data-ttu-id="fe934-133">Az egyidejű előfizetések maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe934-133">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="fe934-134">A paraméter alapértelmezett értéke 1.</span><span class="sxs-lookup"><span data-stu-id="fe934-134">The default value for this parameter is 1.</span></span>

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

### <span data-ttu-id="fe934-135">-Cím</span><span class="sxs-lookup"><span data-stu-id="fe934-135">-Title</span></span>
<span data-ttu-id="fe934-136">A program a parancsmag által megadott terméket adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe934-136">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="fe934-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe934-137">-DefaultProfile</span></span>
<span data-ttu-id="fe934-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe934-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe934-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe934-139">CommonParameters</span></span>
<span data-ttu-id="fe934-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe934-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe934-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe934-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe934-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe934-142">INPUTS</span></span>

## <span data-ttu-id="fe934-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe934-143">OUTPUTS</span></span>

### <span data-ttu-id="fe934-144">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="fe934-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="fe934-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe934-145">NOTES</span></span>

## <span data-ttu-id="fe934-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe934-146">RELATED LINKS</span></span>

[<span data-ttu-id="fe934-147">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="fe934-147">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="fe934-148">Új – AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="fe934-148">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="fe934-149">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="fe934-149">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)


