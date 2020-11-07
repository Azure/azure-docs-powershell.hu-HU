---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
ms.openlocfilehash: b050b55c978313cf038e8a27d5be0f7ad722905b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680443"
---
# <span data-ttu-id="a8eb4-101">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a8eb4-101">Set-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="a8eb4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="a8eb4-103">Az API-kezelési termékek adatainak megadása</span><span class="sxs-lookup"><span data-stu-id="a8eb4-103">Sets the API Management product details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8eb4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8eb4-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8eb4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8eb4-105">DESCRIPTION</span></span>
<span data-ttu-id="a8eb4-106">A **set-AzureRmApiManagementProduct** PARANCSMAG az API-kezelési termékek adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="a8eb4-106">The **Set-AzureRmApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="a8eb4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a8eb4-107">EXAMPLES</span></span>

### <span data-ttu-id="a8eb4-108">1. példa: a termékek részleteinek frissítése</span><span class="sxs-lookup"><span data-stu-id="a8eb4-108">Example 1: Update the product details</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="a8eb4-109">Ez a parancs frissíti az API-kezelési termékek adatait, előfizetést kér, majd közzéteszi a közzétételt.</span><span class="sxs-lookup"><span data-stu-id="a8eb4-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="a8eb4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8eb4-110">PARAMETERS</span></span>

### <span data-ttu-id="a8eb4-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="a8eb4-111">-ApprovalRequired</span></span>
<span data-ttu-id="a8eb4-112">Azt jelzi, hogy a termékké való előfizetés jóváhagyást igényel-e.</span><span class="sxs-lookup"><span data-stu-id="a8eb4-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="a8eb4-113">Az alapértelmezett érték **$false**.</span><span class="sxs-lookup"><span data-stu-id="a8eb4-113">The default value is **$False**.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8eb4-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a8eb4-114">-Context</span></span>
<span data-ttu-id="a8eb4-115">A **PsApiManagementContext** objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8eb4-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8eb4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8eb4-116">-DefaultProfile</span></span>
<span data-ttu-id="a8eb4-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8eb4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="a8eb4-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="a8eb4-118">-Description</span></span>
<span data-ttu-id="a8eb4-119">A termékleírást adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8eb4-119">Specifies the product description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8eb4-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="a8eb4-120">-LegalTerms</span></span>
<span data-ttu-id="a8eb4-121">A szorzat jogi használati feltételeit adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8eb4-121">Specifies the legal terms of use of the product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8eb4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8eb4-122">-PassThru</span></span>
<span data-ttu-id="a8eb4-123">passthru</span><span class="sxs-lookup"><span data-stu-id="a8eb4-123">passthru</span></span>

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

### <span data-ttu-id="a8eb4-124">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="a8eb4-124">-ProductId</span></span>
<span data-ttu-id="a8eb4-125">A meglévő szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8eb4-125">Specifies the identifier of the existing product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8eb4-126">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="a8eb4-126">-State</span></span>
<span data-ttu-id="a8eb4-127">A termékek állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8eb4-127">Specifies the product state.</span></span>
<span data-ttu-id="a8eb4-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="a8eb4-128">psdx_paramvalues</span></span>

- <span data-ttu-id="a8eb4-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="a8eb4-129">NotPublished</span></span>
- <span data-ttu-id="a8eb4-130">Közzétett</span><span class="sxs-lookup"><span data-stu-id="a8eb4-130">Published</span></span>

```yaml
Type: PsApiManagementProductState
Parameter Sets: (All)
Aliases: 
Accepted values: NotPublished, Published

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8eb4-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="a8eb4-131">-SubscriptionRequired</span></span>
<span data-ttu-id="a8eb4-132">Azt jelzi, hogy a terméket előfizetést kell-e adni.</span><span class="sxs-lookup"><span data-stu-id="a8eb4-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="a8eb4-133">A paraméter alapértelmezett értéke **$true**.</span><span class="sxs-lookup"><span data-stu-id="a8eb4-133">The default value for this parameter is **$True**.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8eb4-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="a8eb4-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="a8eb4-135">Az egyidejű előfizetések maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8eb4-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="a8eb4-136">A paraméter alapértelmezett értéke 1.</span><span class="sxs-lookup"><span data-stu-id="a8eb4-136">The default value for this parameter is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8eb4-137">-Cím</span><span class="sxs-lookup"><span data-stu-id="a8eb4-137">-Title</span></span>
<span data-ttu-id="a8eb4-138">A program a parancsmag által megadott terméket adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8eb4-138">Specifies the product title this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8eb4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8eb4-139">CommonParameters</span></span>
<span data-ttu-id="a8eb4-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8eb4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8eb4-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8eb4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8eb4-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8eb4-142">INPUTS</span></span>

### <span data-ttu-id="a8eb4-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="a8eb4-143">None</span></span>
<span data-ttu-id="a8eb4-144">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a8eb4-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a8eb4-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8eb4-145">OUTPUTS</span></span>

### <span data-ttu-id="a8eb4-146">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a8eb4-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="a8eb4-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8eb4-147">NOTES</span></span>

## <span data-ttu-id="a8eb4-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8eb4-148">RELATED LINKS</span></span>

[<span data-ttu-id="a8eb4-149">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a8eb4-149">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="a8eb4-150">Új – AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a8eb4-150">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="a8eb4-151">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a8eb4-151">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)


