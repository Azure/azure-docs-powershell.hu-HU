---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 03092cf9577bb7b8a35fd0ef69f5d3c94e9c92de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667999"
---
# <span data-ttu-id="d5f1e-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d5f1e-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="d5f1e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5f1e-102">SYNOPSIS</span></span>
<span data-ttu-id="d5f1e-103">Egy adott API-verzió készletének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d5f1e-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="d5f1e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5f1e-104">SYNTAX</span></span>

### <span data-ttu-id="d5f1e-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d5f1e-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5f1e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d5f1e-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5f1e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d5f1e-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5f1e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5f1e-108">DESCRIPTION</span></span>

<span data-ttu-id="d5f1e-109">A **Remove-AzAzureRmApiManagementApiVersionSet** parancsmag eltávolítja a meglévő API-verziót.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="d5f1e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d5f1e-110">EXAMPLES</span></span>

### <span data-ttu-id="d5f1e-111">1. példa: egy API-verzió készletének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d5f1e-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="d5f1e-112">Ez a parancs eltávolítja a megadott ApiVersionSetId beállított API-verziót.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="d5f1e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5f1e-113">PARAMETERS</span></span>

### <span data-ttu-id="d5f1e-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="d5f1e-114">-ApiVersionSetId</span></span>
<span data-ttu-id="d5f1e-115">Az API-verzió azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="d5f1e-116">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f1e-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d5f1e-117">-Context</span></span>
<span data-ttu-id="d5f1e-118">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d5f1e-119">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f1e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5f1e-120">-DefaultProfile</span></span>
<span data-ttu-id="d5f1e-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5f1e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5f1e-122">-InputObject</span></span>
<span data-ttu-id="d5f1e-123">A PsApiManagementApiVersionSet példánya.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="d5f1e-124">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f1e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5f1e-125">-PassThru</span></span>
<span data-ttu-id="d5f1e-126">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="d5f1e-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-127">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5f1e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5f1e-128">-ResourceId</span></span>
<span data-ttu-id="d5f1e-129">A kar ResourceId ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="d5f1e-130">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-130">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f1e-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d5f1e-131">-Confirm</span></span>
<span data-ttu-id="d5f1e-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5f1e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5f1e-133">-WhatIf</span></span>
<span data-ttu-id="d5f1e-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5f1e-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5f1e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5f1e-136">CommonParameters</span></span>
<span data-ttu-id="d5f1e-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5f1e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5f1e-138">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5f1e-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5f1e-139">INPUTS</span></span>

### <span data-ttu-id="d5f1e-140">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d5f1e-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d5f1e-141">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d5f1e-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="d5f1e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d5f1e-142">System.String</span></span>

## <span data-ttu-id="d5f1e-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5f1e-143">OUTPUTS</span></span>

### <span data-ttu-id="d5f1e-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d5f1e-144">System.Boolean</span></span>

## <span data-ttu-id="d5f1e-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5f1e-145">NOTES</span></span>

## <span data-ttu-id="d5f1e-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5f1e-146">RELATED LINKS</span></span>

[<span data-ttu-id="d5f1e-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d5f1e-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="d5f1e-148">Új – AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d5f1e-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="d5f1e-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d5f1e-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)