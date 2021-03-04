---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 9a5c4d553f425d7922fa927451ca9f3029a9f4b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929106"
---
# <span data-ttu-id="52f2a-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="52f2a-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="52f2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="52f2a-103">A Háttér eltávolítása gombra.</span><span class="sxs-lookup"><span data-stu-id="52f2a-103">Removes a Backend.</span></span>

## <span data-ttu-id="52f2a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="52f2a-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52f2a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="52f2a-105">DESCRIPTION</span></span>
<span data-ttu-id="52f2a-106">Eltávolítja az Azonosító által megadott háttért az Api-kezelésből.</span><span class="sxs-lookup"><span data-stu-id="52f2a-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="52f2a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="52f2a-107">EXAMPLES</span></span>

### <span data-ttu-id="52f2a-108">1. példa: A Backend 123 eltávolítása</span><span class="sxs-lookup"><span data-stu-id="52f2a-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="52f2a-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52f2a-109">PARAMETERS</span></span>

### <span data-ttu-id="52f2a-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="52f2a-110">-BackendId</span></span>
<span data-ttu-id="52f2a-111">A meglévő háttéren lévő azonosító.</span><span class="sxs-lookup"><span data-stu-id="52f2a-111">Identifier of existing backend.</span></span>
<span data-ttu-id="52f2a-112">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="52f2a-112">This parameter is required.</span></span>

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

### <span data-ttu-id="52f2a-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="52f2a-113">-Context</span></span>
<span data-ttu-id="52f2a-114">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="52f2a-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="52f2a-115">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="52f2a-115">This parameter is required.</span></span>

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

### <span data-ttu-id="52f2a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52f2a-116">-DefaultProfile</span></span>
<span data-ttu-id="52f2a-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="52f2a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52f2a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52f2a-118">-PassThru</span></span>
<span data-ttu-id="52f2a-119">Ha a megadott érték igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="52f2a-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="52f2a-120">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="52f2a-120">This parameter is optional.</span></span>
<span data-ttu-id="52f2a-121">Az alapértelmezett érték hamis.</span><span class="sxs-lookup"><span data-stu-id="52f2a-121">Default value is false.</span></span>

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

### <span data-ttu-id="52f2a-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52f2a-122">-Confirm</span></span>
<span data-ttu-id="52f2a-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="52f2a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52f2a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52f2a-124">-WhatIf</span></span>
<span data-ttu-id="52f2a-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="52f2a-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52f2a-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="52f2a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52f2a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f2a-127">CommonParameters</span></span>
<span data-ttu-id="52f2a-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52f2a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f2a-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52f2a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f2a-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52f2a-130">INPUTS</span></span>

### <span data-ttu-id="52f2a-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="52f2a-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="52f2a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="52f2a-132">System.String</span></span>

### <span data-ttu-id="52f2a-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="52f2a-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="52f2a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52f2a-134">OUTPUTS</span></span>

### <span data-ttu-id="52f2a-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="52f2a-135">System.Boolean</span></span>

## <span data-ttu-id="52f2a-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="52f2a-136">NOTES</span></span>

## <span data-ttu-id="52f2a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52f2a-137">RELATED LINKS</span></span>

[<span data-ttu-id="52f2a-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="52f2a-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="52f2a-139">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="52f2a-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="52f2a-140">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="52f2a-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="52f2a-141">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="52f2a-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="52f2a-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="52f2a-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
