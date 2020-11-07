---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 4ff48709b02cdd0270c559ea8be2f4e269dbce2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93671994"
---
# <span data-ttu-id="dd6e9-101">Remove-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="dd6e9-101">Remove-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="dd6e9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd6e9-102">SYNOPSIS</span></span>
<span data-ttu-id="dd6e9-103">Egy adott API-verzió készletének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dd6e9-103">Removes a particular Api Version Set</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd6e9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd6e9-104">SYNTAX</span></span>

### <span data-ttu-id="dd6e9-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dd6e9-105">ExpandedParameter (Default)</span></span>
```
Remove-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd6e9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dd6e9-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd6e9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd6e9-107">DESCRIPTION</span></span>

<span data-ttu-id="dd6e9-108">A **Remove-AzureRmApiManagementApiVersionSet** parancsmag eltávolítja a meglévő API-verziót.</span><span class="sxs-lookup"><span data-stu-id="dd6e9-108">The **Remove-AzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="dd6e9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dd6e9-109">EXAMPLES</span></span>

### <span data-ttu-id="dd6e9-110">1. példa: egy API-verzió készletének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dd6e9-110">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="dd6e9-111">Ez a parancs eltávolítja a megadott ApiVersionSetId beállított API-verziót.</span><span class="sxs-lookup"><span data-stu-id="dd6e9-111">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="dd6e9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd6e9-112">PARAMETERS</span></span>

### <span data-ttu-id="dd6e9-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="dd6e9-113">-ApiVersionSetId</span></span>
<span data-ttu-id="dd6e9-114">Az API-verzió azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd6e9-114">Identifier of the API Version Set.</span></span>
<span data-ttu-id="dd6e9-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="dd6e9-115">This parameter is required.</span></span>

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

### <span data-ttu-id="dd6e9-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="dd6e9-116">-Context</span></span>
<span data-ttu-id="dd6e9-117">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="dd6e9-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="dd6e9-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="dd6e9-118">This parameter is required.</span></span>

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

### <span data-ttu-id="dd6e9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd6e9-119">-DefaultProfile</span></span>
<span data-ttu-id="dd6e9-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd6e9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd6e9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd6e9-121">-InputObject</span></span>
<span data-ttu-id="dd6e9-122">A PsApiManagementApiVersionSet példánya.</span><span class="sxs-lookup"><span data-stu-id="dd6e9-122">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="dd6e9-123">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="dd6e9-123">This parameter is required.</span></span>

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

### <span data-ttu-id="dd6e9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd6e9-124">-PassThru</span></span>
<span data-ttu-id="dd6e9-125">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="dd6e9-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="dd6e9-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="dd6e9-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="dd6e9-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dd6e9-127">-Confirm</span></span>
<span data-ttu-id="dd6e9-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dd6e9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd6e9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd6e9-129">-WhatIf</span></span>
<span data-ttu-id="dd6e9-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dd6e9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd6e9-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dd6e9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd6e9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd6e9-132">CommonParameters</span></span>
<span data-ttu-id="dd6e9-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd6e9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd6e9-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd6e9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd6e9-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd6e9-135">INPUTS</span></span>

### <span data-ttu-id="dd6e9-136">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dd6e9-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="dd6e9-137">Paraméterek: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dd6e9-137">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="dd6e9-138">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="dd6e9-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>
<span data-ttu-id="dd6e9-139">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dd6e9-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="dd6e9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="dd6e9-140">System.String</span></span>

## <span data-ttu-id="dd6e9-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd6e9-141">OUTPUTS</span></span>

### <span data-ttu-id="dd6e9-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd6e9-142">System.Boolean</span></span>

## <span data-ttu-id="dd6e9-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd6e9-143">NOTES</span></span>

## <span data-ttu-id="dd6e9-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd6e9-144">RELATED LINKS</span></span>

[<span data-ttu-id="dd6e9-145">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="dd6e9-145">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="dd6e9-146">Új – AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="dd6e9-146">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="dd6e9-147">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="dd6e9-147">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)
