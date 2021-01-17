---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 33b00df9e0c9c5b5e0ef04d22b745942535effcb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381987"
---
# <span data-ttu-id="668ee-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="668ee-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="668ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="668ee-102">SYNOPSIS</span></span>
<span data-ttu-id="668ee-103">Eltávolít egy meglévő API-kezelő terméket.</span><span class="sxs-lookup"><span data-stu-id="668ee-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="668ee-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="668ee-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="668ee-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="668ee-105">DESCRIPTION</span></span>
<span data-ttu-id="668ee-106">Az **Remove-AzApiManagementProduct** parancsmag eltávolít egy meglévő API-kezelő terméket.</span><span class="sxs-lookup"><span data-stu-id="668ee-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="668ee-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="668ee-107">EXAMPLES</span></span>

### <span data-ttu-id="668ee-108">1. példa: Meglévő termék és az összes előfizetés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="668ee-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="668ee-109">Ez a parancs eltávolít egy meglévő terméket és az összes előfizetést.</span><span class="sxs-lookup"><span data-stu-id="668ee-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="668ee-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="668ee-110">PARAMETERS</span></span>

### <span data-ttu-id="668ee-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="668ee-111">-Context</span></span>
<span data-ttu-id="668ee-112">A **PsApiManagementContext** objektum egy példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="668ee-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="668ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="668ee-113">-DefaultProfile</span></span>
<span data-ttu-id="668ee-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="668ee-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="668ee-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="668ee-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="668ee-116">Azt jelzi, hogy törölni szeretné-e a termékre vonatkozó előfizetéseket.</span><span class="sxs-lookup"><span data-stu-id="668ee-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="668ee-117">Ha nem adja meg ezt a paramétert, és az előfizetések létezik, kivételt kell beállítania.</span><span class="sxs-lookup"><span data-stu-id="668ee-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="668ee-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="668ee-118">-PassThru</span></span>
<span data-ttu-id="668ee-119">Azt jelzi, hogy ez a parancsmag $True, ha sikeres, vagy egy $False értéket, ha nem sikerül.</span><span class="sxs-lookup"><span data-stu-id="668ee-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="668ee-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="668ee-120">-ProductId</span></span>
<span data-ttu-id="668ee-121">A meglévő termék azonosítója.</span><span class="sxs-lookup"><span data-stu-id="668ee-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="668ee-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="668ee-122">-Confirm</span></span>
<span data-ttu-id="668ee-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="668ee-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="668ee-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="668ee-124">-WhatIf</span></span>
<span data-ttu-id="668ee-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="668ee-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="668ee-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="668ee-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="668ee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="668ee-127">CommonParameters</span></span>
<span data-ttu-id="668ee-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="668ee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="668ee-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="668ee-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="668ee-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="668ee-130">INPUTS</span></span>

### <span data-ttu-id="668ee-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="668ee-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="668ee-132">System.String</span><span class="sxs-lookup"><span data-stu-id="668ee-132">System.String</span></span>

### <span data-ttu-id="668ee-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="668ee-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="668ee-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="668ee-134">OUTPUTS</span></span>

### <span data-ttu-id="668ee-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="668ee-135">System.Boolean</span></span>

## <span data-ttu-id="668ee-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="668ee-136">NOTES</span></span>

## <span data-ttu-id="668ee-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="668ee-137">RELATED LINKS</span></span>

[<span data-ttu-id="668ee-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="668ee-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="668ee-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="668ee-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="668ee-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="668ee-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


