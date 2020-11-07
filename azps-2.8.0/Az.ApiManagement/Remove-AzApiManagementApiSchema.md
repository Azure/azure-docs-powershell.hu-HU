---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
ms.openlocfilehash: 4fa05a0c3568d8d787a7b269cd0f26c0adc82d0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668000"
---
# <span data-ttu-id="4fe27-101">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="4fe27-101">Remove-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="4fe27-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4fe27-102">SYNOPSIS</span></span>
<span data-ttu-id="4fe27-103">Az API-séma eltávolítása az API-ról</span><span class="sxs-lookup"><span data-stu-id="4fe27-103">Removes the API Schema from the API.</span></span>

## <span data-ttu-id="4fe27-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4fe27-104">SYNTAX</span></span>

### <span data-ttu-id="4fe27-105">ByApiSchemaId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4fe27-105">ByApiSchemaId (Default)</span></span>
```
Remove-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fe27-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4fe27-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fe27-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fe27-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementApiSchema -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fe27-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4fe27-108">DESCRIPTION</span></span>
<span data-ttu-id="4fe27-109">A parancsmag **Remove-AzApiManagementSchema** az API-ról</span><span class="sxs-lookup"><span data-stu-id="4fe27-109">The cmdlet **Remove-AzApiManagementSchema** from the Api.</span></span>

## <span data-ttu-id="4fe27-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4fe27-110">EXAMPLES</span></span>

### <span data-ttu-id="4fe27-111">1. példa: az API-séma eltávolítása az API-ról</span><span class="sxs-lookup"><span data-stu-id="4fe27-111">Example 1 : Removes the Api Schema from the API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiSchema -Context $apimContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="4fe27-112">A parancsfájl eltávolítja a sémát `2` az API-ról, `echo-api` Ha az nem hivatkozik rá.</span><span class="sxs-lookup"><span data-stu-id="4fe27-112">The script removes the Schema `2` from the Api `echo-api` if it is not referenced.</span></span>

## <span data-ttu-id="4fe27-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4fe27-113">PARAMETERS</span></span>

### <span data-ttu-id="4fe27-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4fe27-114">-ApiId</span></span>
<span data-ttu-id="4fe27-115">Az API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4fe27-115">Identifier of the API.</span></span>
<span data-ttu-id="4fe27-116">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="4fe27-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe27-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="4fe27-117">-Context</span></span>
<span data-ttu-id="4fe27-118">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="4fe27-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4fe27-119">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="4fe27-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe27-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fe27-120">-DefaultProfile</span></span>
<span data-ttu-id="4fe27-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4fe27-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fe27-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fe27-122">-InputObject</span></span>
<span data-ttu-id="4fe27-123">A PsApiManagementApiSchema példánya.</span><span class="sxs-lookup"><span data-stu-id="4fe27-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="4fe27-124">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="4fe27-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe27-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fe27-125">-PassThru</span></span>
<span data-ttu-id="4fe27-126">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="4fe27-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="4fe27-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4fe27-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="4fe27-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fe27-128">-ResourceId</span></span>
<span data-ttu-id="4fe27-129">A kar ResourceId ApiSchema.</span><span class="sxs-lookup"><span data-stu-id="4fe27-129">Arm ResourceId of ApiSchema.</span></span> <span data-ttu-id="4fe27-130">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="4fe27-130">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe27-131">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="4fe27-131">-SchemaId</span></span>
<span data-ttu-id="4fe27-132">Az API-séma azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4fe27-132">Identifier of the API Schema.</span></span>
<span data-ttu-id="4fe27-133">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="4fe27-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe27-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4fe27-134">-Confirm</span></span>
<span data-ttu-id="4fe27-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4fe27-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fe27-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fe27-136">-WhatIf</span></span>
<span data-ttu-id="4fe27-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4fe27-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fe27-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4fe27-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fe27-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fe27-139">CommonParameters</span></span>
<span data-ttu-id="4fe27-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4fe27-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fe27-141">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4fe27-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fe27-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fe27-142">INPUTS</span></span>

### <span data-ttu-id="4fe27-143">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4fe27-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4fe27-144">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="4fe27-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="4fe27-145">System. String</span><span class="sxs-lookup"><span data-stu-id="4fe27-145">System.String</span></span>

## <span data-ttu-id="4fe27-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fe27-146">OUTPUTS</span></span>

### <span data-ttu-id="4fe27-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4fe27-147">System.Boolean</span></span>

## <span data-ttu-id="4fe27-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4fe27-148">NOTES</span></span>

## <span data-ttu-id="4fe27-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fe27-149">RELATED LINKS</span></span>

[<span data-ttu-id="4fe27-150">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="4fe27-150">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="4fe27-151">Új – AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="4fe27-151">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="4fe27-152">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="4fe27-152">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
