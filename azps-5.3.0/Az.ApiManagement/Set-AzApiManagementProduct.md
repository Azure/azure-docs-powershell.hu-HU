---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: 9bee67dd299163b8e660b0e17c4e3bc11da5b40e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381638"
---
# <span data-ttu-id="25248-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="25248-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="25248-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25248-102">SYNOPSIS</span></span>
<span data-ttu-id="25248-103">Beállítja az API Management termékadatokat.</span><span class="sxs-lookup"><span data-stu-id="25248-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="25248-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="25248-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25248-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="25248-105">DESCRIPTION</span></span>
<span data-ttu-id="25248-106">A **Set-AzApiManagementProduct** parancsmag beállítja az API Management termék részleteit.</span><span class="sxs-lookup"><span data-stu-id="25248-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="25248-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="25248-107">EXAMPLES</span></span>

### <span data-ttu-id="25248-108">1. példa: A termék részleteinek frissítése</span><span class="sxs-lookup"><span data-stu-id="25248-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="25248-109">Ez a parancs frissíti az API Management termék részleteit, előfizetést igényel, majd visszavonja a közzétételt.</span><span class="sxs-lookup"><span data-stu-id="25248-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="25248-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25248-110">PARAMETERS</span></span>

### <span data-ttu-id="25248-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="25248-111">-ApprovalRequired</span></span>
<span data-ttu-id="25248-112">Azt jelzi, hogy a termék előfizetése jóváhagyást igényel-e.</span><span class="sxs-lookup"><span data-stu-id="25248-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="25248-113">Az alapértelmezett érték a **$False.**</span><span class="sxs-lookup"><span data-stu-id="25248-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="25248-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="25248-114">-Context</span></span>
<span data-ttu-id="25248-115">A **PsApiManagementContext** objektum egy példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="25248-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="25248-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25248-116">-DefaultProfile</span></span>
<span data-ttu-id="25248-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25248-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25248-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="25248-118">-Description</span></span>
<span data-ttu-id="25248-119">Megadja a termékleírást.</span><span class="sxs-lookup"><span data-stu-id="25248-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="25248-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="25248-120">-LegalTerms</span></span>
<span data-ttu-id="25248-121">A termék jogi feltételeit határozza meg.</span><span class="sxs-lookup"><span data-stu-id="25248-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="25248-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25248-122">-PassThru</span></span>
<span data-ttu-id="25248-123">passthru</span><span class="sxs-lookup"><span data-stu-id="25248-123">passthru</span></span>

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

### <span data-ttu-id="25248-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="25248-124">-ProductId</span></span>
<span data-ttu-id="25248-125">A meglévő termék azonosítója.</span><span class="sxs-lookup"><span data-stu-id="25248-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="25248-126">-State</span><span class="sxs-lookup"><span data-stu-id="25248-126">-State</span></span>
<span data-ttu-id="25248-127">A termék állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="25248-127">Specifies the product state.</span></span>
<span data-ttu-id="25248-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="25248-128">psdx_paramvalues</span></span>
- <span data-ttu-id="25248-129">Nincs közzétolva</span><span class="sxs-lookup"><span data-stu-id="25248-129">NotPublished</span></span>
- <span data-ttu-id="25248-130">Közzétéve</span><span class="sxs-lookup"><span data-stu-id="25248-130">Published</span></span>

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

### <span data-ttu-id="25248-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="25248-131">-SubscriptionRequired</span></span>
<span data-ttu-id="25248-132">Azt jelzi, hogy a terméknek előfizetésre van-e szüksége.</span><span class="sxs-lookup"><span data-stu-id="25248-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="25248-133">A paraméter alapértelmezett értéke **$True.**</span><span class="sxs-lookup"><span data-stu-id="25248-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="25248-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="25248-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="25248-135">Az egyidejű előfizetések maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="25248-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="25248-136">A paraméter alapértelmezett értéke Nincs.</span><span class="sxs-lookup"><span data-stu-id="25248-136">The default value for this parameter is None.</span></span>

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

### <span data-ttu-id="25248-137">-Title</span><span class="sxs-lookup"><span data-stu-id="25248-137">-Title</span></span>
<span data-ttu-id="25248-138">Ez a parancsmagkészlet termékcímét adja meg.</span><span class="sxs-lookup"><span data-stu-id="25248-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="25248-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25248-139">-Confirm</span></span>
<span data-ttu-id="25248-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="25248-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25248-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25248-141">-WhatIf</span></span>
<span data-ttu-id="25248-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="25248-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25248-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="25248-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25248-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25248-144">CommonParameters</span></span>
<span data-ttu-id="25248-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25248-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25248-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25248-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25248-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25248-147">INPUTS</span></span>

### <span data-ttu-id="25248-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="25248-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="25248-149">System.String</span><span class="sxs-lookup"><span data-stu-id="25248-149">System.String</span></span>

### <span data-ttu-id="25248-150">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="25248-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="25248-151">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="25248-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="25248-152">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="25248-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="25248-153">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="25248-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="25248-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25248-154">OUTPUTS</span></span>

### <span data-ttu-id="25248-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="25248-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="25248-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="25248-156">NOTES</span></span>

## <span data-ttu-id="25248-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25248-157">RELATED LINKS</span></span>

[<span data-ttu-id="25248-158">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="25248-158">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="25248-159">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="25248-159">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="25248-160">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="25248-160">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


