---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 33b00df9e0c9c5b5e0ef04d22b745942535effcb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012141"
---
# <span data-ttu-id="0738e-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="0738e-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="0738e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0738e-102">SYNOPSIS</span></span>
<span data-ttu-id="0738e-103">Eltávolít egy meglévő API-kezelési terméket.</span><span class="sxs-lookup"><span data-stu-id="0738e-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="0738e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0738e-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0738e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0738e-105">DESCRIPTION</span></span>
<span data-ttu-id="0738e-106">A **Remove-AzApiManagementProduct** parancsmag eltávolítja a meglévő API-kezelési terméket.</span><span class="sxs-lookup"><span data-stu-id="0738e-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="0738e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0738e-107">EXAMPLES</span></span>

### <span data-ttu-id="0738e-108">1. példa: meglévő termékek és összes előfizetés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0738e-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="0738e-109">A parancs eltávolítja a meglévő terméket és az összes előfizetést.</span><span class="sxs-lookup"><span data-stu-id="0738e-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="0738e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0738e-110">PARAMETERS</span></span>

### <span data-ttu-id="0738e-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0738e-111">-Context</span></span>
<span data-ttu-id="0738e-112">A **PsApiManagementContext** objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0738e-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0738e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0738e-113">-DefaultProfile</span></span>
<span data-ttu-id="0738e-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0738e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0738e-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="0738e-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="0738e-116">Azt jelzi, hogy törli-e az előfizetéseket a terméket.</span><span class="sxs-lookup"><span data-stu-id="0738e-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="0738e-117">Ha nem állítja be ezt a paramétert és az előfizetéseket, a program kivételt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0738e-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="0738e-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0738e-118">-PassThru</span></span>
<span data-ttu-id="0738e-119">Azt jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha az nem sikerül, vagy ha az $False értéke nem sikerül.</span><span class="sxs-lookup"><span data-stu-id="0738e-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="0738e-120">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="0738e-120">-ProductId</span></span>
<span data-ttu-id="0738e-121">A meglévő szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0738e-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="0738e-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0738e-122">-Confirm</span></span>
<span data-ttu-id="0738e-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0738e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0738e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0738e-124">-WhatIf</span></span>
<span data-ttu-id="0738e-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0738e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0738e-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0738e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0738e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0738e-127">CommonParameters</span></span>
<span data-ttu-id="0738e-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0738e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0738e-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0738e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0738e-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0738e-130">INPUTS</span></span>

### <span data-ttu-id="0738e-131">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0738e-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0738e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0738e-132">System.String</span></span>

### <span data-ttu-id="0738e-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0738e-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0738e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0738e-134">OUTPUTS</span></span>

### <span data-ttu-id="0738e-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0738e-135">System.Boolean</span></span>

## <span data-ttu-id="0738e-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0738e-136">NOTES</span></span>

## <span data-ttu-id="0738e-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0738e-137">RELATED LINKS</span></span>

[<span data-ttu-id="0738e-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="0738e-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="0738e-139">Új – AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="0738e-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="0738e-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="0738e-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


