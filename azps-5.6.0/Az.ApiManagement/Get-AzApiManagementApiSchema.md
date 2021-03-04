---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
ms.openlocfilehash: 3af651595ba51f7e5443a9f6447d07848470dc90
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923090"
---
# <span data-ttu-id="d7e45-101">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="d7e45-101">Get-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="d7e45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7e45-102">SYNOPSIS</span></span>
<span data-ttu-id="d7e45-103">Az API-séma részleteinek lekérte</span><span class="sxs-lookup"><span data-stu-id="d7e45-103">Get the details of the API Schema</span></span>

## <span data-ttu-id="d7e45-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d7e45-104">SYNTAX</span></span>

### <span data-ttu-id="d7e45-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7e45-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7e45-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7e45-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiSchema -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7e45-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d7e45-107">DESCRIPTION</span></span>
<span data-ttu-id="d7e45-108">A **Get-AzApiManagementApiSchema** parancsmag megkapja az API-séma részleteit</span><span class="sxs-lookup"><span data-stu-id="d7e45-108">The **Get-AzApiManagementApiSchema** cmdlet gets the details of the API Schema</span></span>

## <span data-ttu-id="d7e45-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d7e45-109">EXAMPLES</span></span>

### <span data-ttu-id="d7e45-110">1. példa: Az Api api-sémájának részleteinek lekérte</span><span class="sxs-lookup"><span data-stu-id="d7e45-110">Example 1: Get the details of all the Api Schema of an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId wsdlapitest

SchemaId           : 2a03e1b4-1826-4e59-b372-4711f575db28
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <s:schema elementFormDefault="qualified"....

SchemaId           : b6e5497d-f65a-4851-9f5b-b5684cdae688
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <?xml version=""1.0"" encoding=""UTF-8""....
```

<span data-ttu-id="d7e45-111">Ez a parancs az adott ApiManagement környezethez tartozó `swagger-petstore-extensive` API-sémákhoz tartozó összes API-sémát lekérte.</span><span class="sxs-lookup"><span data-stu-id="d7e45-111">This command gets all the API schemas associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

### <span data-ttu-id="d7e45-112">2. példa: Az Api-hoz társított séma lekérte</span><span class="sxs-lookup"><span data-stu-id="d7e45-112">Example 2: Get the specific schema associated with an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaId 5cc9cf67e6ed3b1154e638bd

SchemaId           : 5cc9cf67e6ed3b1154e638bd
Api Id             : swagger-petstore-extensive
Schema ContentType : swaggerdefinition
Schema Document    : {
                       "definitions": {
                         "pet": {
                        ....
```

<span data-ttu-id="d7e45-113">Ez a parancs egy api-hoz társított API-sémát kap egy adott `5cc9cf67e6ed3b1154e638bd` `swagger-petstore-extensive` ApiManagement környezetben.</span><span class="sxs-lookup"><span data-stu-id="d7e45-113">This command gets the API schema `5cc9cf67e6ed3b1154e638bd` associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

## <span data-ttu-id="d7e45-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7e45-114">PARAMETERS</span></span>

### <span data-ttu-id="d7e45-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d7e45-115">-ApiId</span></span>
<span data-ttu-id="d7e45-116">Keresend meg az API-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="d7e45-116">API identifier to look for.</span></span>
<span data-ttu-id="d7e45-117">Ha meg van adva, az API-t az azonosító próbálja meg lehozni.</span><span class="sxs-lookup"><span data-stu-id="d7e45-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e45-118">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d7e45-118">-Context</span></span>
<span data-ttu-id="d7e45-119">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="d7e45-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d7e45-120">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="d7e45-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7e45-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7e45-121">-DefaultProfile</span></span>
<span data-ttu-id="d7e45-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7e45-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7e45-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7e45-123">-ResourceId</span></span>
<span data-ttu-id="d7e45-124">Api-séma arm resource identifier.</span><span class="sxs-lookup"><span data-stu-id="d7e45-124">Arm Resource Identifier of a Api Schema.</span></span> <span data-ttu-id="d7e45-125">Ha meg van adva, a rendszer megpróbálja megtalálni az api-sémát az azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="d7e45-125">If specified will try to find api schema by the identifier.</span></span> <span data-ttu-id="d7e45-126">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="d7e45-126">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7e45-127">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="d7e45-127">-SchemaId</span></span>
<span data-ttu-id="d7e45-128">A séma azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d7e45-128">The identifier of the Schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e45-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7e45-129">CommonParameters</span></span>
<span data-ttu-id="d7e45-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7e45-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7e45-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7e45-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7e45-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7e45-132">INPUTS</span></span>

### <span data-ttu-id="d7e45-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d7e45-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d7e45-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d7e45-134">System.String</span></span>

## <span data-ttu-id="d7e45-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7e45-135">OUTPUTS</span></span>

### <span data-ttu-id="d7e45-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="d7e45-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="d7e45-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d7e45-137">NOTES</span></span>

## <span data-ttu-id="d7e45-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7e45-138">RELATED LINKS</span></span>

[<span data-ttu-id="d7e45-139">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="d7e45-139">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="d7e45-140">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="d7e45-140">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="d7e45-141">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="d7e45-141">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)