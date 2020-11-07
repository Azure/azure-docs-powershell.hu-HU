---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 681ce525d1d00802cc226539fd9c3014c1786098
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836968"
---
# <span data-ttu-id="9ad58-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9ad58-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="9ad58-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ad58-102">SYNOPSIS</span></span>
<span data-ttu-id="9ad58-103">Egy adott API-verzió készletének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9ad58-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="9ad58-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ad58-104">SYNTAX</span></span>

### <span data-ttu-id="9ad58-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9ad58-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ad58-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9ad58-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ad58-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ad58-107">DESCRIPTION</span></span>

<span data-ttu-id="9ad58-108">A **Remove-AzAzureRmApiManagementApiVersionSet** parancsmag eltávolítja a meglévő API-verziót.</span><span class="sxs-lookup"><span data-stu-id="9ad58-108">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="9ad58-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9ad58-109">EXAMPLES</span></span>

### <span data-ttu-id="9ad58-110">1. példa: egy API-verzió készletének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9ad58-110">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="9ad58-111">Ez a parancs eltávolítja a megadott ApiVersionSetId beállított API-verziót.</span><span class="sxs-lookup"><span data-stu-id="9ad58-111">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="9ad58-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ad58-112">PARAMETERS</span></span>

### <span data-ttu-id="9ad58-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="9ad58-113">-ApiVersionSetId</span></span>
<span data-ttu-id="9ad58-114">Az API-verzió azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ad58-114">Identifier of the API Version Set.</span></span>
<span data-ttu-id="9ad58-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="9ad58-115">This parameter is required.</span></span>

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

### <span data-ttu-id="9ad58-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9ad58-116">-Context</span></span>
<span data-ttu-id="9ad58-117">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="9ad58-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9ad58-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="9ad58-118">This parameter is required.</span></span>

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

### <span data-ttu-id="9ad58-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ad58-119">-DefaultProfile</span></span>
<span data-ttu-id="9ad58-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ad58-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ad58-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ad58-121">-InputObject</span></span>
<span data-ttu-id="9ad58-122">A PsApiManagementApiVersionSet példánya.</span><span class="sxs-lookup"><span data-stu-id="9ad58-122">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="9ad58-123">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="9ad58-123">This parameter is required.</span></span>

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

### <span data-ttu-id="9ad58-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ad58-124">-PassThru</span></span>
<span data-ttu-id="9ad58-125">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="9ad58-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="9ad58-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9ad58-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="9ad58-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9ad58-127">-Confirm</span></span>
<span data-ttu-id="9ad58-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9ad58-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ad58-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ad58-129">-WhatIf</span></span>
<span data-ttu-id="9ad58-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9ad58-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ad58-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9ad58-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ad58-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ad58-132">CommonParameters</span></span>
<span data-ttu-id="9ad58-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9ad58-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ad58-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ad58-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ad58-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ad58-135">INPUTS</span></span>

### <span data-ttu-id="9ad58-136">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9ad58-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9ad58-137">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9ad58-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="9ad58-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9ad58-138">System.String</span></span>

## <span data-ttu-id="9ad58-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ad58-139">OUTPUTS</span></span>

### <span data-ttu-id="9ad58-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9ad58-140">System.Boolean</span></span>

## <span data-ttu-id="9ad58-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ad58-141">NOTES</span></span>

## <span data-ttu-id="9ad58-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ad58-142">RELATED LINKS</span></span>

[<span data-ttu-id="9ad58-143">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9ad58-143">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="9ad58-144">Új – AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9ad58-144">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="9ad58-145">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9ad58-145">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)