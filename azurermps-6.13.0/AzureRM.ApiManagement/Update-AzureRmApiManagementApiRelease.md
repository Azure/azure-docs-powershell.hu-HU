---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 5b863c0d0c808c8cb993e4f78f9767d13fb634d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492899"
---
# <span data-ttu-id="cf93e-101">Update-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="cf93e-101">Update-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="cf93e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf93e-102">SYNOPSIS</span></span>
<span data-ttu-id="cf93e-103">Egy adott API-kiadás frissítése</span><span class="sxs-lookup"><span data-stu-id="cf93e-103">Updates a particular Api Release.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf93e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf93e-104">SYNTAX</span></span>

### <span data-ttu-id="cf93e-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cf93e-105">ExpandedParameter (Default)</span></span>
```
Update-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf93e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cf93e-106">ByInputObject</span></span>
```
Update-AzureRmApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf93e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf93e-107">DESCRIPTION</span></span>
<span data-ttu-id="cf93e-108">Az **Update-AzureRmApiManagementApiRelease** parancsmag egy Azure API-kezelési API-kiadást módosít.</span><span class="sxs-lookup"><span data-stu-id="cf93e-108">The **Update-AzureRmApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="cf93e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cf93e-109">EXAMPLES</span></span>

### <span data-ttu-id="cf93e-110">1. példa: az API-kiadás API-kiadásának frissítése</span><span class="sxs-lookup"><span data-stu-id="cf93e-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="cf93e-111">A parancs az `echo-api-release` új megjegyzéssel frissíti az API API-kiadását `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="cf93e-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="cf93e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf93e-112">PARAMETERS</span></span>

### <span data-ttu-id="cf93e-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="cf93e-113">-ApiId</span></span>
<span data-ttu-id="cf93e-114">A meglévő API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="cf93e-114">Identifier of existing API.</span></span>
<span data-ttu-id="cf93e-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="cf93e-115">This parameter is required.</span></span>

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

### <span data-ttu-id="cf93e-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="cf93e-116">-Context</span></span>
<span data-ttu-id="cf93e-117">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="cf93e-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="cf93e-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="cf93e-118">This parameter is required.</span></span>

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

### <span data-ttu-id="cf93e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf93e-119">-DefaultProfile</span></span>
<span data-ttu-id="cf93e-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf93e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf93e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf93e-121">-InputObject</span></span>
<span data-ttu-id="cf93e-122">Példa: Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="cf93e-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf93e-123">-Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="cf93e-123">-Note</span></span>
<span data-ttu-id="cf93e-124">API-kibocsátási megjegyzések.</span><span class="sxs-lookup"><span data-stu-id="cf93e-124">Api Release Notes.</span></span>
<span data-ttu-id="cf93e-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="cf93e-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="cf93e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf93e-126">-PassThru</span></span>
<span data-ttu-id="cf93e-127">Ha a Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiRelease típust adja meg, amely a set API-kiadást adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf93e-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="cf93e-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="cf93e-128">-ReleaseId</span></span>
<span data-ttu-id="cf93e-129">Az API-felülvizsgálati ReleaseId azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cf93e-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="cf93e-130">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="cf93e-130">This parameter is required.</span></span>

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

### <span data-ttu-id="cf93e-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cf93e-131">-Confirm</span></span>
<span data-ttu-id="cf93e-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cf93e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf93e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf93e-133">-WhatIf</span></span>
<span data-ttu-id="cf93e-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cf93e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf93e-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cf93e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf93e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf93e-136">CommonParameters</span></span>
<span data-ttu-id="cf93e-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf93e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf93e-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf93e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf93e-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf93e-139">INPUTS</span></span>

### <span data-ttu-id="cf93e-140">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cf93e-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="cf93e-141">Paraméterek: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cf93e-141">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="cf93e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="cf93e-142">System.String</span></span>

### <span data-ttu-id="cf93e-143">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="cf93e-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="cf93e-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf93e-144">OUTPUTS</span></span>

### <span data-ttu-id="cf93e-145">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="cf93e-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="cf93e-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf93e-146">NOTES</span></span>

## <span data-ttu-id="cf93e-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf93e-147">RELATED LINKS</span></span>

[<span data-ttu-id="cf93e-148">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="cf93e-148">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="cf93e-149">Új – AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="cf93e-149">New-AzureRmApiManagementApiRelease</span></span>](./New-AzureRmApiManagementApiRelease.md)
