---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 58a082288a121e5e6b04353bad862edaea4c20fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187867"
---
# <span data-ttu-id="cc1fe-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="cc1fe-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="cc1fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc1fe-102">SYNOPSIS</span></span>
<span data-ttu-id="cc1fe-103">Egy adott API-verzió készletének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="cc1fe-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="cc1fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc1fe-104">SYNTAX</span></span>

### <span data-ttu-id="cc1fe-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cc1fe-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc1fe-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cc1fe-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc1fe-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cc1fe-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc1fe-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc1fe-108">DESCRIPTION</span></span>

<span data-ttu-id="cc1fe-109">A **Remove-AzAzureRmApiManagementApiVersionSet** parancsmag eltávolítja a meglévő API-verziót.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="cc1fe-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cc1fe-110">EXAMPLES</span></span>

### <span data-ttu-id="cc1fe-111">1. példa: egy API-verzió készletének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="cc1fe-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="cc1fe-112">Ez a parancs eltávolítja a megadott ApiVersionSetId beállított API-verziót.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="cc1fe-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc1fe-113">PARAMETERS</span></span>

### <span data-ttu-id="cc1fe-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="cc1fe-114">-ApiVersionSetId</span></span>
<span data-ttu-id="cc1fe-115">Az API-verzió azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="cc1fe-116">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-116">This parameter is required.</span></span>

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

### <span data-ttu-id="cc1fe-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="cc1fe-117">-Context</span></span>
<span data-ttu-id="cc1fe-118">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="cc1fe-119">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-119">This parameter is required.</span></span>

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

### <span data-ttu-id="cc1fe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc1fe-120">-DefaultProfile</span></span>
<span data-ttu-id="cc1fe-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc1fe-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc1fe-122">-InputObject</span></span>
<span data-ttu-id="cc1fe-123">A PsApiManagementApiVersionSet példánya.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="cc1fe-124">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-124">This parameter is required.</span></span>

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

### <span data-ttu-id="cc1fe-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc1fe-125">-PassThru</span></span>
<span data-ttu-id="cc1fe-126">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="cc1fe-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="cc1fe-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc1fe-128">-ResourceId</span></span>
<span data-ttu-id="cc1fe-129">A kar ResourceId ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="cc1fe-130">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-130">This parameter is required.</span></span>

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

### <span data-ttu-id="cc1fe-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cc1fe-131">-Confirm</span></span>
<span data-ttu-id="cc1fe-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc1fe-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc1fe-133">-WhatIf</span></span>
<span data-ttu-id="cc1fe-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc1fe-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc1fe-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc1fe-136">CommonParameters</span></span>
<span data-ttu-id="cc1fe-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc1fe-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc1fe-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc1fe-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc1fe-139">INPUTS</span></span>

### <span data-ttu-id="cc1fe-140">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cc1fe-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cc1fe-141">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="cc1fe-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="cc1fe-142">System. String</span><span class="sxs-lookup"><span data-stu-id="cc1fe-142">System.String</span></span>

## <span data-ttu-id="cc1fe-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc1fe-143">OUTPUTS</span></span>

### <span data-ttu-id="cc1fe-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cc1fe-144">System.Boolean</span></span>

## <span data-ttu-id="cc1fe-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc1fe-145">NOTES</span></span>

## <span data-ttu-id="cc1fe-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc1fe-146">RELATED LINKS</span></span>

[<span data-ttu-id="cc1fe-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="cc1fe-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="cc1fe-148">Új – AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="cc1fe-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="cc1fe-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="cc1fe-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)