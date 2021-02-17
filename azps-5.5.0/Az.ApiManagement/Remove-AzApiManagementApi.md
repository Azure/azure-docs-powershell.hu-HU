---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: 13f5297efc19aa56cc5af55962c072f5ff2a32d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210359"
---
# <span data-ttu-id="6855a-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6855a-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="6855a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6855a-102">SYNOPSIS</span></span>
<span data-ttu-id="6855a-103">Eltávolít egy API-t.</span><span class="sxs-lookup"><span data-stu-id="6855a-103">Removes an API.</span></span>

## <span data-ttu-id="6855a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6855a-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6855a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6855a-105">DESCRIPTION</span></span>
<span data-ttu-id="6855a-106">Az **Remove-AzApiManagementApi** parancsmag eltávolít egy meglévő API-t.</span><span class="sxs-lookup"><span data-stu-id="6855a-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="6855a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6855a-107">EXAMPLES</span></span>

### <span data-ttu-id="6855a-108">1. példa: API eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6855a-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="6855a-109">Ez a parancs eltávolítja az API-t a megadott azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="6855a-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="6855a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6855a-110">PARAMETERS</span></span>

### <span data-ttu-id="6855a-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6855a-111">-ApiId</span></span>
<span data-ttu-id="6855a-112">Az API-eltávolítás azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6855a-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="6855a-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="6855a-113">-Context</span></span>
<span data-ttu-id="6855a-114">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="6855a-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6855a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6855a-115">-DefaultProfile</span></span>
<span data-ttu-id="6855a-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6855a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6855a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6855a-117">-PassThru</span></span>
<span data-ttu-id="6855a-118">passthru</span><span class="sxs-lookup"><span data-stu-id="6855a-118">passthru</span></span>

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

### <span data-ttu-id="6855a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6855a-119">-Confirm</span></span>
<span data-ttu-id="6855a-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6855a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6855a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6855a-121">-WhatIf</span></span>
<span data-ttu-id="6855a-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6855a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6855a-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6855a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6855a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6855a-124">CommonParameters</span></span>
<span data-ttu-id="6855a-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6855a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6855a-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6855a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6855a-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6855a-127">INPUTS</span></span>

### <span data-ttu-id="6855a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6855a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6855a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="6855a-129">System.String</span></span>

### <span data-ttu-id="6855a-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6855a-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6855a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6855a-131">OUTPUTS</span></span>

### <span data-ttu-id="6855a-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6855a-132">System.Boolean</span></span>

## <span data-ttu-id="6855a-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6855a-133">NOTES</span></span>

## <span data-ttu-id="6855a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6855a-134">RELATED LINKS</span></span>

[<span data-ttu-id="6855a-135">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6855a-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="6855a-136">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6855a-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="6855a-137">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6855a-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="6855a-138">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6855a-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="6855a-139">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6855a-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


