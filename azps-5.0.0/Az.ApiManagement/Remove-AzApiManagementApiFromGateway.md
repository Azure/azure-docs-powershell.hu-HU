---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
ms.openlocfilehash: 506287812f684a778fdb96e750aac34049912b58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195437"
---
# <span data-ttu-id="a68cf-101">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="a68cf-101">Remove-AzApiManagementApiFromGateway</span></span>

## <span data-ttu-id="a68cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a68cf-102">SYNOPSIS</span></span>
<span data-ttu-id="a68cf-103">API-t csatol az átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="a68cf-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="a68cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a68cf-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a68cf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a68cf-105">DESCRIPTION</span></span>
<span data-ttu-id="a68cf-106">A **Remove-AzApiManagementApiFromGateway** parancsmag API-t csatol az átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="a68cf-106">The **Remove-AzApiManagementApiFromGateway** cmdlet attaches an API to a gateway.</span></span>

## <span data-ttu-id="a68cf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a68cf-107">EXAMPLES</span></span>

### <span data-ttu-id="a68cf-108">1. példa: API eltávolítása átjáróról</span><span class="sxs-lookup"><span data-stu-id="a68cf-108">Example 1: Remove an API from a gateway</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="a68cf-109">Ez a parancs eltávolítja a megadott API-t egy átjáróról.</span><span class="sxs-lookup"><span data-stu-id="a68cf-109">This command removes the specified API from a gateway.</span></span>

## <span data-ttu-id="a68cf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a68cf-110">PARAMETERS</span></span>

### <span data-ttu-id="a68cf-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a68cf-111">-ApiId</span></span>
<span data-ttu-id="a68cf-112">Az Átjáróból eltávolítandó meglévő API-k azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a68cf-112">Identifier of existing APIs to remove from the Gateway.</span></span>
<span data-ttu-id="a68cf-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="a68cf-113">This parameter is required.</span></span>

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

### <span data-ttu-id="a68cf-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a68cf-114">-Context</span></span>
<span data-ttu-id="a68cf-115">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="a68cf-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a68cf-116">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="a68cf-116">This parameter is required.</span></span>

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

### <span data-ttu-id="a68cf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a68cf-117">-DefaultProfile</span></span>
<span data-ttu-id="a68cf-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a68cf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a68cf-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="a68cf-119">-GatewayId</span></span>
<span data-ttu-id="a68cf-120">A meglévő átjáró azonosítója az API eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="a68cf-120">Identifier of existing Gateway to remove API from.</span></span>
<span data-ttu-id="a68cf-121">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="a68cf-121">This parameter is required.</span></span>

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

### <span data-ttu-id="a68cf-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a68cf-122">-PassThru</span></span>
<span data-ttu-id="a68cf-123">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="a68cf-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="a68cf-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="a68cf-124">This parameter is optional.</span></span>
<span data-ttu-id="a68cf-125">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="a68cf-125">Default value is false.</span></span>

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

### <span data-ttu-id="a68cf-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a68cf-126">-Confirm</span></span>
<span data-ttu-id="a68cf-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a68cf-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a68cf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a68cf-128">-WhatIf</span></span>
<span data-ttu-id="a68cf-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a68cf-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a68cf-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a68cf-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a68cf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a68cf-131">CommonParameters</span></span>
<span data-ttu-id="a68cf-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a68cf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a68cf-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a68cf-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a68cf-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a68cf-134">INPUTS</span></span>

### <span data-ttu-id="a68cf-135">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a68cf-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a68cf-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a68cf-136">System.String</span></span>

### <span data-ttu-id="a68cf-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a68cf-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a68cf-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a68cf-138">OUTPUTS</span></span>

### <span data-ttu-id="a68cf-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a68cf-139">System.Boolean</span></span>

## <span data-ttu-id="a68cf-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a68cf-140">NOTES</span></span>

## <span data-ttu-id="a68cf-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a68cf-141">RELATED LINKS</span></span>
