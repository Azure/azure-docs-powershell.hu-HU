---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
ms.openlocfilehash: 837494b8f042d3ea788eda69d47845b02859c805
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182673"
---
# <span data-ttu-id="8c800-101">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="8c800-101">Get-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="8c800-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c800-102">SYNOPSIS</span></span>
<span data-ttu-id="8c800-103">Az API-séma részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="8c800-103">Get the details of the API Schema</span></span>

## <span data-ttu-id="8c800-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c800-104">SYNTAX</span></span>

### <span data-ttu-id="8c800-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c800-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c800-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c800-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiSchema -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c800-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c800-107">DESCRIPTION</span></span>
<span data-ttu-id="8c800-108">A **Get-AzApiManagementApiSchema** PARANCSMAG az API-séma részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8c800-108">The **Get-AzApiManagementApiSchema** cmdlet gets the details of the API Schema</span></span>

## <span data-ttu-id="8c800-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8c800-109">EXAMPLES</span></span>

### <span data-ttu-id="8c800-110">Példa 1: az API-t tartalmazó API-séma részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="8c800-110">Example 1: Get the details of all the Api Schema of an Api</span></span>
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

<span data-ttu-id="8c800-111">Ez a parancs az API-t `swagger-petstore-extensive` adott ApiManagement környezethez társított összes API-sémát kapja.</span><span class="sxs-lookup"><span data-stu-id="8c800-111">This command gets all the API schemas associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

### <span data-ttu-id="8c800-112">2. példa: az adott API-hoz társított séma beszerzése</span><span class="sxs-lookup"><span data-stu-id="8c800-112">Example 2: Get the specific schema associated with an Api</span></span>
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

<span data-ttu-id="8c800-113">Ez a parancs az API-hoz társított API-sémát `5cc9cf67e6ed3b1154e638bd` egy `swagger-petstore-extensive` adott ApiManagement környezethez társítja.</span><span class="sxs-lookup"><span data-stu-id="8c800-113">This command gets the API schema `5cc9cf67e6ed3b1154e638bd` associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

## <span data-ttu-id="8c800-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c800-114">PARAMETERS</span></span>

### <span data-ttu-id="8c800-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8c800-115">-ApiId</span></span>
<span data-ttu-id="8c800-116">A keresni kívánt API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="8c800-116">API identifier to look for.</span></span>
<span data-ttu-id="8c800-117">Ha meg van adva az API-t, az azonosítóval is próbálkozhat.</span><span class="sxs-lookup"><span data-stu-id="8c800-117">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="8c800-118">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8c800-118">-Context</span></span>
<span data-ttu-id="8c800-119">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="8c800-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8c800-120">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="8c800-120">This parameter is required.</span></span>

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

### <span data-ttu-id="8c800-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c800-121">-DefaultProfile</span></span>
<span data-ttu-id="8c800-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c800-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c800-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c800-123">-ResourceId</span></span>
<span data-ttu-id="8c800-124">Az API-séma erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8c800-124">Arm Resource Identifier of a Api Schema.</span></span> <span data-ttu-id="8c800-125">Ha meg van adva az API-séma megkeresése az azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="8c800-125">If specified will try to find api schema by the identifier.</span></span> <span data-ttu-id="8c800-126">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="8c800-126">This parameter is required.</span></span>

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

### <span data-ttu-id="8c800-127">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="8c800-127">-SchemaId</span></span>
<span data-ttu-id="8c800-128">A séma azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8c800-128">The identifier of the Schema.</span></span>

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

### <span data-ttu-id="8c800-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c800-129">CommonParameters</span></span>
<span data-ttu-id="8c800-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c800-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c800-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8c800-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c800-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c800-132">INPUTS</span></span>

### <span data-ttu-id="8c800-133">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8c800-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8c800-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8c800-134">System.String</span></span>

## <span data-ttu-id="8c800-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c800-135">OUTPUTS</span></span>

### <span data-ttu-id="8c800-136">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="8c800-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="8c800-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c800-137">NOTES</span></span>

## <span data-ttu-id="8c800-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c800-138">RELATED LINKS</span></span>

[<span data-ttu-id="8c800-139">Új – AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="8c800-139">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="8c800-140">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="8c800-140">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="8c800-141">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="8c800-141">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)