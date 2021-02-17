---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: 9bee67dd299163b8e660b0e17c4e3bc11da5b40e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210294"
---
# <span data-ttu-id="0ea37-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="0ea37-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="0ea37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ea37-102">SYNOPSIS</span></span>
<span data-ttu-id="0ea37-103">Beállítja az API Management termékadatokat.</span><span class="sxs-lookup"><span data-stu-id="0ea37-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="0ea37-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0ea37-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ea37-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0ea37-105">DESCRIPTION</span></span>
<span data-ttu-id="0ea37-106">A **Set-AzApiManagementProduct** parancsmag beállítja az API Management termék részleteit.</span><span class="sxs-lookup"><span data-stu-id="0ea37-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="0ea37-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0ea37-107">EXAMPLES</span></span>

### <span data-ttu-id="0ea37-108">1. példa: A termék részleteinek frissítése</span><span class="sxs-lookup"><span data-stu-id="0ea37-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="0ea37-109">Ez a parancs frissíti az API Management termék részleteit, előfizetést igényel, majd visszavonja a közzétételt.</span><span class="sxs-lookup"><span data-stu-id="0ea37-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="0ea37-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ea37-110">PARAMETERS</span></span>

### <span data-ttu-id="0ea37-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="0ea37-111">-ApprovalRequired</span></span>
<span data-ttu-id="0ea37-112">Azt jelzi, hogy a termék előfizetése jóváhagyást igényel-e.</span><span class="sxs-lookup"><span data-stu-id="0ea37-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="0ea37-113">Az alapértelmezett érték a **$False.**</span><span class="sxs-lookup"><span data-stu-id="0ea37-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="0ea37-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0ea37-114">-Context</span></span>
<span data-ttu-id="0ea37-115">A **PsApiManagementContext** objektum egy példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ea37-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0ea37-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ea37-116">-DefaultProfile</span></span>
<span data-ttu-id="0ea37-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ea37-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ea37-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="0ea37-118">-Description</span></span>
<span data-ttu-id="0ea37-119">Megadja a termékleírást.</span><span class="sxs-lookup"><span data-stu-id="0ea37-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="0ea37-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="0ea37-120">-LegalTerms</span></span>
<span data-ttu-id="0ea37-121">A termék jogi feltételeit határozza meg.</span><span class="sxs-lookup"><span data-stu-id="0ea37-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="0ea37-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ea37-122">-PassThru</span></span>
<span data-ttu-id="0ea37-123">passthru</span><span class="sxs-lookup"><span data-stu-id="0ea37-123">passthru</span></span>

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

### <span data-ttu-id="0ea37-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="0ea37-124">-ProductId</span></span>
<span data-ttu-id="0ea37-125">A meglévő termék azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0ea37-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="0ea37-126">-State</span><span class="sxs-lookup"><span data-stu-id="0ea37-126">-State</span></span>
<span data-ttu-id="0ea37-127">A termék állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="0ea37-127">Specifies the product state.</span></span>
<span data-ttu-id="0ea37-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="0ea37-128">psdx_paramvalues</span></span>
- <span data-ttu-id="0ea37-129">Nincs közzétolva</span><span class="sxs-lookup"><span data-stu-id="0ea37-129">NotPublished</span></span>
- <span data-ttu-id="0ea37-130">Közzétéve</span><span class="sxs-lookup"><span data-stu-id="0ea37-130">Published</span></span>

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

### <span data-ttu-id="0ea37-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="0ea37-131">-SubscriptionRequired</span></span>
<span data-ttu-id="0ea37-132">Azt jelzi, hogy a terméknek előfizetésre van-e szüksége.</span><span class="sxs-lookup"><span data-stu-id="0ea37-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="0ea37-133">A paraméter alapértelmezett értéke **$True.**</span><span class="sxs-lookup"><span data-stu-id="0ea37-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="0ea37-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="0ea37-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="0ea37-135">Az egyidejű előfizetések maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ea37-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="0ea37-136">A paraméter alapértelmezett értéke Nincs.</span><span class="sxs-lookup"><span data-stu-id="0ea37-136">The default value for this parameter is None.</span></span>

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

### <span data-ttu-id="0ea37-137">-Title</span><span class="sxs-lookup"><span data-stu-id="0ea37-137">-Title</span></span>
<span data-ttu-id="0ea37-138">Ez a parancsmag-készlet termékcímét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ea37-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="0ea37-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ea37-139">-Confirm</span></span>
<span data-ttu-id="0ea37-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0ea37-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ea37-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ea37-141">-WhatIf</span></span>
<span data-ttu-id="0ea37-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0ea37-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ea37-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0ea37-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ea37-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ea37-144">CommonParameters</span></span>
<span data-ttu-id="0ea37-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ea37-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ea37-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ea37-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ea37-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ea37-147">INPUTS</span></span>

### <span data-ttu-id="0ea37-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0ea37-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0ea37-149">System.String</span><span class="sxs-lookup"><span data-stu-id="0ea37-149">System.String</span></span>

### <span data-ttu-id="0ea37-150">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0ea37-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0ea37-151">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0ea37-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0ea37-152">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="0ea37-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0ea37-153">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0ea37-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0ea37-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ea37-154">OUTPUTS</span></span>

### <span data-ttu-id="0ea37-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="0ea37-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="0ea37-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0ea37-156">NOTES</span></span>

## <span data-ttu-id="0ea37-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ea37-157">RELATED LINKS</span></span>

[<span data-ttu-id="0ea37-158">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="0ea37-158">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="0ea37-159">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="0ea37-159">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="0ea37-160">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="0ea37-160">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


