---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: e827fcf43c151f0812d96456de430f57686d4562
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922530"
---
# <span data-ttu-id="edb28-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="edb28-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="edb28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edb28-102">SYNOPSIS</span></span>
<span data-ttu-id="edb28-103">Beállítja az API Management termékadatokat.</span><span class="sxs-lookup"><span data-stu-id="edb28-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="edb28-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="edb28-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edb28-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="edb28-105">DESCRIPTION</span></span>
<span data-ttu-id="edb28-106">A **Set-AzApiManagementProduct** parancsmag beállítja az API Management termék részleteit.</span><span class="sxs-lookup"><span data-stu-id="edb28-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="edb28-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="edb28-107">EXAMPLES</span></span>

### <span data-ttu-id="edb28-108">1. példa: A termék részleteinek frissítése</span><span class="sxs-lookup"><span data-stu-id="edb28-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="edb28-109">Ez a parancs frissíti az API Management termék részleteit, előfizetést igényel, majd visszavonja a közzétételt.</span><span class="sxs-lookup"><span data-stu-id="edb28-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="edb28-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edb28-110">PARAMETERS</span></span>

### <span data-ttu-id="edb28-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="edb28-111">-ApprovalRequired</span></span>
<span data-ttu-id="edb28-112">Azt jelzi, hogy a termék előfizetése jóváhagyást igényel-e.</span><span class="sxs-lookup"><span data-stu-id="edb28-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="edb28-113">Az alapértelmezett érték a **$False.**</span><span class="sxs-lookup"><span data-stu-id="edb28-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="edb28-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="edb28-114">-Context</span></span>
<span data-ttu-id="edb28-115">A **PsApiManagementContext** objektum egy példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="edb28-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="edb28-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edb28-116">-DefaultProfile</span></span>
<span data-ttu-id="edb28-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="edb28-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edb28-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="edb28-118">-Description</span></span>
<span data-ttu-id="edb28-119">Megadja a termékleírást.</span><span class="sxs-lookup"><span data-stu-id="edb28-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="edb28-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="edb28-120">-LegalTerms</span></span>
<span data-ttu-id="edb28-121">A termék jogi feltételeit határozza meg.</span><span class="sxs-lookup"><span data-stu-id="edb28-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="edb28-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edb28-122">-PassThru</span></span>
<span data-ttu-id="edb28-123">passthru</span><span class="sxs-lookup"><span data-stu-id="edb28-123">passthru</span></span>

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

### <span data-ttu-id="edb28-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="edb28-124">-ProductId</span></span>
<span data-ttu-id="edb28-125">A meglévő termék azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="edb28-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="edb28-126">-State</span><span class="sxs-lookup"><span data-stu-id="edb28-126">-State</span></span>
<span data-ttu-id="edb28-127">A termék állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="edb28-127">Specifies the product state.</span></span>
<span data-ttu-id="edb28-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="edb28-128">psdx_paramvalues</span></span>
- <span data-ttu-id="edb28-129">Nincs közzétolva</span><span class="sxs-lookup"><span data-stu-id="edb28-129">NotPublished</span></span>
- <span data-ttu-id="edb28-130">Közzétéve</span><span class="sxs-lookup"><span data-stu-id="edb28-130">Published</span></span>

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

### <span data-ttu-id="edb28-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="edb28-131">-SubscriptionRequired</span></span>
<span data-ttu-id="edb28-132">Azt jelzi, hogy a terméknek előfizetésre van-e szüksége.</span><span class="sxs-lookup"><span data-stu-id="edb28-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="edb28-133">A paraméter alapértelmezett értéke **$True.**</span><span class="sxs-lookup"><span data-stu-id="edb28-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="edb28-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="edb28-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="edb28-135">Az egyidejű előfizetések maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="edb28-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="edb28-136">A paraméter alapértelmezett értéke Nincs.</span><span class="sxs-lookup"><span data-stu-id="edb28-136">The default value for this parameter is None.</span></span>

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

### <span data-ttu-id="edb28-137">-Title</span><span class="sxs-lookup"><span data-stu-id="edb28-137">-Title</span></span>
<span data-ttu-id="edb28-138">Ez a parancsmagkészlet termékcímét adja meg.</span><span class="sxs-lookup"><span data-stu-id="edb28-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="edb28-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="edb28-139">-Confirm</span></span>
<span data-ttu-id="edb28-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="edb28-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edb28-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edb28-141">-WhatIf</span></span>
<span data-ttu-id="edb28-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="edb28-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="edb28-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="edb28-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edb28-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edb28-144">CommonParameters</span></span>
<span data-ttu-id="edb28-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edb28-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edb28-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="edb28-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edb28-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="edb28-147">INPUTS</span></span>

### <span data-ttu-id="edb28-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="edb28-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="edb28-149">System.String</span><span class="sxs-lookup"><span data-stu-id="edb28-149">System.String</span></span>

### <span data-ttu-id="edb28-150">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="edb28-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="edb28-151">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="edb28-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="edb28-152">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="edb28-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="edb28-153">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="edb28-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="edb28-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="edb28-154">OUTPUTS</span></span>

### <span data-ttu-id="edb28-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="edb28-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="edb28-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="edb28-156">NOTES</span></span>

## <span data-ttu-id="edb28-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="edb28-157">RELATED LINKS</span></span>

[<span data-ttu-id="edb28-158">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="edb28-158">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="edb28-159">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="edb28-159">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="edb28-160">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="edb28-160">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


