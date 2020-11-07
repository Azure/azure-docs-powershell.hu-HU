---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
ms.openlocfilehash: f28bfc223ed187724aa8702c378bfce5d88755fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672126"
---
# <span data-ttu-id="cde18-101">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="cde18-101">Set-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="cde18-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cde18-102">SYNOPSIS</span></span>
<span data-ttu-id="cde18-103">Az API-kezelési termékek adatainak megadása</span><span class="sxs-lookup"><span data-stu-id="cde18-103">Sets the API Management product details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cde18-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cde18-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cde18-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cde18-105">DESCRIPTION</span></span>
<span data-ttu-id="cde18-106">A **set-AzureRmApiManagementProduct** PARANCSMAG az API-kezelési termékek adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="cde18-106">The **Set-AzureRmApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="cde18-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cde18-107">EXAMPLES</span></span>

### <span data-ttu-id="cde18-108">1. példa: a termékek részleteinek frissítése</span><span class="sxs-lookup"><span data-stu-id="cde18-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="cde18-109">Ez a parancs frissíti az API-kezelési termékek adatait, előfizetést kér, majd közzéteszi a közzétételt.</span><span class="sxs-lookup"><span data-stu-id="cde18-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="cde18-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cde18-110">PARAMETERS</span></span>

### <span data-ttu-id="cde18-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="cde18-111">-ApprovalRequired</span></span>
<span data-ttu-id="cde18-112">Azt jelzi, hogy a termékké való előfizetés jóváhagyást igényel-e.</span><span class="sxs-lookup"><span data-stu-id="cde18-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="cde18-113">Az alapértelmezett érték **$false**.</span><span class="sxs-lookup"><span data-stu-id="cde18-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="cde18-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="cde18-114">-Context</span></span>
<span data-ttu-id="cde18-115">A **PsApiManagementContext** objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cde18-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="cde18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cde18-116">-DefaultProfile</span></span>
<span data-ttu-id="cde18-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cde18-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cde18-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="cde18-118">-Description</span></span>
<span data-ttu-id="cde18-119">A termékleírást adja meg.</span><span class="sxs-lookup"><span data-stu-id="cde18-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="cde18-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="cde18-120">-LegalTerms</span></span>
<span data-ttu-id="cde18-121">A szorzat jogi használati feltételeit adja meg.</span><span class="sxs-lookup"><span data-stu-id="cde18-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="cde18-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cde18-122">-PassThru</span></span>
<span data-ttu-id="cde18-123">passthru</span><span class="sxs-lookup"><span data-stu-id="cde18-123">passthru</span></span>

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

### <span data-ttu-id="cde18-124">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="cde18-124">-ProductId</span></span>
<span data-ttu-id="cde18-125">A meglévő szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cde18-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="cde18-126">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="cde18-126">-State</span></span>
<span data-ttu-id="cde18-127">A termékek állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cde18-127">Specifies the product state.</span></span>
<span data-ttu-id="cde18-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="cde18-128">psdx_paramvalues</span></span>
- <span data-ttu-id="cde18-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="cde18-129">NotPublished</span></span>
- <span data-ttu-id="cde18-130">Közzétett</span><span class="sxs-lookup"><span data-stu-id="cde18-130">Published</span></span>

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

### <span data-ttu-id="cde18-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="cde18-131">-SubscriptionRequired</span></span>
<span data-ttu-id="cde18-132">Azt jelzi, hogy a terméket előfizetést kell-e adni.</span><span class="sxs-lookup"><span data-stu-id="cde18-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="cde18-133">A paraméter alapértelmezett értéke **$true**.</span><span class="sxs-lookup"><span data-stu-id="cde18-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="cde18-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="cde18-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="cde18-135">Az egyidejű előfizetések maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cde18-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="cde18-136">A paraméter alapértelmezett értéke 1.</span><span class="sxs-lookup"><span data-stu-id="cde18-136">The default value for this parameter is 1.</span></span>

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

### <span data-ttu-id="cde18-137">-Cím</span><span class="sxs-lookup"><span data-stu-id="cde18-137">-Title</span></span>
<span data-ttu-id="cde18-138">A program a parancsmag által megadott terméket adja meg.</span><span class="sxs-lookup"><span data-stu-id="cde18-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="cde18-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cde18-139">CommonParameters</span></span>
<span data-ttu-id="cde18-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cde18-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cde18-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cde18-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cde18-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cde18-142">INPUTS</span></span>

### <span data-ttu-id="cde18-143">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cde18-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cde18-144">System. String</span><span class="sxs-lookup"><span data-stu-id="cde18-144">System.String</span></span>

### <span data-ttu-id="cde18-145">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="cde18-145">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="cde18-146">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="cde18-146">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="cde18-147">System. null ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementProductState, Microsoft. Azure. commands. ApiManagement. ServiceManagement, Version = 6.1.0.0</span><span class="sxs-lookup"><span data-stu-id="cde18-147">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="cde18-148">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cde18-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cde18-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cde18-149">OUTPUTS</span></span>

### <span data-ttu-id="cde18-150">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="cde18-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="cde18-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cde18-151">NOTES</span></span>

## <span data-ttu-id="cde18-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cde18-152">RELATED LINKS</span></span>

[<span data-ttu-id="cde18-153">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="cde18-153">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="cde18-154">Új – AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="cde18-154">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="cde18-155">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="cde18-155">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)


