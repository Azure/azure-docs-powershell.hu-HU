---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
ms.openlocfilehash: 506287812f684a778fdb96e750aac34049912b58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210343"
---
# <span data-ttu-id="0e1c9-101">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="0e1c9-101">Remove-AzApiManagementApiFromGateway</span></span>

## <span data-ttu-id="0e1c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e1c9-102">SYNOPSIS</span></span>
<span data-ttu-id="0e1c9-103">API-t csatol egy átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="0e1c9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0e1c9-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e1c9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0e1c9-105">DESCRIPTION</span></span>
<span data-ttu-id="0e1c9-106">A **Remove-AzApiManagementApiFromGateway** parancsmag egy API-t csatol egy átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-106">The **Remove-AzApiManagementApiFromGateway** cmdlet attaches an API to a gateway.</span></span>

## <span data-ttu-id="0e1c9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0e1c9-107">EXAMPLES</span></span>

### <span data-ttu-id="0e1c9-108">1. példa: API eltávolítása átjáróból</span><span class="sxs-lookup"><span data-stu-id="0e1c9-108">Example 1: Remove an API from a gateway</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="0e1c9-109">Ez a parancs eltávolítja a megadott API-t egy átjáróból.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-109">This command removes the specified API from a gateway.</span></span>

## <span data-ttu-id="0e1c9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e1c9-110">PARAMETERS</span></span>

### <span data-ttu-id="0e1c9-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0e1c9-111">-ApiId</span></span>
<span data-ttu-id="0e1c9-112">Az átjáróból eltávolítható meglévő API-k azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-112">Identifier of existing APIs to remove from the Gateway.</span></span>
<span data-ttu-id="0e1c9-113">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-113">This parameter is required.</span></span>

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

### <span data-ttu-id="0e1c9-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0e1c9-114">-Context</span></span>
<span data-ttu-id="0e1c9-115">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0e1c9-116">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-116">This parameter is required.</span></span>

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

### <span data-ttu-id="0e1c9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e1c9-117">-DefaultProfile</span></span>
<span data-ttu-id="0e1c9-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e1c9-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="0e1c9-119">-GatewayId</span></span>
<span data-ttu-id="0e1c9-120">Annak a meglévő átjárónak az azonosítója, amelyből el szeretné távolítani az API-t.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-120">Identifier of existing Gateway to remove API from.</span></span>
<span data-ttu-id="0e1c9-121">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-121">This parameter is required.</span></span>

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

### <span data-ttu-id="0e1c9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e1c9-122">-PassThru</span></span>
<span data-ttu-id="0e1c9-123">Ha a megadott érték igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="0e1c9-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-124">This parameter is optional.</span></span>
<span data-ttu-id="0e1c9-125">Az alapértelmezett érték hamis.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-125">Default value is false.</span></span>

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

### <span data-ttu-id="0e1c9-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e1c9-126">-Confirm</span></span>
<span data-ttu-id="0e1c9-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e1c9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e1c9-128">-WhatIf</span></span>
<span data-ttu-id="0e1c9-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e1c9-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e1c9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e1c9-131">CommonParameters</span></span>
<span data-ttu-id="0e1c9-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e1c9-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e1c9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e1c9-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0e1c9-134">INPUTS</span></span>

### <span data-ttu-id="0e1c9-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0e1c9-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0e1c9-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0e1c9-136">System.String</span></span>

### <span data-ttu-id="0e1c9-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0e1c9-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0e1c9-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e1c9-138">OUTPUTS</span></span>

### <span data-ttu-id="0e1c9-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0e1c9-139">System.Boolean</span></span>

## <span data-ttu-id="0e1c9-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0e1c9-140">NOTES</span></span>

## <span data-ttu-id="0e1c9-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e1c9-141">RELATED LINKS</span></span>
