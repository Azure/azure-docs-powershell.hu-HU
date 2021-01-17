---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: c2cf7f46a7f7f73443a9d7d2b06dbfde943b28d0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361351"
---
# <span data-ttu-id="b670f-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="b670f-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="b670f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b670f-102">SYNOPSIS</span></span>
<span data-ttu-id="b670f-103">Eltávolít egy elnevezett API-kezelési értéket.</span><span class="sxs-lookup"><span data-stu-id="b670f-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="b670f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b670f-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b670f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b670f-105">DESCRIPTION</span></span>
<span data-ttu-id="b670f-106">A **Remove-AzApiManagementNamedValue** parancsmag eltávolítja az Azure API Management **elnevezett értékét.**</span><span class="sxs-lookup"><span data-stu-id="b670f-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="b670f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b670f-107">EXAMPLES</span></span>

### <span data-ttu-id="b670f-108">1. példa: A névvel megadott érték eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b670f-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="b670f-109">Ez a parancs eltávolítja az ID tulajdonság11 azonosítójú elnevezett értéket.</span><span class="sxs-lookup"><span data-stu-id="b670f-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="b670f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b670f-110">PARAMETERS</span></span>

### <span data-ttu-id="b670f-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b670f-111">-Context</span></span>
<span data-ttu-id="b670f-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="b670f-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b670f-113">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="b670f-113">This parameter is required.</span></span>

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

### <span data-ttu-id="b670f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b670f-114">-DefaultProfile</span></span>
<span data-ttu-id="b670f-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b670f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b670f-116">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="b670f-116">-NamedValueId</span></span>
<span data-ttu-id="b670f-117">A meglévő elnevezett érték azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b670f-117">Identifier of existing named value.</span></span>
<span data-ttu-id="b670f-118">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="b670f-118">This parameter is required.</span></span>

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

### <span data-ttu-id="b670f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b670f-119">-PassThru</span></span>
<span data-ttu-id="b670f-120">Ha a megadott érték igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="b670f-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="b670f-121">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b670f-121">This parameter is optional.</span></span>
<span data-ttu-id="b670f-122">Az alapértelmezett érték hamis.</span><span class="sxs-lookup"><span data-stu-id="b670f-122">Default value is false.</span></span>

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

### <span data-ttu-id="b670f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b670f-123">-Confirm</span></span>
<span data-ttu-id="b670f-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b670f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b670f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b670f-125">-WhatIf</span></span>
<span data-ttu-id="b670f-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b670f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b670f-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b670f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b670f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b670f-128">CommonParameters</span></span>
<span data-ttu-id="b670f-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b670f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b670f-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b670f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b670f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b670f-131">INPUTS</span></span>

### <span data-ttu-id="b670f-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b670f-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b670f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b670f-133">System.String</span></span>

### <span data-ttu-id="b670f-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b670f-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b670f-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b670f-135">OUTPUTS</span></span>

### <span data-ttu-id="b670f-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b670f-136">System.Boolean</span></span>

## <span data-ttu-id="b670f-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b670f-137">NOTES</span></span>

## <span data-ttu-id="b670f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b670f-138">RELATED LINKS</span></span>
