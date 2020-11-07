---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: f60bf40cd6226979955f71e413be3914fc05c417
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836901"
---
# <span data-ttu-id="4ceae-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4ceae-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="4ceae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ceae-102">SYNOPSIS</span></span>
<span data-ttu-id="4ceae-103">Az API-kezelési termékek adatainak megadása</span><span class="sxs-lookup"><span data-stu-id="4ceae-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="4ceae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ceae-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ceae-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ceae-105">DESCRIPTION</span></span>
<span data-ttu-id="4ceae-106">A **set-AzApiManagementProduct** PARANCSMAG az API-kezelési termékek adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="4ceae-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="4ceae-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4ceae-107">EXAMPLES</span></span>

### <span data-ttu-id="4ceae-108">1. példa: a termékek részleteinek frissítése</span><span class="sxs-lookup"><span data-stu-id="4ceae-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="4ceae-109">Ez a parancs frissíti az API-kezelési termékek adatait, előfizetést kér, majd közzéteszi a közzétételt.</span><span class="sxs-lookup"><span data-stu-id="4ceae-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="4ceae-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ceae-110">PARAMETERS</span></span>

### <span data-ttu-id="4ceae-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="4ceae-111">-ApprovalRequired</span></span>
<span data-ttu-id="4ceae-112">Azt jelzi, hogy a termékké való előfizetés jóváhagyást igényel-e.</span><span class="sxs-lookup"><span data-stu-id="4ceae-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="4ceae-113">Az alapértelmezett érték **$false**.</span><span class="sxs-lookup"><span data-stu-id="4ceae-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="4ceae-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="4ceae-114">-Context</span></span>
<span data-ttu-id="4ceae-115">A **PsApiManagementContext** objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ceae-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4ceae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ceae-116">-DefaultProfile</span></span>
<span data-ttu-id="4ceae-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ceae-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ceae-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="4ceae-118">-Description</span></span>
<span data-ttu-id="4ceae-119">A termékleírást adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ceae-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="4ceae-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="4ceae-120">-LegalTerms</span></span>
<span data-ttu-id="4ceae-121">A szorzat jogi használati feltételeit adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ceae-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="4ceae-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ceae-122">-PassThru</span></span>
<span data-ttu-id="4ceae-123">passthru</span><span class="sxs-lookup"><span data-stu-id="4ceae-123">passthru</span></span>

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

### <span data-ttu-id="4ceae-124">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="4ceae-124">-ProductId</span></span>
<span data-ttu-id="4ceae-125">A meglévő szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ceae-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="4ceae-126">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="4ceae-126">-State</span></span>
<span data-ttu-id="4ceae-127">A termékek állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ceae-127">Specifies the product state.</span></span>
<span data-ttu-id="4ceae-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="4ceae-128">psdx_paramvalues</span></span>
- <span data-ttu-id="4ceae-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="4ceae-129">NotPublished</span></span>
- <span data-ttu-id="4ceae-130">Közzétett</span><span class="sxs-lookup"><span data-stu-id="4ceae-130">Published</span></span>

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

### <span data-ttu-id="4ceae-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="4ceae-131">-SubscriptionRequired</span></span>
<span data-ttu-id="4ceae-132">Azt jelzi, hogy a terméket előfizetést kell-e adni.</span><span class="sxs-lookup"><span data-stu-id="4ceae-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="4ceae-133">A paraméter alapértelmezett értéke **$true**.</span><span class="sxs-lookup"><span data-stu-id="4ceae-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="4ceae-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="4ceae-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="4ceae-135">Az egyidejű előfizetések maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ceae-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="4ceae-136">A paraméter alapértelmezett értéke 1.</span><span class="sxs-lookup"><span data-stu-id="4ceae-136">The default value for this parameter is 1.</span></span>

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

### <span data-ttu-id="4ceae-137">-Cím</span><span class="sxs-lookup"><span data-stu-id="4ceae-137">-Title</span></span>
<span data-ttu-id="4ceae-138">A program a parancsmag által megadott terméket adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ceae-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="4ceae-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ceae-139">CommonParameters</span></span>
<span data-ttu-id="4ceae-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ceae-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ceae-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ceae-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ceae-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ceae-142">INPUTS</span></span>

### <span data-ttu-id="4ceae-143">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4ceae-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4ceae-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4ceae-144">System.String</span></span>

### <span data-ttu-id="4ceae-145">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4ceae-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4ceae-146">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4ceae-146">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4ceae-147">System. nulla ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementProductState, Microsoft. Azure. PowerShell. parancsmagok. ApiManagement. ServiceManagement, Version = 1.0.0.0, = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4ceae-147">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4ceae-148">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4ceae-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4ceae-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ceae-149">OUTPUTS</span></span>

### <span data-ttu-id="4ceae-150">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4ceae-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="4ceae-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ceae-151">NOTES</span></span>

## <span data-ttu-id="4ceae-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ceae-152">RELATED LINKS</span></span>

[<span data-ttu-id="4ceae-153">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4ceae-153">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="4ceae-154">Új – AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4ceae-154">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="4ceae-155">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4ceae-155">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


