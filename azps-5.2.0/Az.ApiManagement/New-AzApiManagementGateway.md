---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
ms.openlocfilehash: c06442ef9ab4b5f80943da33ed87fc24c276107d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332345"
---
# <span data-ttu-id="36998-101">New-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="36998-101">New-AzApiManagementGateway</span></span>

## <span data-ttu-id="36998-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36998-102">SYNOPSIS</span></span>
<span data-ttu-id="36998-103">Új átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="36998-103">Creates new Gateway entity.</span></span>

## <span data-ttu-id="36998-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="36998-104">SYNTAX</span></span>

```
New-AzApiManagementGateway -Context <PsApiManagementContext> [-GatewayId <String>] [-Description <String>]
 -LocationData <PsApiManagementResourceLocation> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36998-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="36998-105">DESCRIPTION</span></span>
<span data-ttu-id="36998-106">A **New-AzApiManagementGateway** parancsmag új átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="36998-106">The **New-AzApiManagementGateway** cmdlet creates new Gateway entity.</span></span>

## <span data-ttu-id="36998-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="36998-107">EXAMPLES</span></span>

### <span data-ttu-id="36998-108">1. példa: Átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="36998-108">Example 1: Create a gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
PS C:\>New-AzApiManagementGateway -Context $apimContext -GatewayId "123" -Description "desc" -LocationData $location
```

<span data-ttu-id="36998-109">Ez a parancs átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="36998-109">This command creates a gateway.</span></span>

## <span data-ttu-id="36998-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36998-110">PARAMETERS</span></span>

### <span data-ttu-id="36998-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="36998-111">-Context</span></span>
<span data-ttu-id="36998-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="36998-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="36998-113">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="36998-113">This parameter is required.</span></span>

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

### <span data-ttu-id="36998-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36998-114">-DefaultProfile</span></span>
<span data-ttu-id="36998-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36998-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36998-116">-Leírás</span><span class="sxs-lookup"><span data-stu-id="36998-116">-Description</span></span>
<span data-ttu-id="36998-117">Az átjáró leírása.</span><span class="sxs-lookup"><span data-stu-id="36998-117">Gateway description.</span></span>
<span data-ttu-id="36998-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="36998-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="36998-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="36998-119">-GatewayId</span></span>
<span data-ttu-id="36998-120">Az új átjáró azonosítója.</span><span class="sxs-lookup"><span data-stu-id="36998-120">Identifier of new gateway.</span></span>
<span data-ttu-id="36998-121">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="36998-121">This parameter is optional.</span></span>
<span data-ttu-id="36998-122">Ha nincs megadva, akkor a program létrehoz egy újat.</span><span class="sxs-lookup"><span data-stu-id="36998-122">If not specified will be generated.</span></span>

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

### <span data-ttu-id="36998-123">-LocationData</span><span class="sxs-lookup"><span data-stu-id="36998-123">-LocationData</span></span>
<span data-ttu-id="36998-124">Átjáró helye.</span><span class="sxs-lookup"><span data-stu-id="36998-124">Gateway location.</span></span>
<span data-ttu-id="36998-125">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="36998-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36998-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36998-126">-Confirm</span></span>
<span data-ttu-id="36998-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="36998-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36998-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36998-128">-WhatIf</span></span>
<span data-ttu-id="36998-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="36998-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36998-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36998-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36998-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36998-131">CommonParameters</span></span>
<span data-ttu-id="36998-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36998-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36998-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36998-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36998-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36998-134">INPUTS</span></span>

### <span data-ttu-id="36998-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="36998-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="36998-136">System.String</span><span class="sxs-lookup"><span data-stu-id="36998-136">System.String</span></span>

### <span data-ttu-id="36998-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="36998-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="36998-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36998-138">OUTPUTS</span></span>

### <span data-ttu-id="36998-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="36998-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="36998-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="36998-140">NOTES</span></span>

## <span data-ttu-id="36998-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36998-141">RELATED LINKS</span></span>
