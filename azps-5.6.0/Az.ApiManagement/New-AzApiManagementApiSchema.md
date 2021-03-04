---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
ms.openlocfilehash: 7ac8d0b243f70d9e0f02c620febc7062f0c2e3ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923866"
---
# <span data-ttu-id="1db4f-101">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="1db4f-101">New-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="1db4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1db4f-102">SYNOPSIS</span></span>
<span data-ttu-id="1db4f-103">Az új API-séma létrehozása az ApiManagement szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="1db4f-103">Creates the new API Schema in the ApiManagement service</span></span>

## <span data-ttu-id="1db4f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1db4f-104">SYNTAX</span></span>

### <span data-ttu-id="1db4f-105">SchemaDocumentInline (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1db4f-105">SchemaDocumentInline (Default)</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocument <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1db4f-106">SchemaDocumentFromFile</span><span class="sxs-lookup"><span data-stu-id="1db4f-106">SchemaDocumentFromFile</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocumentFilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1db4f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1db4f-107">DESCRIPTION</span></span>
<span data-ttu-id="1db4f-108">Létrehozza az API új API-sémáját.</span><span class="sxs-lookup"><span data-stu-id="1db4f-108">Creates the new API Schema of the API.</span></span>

## <span data-ttu-id="1db4f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1db4f-109">EXAMPLES</span></span>

### <span data-ttu-id="1db4f-110">1. példa: Új séma létrehozása a Swagger Petstore extensive API-hoz</span><span class="sxs-lookup"><span data-stu-id="1db4f-110">Example 1: Create new Schema for Swagger Petstore Extensive API</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> New-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaDocumentContentType swaggerdefinition -SchemaDocumentFilePath C:\Users\sasolank\Downloads\petstoreschema.json
Schema Id                            Api Id                     Schema ContentType
---------                            ------                     ------------------
3e8892eb-98e4-408d-b77a-f424185c1044 swagger-petstore-extensive swaggerdefinition
```

<span data-ttu-id="1db4f-111">A **New-AzApiManagementApiSchema** parancsmag létrehozza vagy frissíti az `swagger-petstore-extensive` aPI sémáját.</span><span class="sxs-lookup"><span data-stu-id="1db4f-111">The cmdlet **New-AzApiManagementApiSchema** creates or updates the schema of the `swagger-petstore-extensive` aPI.</span></span>

## <span data-ttu-id="1db4f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1db4f-112">PARAMETERS</span></span>

### <span data-ttu-id="1db4f-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1db4f-113">-ApiId</span></span>
<span data-ttu-id="1db4f-114">Az api azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1db4f-114">Identifier of api.</span></span> <span data-ttu-id="1db4f-115">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="1db4f-115">This parameter is required.</span></span>

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

### <span data-ttu-id="1db4f-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="1db4f-116">-Context</span></span>
<span data-ttu-id="1db4f-117">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="1db4f-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1db4f-118">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="1db4f-118">This parameter is required.</span></span>

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

### <span data-ttu-id="1db4f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1db4f-119">-DefaultProfile</span></span>
<span data-ttu-id="1db4f-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1db4f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1db4f-121">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="1db4f-121">-SchemaDocument</span></span>
<span data-ttu-id="1db4f-122">Api-sémadokumentum karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="1db4f-122">Api schema document as a string.</span></span> <span data-ttu-id="1db4f-123">Ez a paraméter kötelező, mert a -SchemaDocumentFile nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="1db4f-123">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

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

### <span data-ttu-id="1db4f-124">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="1db4f-124">-SchemaDocumentContentType</span></span>
<span data-ttu-id="1db4f-125">Az api-séma ContentType-típusa.</span><span class="sxs-lookup"><span data-stu-id="1db4f-125">ContentType of the api Schema.</span></span> <span data-ttu-id="1db4f-126">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="1db4f-126">This parameter is required.</span></span>

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

### <span data-ttu-id="1db4f-127">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="1db4f-127">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="1db4f-128">Api-sémadokumentum fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="1db4f-128">Api schema document file path.</span></span> <span data-ttu-id="1db4f-129">Ez a paraméter kötelező, mert nincs megadva a -SchemaDocument paraméter.</span><span class="sxs-lookup"><span data-stu-id="1db4f-129">This parameter is required is -SchemaDocument is not specified.</span></span>

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

### <span data-ttu-id="1db4f-130">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="1db4f-130">-SchemaId</span></span>
<span data-ttu-id="1db4f-131">Az új séma azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1db4f-131">Identifier of new schema.</span></span>
<span data-ttu-id="1db4f-132">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1db4f-132">This parameter is optional.</span></span>
<span data-ttu-id="1db4f-133">Ha nincs megadva, akkor a program létrehoz egy újat.</span><span class="sxs-lookup"><span data-stu-id="1db4f-133">If not specified will be generated.</span></span>

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

### <span data-ttu-id="1db4f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1db4f-134">-Confirm</span></span>
<span data-ttu-id="1db4f-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1db4f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1db4f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1db4f-136">-WhatIf</span></span>
<span data-ttu-id="1db4f-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1db4f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1db4f-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1db4f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1db4f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1db4f-139">CommonParameters</span></span>
<span data-ttu-id="1db4f-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1db4f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1db4f-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1db4f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1db4f-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1db4f-142">INPUTS</span></span>

### <span data-ttu-id="1db4f-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1db4f-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1db4f-144">System.String</span><span class="sxs-lookup"><span data-stu-id="1db4f-144">System.String</span></span>

## <span data-ttu-id="1db4f-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1db4f-145">OUTPUTS</span></span>

### <span data-ttu-id="1db4f-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="1db4f-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="1db4f-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1db4f-147">NOTES</span></span>

## <span data-ttu-id="1db4f-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1db4f-148">RELATED LINKS</span></span>

[<span data-ttu-id="1db4f-149">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="1db4f-149">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="1db4f-150">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="1db4f-150">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="1db4f-151">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="1db4f-151">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
