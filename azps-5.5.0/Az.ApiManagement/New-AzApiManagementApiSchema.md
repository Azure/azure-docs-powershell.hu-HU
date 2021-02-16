---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
ms.openlocfilehash: 7714c9118364f0d2ecc6e8773983acb916702281
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145338"
---
# <span data-ttu-id="8a618-101">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="8a618-101">New-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="8a618-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a618-102">SYNOPSIS</span></span>
<span data-ttu-id="8a618-103">Az új API-séma létrehozása az ApiManagement szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="8a618-103">Creates the new API Schema in the ApiManagement service</span></span>

## <span data-ttu-id="8a618-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8a618-104">SYNTAX</span></span>

### <span data-ttu-id="8a618-105">SchemaDocumentInline (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8a618-105">SchemaDocumentInline (Default)</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocument <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a618-106">SchemaDocumentFromFile</span><span class="sxs-lookup"><span data-stu-id="8a618-106">SchemaDocumentFromFile</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocumentFilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a618-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8a618-107">DESCRIPTION</span></span>
<span data-ttu-id="8a618-108">Létrehozza az API új API-sémáját.</span><span class="sxs-lookup"><span data-stu-id="8a618-108">Creates the new API Schema of the API.</span></span>

## <span data-ttu-id="8a618-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8a618-109">EXAMPLES</span></span>

### <span data-ttu-id="8a618-110">1. példa: Új séma létrehozása a Swagger Petstore extensive API-hoz</span><span class="sxs-lookup"><span data-stu-id="8a618-110">Example 1: Create new Schema for Swagger Petstore Extensive API</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> New-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaDocumentContentType swaggerdefinition -SchemaDocumentFilePath C:\Users\sasolank\Downloads\petstoreschema.json
Schema Id                            Api Id                     Schema ContentType
---------                            ------                     ------------------
3e8892eb-98e4-408d-b77a-f424185c1044 swagger-petstore-extensive swaggerdefinition
```

<span data-ttu-id="8a618-111">A **New-AzApiManagementApiSchema** parancsmag létrehozza vagy frissíti az `swagger-petstore-extensive` aPI sémáját.</span><span class="sxs-lookup"><span data-stu-id="8a618-111">The cmdlet **New-AzApiManagementApiSchema** creates or updates the schema of the `swagger-petstore-extensive` aPI.</span></span>

## <span data-ttu-id="8a618-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a618-112">PARAMETERS</span></span>

### <span data-ttu-id="8a618-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8a618-113">-ApiId</span></span>
<span data-ttu-id="8a618-114">Az api azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8a618-114">Identifier of api.</span></span> <span data-ttu-id="8a618-115">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8a618-115">This parameter is required.</span></span>

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

### <span data-ttu-id="8a618-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8a618-116">-Context</span></span>
<span data-ttu-id="8a618-117">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="8a618-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8a618-118">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8a618-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a618-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a618-119">-DefaultProfile</span></span>
<span data-ttu-id="8a618-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8a618-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a618-121">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="8a618-121">-SchemaDocument</span></span>
<span data-ttu-id="8a618-122">Api-sémadokumentum karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="8a618-122">Api schema document as a string.</span></span> <span data-ttu-id="8a618-123">Ez a paraméter kötelező, mert a -SchemaDocumentFile nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="8a618-123">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentInline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a618-124">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="8a618-124">-SchemaDocumentContentType</span></span>
<span data-ttu-id="8a618-125">Az api-séma ContentType-típusa.</span><span class="sxs-lookup"><span data-stu-id="8a618-125">ContentType of the api Schema.</span></span> <span data-ttu-id="8a618-126">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8a618-126">This parameter is required.</span></span>

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

### <span data-ttu-id="8a618-127">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="8a618-127">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="8a618-128">Api-sémadokumentum fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="8a618-128">Api schema document file path.</span></span> <span data-ttu-id="8a618-129">Ez a paraméter kötelező, mert nincs megadva a -SchemaDocument paraméter.</span><span class="sxs-lookup"><span data-stu-id="8a618-129">This parameter is required is -SchemaDocument is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a618-130">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="8a618-130">-SchemaId</span></span>
<span data-ttu-id="8a618-131">Az új séma azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8a618-131">Identifier of new schema.</span></span>
<span data-ttu-id="8a618-132">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8a618-132">This parameter is optional.</span></span>
<span data-ttu-id="8a618-133">Ha nincs megadva, akkor a program létrehoz egy újat.</span><span class="sxs-lookup"><span data-stu-id="8a618-133">If not specified will be generated.</span></span>

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

### <span data-ttu-id="8a618-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a618-134">-Confirm</span></span>
<span data-ttu-id="8a618-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8a618-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a618-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a618-136">-WhatIf</span></span>
<span data-ttu-id="8a618-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8a618-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a618-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8a618-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a618-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a618-139">CommonParameters</span></span>
<span data-ttu-id="8a618-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a618-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a618-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a618-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a618-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a618-142">INPUTS</span></span>

### <span data-ttu-id="8a618-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8a618-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8a618-144">System.String</span><span class="sxs-lookup"><span data-stu-id="8a618-144">System.String</span></span>

## <span data-ttu-id="8a618-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a618-145">OUTPUTS</span></span>

### <span data-ttu-id="8a618-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="8a618-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="8a618-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8a618-147">NOTES</span></span>

## <span data-ttu-id="8a618-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a618-148">RELATED LINKS</span></span>

[<span data-ttu-id="8a618-149">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="8a618-149">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="8a618-150">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="8a618-150">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="8a618-151">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="8a618-151">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
