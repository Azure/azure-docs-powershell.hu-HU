---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
ms.openlocfilehash: fb144bfa228b07501c374f054970d1e3e0337ec1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94015069"
---
# <span data-ttu-id="3ef07-101">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3ef07-101">Remove-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="3ef07-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ef07-102">SYNOPSIS</span></span>
<span data-ttu-id="3ef07-103">Az API-séma eltávolítása az API-ról</span><span class="sxs-lookup"><span data-stu-id="3ef07-103">Removes the API Schema from the API.</span></span>

## <span data-ttu-id="3ef07-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ef07-104">SYNTAX</span></span>

### <span data-ttu-id="3ef07-105">ByApiSchemaId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3ef07-105">ByApiSchemaId (Default)</span></span>
```
Remove-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ef07-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3ef07-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ef07-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ef07-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementApiSchema -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ef07-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ef07-108">DESCRIPTION</span></span>
<span data-ttu-id="3ef07-109">A parancsmag **Remove-AzApiManagementSchema** az API-ról</span><span class="sxs-lookup"><span data-stu-id="3ef07-109">The cmdlet **Remove-AzApiManagementSchema** from the Api.</span></span>

## <span data-ttu-id="3ef07-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3ef07-110">EXAMPLES</span></span>

### <span data-ttu-id="3ef07-111">1. példa: az API-séma eltávolítása az API-ról</span><span class="sxs-lookup"><span data-stu-id="3ef07-111">Example 1 : Removes the Api Schema from the API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiSchema -Context $apimContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="3ef07-112">A parancsfájl eltávolítja a sémát `2` az API-ról, `echo-api` Ha az nem hivatkozik rá.</span><span class="sxs-lookup"><span data-stu-id="3ef07-112">The script removes the Schema `2` from the Api `echo-api` if it is not referenced.</span></span>

## <span data-ttu-id="3ef07-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ef07-113">PARAMETERS</span></span>

### <span data-ttu-id="3ef07-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3ef07-114">-ApiId</span></span>
<span data-ttu-id="3ef07-115">Az API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="3ef07-115">Identifier of the API.</span></span>
<span data-ttu-id="3ef07-116">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="3ef07-116">This parameter is required.</span></span>

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

### <span data-ttu-id="3ef07-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="3ef07-117">-Context</span></span>
<span data-ttu-id="3ef07-118">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="3ef07-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3ef07-119">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="3ef07-119">This parameter is required.</span></span>

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

### <span data-ttu-id="3ef07-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ef07-120">-DefaultProfile</span></span>
<span data-ttu-id="3ef07-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ef07-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ef07-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ef07-122">-InputObject</span></span>
<span data-ttu-id="3ef07-123">A PsApiManagementApiSchema példánya.</span><span class="sxs-lookup"><span data-stu-id="3ef07-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="3ef07-124">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="3ef07-124">This parameter is required.</span></span>

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

### <span data-ttu-id="3ef07-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ef07-125">-PassThru</span></span>
<span data-ttu-id="3ef07-126">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="3ef07-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="3ef07-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="3ef07-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="3ef07-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ef07-128">-ResourceId</span></span>
<span data-ttu-id="3ef07-129">A kar ResourceId ApiSchema.</span><span class="sxs-lookup"><span data-stu-id="3ef07-129">Arm ResourceId of ApiSchema.</span></span> <span data-ttu-id="3ef07-130">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="3ef07-130">This parameter is required.</span></span>

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

### <span data-ttu-id="3ef07-131">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="3ef07-131">-SchemaId</span></span>
<span data-ttu-id="3ef07-132">Az API-séma azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3ef07-132">Identifier of the API Schema.</span></span>
<span data-ttu-id="3ef07-133">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="3ef07-133">This parameter is required.</span></span>

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

### <span data-ttu-id="3ef07-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3ef07-134">-Confirm</span></span>
<span data-ttu-id="3ef07-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3ef07-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ef07-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ef07-136">-WhatIf</span></span>
<span data-ttu-id="3ef07-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3ef07-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ef07-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3ef07-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ef07-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ef07-139">CommonParameters</span></span>
<span data-ttu-id="3ef07-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ef07-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ef07-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3ef07-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ef07-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ef07-142">INPUTS</span></span>

### <span data-ttu-id="3ef07-143">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3ef07-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3ef07-144">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3ef07-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="3ef07-145">System. String</span><span class="sxs-lookup"><span data-stu-id="3ef07-145">System.String</span></span>

## <span data-ttu-id="3ef07-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ef07-146">OUTPUTS</span></span>

### <span data-ttu-id="3ef07-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ef07-147">System.Boolean</span></span>

## <span data-ttu-id="3ef07-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ef07-148">NOTES</span></span>

## <span data-ttu-id="3ef07-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ef07-149">RELATED LINKS</span></span>

[<span data-ttu-id="3ef07-150">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3ef07-150">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="3ef07-151">Új – AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3ef07-151">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="3ef07-152">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3ef07-152">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
