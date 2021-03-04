---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 9ad08f867bf78dc4a6bc2df5c4dd3086c3cea33c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932129"
---
# <span data-ttu-id="2e3d0-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2e3d0-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="2e3d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e3d0-102">SYNOPSIS</span></span>
<span data-ttu-id="2e3d0-103">Eltávolít egy meglévő API-kezelő terméket.</span><span class="sxs-lookup"><span data-stu-id="2e3d0-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="2e3d0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2e3d0-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e3d0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2e3d0-105">DESCRIPTION</span></span>
<span data-ttu-id="2e3d0-106">Az **Remove-AzApiManagementProduct** parancsmag eltávolít egy meglévő API-kezelő terméket.</span><span class="sxs-lookup"><span data-stu-id="2e3d0-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="2e3d0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2e3d0-107">EXAMPLES</span></span>

### <span data-ttu-id="2e3d0-108">1. példa: Meglévő termék és az összes előfizetés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2e3d0-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="2e3d0-109">Ez a parancs eltávolít egy meglévő terméket és az összes előfizetést.</span><span class="sxs-lookup"><span data-stu-id="2e3d0-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="2e3d0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e3d0-110">PARAMETERS</span></span>

### <span data-ttu-id="2e3d0-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2e3d0-111">-Context</span></span>
<span data-ttu-id="2e3d0-112">A **PsApiManagementContext** objektum egy példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e3d0-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2e3d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e3d0-113">-DefaultProfile</span></span>
<span data-ttu-id="2e3d0-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e3d0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e3d0-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="2e3d0-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="2e3d0-116">Azt jelzi, hogy törölni szeretné-e a termékre vonatkozó előfizetéseket.</span><span class="sxs-lookup"><span data-stu-id="2e3d0-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="2e3d0-117">Ha nem adja meg ezt a paramétert, és az előfizetések létezik, kivételt kell beállítania.</span><span class="sxs-lookup"><span data-stu-id="2e3d0-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="2e3d0-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e3d0-118">-PassThru</span></span>
<span data-ttu-id="2e3d0-119">Azt jelzi, hogy ez a parancsmag $True, ha sikeres, vagy egy $False értéket, ha nem sikerül.</span><span class="sxs-lookup"><span data-stu-id="2e3d0-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="2e3d0-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="2e3d0-120">-ProductId</span></span>
<span data-ttu-id="2e3d0-121">A meglévő termék azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e3d0-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="2e3d0-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e3d0-122">-Confirm</span></span>
<span data-ttu-id="2e3d0-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2e3d0-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3d0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e3d0-124">-WhatIf</span></span>
<span data-ttu-id="2e3d0-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2e3d0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e3d0-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e3d0-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3d0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e3d0-127">CommonParameters</span></span>
<span data-ttu-id="2e3d0-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e3d0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e3d0-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e3d0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e3d0-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e3d0-130">INPUTS</span></span>

### <span data-ttu-id="2e3d0-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2e3d0-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2e3d0-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2e3d0-132">System.String</span></span>

### <span data-ttu-id="2e3d0-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2e3d0-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2e3d0-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e3d0-134">OUTPUTS</span></span>

### <span data-ttu-id="2e3d0-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2e3d0-135">System.Boolean</span></span>

## <span data-ttu-id="2e3d0-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2e3d0-136">NOTES</span></span>

## <span data-ttu-id="2e3d0-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e3d0-137">RELATED LINKS</span></span>

[<span data-ttu-id="2e3d0-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2e3d0-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="2e3d0-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2e3d0-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="2e3d0-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2e3d0-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


